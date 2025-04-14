---
title: "Go-lift"
draft: true
---

# Introduction
I've wanted to learn web development for a while now. It allows for un-paralleled cross-platform distribution, while allowing me to tinker some more with my HomeLab and host my own applications with Docker. When thinking of a project I could embark on to help keep me motivated and with me a clear goal, I was reminded of my love-hate (mostly hate) relationship with workout tracking apps. I love the idea of having lots of data and seeing pretty graphs go up, but every app I've tried in one way or another doesn't fit my routine and/or lacks features I want, while having lots of features I don't. It was decided then, make a simple web app allowing me to track my workouts simply and view historic metrics, how hard can it be, right? 

After trying some web frameworks recommended on the internet, including Django and React, I decided to search for something newer and simpler, fitting the small scope of my project, and found HTMX. This allows for minimal javascript while building responsive web pages and paired well with language I had been learning, Go! This combination of technologies was far less documented than building React apps, but I thought this more stripped down framework could teach me more and lead to a more elegant end product.

# The Backend
To handle requests sent to the web-page and interface with a database, I started writing a back-end in Go, using the test-driven development practices I had been learning in a Go TTD course. In the process, I learnt how to initialise and write requests to a SQL database through Go's powerful standard library and create the basic CRUD operations. Due to the relative lack of less formal tutorials, I had to rely on the official documentation which, after some initial grumbling, proved an important lesson which has helped in many a project since.
