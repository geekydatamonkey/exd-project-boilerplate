# Experimental Interaction Project Boilerplate

## Setup

1. Create a new project folder: `mkdir <yourprojectname>`

2. `cd <yourprojectname>`

3. `git clone git@github.com:johnsojr/exd-project-boilerplate.git .` to clone this boilerplate into your current directory.

3. Create a new repo to house your project on Github

4. Change the remote url to point to your new repo, and upload to git
  ```
  git remote remove origin
  git remote add origin <your github repo url>
  git push -u origin master
  ```

5. copy `.deploy.example.json` to `.deploy.json`. Fill in with your server information. BE VERY CAREFUL that you put the correct folder name. You don't want this project to overwrite all the others.

7. `npm install && bower install` to install npm and bower dependencies such as browserify, gulp, etc.

Your project is now ready for code

## Scripted setup
See [new-project.sh](https://gist.github.com/geekydatamonkey/034a7141a6dac1b288f4) for a script to setup new projects. Note: You will need to setup a github token for this to work.

## Important gulp commands

`gulp serve`
Starts a server for your project on `localhost:9000`. Compiles Sass, JS and live reloads changes on save.

`gulp tdd`
Starts karma for test driven development

`gulp`
Compiles the project so that its ready for deploy.

`gulp deploy`
Uploads your project to your server (using rsync). You must configure your `.deploy.json` file and public ssh key first. Decent instructions here: [Setup your public ssh key](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2).

