# mca-db-web-scraper

## Context

I was tasked with coming up with a project idea for my Capstone/Thesis course.  I came up with an idea to create a web application that would use drop down menus to select parts of specific Title of laws in the Montana Code Annotated 2021.  As part of the implementation, I would need a database that would store the laws and could be used by the MVC project I created for another class.  See my [MCA MVC project](https://github.com/tlhausler/mca-mvc).  

## Action

I created a class library with a simple entity that would store the necessary information from the specific title I was handling from the MCA.  In order to get all the parts necessary in the title, I implemented a web scraper that would grab the information I needed from the web page.  When all the information was gathered, it was looped over in order to create the objects which were then saved to the database.  The table was generated off of the Title 45 entity using Entity Framework.  The web scraper used the HtmlAgilityPack package.  

## Result and Reflection

The web scraper operated as intended and the table was generated with all items I wanted from the website.  The project was then successfully used to build the MVC project that would utilize the database's data.  

I had never had experience with a web scraper before.  It was a very useful tool for getting a lot of information as the original plan was just to put a few items in the database manually.  In the implementation of the MVC, I learned that I should have cleaned the information I scraped of all excessive white space, newlines, and returns before storing to the database.  This was handled in the MVC using the Trim method, but could have been avoided had I done that step here instead.  I also gained valuable insight in the consturction and use of class libraries for actual project work.  
