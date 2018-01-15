# wikipedia-api

This script is made specifically to check if a celebrity had parents who divorced and if the celebrity had a divorce later in life. With the data that I gathered I then wrote this [article](https://theglobalaffairs.com/2018/01/15/celebrities-with-divorced-parents-are-more-likely-to-divorce-later-in-life/).

## Gathering Data

To access the wikipedia json files, I initially tried using a ```XMLHttpRequest``` but I got several errors and in the end I gave up trying. Then I tried using the ```$.getJSON()``` function from the jQuery library but then I received CORS errors. Finally, after so many failed attempts, I used the ```loadJSON()``` from the p5.js library and I was able to extract data from the json files.

Hardest part was for someone to be able to copy a list from the internet, then assign the list as a string in a variable. From then the script would read the string and search the names on Wikipedia. I wanted this to be possible so I could just find a list, paste in the script and then the script would do the rest of the job. It took some time for me to solve this but in the end, I made an empty array and a ```for``` loop that would take substrings (the names) of the variable (with the list) and push them to the array. After that, the ```forEach``` method takes care of the rest.

Also this project was a great opportunity to test if my [EasyRegex](https://github.com/gogeorge/EasyRegex) library works properly.

## How to use this

While this script was made for a specific purpose. You can use it in general to take a long list of names (names of the wikipedia pages) convert them into an array and for each name let the script search for specific keywords.

1.) Go to crawl.js

2.) Go to line 8 and put your own list (maybe change the ```var celebrities``` to something more appropriate)

3.) Write your own if statements depending on what you want to do.


