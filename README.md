# A simplified Jira clone built with React and Node
Auto formatted with Prettier, tested with Cypress 🎗
Visit the live app | View client | View API
Tech logos

App screenshot

What is this and who is it for 🤷‍♀️
I do React consulting and this is a showcase product I've built in my spare time. It's a very good example of modern, real-world React codebase.

There are many showcase/example React projects out there but most of them are way too simple. I like to think that this codebase contains enough complexity to offer valuable insights to React developers of all skill levels while still being relatively easy to understand.

Features
Proven, scalable, and easy to understand project structure
Written in modern React, only functional components with hooks
A variety of custom light-weight UI components such as datepicker, modal, various form elements etc
Simple local React state management, without redux, mobx, or similar
Custom webpack setup, without create-react-app or similar
Client written in Babel powered JavaScript
API written in TypeScript and using TypeORM
Setting up development environment 🛠
Install postgreSQL if you don't have it already and create a database named jira_development.
git clone https://github.com/oldboyxx/jira_clone.git
Create an empty .env file in /api, copy /api/.env.example contents into it, and fill in your database username and password.
npm run install-dependencies
cd api && npm start
cd client && npm start in another terminal tab
App should now be running on http://localhost:8080/
Running cypress end-to-end tests 🚥
Set up development environment
Create a database named jira_test and start the api with cd api && npm run start:test
cd client && npm run test:cypress
What's missing?
There are features missing from this showcase product which should exist in a real product:

Migrations 🗄
We're currently using TypeORM's synchronize feature which auto creates the database schema on every application launch. It's fine to do this in a showcase product or during early development while the product is not used by anyone, but before going live with a real product, we should introduce migrations.

Proper authentication system 🔐
We currently auto create an auth token and seed a project with issues and users for anyone who visits the API without valid credentials. In a real product we'd want to implement a proper email and password authentication system.

Accessibility ♿
Not all components have properly defined aria attributes, visual focus indicators etc. Most early stage companies tend to ignore this aspect of their product but in many cases they shouldn't, especially once their userbase starts growing.

Unit/Integration tests 🧪
Both Client and API are currently tested through end-to-end Cypress tests. That's good enough for a relatively simple application such as this, even if it was a real product. However, as the app grows in complexity, it might be wise to start writing additional unit/integration tests.

Contributing
I will not be accepting PR's on this repository. Feel free to fork and maintain your own version.
