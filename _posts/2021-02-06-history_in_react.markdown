---
layout: post
title:      "History in React"
date:       2021-02-06 17:23:19 -0500
permalink:  history_in_react
---


One of the requirements of the React project was to utilize React Router. My experience with React Router was quite rewarding, as it prompted me to read carefully through the online documentation in order to understand how it works, which consequently lead me to discovering useful features that I then successfully implemented in my application. One of such features is *history*. 

History, or history object, refers to a major dependency of React Router and is extremely convenient when you want your app to manage your browser's session history. History objects have many properties and methods, such as push(), which pushes a new entry onto your browser's histor stack and essentially allows you redirect your app to a provided location, or goBack(), which does... exactly what it says it does. In order to use history in my project, I passed it down as a prop through Router to the specific components that would use it. For example, like this:

`` <Route exact path='/posts' render={(routerProps) => <PostList {...routerProps} posts={this.props.posts}/>}/>``

Once my components had access to history, I decided to implement it in my forms. For example, once a post is made, my app automatically takes you to the page where you see all posts (including your new one) which was already accessible to me as one of my Routes. I did that by adding the following line inside my handleOnSubmit method:

``this.props.history.push('/posts')``


I also made a Back button, which would take a user back to the previous page. I placed this button in my Edit Post form. This was super easy to implement through my handleGoBack function that would execute upon clicking the button:

``handleGoBack = (e) => {
      this.props.history.goBack()
    }``


These are just two simple examples of how you can use Router history in React to add functionality to your application. 

I encourage everyone to learn about React Router's history prop from its official documentation here: https://reactrouter.com/web/api/history . You won't regret it!
