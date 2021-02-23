# VanillaJSWikiSearch #

## Acknowledgements/Disclaimers ##
This project is from Dave Gray's video "Vanilla JavaScript Search App | Wikipedia API" posted to YouTube by user Traversy Media.

All code within this project was typed out by me as I followed along with the video and copied Dave's input.

## Rationale ##
The hope was to follow along with the video to get a feel for how a developer fluent in the languages I am learning would tackle a problem we might see in the real world. If all went well, this would get my hands used to typing common JavaScript terms, introduce me to various JavaScript functionalities and how to implement them, and give insight into how fluent developers design the structure of files and code.

## Lessons ##
### Sections allow easy separation of stylesheets and code ###
This is a newer HTML5 feature, as far as I know. Separating the page into sections allows for easy styling (as noted in the next lesson) AND JavaScript code. If you have a section called "searchBar", then you can have a stylesheet called "searchBar.scss" and a JavaScript file called "searchBar.js". It's almost like a vanilla JS version of React/Vue/Angular components. Separating the HTML page into sections makes development much more modular and less overwhelming than a giant monolithic structure would be.
### The structure of stylesheets should represent the layout of the web app. ###
Historically, I had never consciously considered how to structure my stylesheets in relation to the final web app. Watching Dave code out SASS files cause something to "click" for me. You can structure you SASS files (.scss file format) such that they mirror the final web app layout. This makes debugging much simpler, because if something is not styled correctly on the web app, then you can visually see where the styling is off, look at the SASS files for that section and scroll to the approximate location of the error.
### If the data can be styled down, then it might be easier to do that than to programmatically manipulate the shape of data. ###
I should note that this lesson is conditional on the concern level of data transfer limits (such as bandwidth issues). If data bandwidth is limited, then it's better to reduce the amount of data sent by the API programmatically. However, if we aren't worried about the amount of data being sent and received, then it is very easy to reduce the data down stylistically by hiding text overflows, for example.
### Calling APIs is not as scary as I thought it was ###
The Wikipedia API was very easy to interact with. A simple request using fetch() was made and arrayed data that could be converted to JSON was returned. Because JavaScript seamlessly interacts with JSON, it made it easy to work with the data returned after a fetch() request.