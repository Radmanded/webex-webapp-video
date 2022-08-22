[Add Webex photo]: # 
# Embedding a Webex SDK video 'Space Widget' into a web app

Tell them what they are going to do...

Take a standard HTML web page and embed a Webex SDK 'Space Widget' to easily enable Webex collaboration.
 
[Add a gif of end product]: #  

## Pre-Reqs
- Git: https://git-scm.com/
- 2 Webex accounts (One for testing)

<details>
<summary>Tutorial</summary>

# Installation

To embed a Space Widget into a web page, we first need to have a web page! A basic HTML/CSS project for the fictitious 'OneBank' company can be downloaded from GitHub, or cloned via Git:
 
## Obtain your Webex Personal Access Token 

[Click here for your Webex Access Token!](https://developer.webex.com/docs/getting-started)

or https://developer.webex.com/docs/getting-started 
 > Important: Copy Personal Access Token for later use
<br/>
 
![CleanShot-Google Chrome202207-14 at 11 17 36](https://user-images.githubusercontent.com/9085386/179029658-ecdb4a93-b1a1-47c9-8d87-4a0af12e15db.png)


## Configure

1. Clone the repository with git 
```
git clone https://github.com/Radmanded/webex-spaceWidget.git

```
<br/>

2. Change to the onebank folder `cd /webex-spaceWidget/onebank` 

<br/>

3. Open `webex-teams.html` in an editor
  -- add your Webex personal access token and an 
  -- add an email address to a webex user that is not yourself
  -- Save the file

<br/>

4. Next make changes to `onebank.html` in your editor
  - Find Line 69, which defines the blue button on the page labeled 'Ask Sandy':
 
 <br/>
 
 `<input type='submit' value='Ask Sandy' name='submit' class='submit' onclick='' />`

<br/>

> Note: the `oneclick` handler is empty

<br/>

5. Place `window.open("webex-teams.html","","height=500,width=450")` inside the `onclick=''`

<br/>

> Example of Line 69 after change:  

```
<input type='submit' value='Ask Sandy' name='submit' class='submit' onclick='window.open("webex-teams.html","","height=500,width=450")' />

```
<br/>

## Test Configuration

1. Open the onebank.html file in your browser

<br/>

2. Right-click on the 'Ask Sandy' button, and choose Inspect Element

> Note: You should see the window.open JavaScript code you entered above:

<br/>

3. Click 'Ask Sandy'

<br/>

4. Check to see that your pop-up window appears, and automatically starts loading the Webex Space Widget. Collaborate away!

</details>


