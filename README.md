After trying to run a Flash game on my blog and not finding an easy and didactic way to learn how, I'm going to share how to do it.

Tutorial 2026

Step 1: Create a repository on Github.

Github is where you will store your files to make a functional Flash game page work.

Create a Github account. After that, at the top of the page, click the + icon and then "New Repository". 

Choose any name you want and keep the Visibility as Public. Click the green "Create Repository" button. 

On the next page, find "Quick Setup" and then "Get started by creating a new file". 

In "Create new file", you must create an Index File. This is the file where you will create the configuration for your game to work properly.

Creating this file is easy. Here is the code you need. Just copy and paste:

<!DOCTYPE html>
<html lang="en">
<head> 
<meta charset="UTF-8"> 
<title></title> 

<script src="https://unpkg.com/@ruffle-rs/ruffle/ruffle.js"></script> 

<style> 
body { 
display: flex; 
justify-content: center; 
align-items: center; 
height: 100vh; 
margin: 0; 
} 

#game-container { 
width: 800px; 
height: 600px; 
position: relative; 
top: 100px; 
left: 140px; 
} 

h1 { 
position: absolute; 
top: 90px; 
text-align: center; 
width: 100%; 
color: #333; 
} 
</style>
</head>
<body> 
<div id="game-container"></div> <!-- Container where the game will be loaded --> 

<script> 
window.addEventListener("load", () => { 
const ruffle = window.RufflePlayer.newest(); // Create the newest version of the Ruffle player 
const player = ruffle.createPlayer(); // Create the player to run the SWF file 

const container = document.getElementById("game-container"); // Get the container where the game will be inserted 
container.appendChild(player); //Append the player to the container 

player.load("YourGameHere.swf"); // Load the Flash game (SWF file) into the player 
}); 

  
After that, at the top of the page, name the file exactly like this: "Index.html" (without the quotes).

After that, you need to activate Github Pages (which allows you to have an online page with your game running).

Still in your repository, find Settings at the top of the page (to the right of Insights). Scroll down a bit and find Pages (above Advanced Security).

As soon as you enter this page you can read "Build and deployment". Right below in Branch, click on None and then on main. New options will appear. Keep everything as it is "Main/Root/" and click Save.
  

Step 2: Downloading your Flash game file.

The next step is to have your game file. Flash game files are SWF files. You can find them in several places. I recommend Flashpoint Browser. It saves the games you open directly to the computer and you can extract the SWF file from each one. You can also find SFW files from websites using the Wayback Machine. For example, I go to the famous 2000s girl game website, GirlGoGames, find a page where the game is working correctly, right-click on the game screen and select the "download swf" option. You can find other methods by searching online.
  

Step 3: Final Settings to Create Your Page.

Once you have your file downloaded, you need to store it in the same repository you created.

Still at the top of the Github page, click on the name of your repository (next to the cat icon). Click on the + icon next to the green "Code" button. Select "Upload Files". Drag or select your chosen game file from your computer (the file that should end with .swf).

Scroll down the page a bit and select the green "Commit Changes" button.

Now let's finish configuring your Index file so we can then create the page with your game already working!

Still in your repository, click on your game file (swf). Next to its name you can see two overlapping squares. Click on this icon to copy the name of your game (or just copy or type it manually in the next step). 
  
Go back to the previous page (your repository). Click on your File Index. In the right corner find the pencil icon. The edit mode of your file will open. 
  
Scroll to the bottom of the page and find "player.load" (or search the page using the F3 shortcut). 
  
Replace "YourGameHere.swf" with the name of your game that you copied. Keep the quotation marks and the result should look like this, for example: ("icecreamgame.swf"). 
  
Scroll to the top of the page and click on the green "Commit Changes" button and then again.
  

Step 4: Congratulations, your page has been created and your flash game is ready to play!

Your new page should already be available at this step. So, still on that page, go to Settings on the right, then scroll down a bit and go to Pages in the bottom left corner. 
  
You will see the message "Your page is live at" with the link to it right next to it. 
  
Click on the link or View Site. Voila! Your game should be running on that page.

Step 5: Adding the page to your website/blog and final touches.
  
If you want your audience to access the game on that page, simply share the link with them.
  

If you want them to play directly on your blog or website, I'll teach you how to "Embed" the page you created on your blog/website.

On Blogger

On Blogger, for example, you just need to select "Create a new Post," click the pencil icon below the title, then the "HTML view" option, and paste this line of code:


<iframe src="YourPageLinkHere" width="470" height="600" frameborder="0" allowfullscreen></iframe>.
  

Replace "YourPageLinkHere" with the link to the page you just created on GitHub.
That's all, and your audience will be able to play from your post.
  

On Google Sites

On Google Sites, for example, select a new publication and find the yellow "Embed" icon in the right corner. Then click on "Embed Code" and paste that same code. 
  
Remember to replace "YourPageLinkHere" with the link to the page you just created on GitHub. 
  
For example, it will look like this: 

<iframe allowfullscreen="" frameborder="0" height="600" src="https://y2kgamestinygirl.github.io/MyGameFlash/" width="470"></iframe>

Note that within the code line there are numbers. You can adjust these numbers, decrease or increase them so that the game screen fits better on your website/blog.

I think that's all. I'll make a new tutorial with more details later. For example, how to add more than one game in your repository, the code to change the background color of your Github page and add a cool, colorful border to your game screen. I hope this helps someone. If you have any questions or something doesn't work for you, just ask!

*Note that Ruffle is an incomplete tool and some games may not work properly, have bugs, glitches, or not work at all due to compatibility errors. An example of this is the game Tutti Cuti Ice Cream Parlour. The only place where you can play it properly is in the Flashpoint Browser, which emulates the original old systems, because in Ruffle it has a texture bug that prevents you from adding toppings to the ice cream correctly.
