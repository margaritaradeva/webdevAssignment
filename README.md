### CS1031 REPORT

Let’s start with the design. I kind of struggled at first, because I was not sure what I want my pages to look like. My first idea was to keep everything consistent-that’s why I followed the same colour theme with
a colour I like since it is also a website about us. I decided to have a banner in Home Page and About to make it visually more appealing. I thought that having a light background colour for all the pages would make
it better and I decided to make all the text stand out by using rounded borders. For the Home Page I did use the same approach as my last assignment-using a jumbotron to separate the content, adding a carousel 
for pictures and I reused the code for the nav menu.

I decided to once again use Bootstrap to make my website responsive and that is why I used grids. For the content of Home Page, I just decided to make it more generic and add some “interesting”, kind of more 
non-formal information about myself. That is when I first started getting issues with responsiveness. I wanted to add a section about where I am from and add an interactive map. I didn’t know at first that 
the code I was using to embed it into my website was messing up the responsiveness. I had this issue for hours and I generally though I don’t understand how Bootstrap works. That is why I started doing the 
About page for which I found a very easy to use library-W3.CSS which provides you with many options when it comes down to responsiveness and styling. That is why I used W3.CSS for the grid, some interesting
icons, and some styling of the page. But of course, it took me some time to get how it works and then I learnt how to override the styling to make it consistent with my Home Page. Not to mention I really 
struggled with writing my CV, since I haven’t done that in a long time, and I dint have my own CV to use already. Then I just added a small section listing very briefly how I developed the website. 

I came back to my Home Page and started deleting element by element too see what was messing up my responsiveness. In the end I saw it was the map and just decided to delete it since I had enough content.
Then I finally started the chat. Saying that the user has connected/disconnected wasn’t an issue, because it’s easy to notice the socket.on "disconnect”/”connect” functions where you need to add the code 
for displaying a message using io.emit(). Then I created the notification using alert box(https://www.w3schools.com/js/js_popup.asp helped me with that)-simple function in client.js when a “new user” joins. 
I had much more issues with the “typing”. I have used event listeners in Java so thanks to that at least I had a rough idea what needed to be done. Then I found a useful and easy to follow 
website(https://tsh.io/blog/socket-io-tutorial-real-time-communication/). I had some time playing around with the code and I added that whenever no one is typing it displays “no users are typing...”. However, 
I do have an issue with that-the code works perfectly if you don’t press the enter button. Once you press it, the “user__ is typing...” never disappears. I think it is to do with my event listener, but I was 
running out of time so I just decided to remove the “Enter” button, so this way no user would have the option to click on it and I also think the website if visually more appealing without it. 

I wanted to change the colours of the messages depending on if they are received or sent. I had no idea how to do it so I started messing up with the code. I knew it was something in client.js, especially this 
“messageBox.innerHTML += user === userName ? myMsg : receivedMsg;” really got my attention. I never got this to work, however, I found another way. When we define receivedMsg and myMsg there was some HTML 
code, so I tried adding style attribute-that worked, so I made the messages look like little bubbles. I did want to move on of them on the right side, but unfortunately-unsuccessfully. As an extra I did want to add 
a library to suggest words for autocompleting the input, but I got a lot of JavaScript errors, so I decided to delete it. Another idea I had was making the user type their own username, but I  got too many errors
and I was short of time so I decided to keep it as it was plus I have seen chats that use that random usernames if you are not registered, so it is not uncommon. 
I had troubles with the sidenav, because whenever I had my nav menu it either went under the sidenav or when I changed properties it added a small gap. It was also not responsive. That is why I decided to use the same 
grid as my About page since I knew it would fit perfectly. I changed some CSS properties and made it look very clean and also responsive. If we had more time in general, it would e a good idea if we were restricted 
to keeping the messege history of lets say only 10 last messages.
Every now and then, I used https://validator.w3.org/nu/#l203c10 to validate my code, the console to check for JavaScript errors and git to save my code in case something happens.

Overall, I loved the idea of the website, because it “forces” us to think about how we could make our CV as CS students.

### RESOURCES:
W3schools.com. (2019). JavaScript Popup Boxes. [online] Available at: https://www.w3schools.com/js/js_popup.asp.
validator.w3.org. (n.d.). Ready to check - Nu Html Checker. [online] Available at: https://validator.w3.org/nu/#l203c10 [Accessed 10 Dec. 2021].
tsh.io. (2020). Node.js Socket.io tutorial: Real-time chat application | TSH.io. [online] Available at: https://tsh.io/blog/socket-io-tutorial-real-time-communication/ [Accessed 10 Dec. 2021].
W3schools.com. (2020). W3.CSS Home. [online] Available at: https://www.w3schools.com/w3css/default.asp.
W3schools.com. (2019). JavaScript Tutorial. [online] Available at: https://www.w3schools.com/js/default.asp.
Pixabay (2018). Pixabay. [online] Pixabay.com. Available at: https://pixabay.com/.

### WHAT I OVERRIDE:
Some of the CSS I use is me reusing my own code from the previous assignment
.nav-tabs-to change the background colour of the nav menu to purple
.nav-item-to change text colour for nav menu to white
.nav-tabs a:hover-to change colour of the tab and text of nav menu item when hovering over it
#act- color for the active tab we are on
.banner- to use the whole banner picture
.banner .jumbotron - fixing the text box position and not letting the background picture erepeat itself
#banner-text-sligtly transparent background of the text with rounded borders and fixing the text properties
#banner-text h1 - change the text colour of the heading
.page-footer - to change colour of text, background, link colours of my footer
.li-color li::before and .li-color- to change bullet points to pink
.border - borders for all the text boxes for content
.border-chat - borders for all boxes for the chat

### WHAT I WANTED TO USE
Algolia-AI-powered search and discovery platform for dynamic experiences which I intended to use for my input box, suggesting words to the user. Later I understood it is more for like a search 
so if I had the time I would implement a search bar in my code to search by a key word.