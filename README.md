#DAM DIGITAL CODE TEST

##Approach: 
<li>Read through brief and viewed designs 

<li>Looked over brief again and made bullet points from background, requirements and user stories as to what was required 

<li>Put together basic HTML and CSS as per the requirement to work from as a starting point 

![alt text](http://i.imgur.com/kjataFx.png "Basic HTML for DAM Digital code test") 

<li>Added an event listener to the 'X's to display a modal (.modal('show')). 

<li>By binding 'this' and using .parent() I added the functionality to delete the entire objective from the modal. 

<li>I then added a checkbox to the objective divs so they could be ticked when an objective is completed and added an event listener to listen for a change on the checkbox so it could change the background color of the div accordingly.

<li>I also thought it would be useful to add in an add new objective button for the dashboard. I created that by adding a button to open a new entry point for an objective title and for an objective's content with its own add objective button.

<li>I then added a back to top button to only appear on mobile devices (480px) as per the requirements. 

<li>I finished by making the design responsive using media queries in the css and device detection in the javascript. The reason I decided to use device detection in the javascript and not just regular media queries is becuase I noticed that Ipad Pros have quite large screens and that if I were to use a media query specifically for that device it could compromise the look of the site on desktop windows that are smaller.

##Problems: 
<li>One of the main problems that I encountered was that when I was creating delete buttons on modals for the objectives, I found that if I clicked an "X" to open a modal but instead pressed "cancel" and then tried to delete a different objective, it would also delete the the objective that I decided to cancel deleting. I resolved this by console logging 'this' to find where the problem was occuring in my code and noticed that 'this' was being bound multiple times by the event listener. I figured out that if I were to switch off the event listener (.off('click')), it would also reset the 'this' that was previously stored and that was causing the issue. 

<li>I faced a similar problem with adding objectives, where the add button would add multiple objectives according to how many objectives I had previously added. I solved this in the same way using the .off('click') function.

<li>As previously mentioned another problem that occured, was that when I would create media queries for the iPad Pro I found that since the screen was quite large, it would compromise the look of the site on a desktop browser that has been made slightly smaller. So to resolve this issue I decided to add a function in the javascript to detect whether the site was opened on a browser or a on a device and adjust the css accordingly instead of using a media query in the css. 