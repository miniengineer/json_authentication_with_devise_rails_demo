# README

<h2 id="table-of-contents"> :book: Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#testing-authentication">Testing authentication</a></li>
    <li><a href="#credits">Credits</a></li>
  </ol>
</details>

<h2 id="about-the-project"> :pencil: About The Project</h2>

I wrote an article which describes the process of setting up JSON API authentication for Rails application with [devise gem](https://github.com/heartcombo/devise).

<p>Devise is a powerful and customizable authentication library used for Rails application. It comes with its own controllers, views, so essentially it's an MVC.
My application had a separate frontend framework (React) that was suppose to make API calls to Rails server to authenticaticate a user.
So, in my case I had to figure out a way to make devise accept and respond with JSON. It took me a while and I learned a lot along the way, so I wrote an article to share this knowledge.</p>

I explain the whole configuration and thought process step by step in the article that can be found here. 

This application is for devise JSON API authentication demo purpose only. It has only a User model and devise gem installed and set up to work with JSON.

<h2 id="getting-started"> :book: Getting Started</h2>

Install all gems `bundle install`

Create database `rails db:create`

Migrate database `rails db:migrate`

Start the app `rails s`

<h2 id="testing-authentication"> :book: Testing authentication</h2>

Check the endpoints `rails routes --expanded` to view all endpoints. <br />
Don't forget to add `{ Accept: application/json }` header to the request, or you won't see the JSON response ❗

### User sign up
```
URL: /api/v1/users
Method: POST
Body (JSON): {
    user: {
        email: test@mail.com,
        password: 123456,
        password_confirmation: 123456
    }
}
```

### User sign in
```
URL: /api/v1/users/sign_in
Method: POST
Body (JSON): {
    user: {
        email: test@mail.com,
        password: 123456
    }
}
```


<h2 id="credits"> :scroll: Credits</h2>

MiniEngineer

[![Hashnode Badge](https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white)](https://miniland.hashnode.dev/)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/miniengineer)
[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/minira-samadova/)
