---
layout: post
title:      "Tales of a project assessment "
date:       2018-11-21 16:00:46 +0000
permalink:  tales_of_a_project_assessment
---


So as promised, I'm updating my blog with the results of my first project assessment for my CLI Data Gem project. I'm excited to say that I've passed! It certainly wasn't an easy task, but all the hard work and effort I put in made hearing the words, "You've passed" sound even sweeter. I was very anxious about this first project assessment, so if anyone out there is feeling the same, this post is for you! 

Right before my project review, I was frightened, nervous, sweaty and feeling a rollercoaster of emotions. Was I ready? Did I prepare enough information about my program? Is my project "good enough"? I realize now that these are reasonable feelings to have when you're doing something you've never done before. 

When you read the requirements of the CLI Data Gem Portfolio project, it's emphasized that the instructor going over your program is there to help you and prepare you for a real life technical interview. They aren't people you should be afraid of. I was a bit skeptical of that at first, but they were right! My instructor was the nicest person who really made me feel comfortable talking about my code and also made me proud of the work I did. 

After my assessment, there were a few details that I tweaked to improve my program:

Validate all user input:

 My program was meant to display a list of the best movies made by Netflix with the data scraped from a Rotten Tomatoes editorial site. After displaying the list, the user would then be asked to choose a movie's rank number to display further details about it. My program was finding the movies based on the rank number, but it was also finding a movie if I entered something other than a number. I knew that the list only had 65 movies in it so I fixed the code to ensure that it was only finding movies numbered from 1-65.
 
<img src="https://drive.google.com/file/d/1Xu0fsYRwFKBD4KAEAkfz0Rojxc_ND2RX/view?usp=sharing">

Now if a user enters anything other than a number between 1 to 65, the program outputs an error message. One cool thing I learned while fixing the validations was that Ruby can automatically convert a user's string input to either all lowercase or uppercase letters to avoid any edge case issues. 

Instead of the code looking like this:

input = gets.chomp

    if input == "y" || "Y"
      execute_code
    elsif input == "n" || "N"
      execute_other_code
    else
      puts "I'm not sure I understand."
			
The code will look like this:

    input = gets.chomp.downcase

      if input == "y"
        run
      elsif input == "n"
        view_again
      else
        puts "I'm not sure I understand."
  
Chaining .downcase to gets.chomp will automatically convert the user's input of an uppercase "Y" or "N" to a lowercase and continue executing the code accordingly. 

Make sure the 2nd level scrape only occurs if the details for a given movie have not already been scraped:

Instead of scraping details for a movie only once, my program was scraping the details everytime a user entered it's number. This really made my program much slower than it needed to be. How did I fix that? By using the or-equals operator ( ||= ):

    movie_object.movie_profile_doc ||= Nokogiri::HTML(open(movie_object.movie_url))
		
Or-equals was really useful in making sure the details of a movie were only scraped once. Reading the code from left to right shows if there are already details in movie_object.movie_profile_doc, don't scrape. But if the details are empty, then proceed with scraping. This made the program much faster when displaying the details of each movie. 

Submitting the improved version of my project made me feel even more proud of myself. Even though there were some things that needed to be fixed, I found the solution with a little time, patience, and perseverance. So if after your first assessment, you fee like you've failed, I promise that you haven't. Just because you run into an obstacle, it doesn't mean that it's the end. It's just the beginning in the world of coding. 

