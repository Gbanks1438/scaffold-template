# scaffold-template
Setting up a React/RoR Monorepo

*Assumes the environment is set up
*Run tests below to confirm versions before proceeding:
    $ruby --version
    $rails --version
    $postgres --version

https://reactjs.org/docs/create-a-new-react-app.html
https://docs.bitnami.com/aws/infrastructure/ruby/get-started/create-rails-app/
https://guides.rubyonrails.org/getting_started.html


- [1] open Terminal and navigate to desired directory
- [2] $mkdir to create a project subdirectory
- [3] $cd into the project folder
- [4] $npx create-react-app frontend-name
- [5] $rails new backend-name --database postgresql
- [6] $code .   -->to open in VSC
- [7] in VSC, add an “images” folder inside the src folder
- [8] confirm in config/database.yml and Ruby Gemfiles that all dependencies are installed and enabled (*bcrypt, spring, Rspec, etc)
- [9] $cd into the React folder
- [10] $npm start   --->to start the React app on local host port 3000
- [11] in VSC, edit the React welcome message by navigating to src/App.js
- [12] open a new Terminal window
- [13] $cd back into the main project folder, then into the Rails folder
- [14] $bundle exec rails db:prepare   --->to create the application database and initialize the schema
- [15] $rails generate controller Welcome index   --->to create a welcome page
- [16] edit the config/routes.rb file to add the following line--->   root 'welcome#index'
- [17] change ports in the config/puma file to 3001
- [18] $bundle exec rails server   --->to start the rails app on local host port 3001
- [19] in VSC, edit the Rails welcome message by navigating to app/views/welcome/index.html.erb
- [20] open a third Terminal window and navigate to the main project folder. Use it to enter CLI commands in the appropriate subdirectories as needed during development
- [21] make a new GitHub repository with the steps below to save and share your work

To create a new repository on the command line:
	$echo "# example-name”>> README.md
	$git init
	$git add README.md
	$git commit -m "first commit"
$git branch -M main
	$git remote add origin git@github.com:user-name/example-name.git
	$git push -u origin main



Project workflow & goals:
    Work on the backend database formatting and relationships first
    db:create, db:migrate, & db:seed
    Use Postgres as the object-relational database manager
    Set up the Models, Views, & Controllers
    Set up config/routes.rb
    Edit config/database.yml as needed
    Change favicon.ico if desired
    Move on to the frontend and work on a landing page
    Build out a functional website or application using React, HTML, CSS, and Javascript!