---
title: "Using PHP Variables in CSS"
date: 2015-07-21
excerpt: <p>Wouldn't it be nice to be able to write CSS, but use variables for commonly used elements like colors and fonts? The good news is, there is! And, it's pretty simple too.</p>
feat-img: css-and-php.jpg
---

Wouldn't it be nice to be able to write CSS, but use variables for commonly used elements like colors and fonts? The good news is, there is! And, it's pretty simple too. All you need to know is a little bit of PHP, and you're on your way to more efficient, easier to write CSS. Plus, if you need to change that color or font, you'll only have to change it in one place instead of who knows how many...Plus, remembering _lightGold_ is much easier than remembering something like _#fceb8d_.

### Getting Started

1\. Change your .css file to .php <br> _(Note: Make sure you change the filename in the call to your stylesheet in your HTML as well)_

2\. Open a php block at the top of your php stylesheet

	<?php ...Your PHP code goes here... ?>

3\. Inside the PHP block, tell the file that it's actually a CSS document with this line of code:

	header("Content-type: text/css; charset: UTF-8");

4\. Write your PHP variables, using the following syntax:

	$primaryColor = "#666666";
	$primaryFont = "Raleway";

### Using the Variables

Using the variables you created is easy. Inside any CSS rule, where you would usually write out the color, font, or other value, replace that with the following code structure:

	<?php echo $primaryColor; ?>

See a full example of this below:

	a {
		color: <?php echo $primaryColor; ?>;
	}

There, you're done! That's wasn't so bad. If you want more on using PHP in CSS, your can learn more with [this article](https://css-tricks.com/css-variables-with-php/) from CSS Tricks.