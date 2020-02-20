---
layout: post
slug: how-i-migrated-my-medium-posts-to-site-in-2020
title: "How I Migrated My Medium Posts To My Website In 2020"
image: img/number.jpg
date: "2020-02-19T15:11:55.000Z"
draft: false
author: Suibin Hong
tags: ["learn"]

---


# How I Migrated My Medium Posts To My Website In 2020

#### Why Gatsby.js is the GOAT for blog building right now

Having set my mind to documenting my journey of entrepreneurship in 2020, the platform I chose was medium as it was the most simple and stylish choice. Unfortunately, not everybody I knew had access to a medium membership or were willing to pay for it. I decided to recreate my personal site and migrate all my medium contents over.

![Photo by [Adrian Pelletier](https://unsplash.com/@adrianpelletier?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)](https://cdn-images-1.medium.com/max/10894/0*kuXu8c4LdfF-7V6c)

# Understanding the available technology for building blog sites

Having never made a blog or built a blog site, I started looking around answers on the internet. There are so many multiple options on the market right now and the ones I looked at were:

- [Wordpress](http://wordpress.com)

- [Jekyll](https://jekyllrb.com/)

- [Hugo](https://gohugo.io/)

- [Gatsbyjs](https://www.gatsbyjs.org/)

Wordpress in plain sight sounds like the most simple answer but with a membership fee of 4 euro per month. I wanted to take the opportunity to learn how blog sites are created. I learned that blog sites are operated via the use of SPG(static page generators).

![image from Hacker news [article](https://hackernoon.com/overview-of-popular-static-site-generators-e469cf353625) on static page generators](https://cdn-images-1.medium.com/max/3440/1*vd8RzkP_U7OHfSg8qLTEYg.png)

I ran the options down the list and spent the next few hours checking out both Jekyll and Hugo. The two options are highly used in the blogging industry and can be created quickly with a few clicks. The option I chose to go with was gatsbyjs because of how much it had been praised by my friends and the rapid load time I experienced with websites built by gatsby. With the experience I had with [react](https://reactjs.org/) last summer, I believed that gatsby will be easy to get used to.

I looked around the website gatsby and formulated the following list of tasks to do:

- Launch a gatsby site

The purpose of this was to understand how gatsby work

- Find and understand how to use a gatsby theme

You know the saying “walk before you run”. You may say “this is running!” But it’s more like a modern way of running because it’ll be very time-consuming to start from scratch. The purpose of this isn’t to learn how to build a gatsbyjs app so we’ll “run” this time.

- Migrate my medium posts to the site



# Working on the task list

#### Launch a gatsby site

For this task, I followed this [tutorial](https://www.gatsbyjs.org/tutorial/blog-netlify-cms-tutorial/) from gatsbyjs.

It was straightforward and the theme in the tutorial also allowed easy access to [netlify CMS](https://www.netlifycms.org/)(content management service). Since markdown files are usually stored in the content folder of the SPG, which means you need to add a new file to the folder every time you create a new blog post. CMS offers content update via a UI and will upload your content to the folder in Github. This makes content management easy enough.

---

#### Find and understand how to use a gatsby theme

Gatsby has a huge range of themes, which they call starters that are available on the [site](https://www.gatsbyjs.org/starters/?v=2). I ended up picking [gatsby-casper](https://github.com/scttcper/gatsby-casper.git) as it had simple functionality of a blog site and had the professional UI in place, exactly what I needed! After deploying the site to netlify and making some modifications to the theme and learned the hierarchy of each folder in the system. I was ready to go.

![](https://cdn-images-1.medium.com/max/8172/1*Il4o3vFD0kUFVEQ-CV7e7A.png)






---
#### Migrate my medium posts to the site

**1.Convert your medium post to markdown**

Please note that I’ve taken this approach in a one by one fashion because mass migration can be tricky depending on your SPG. This is because, in every markdown file for SPGs, there’s a section of metadata at the beginning known as the frontmatter that is responsible for notifying its most important properties. After playing around with the available medium-to-markdown converters, I decided that it wasn’t worth the time to mass convert as every converter resulted in different frontmatter and markdown files. I went with the most straightforward [tool](https://medium-to-markdown.now.sh/), by Eric Clemmons. This converter was good because

- All the image links are preserved and rendered by the browser upon conversion to HTML by the SPG
- No attachments get generated
- Clean and easy to edit
- Easy access as the archive of the medium account isn’t needed for the converter to work

---


**2.Place all your markdown files in the content folder**

One more step.

Follow the frontmatter of example markdown files in the theme’s content folder

That’s it. It’s go time!


**3.Deploy to netlify**

You can find the site created here: [https://suibinhong.me](https://suibinhong.me)

# Overview

Having experienced gatsbyjs first hand, it was definitely the right choice and one of the best SPG on the market right now. The load time of gatsbyjs sites are simply incredible. In addition, the site to be able to archive incredible page speed insight score out of the box.

![](https://cdn-images-1.medium.com/max/3104/1*re2gMm8cln0UX7X9Fs3z4w.png)

---

To update on the product making journey:

Unfortunately, the past 2 days had been spent on researching and working out the migration of the medium posts. The journey hopefully continues tomorrow!

**Thanks for reading! :)**

**Have interesting ideas you want to share or want a chat about anything in general? You can find me on Twitter @suibinhong**
