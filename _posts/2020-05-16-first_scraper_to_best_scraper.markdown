---
layout: post
title:      "First Scraper to 'best' Scraper"
date:       2020-05-16 21:02:30 -0400
permalink:  first_scraper_to_best_scraper
---

The idea for my scraper came from one of my friends who I was in a call with when I got the project portion. He always complains about not having money and about how poor he is. But refuses to get a job at the same time. So I thought it would be funny to make a scraper to go through a job site and find jobs based on cities. 

 First thought was I would just use google and send the http request to something like "https://www.google.com/search?q=jobsinarizona". But google uses little modules that are linked to other websites and their urls are complicated. So i went over to indeed.com and found they have a search by city function that just puts what you typed into their url "https://www.indeed.com/l-CITY-jobs.html" all i had to do was get the city from the user and put it into the url, easy. Now that we had the url all we had to do was send the http request then inspect the data we got back and correlate that to what we see on indeeds website. The easiest way to do this was to inspect elements of indeeds website and look at the class and div names and use nokogiri to select them with .css('css name').text. That gave us all the names and information we wanted from indeed, now we needed to store that info. So I made a Job class to store all this info in, and gave the job class a few methods to help return this info.
 
Now all that was left was to create the cli for the user to interact with. I started this out by making little boxes with information in them so they stood out from the rest of the terminal, but everything still blended together. So I wanted to change the color of every line to help with readability. To do this I found a gem called colorize that easily allows you to change the color of every line of text. All that was left to do was to push it to github :)




