---
title: "Hosting, DNS, and Caching Issues"
date: 2015-07-09
excerpt: <p>Switching hosting companies can be tough, especially if you want to transfer peices at a time. Specifically, I worked through transferring a WordPress install to the new hosting company, without the domain name being transferred yet. Here are some helpful tips I've collected as I've learned about hosting, DNS, caching, and more.</p>
feat-img: hosting-name-servers.jpg
---

Switching hosting companies can be tough, especially if you want to transfer peices at a time. Specifically, I worked through transferring a WordPress install to the new hosting company, without the domain name being transferred yet. Here are some helpful tips I've collected as I've learned about hosting, DNS, caching, and more.

### What is DNS?

DNS means domain name system. Basically, they connect web pages with their domain names. Without DNS, people would have to type in a website's IP address to access the site. Domains make things a lot simpler. Aren't you glad you don't have to remember a long string of numbers just to get to Google or Facebook? Well, I am.

You can easily find any website's IP address with a command prompt. For example, in Terminal use this simple command:

	nslookup

Follow this command with a space, and the website's url. [(Thanks to the Bohemian Blog for this info)](http://www.bohemianalps.com/blog/2007/nslookup/)

### The Challenge

So the challenge is to install wordpress on a new host, with the domain still pointing to the old website. First, you'll back-up your WordPress installation on the  OLD server and then move it to the new server. See [this article from the Wordpress Codex](https://codex.wordpress.org/Moving_WordPress) for more information on how to do this.

#### **Issue #1:** Your WordPress Install returns a Server Not Found error. 

This is because the domain name is still pointing to your old site, and wordpress gets confused on what you're trying to access. To fix this to work on your computer, you'll have to edit the hosts file on your computer. Here's [a link](http://www.tekrevue.com/tip/edit-hosts-file-mac-os-x/) on how to do this on a Mac.

#### **Issue #2:** It's still not working...

Know that your computer keeps a DNS cache for websites you've visited, so the edits you just made to the hosts file are actually doing nothing, until you clear your local DNS cache. Here's a link from Apple on [how to clear your DNS cache](https://support.apple.com/en-us/HT202516).

#### **Issue #3:** It's STILL not working...

If you've completed these steps and there still seems to be issues, there is a larger problem, most likely with your hosting DNS configuration. Contact your hosting company, and see if migrating WordPress on your website without transferring the domain name will be possible.

**Good Luck!**

