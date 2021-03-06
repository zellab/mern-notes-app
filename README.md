## Please install the following applications before running the code

1. Node.js - [https://nodejs.org/en/download](https://nodejs.org/en/download/)
2. Node package manager (npm) - [https://www.npmjs.com/get-npm](https://www.npmjs.com/get-npm)
3. MongoDB - [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community)
4. Postman - [https://www.postman.com/downloads](https://www.postman.com/downloads/)
5. Visual Studio Code - [https://code.visualstudio.com/download](https://code.visualstudio.com/download)


### Frontend Configuration

1. Create a React app

```
npm i create-react-app -g
create-react-app client
```

2. Add Axios and Concurrently to the React App

```
cd client
npm i axios --save
npm i concurrently -g
```

3. add the following to package.json inside the client folder

```json
"scripts": {
    "client": "npm run start --prefix client",
    "server": "nodemon server.js",
    "dev": "concurrently --kill-others-on-fail \"npm run server\" \"npm run client\"",
    "start": "node server.js"
},
```

4. Add Bootstrap to `<head>` tag 

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
```