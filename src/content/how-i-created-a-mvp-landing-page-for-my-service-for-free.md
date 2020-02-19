---
layout: post
slug: how-i-created-a-mvp-landing-page-for-my-service-for-free
title: "How I Created A MVP/Landing page For My Service For Free"
image: img/mac.jpg
date: "2020-02-14T15:11:55.000Z"
draft: false
author: Suibin Hong
tags: ["product"]

---

#### Using Heroku, Netlify, Typeform, Bootstrap, and DynamoDB

There are many options for out there for creating landing pages these days depending on your level of knowledge in technology; how quickly you’d like to do it; your end goal of the landing page. During my move to Dublin I found the process of property search on daft.ie (the most famous property site in Ireland) to be tiresome and unrewarding for my time. Thanks to a friend who introduced the idea of automating the process, I got to work and set up a free Heroku dyno to monitor and submit my interest to any new listing that fits the criteria of my search. For 2020, I thought why not use my free time to offer the same automation to others. Not knowing whether this is a service that will be useful for many people, I wanted to validate the idea by checking whether there’s a demand for the product. With this idea in mind, I needed to create an MVP that does the minimal so I can test my idea.

---

The goal is to introduce the service to people with as little resources and time as possible. This meant that creating a static page alone wasn’t sufficient. Because I needed:

A website that:

- showcases the concept

- Takes in user information

A database to store the information

A web-server that:

- Serves the automation for the users

On top of that my goal was to produce no cost for this project and keep it as minimal as possible.

---

**1.Domain**

Seemingly the service is to be used in Ireland mainly, I opted for an ie domain. Having quickly applied and purchased a domain from [HostingIreland](https://www.hostingireland.ie/), I moved onto the next stage.

---

**2.Web Page**

Deciding whether to use a web server or a static page was simple because using a web server would cost more to be hosted and for this purpose, a static page can be sufficient. One of my favourite services to use for hosting static webpages is [netlify](http://netlify.com) because of how simple it is to set up. To make the website look presentable I chose the online course bootstrap template from [grayic](https://grayic.com/shade/), which offers stylish, mobile-compatible templates for free. After a few modifications, the site was customised to showcase the service.

![](https://cdn-images-1.medium.com/max/8176/1*tJhKfKAwm7IFd-VPv43TEg.png)

With the website hosted and hooked up with the domain I purchased, I needed to create an interface to take in user information. This would simply involve a form to be sent, processed and stored in my database. For this, I chose [TypeForm](http://typeform.com), a simple straightforward way to gather information. Typeform offers notifications to be delivered to a range of external services. I opted for the use of webhook which is something I’m familiar with. For the webhook handler, I spun up a flask [Heroku](http://www.heroku.com) instance which takes the result of the user input and then stores it inside [DynamoDB](https://aws.amazon.com/dynamodb/), one of my go-to databases to use. I chose Heroku in this instance because it’s easy to set up as well as the fact that 1,000 free Dyno hours are available, which is sufficient at this stage.

---

**3.Web-Server**

Having already created a flask Heroku instance that serves the data, I continued to build on top by adding a scheduler and a listener that handles all the users’ automation requests.

The listener would check and store new listings from daft.ie 24/7.

![Photo by [chuttersnap](https://unsplash.com/@chuttersnap?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)](https://cdn-images-1.medium.com/max/12096/0*sCWDgNf5aZ9CRrLm)

The scheduler would trigger periodically which

- Checks the list of user requests

- Automatically messages listings that fit the user’s criteria

- Stores the listing link to prevent spam

---

It’s that simple! I created the project during my free time over the span of a week for no cost. If you are looking to rent a place in Dublin and would very much like to save your time from looking at daft.ie mindlessly or just curious to see the result of the project, please do check out the site. It is [https://dafthelper.ie.](http://dafthelper.ie)

---

**Thanks for reading! :)**

**Have interesting ideas you want to share or want a chat about anything in general? You can find me on Twitter @suibinhong.**
