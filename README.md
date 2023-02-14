# 🌦️ Weather App

Before you host this application, read the following:

1. Client api secrets cannot be hidden by default
2. JavaScript as a standalone language donot offer such features
3. The standalone HTML, CSS, JavaScript application is now bundled into a single package
4. How are we doing it? We are going to take help of `Parcel` read through their documentation to understand more

## Steps I followed to make a deployable application

- Fix the bug that was existing in our class, that was on click on search the data was not coming although API key is given. There is a logic change check the script file

```
<form class="searchData">
  <input id="inputBox" type="text" placeholder="Enter the city name" />
  <button id="searchBtn">Search</button>
</form>
```

```
const searchBtn = document.getElementById('searchBtn');

searchBtn.addEventListener('click', async (event) => {};
```

- Initialize the project to run inside node environment

```
npm init
```

- Take the round of questionare and fill the details
- Rename the `.env.sample` to `.env` and update with your API_KEY value
- Configure the app with parcel

```
npm install -D parcel process os-browserify path-browserify
```

- Configure the app to pick environment values

```
npm install dotenv
```

- Add new `"scripts"` inside `package.json` file to run/build the application

```
"start": "parcel index.html",
"build": "parcel build index.html",
"test": "jest"
```

- Update `index.html` to load our script as a module

```
<script type="module" src="./script.js"></script>
```

- Now push your code to GitHub, link with Netlify and deploy it freshly! ✨
