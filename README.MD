# Unit 14 Sequelize Homework: Reverse Engineering Code

## Table Of Content

Following are the table of content.

1. Overview
2. Getting Started
3. Dependencies
4. Database Modals
5. Folder structure
6. Modules

### Overview

This is simple Authenticating Login/Signup System for users

### Getting Started

1. Clone repo
2. Open & use `Develop` folder as root folder of your app
3. Run `npm i` at root of your project
4. Create Database with `passport_demo` name
5. Update mysql credentials at `/config/config.json`
6. Run `npm start` OR `npm run watch` at root of your project
7. Open `http://localhost:8080/` at browser
8. Enjoy your app

### Dependencies

1. bcryptjs@2.4.3
2. express@4.17.0
3. express-session@1.16.1
4. mysql2@1.6.5
5. passport@0.4.0
6. passport-local@1.0.0
7. sequelize@5.8.6

### Database Modals

Following are the database modals

#### Users

```
email: {
    type: DataTypes.STRING,
    allowNull: false,
    unique: true,
    validate: {
    isEmail: true
    }
},
password: {
    type: DataTypes.STRING,
    allowNull: false
}
```

### Folder structure

```
.
├── config
│   ├── config.json
│   ├── middleware
│   │   └── isAuthenticated.js
│   └── passport.js
├── models
│   ├── index.js
│   └── user.js
├── package.json
├── package-lock.json
├── public
│   ├── js
│   │   ├── login.js
│   │   ├── members.js
│   │   └── signup.js
│   ├── login.html
│   ├── members.html
│   ├── signup.html
│   └── stylesheets
│   └── style.css
├── routes
│   ├── api-routes.js
│   └── html-routes.js
└── server.js
```

### Modules

#### Routers

There are two router `html-routes.js` & `api-routes.js`

##### html-routes.js

This router handle all UI of app

##### api-routes.js

This router handle all apis & bushiness logic of app

#### Template

The `/public` folder mange all template and UI of the app it has stylesheets and js for the app

#### Models

This folder has all database and models it's uses `Sequelize` to manage models/database

#### Config

This has middleware for authenticate the app & passport.js manage main bushiness logic for login/signup with database
