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

<p> Not a while ago, I started a side project to improve my engineering skills.
I decided to make a web application with Rails + React stack. When it came to the authentication implementation, I went with the devise gem. </p>

[Devise](https://github.com/heartcombo/devise) is a powerful and customizable authentication library used for Rails applications. It comes with controllers, views and there are a few commands you need to run to make the authorization work.

However, my application had a different frontend framework (React) that handled the views and was supposed to make API calls to the Rails server to authenticate a user.

It took some research till finding a way to make the devise work with my configuration or, in other words, to make it accept and respond with JSON.

I learned a lot along the way, and I summarised my thoughts in an [article](https://miniland.hashnode.dev/json-api-authentication-for-rails-application-with-devise).
While researching, I got a suggestion to read an article from a [blog](https://andrewray.me/blog) that solved 99% of the devise configuration problem. There were comments under the article asking the author for a demo application. Unfortunately, it seems like author removed the article as I haven't found THE article which helped me :(

So, I decided to make a demo application myself, hoping that it would help people who are looking for a solution to the same configuration problems.

If you need a detailed explanation of the whole process, you can check out [this article](https://miniland.hashnode.dev/json-api-authentication-for-rails-application-with-devise).

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
