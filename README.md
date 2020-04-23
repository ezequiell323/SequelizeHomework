# SequelizeHomework

--PASSWORD AUTHENTICATION

This app allows users to log into the account and create an account. 



--USER STORY

As a User  who wants to safely log into , I want to know my personal details are safely stored. 



--TECH USED --
-EXPRESS
-EXPRESS-SESSION
-MYSQL2
-PASSPORT
-SEQUELIZE
-PATH



--GETTING STARTED

to begin using this app, please open homework folder for week 14.

1)create a mysql db called "passport_demo"
2)open terminal in current repo and run "npm i" to install all node packages 
3)while in terminal, run "node server.js" and you will successfully connect to server
4)go into the config file, open config.js and insert your personal data ie username, password etc
5)User can use the app.



--FILES EXPLAINED

CONFIG

  MIDDLEWARE

  isAuthenticated.js-- 
  restricts routes that user is not allowed to visit if not logged in. if user is logged in, it continues with request 

  config.json--
  connection configuration to connect to server };

  passport.js--
  contains javascript logic that tells passport we want to log in with an email address and password

MODELS

  index.js--
  connects to database and imports users log in data using FS,Path,sequelize

  user.js--
  requires "bcrypt" for password. this makes our database secure even if compromised. Here we have JS that defines what is stored on our database 

ROUTES

  api-routes.js-- 
  contains routes for signing in, logging out and getting users specific data to be displayed client side 

html-routes.js --
  routes that check whether user is signed in, whether user already has account  and sends them to the correct  page


server.js==
requires packages, sets up PORT, creates express and middleware, creates routes and syncs database 
