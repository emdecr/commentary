#Commentary
##Director's Commentary for your webpage

This jQuery plugin was created for Week 6 of [HackerYou](http://hackeryou.com/)'s Full-time Front-End Bootcamp <3 #hythe6ix

####What is 'Commentary'?
**Commentary** is a jQuery plugin that allows you to add hidden notes to your page that are only visible once the plugin is turned on. 

When *Commentary* is turned on by the user, they'll see chunks of highlighted text/content. When the user clicks on the highlights, new commentary written by you will appear close by. It's like the Director's Commentary in the Special Features on DVDs (*I still buy them*) – but for the web. 

####Getting Started 

Add the *Commentary* folder to your project.

Include the following in the `<head>` section of your html document to link to jQuery and *Commentary*'s styling.

HTML 
`<script src="http://code.jquery.com/jquery-1.11.3.min.js"></script>`
`<link rel="stylesheet" href="commentary/commentary.css">`

Call the .commentaryOn() and .commentaryOff() methods. Include this right before the end of your `</body>`.

HTML
`<script src="commentary/commentary.js"></script>`
`<script> $('#onButton').commentaryOn(); $('#offButton').commentaryOff();</script>`

`#onButton` and `#onButton` are to be replaced with whatever elements (div, img, etc.) that will act as the 'on' and 'off' switches, respectively.

In the [demo](REPLACE LINK WITH GITHUB PAGE), I used two divs with fixed position, so they were visible. I gave the 'on' button an id of `#onButton` and the 'off' button an id `#onButton`. This just makes things a bit more semantic, and easier for you to distinguish these key components.

####Adding Actual Commentary

*Commentary* relies on `<span` tags.

For the text that you will act as the highlighted cue that a user will click on, wrap the content in the following span:

`<span class="cmmtRef">HIGHLIGHTED CUE TEXT GOES HERE</span>`

*OPTION*: You can change the colour of highlighted text by going into the `commentary.css` file, and changing the `background-color` property for `.highlight`.

For the content that will appear when the highlighted span in clicked, wrap it in the following span.
`<span class="cmmtBub">CONTENT THAT WILL APPEAR</span>`

*OPTION*: You can change the styling of the comment bubble by changing the css of `.cmmtBub` in the `commentary.css` file.

**Note**: Be strategic about where you place the comment bubbles (`.cmmtBub`). They're `<span>`s, which means they're inline elements. When they're revealed once the highlighted text appears, they may disrupt the flow of whatever container they're in. Try adding the comment bubble spans to the end of the container, so it doesn't disrupt as much content.

---

I'm working on adding options, and more individualized indications for each comment (ie. puttings numbers next to each comment and their respective comment bubbles, so it's easier to tell which highlights and bubbles go together).

Please do fork this project and submit pull requests :)
