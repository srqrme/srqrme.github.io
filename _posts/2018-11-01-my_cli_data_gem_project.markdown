---
layout: post
title:      "My CLI Data Gem Project"
date:       2018-11-01 17:32:55 +0000
permalink:  my_cli_data_gem_project
---


Well everyone, I finally did it. I finally submitted my CLI Data Gem Portfolio Project for review. I know I still have to get through the project review before I can move forward, but it feels good to be able to celebrate this small victory. 

The idea for this project actually came from a friend who had been complaining about searching for a good movie on Netflix. I found a great [Rotten Tomatoes editorial](https://editorial.rottentomatoes.com/guide/best-netflix-movies-to-watch-right-now/) on popular movies made directly by Netflix (aka Netflix Originals). 

<h6>Read the instructions!</h6> 

Though the instructions won't tell you how to start and work on the project, it still has a few "gems" (get it? Hahaha) that are super helpful. One of those helpful tips was to watch Avi's video walkthrough of his [Daily Deal Gem CLI](https://www.youtube.com/watch?v=_lDExWIhYKI). I was so nervous about starting this project because it just seemed like such a huge ordeal. Watching that video alleviated a lot of my anxiety because it really teaches you the basics of building a CLI gem. Another tip was to review the [Student Scraper](https://learn.co/tracks/full-stack-web-development-v5/object-oriented-ruby/final-projects/student-scraper) lab. I quickly learned that a lot of what I did in that lab can also be applied to this project. There are other helpful tips, of course, but for anyone starting this project, if you haven't read the instructions in full and followed at least these two suggestions, I would highly recommend doing so. 

<h6>Getting down to business</h6> 

The easiest way for me to begin this project was by using a bundler in the terminal: 

> bundle gem *GEMNAME*

This one short command packs quite a punch. It created a folder structure complete with everything I needed to start my project, including a Gemfile to hold any gems my program might be dependent on, as well as a License file and Code of Conduct file. I was finally on my way! 

I first created an executable file, 'bestNetflixMadeMovies', in the bin folder. I created it first because I knew users of my program wouldn't even be able to get it started if I didn't have an executable file. I wrote in a code that would instantiate my CLI class and call a start method to fire up the program.

Then I started to create the files for my CLI, Scraper, and Movie classes. I had some trouble with giving my files access to one another, mainly whether to use require vs. require_relative. After getting help from my section lead, doing some light reading as well as talking to some of my peers, these are the key differences I've found between the two:

> ***require*** loads files outside of my program (i.e. gems that my program might be dependent on), while
> ***require_relative*** loads files within my program's directory that are related to the file I'm currently working on

Once I added the correct file requirements, I was able to see my program work the way a user would. That helped tremendously when it came to details I was missing or code that needed tweaking. 

<h6>The hard stuff</h6>

After getting through the initial difficulties, it was time for me to code my classes. I needed to get the list of movies from the Rotten Tomatoes editorial (Scaper class), create movie objects (Movie class), and display them in rank order from most popular to least popular (CLI class). 

Scraping data from my chosen website had to be the most difficult and what took me the longest to do. Between identifying the correct CSS selectors that would display the exact text I wanted and ensuring that text actually displayed, it was a tedious process. I did a whole lot of testing and 'pry'ing. There were times when I would add attributes, find that they weren't displaying the way I wanted them to and delete them. After testing over and over, I would re-add them again when I figured out how to present them properly. 

<h6>This isn't the end</h6>

In Avi's Daily Deal Gem CLI video, he mentions that the most intimidating thing about being a programmer is a blank file. In my case, he was totally right. That first blank file had me sweating bullets for a little while there. But once I got a few lines in, I started getting excited about my project. I was so worried that I wasn't smart enough to get through this on my own. Looking back on it, I realize that I should really give myself a little more credit. I'm hoping my review goes well and will be writing a post with an update of how it went. In the meantime, here's a video of my program demo:

<iframe width="560" height="315" src="https://www.youtube.com/embed/dyfm0ZxOHGw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

