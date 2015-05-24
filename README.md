#Commentary
##Director's Commentary for your webpage

This jQuery plugin was created for Week 6 of [HackerYou](http://hackeryou.com/)'s Full-time Front-End Bootcamp <3 #hythe6ix

###What is 'Commentary'?
**Commentary** is a jQuery plugin that allows you to add hidden notes to your page that are only visible once the plugin is turned on. 

When *Commentary* is turned on by the user, they'll see chunks of highlighted text/content. When the user clicks on the highlights, new commentary written by you will appear close by. It's like the Director's Commentary in the Special Features on DVDs (*I still buy them*) – but for the web. 

####[Demo](http://emdecr.github.io/commentary/)

###Getting Started 

Add the *Commentary* folder to your project.

Include the following in the `<head>` section of your html document to link to jQuery and *Commentary*'s styling.

HTML 
`<script src="http://code.jquery.com/jquery-1.11.3.min.js"></script>`
`<link rel="stylesheet" href="commentary/commentary.css">`

**Call the .commentaryOn() and .commentaryOff() methods. Include this right before the end of your `</body>`.**

HTML
`<script src="commentary/commentary.js"></script>`
`<script> $('#onButton').commentaryOn(); $('#offButton').commentaryOff();</script>`

`#onButton` and `#offButton` are to be replaced with whatever elements (div, img, etc.) that will act as the 'on' and 'off' switches, respectively.

In the [demo](http://emdecr.github.io/commentary/), I used two divs with fixed position, so they were visible all the way down the page. I gave the 'on' button an id of `#onButton` and the 'off' button an id `#offButton`. This just makes things a bit more semantic, and easier for you to distinguish these key components.

###Adding Actual Commentary

*Commentary* relies on `<span>` tags.

For the text that you will act as the highlighted cue that a user will click on, wrap the content in the following span:

`<span class="cmmtRef">HIGHLIGHTED CUE TEXT GOES HERE</span>`

__*OPTION*__: You can change the colour of highlighted text by going into the `commentary.css` file, and changing the `background-color` property for `.highlight`.

For the content that will appear when the highlighted span in clicked, wrap it in the following span.
`<span class="cmmtBub">CONTENT THAT WILL APPEAR</span>`

__*OPTION*__: You can change the styling of the comment bubble by changing the css of `.cmmtBub` in the `commentary.css` file.

**Note**: You _must_ put the `.cmmtBub` `<span>` after the  `.cmmtRef` `<span>`. Do **not** put another `<span>` in between these two `<span>`s. Something may break. The jQuery used in this plugin relies on the `.next()` method. This method targets the immediately following sibling. 

###Possible Uses

####Easter Eggs
Use this plugin to make an 'easter egg'-version of your site. Include little inside jokes or after thoughts about content on the page.

####Create an interactive 'before and after' site for a piece of writing
Maybe you want to display how you edited an article.

####Just for highlighting
You could just use this plugin for highlighting text -shrugs-. Maybe you want to highlight certain terms or links? Cool. You can do that. Just skip the addition of the `.cmmtBub` `<span>`.

###Styling Tips

The use of this plugin relies on styling and plcement choice. Be strategic about where you place the comment bubbles (`.cmmtBub`). The content's wrapped in a `<span>`, which means it's an inline element. Once the highlighted text is clicked and the bubble appears, they may disrupt the flow of whatever container they're in. Try adding the comment bubble spans to the end of the container, so it doesn't disrupt as much content. 

Styling is also a big part of using this plugin.

---

I'm working on adding options, and more individualized indications for each comment (ie. puttings numbers next to each comment and their respective comment bubbles, so it's easier to tell which highlights and bubbles go together). I'm also trying to make _Commentary_ less intrusive to the html content, so V2 may make the `.cmmtBub` spans appear in a tooltip-like bubble when you hover over the highlighted text. Stay tuned!

Please do fork this project and submit pull requests :)
