# :newspaper: NY Times ReactJS App

A `NodeJS`, `MongoDB`, `Express`, and `ReactJS` application where users can query, display, and save articles from the [New York Times Article Search API](http://developer.nytimes.com/). Users can remove saved articles as well.

Please check out the deployed version in Heroku [here](https://new-york-time-react.herokuapp.com/)!

Click on the headlines to be re-directed to the full New York Times articles.


## Functionality

On the backend, the app uses `express` to serve routes and `mongoose` to interact with a `MongoDB` database.

On the frontend, the app uses `ReactJS` for rendering components, `axios` for internal/external API calls, and `bootstrap` as a styling framework.

In order to transpile the JSX code, `webpack` and `babel` were utilized. All of the JSX  code in the `/app` folder was transpiled into the `bundle.js` file located in the `/public` folder.


## Cloning down the repo

If you wish to clone the app down to your local machine...

  1. Ensure that you have MongoDB set up on your laptop

    * An amazing repo to get you started with that can be found [here](https://github.com/dannyvassallo/mongo_lesson).

  2. Once you are set up, `cd` into this repo and run `npm install`.

  3. Then open another bash or terminal window and run `mongod`

  4. Run the script with `node server.js`.
  
  5. Navigate to `localhost:3000` in your browser.

Note that if you made changes to the JSX code in the `/app` folder, you must transpile it to see your changes. When `cd`-ed into this repo, enter `npm run bundle` in the command line to trigger my `webpack` script.

The `/test` folder can be disregarded since its files were made just for laying out the design of the app.


## Screenshots

#### Users are able to submit a topic, start year, and end year to query the New York Times

![Query Articles](/images/query-articles.png)

#### Press the Save button and the article is bookmarked via an `/api/saved` post route

![Article Content](/images/add-bookmark.png)

#### Press the Delete button and the bookmarked article is removed via an `/api/delete/:id` post route

![Add Comment](/images/remove-bookmark.png)

#### Note that the get routes include an **internal route** to `/api/saved` for querying and displaying all the bookmarked articles from the Mongo database.

#### Note that the get routes also include an **external route** to `https://api.nytimes.com/svc/search/v2/articlesearch.json` for querying the New York Times.

### Technologies used

- Node.js
- React
- MongoDB - https://www.mongodb.com/download-center#community
- Mongoose - http://mongoosejs.com/docs/
- express NPM Package - https://www.npmjs.com/package/express
- body-parser NPM Package - https://www.npmjs.com/package/body-parser
- morgan NPM Package - https://www.npmjs.com/package/morgan
- request NPM Package - https://www.npmjs.com/package/request

### Prerequisites

```
- Node.js - Download the latest version of Node https://nodejs.org/en/
- Bootstrap - Add CDN link https://getbootstrap.com/docs/4.0/getting-started/introduction/
```

### Built With

* Visual Studio Code - Text Editor

### Copyright

Paul Pinho © 2018. All Rights Reserved.
