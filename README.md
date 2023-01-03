# scaffold-template
Setting up a React/RoR Monorepo

*Run tests below to confirm versions before proceeding:
    $ruby --version
    $rails --version
    $postgres --version

https://reactjs.org/docs/create-a-new-react-app.html

https://docs.bitnami.com/aws/infrastructure/ruby/get-started/create-rails-app/

https://guides.rubyonrails.org/getting_started.html

---

Walkthrough:
1) open Terminal and navigate to desired directory
2) $mkdir project-scaffold {*to create a project subdirectory}
3) $cd project-scaffold {*go into the project-scaffold folder}
4) $npx create-react-app frontend-name
5) $rails new backend-name - -database postgresql
6) $code . {*to open in VSC}
7) in VSC, add an "images" folder inside the src folder
8) confirm in config/database.yml and Ruby Gemfiles that all dependencies are installed and enabled (*bcrypt, spring, Rspec, etc)
9) $cd frontend-name {*go into the React folder}
10) $ls -la {*to check for git files and use [$rm -rf] to clear them if present}
11) $npm start {*to start the React app on local host port 3000}
12) in VSC, edit the React welcome message by navigating to src/App.js
13) open a new Terminal window
14) $cd ./project-scaffold/backend-name {*go back into the main project folder, then into the Rails folder}
15) $ls -la {*to check for git files and use [$rm -rf] to clear them if present}
16) $bundle exec rails db:prepare {*to create the application database and initialize the schema}
17) $rails generate controller Welcome index {*to create a welcome page}
18) edit the config/routes.rb file to add the line from inside the bracket [root 'welcome#index']
19) change ports in the config/puma file to 3001
20) $bundle exec rails server {*to start the rails app on local host port 3001}
21) in VSC, edit the Rails welcome message by navigating to app/views/welcome/index.html.erb
22) open a third Terminal window
23) $cd ./project-scaffold {*go to the main project folder}
24) make a new GitHub repository for your project and initialize it
25) use git commands to add files, commit the changes with a comment, and then push 

---

Project workflow & goals:
Work on the backend database formatting and relationships
db:create, db:migrate, & db:seed
Use Postgres as the object-relational database manager
Set up the Models, Views, & Controllers
Set up config/routes.rb
Edit config/database.yml as needed
Change favicon.ico if desired
Move on to the frontend and work on a landing page
Build out a functional website or application using React, HTML, CSS, and Javascript!
