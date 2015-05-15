---
layout: post
title: "Analyzing R-Bloggers' posts via Twitter"
tags: [professional, rstats, r, r-bloggers, shiny, twitter]
date: 2015-05-17 21:30:00 -0700
fb-img: TODO choose an image
---

For those who don't know, every time a new blog post gets added to R-Bloggers, it gets a corresponding tweet by [@Rbloggers](https://twitter.com/rbloggers), which gets seen by Rbloggers' ~20k followers fairly fast. And every time **my** post gets published, I can't help but check up on how many people gave that tweet some Twitter love, ie. "favorite"d or "retweet"ed it. It's even more exciting than getting a Facebook "like" on a photo from Costa Rica! 

Seeing all these tweets and how some tweets get much more attention than others has gotten me thinking. Are there some power users who post almost all the content, or so many blogs contribute equally?  Which posts were the most shared?  Which blog produces the highest quality posts consistently? Is there a correlation between how often a specific blog outputs posts and how successful these posts are?  Are there more posts during the weekdays then weekends? And of course the holy grail of bloggers - is there a day when it's better to post?

I'm going to use some terminology very loosely and interchangeably throughout this post:  

- "blog" == "author" == "contributor"  
- "tweet" == "post"  
- "successful" post == "viral" == "highly shared" == "high score" == "high quality" == "gets Twitter love"

It's cleat that all those terms not necessarily the same thing (for example, varlity does not necessarily mean high quality), but I'll be using them all as the same.

There is also [an accompanying interactive document](http://daattali.com/shiny/rbloggers-twitter/#data-exlorationvisualization) to accompany this post.  That document has a few interactive plots/tables for data that is better explored interactively than with an image, and it also contains all the source code that was used to make the analysis and all the figures here. The source code is also [available on GitHub](https://github.com/daattali/shiny-server/tree/master/rbloggers-twitter) - this is just the raw text version of the interactive document.

(lots of cutting corners: not considering any other social media, not looking at # of times post was shared directly from r-bloggers website, not looking at how much discussion the post generated by only at number of favorites and retweets)
didnt do statistical significance tests, didnt include fb data, didnt include # of shares via tweet button because it looks like most posts pre 2014 mostly have 0 so it'll introduce an unfair bias towards new posts