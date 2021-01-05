**1. Project Title:**

Word Jumble aka "Jumble2"

**2. Brief Description:**

Word Jumble is a fun scramble game. The object of the game is to unscramble the words that are randomly generated and for each word that is guessed correctly, the user earns 5 points. The set of words used for this game are the states within the USA.

**3. Framework**

Built with Node.js & Express

**4. Dependencies**

The following dependencies were installed to develop this app:
a. npm init -y (for the pkg.json)
b. npm i express (provides a robust set of features to develop web & mobile apps)
c. npm i -D nodemon (helps automatically restart the node application when changes are detected)
d. npm i passport (authentication middleware for node.js)
e. npm i ejs (Embedded Javascript Templating helps to create HTML template with minimal code)
f. npm i dotenv pg (dotenv is a module used to access environment variables in the application & pg is used to interface with my postgresql database)
g. npm i bcrypt (used to hash a password before it is stored in a database)

**5. Deployment**

Heroku was used to deploy this application (deploying moves the app from your local server to an actual website that can host your app)

    - To deploy with Heroku: go to Heroku.com and create and account if you don't already have one
    - While creating my account I selected Node.js as the primary development language
    - Once logged in, click the "New" button on the top right hand corner and select "Create New App"
    - Fill out app name and choose a region, then click "Create App"
    - Once in the dashboard, click the link to the Heroku CLI
    - This brings you to a screen whereas you can download the installer for macOS or Windows
    - Open the installer and go through the steps
    - Once all the steps are completed, go to your terminal and type in "heroku login"
    - It will then ask for your Heroku login credential such as: email & password
    - You should the recieve a message that states " Logged in as youremail"
    - Now ensure your app is initialized as a git repository by typing "git status"
    - If your app is not initialized, type "git init"
    - Now connect the repository to the app on Heroku by running this command " heroku git:remote -a yourappname" on terminal
    - Then stage your files for commit just like in github (git add ., git commit -m "message", git push heroku master)
    - Now the app is online, but not working yet
    - So, create a procfile by typing "touch Procfile" in terminal so you can provide instructions to Heroku on how to run the app
    - Since I ran the app locally using node index.js, I typed "web node index.js" so Heroku could run the app the same way I ran it locally
    - Since we can't specify the port number like we do locally, we have to use the port number that Heroku assigns it which is available the the Process.env.port variable.
    - If the port is not available, we can specify the app to run on port 5000
    - Now commit the files (git add ., git commit -m "changed port")
    - Now push to Heroku (git push heroku master) and once that's done you can go back to your app and refresh it and it should be working
