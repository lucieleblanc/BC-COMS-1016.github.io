<ul id="ProjectSubmenu">
    <li><a class="home" href="../index.html" title="Home">Home</a></li>
    <li><a class="syllabus" href="../syllabus.html" title="Syllabus">Syllabus</a></li>
    <li><a class="assignments" href="../assignments.html" title="Assignments">Assignments</a></li>
    <li><a class="resources" href="../resources.html" title="Resources">Resources</a></li>
</ul>

<link rel="stylesheet" type="text/css" href="../stylesheet.css" />

# Crowdsourcing and Human Computation

##Programming Assignment 1 : Due TBA 

In this assignment, we will be collecting data from Twitter which we will use to train our sentiment classifiers. Scraping Twitter for news and sentiment data has become a huge deal for businesses and researchers, and not *just* because people care about [kittens](https://twitter.com/CatsPorn/status/367992670745927680/photo/1). Governments and academics are interested in whether Twitter and other [social media can reveal breaking news](http://homepages.inf.ed.ac.uk/miles/papers/short-breaking.pdf) before news networks can, and [many investors](http://www.sntmnt.com/), despite all [economic theory](http://en.wikipedia.org/wiki/Efficient_market_hypothesis), believe social media can help them beat the market. Being able to use Twitter data at scale is a great skill for graduating computer scientists and business-minded students, and not a bad starting point for those of you who want to get rich ([boost UPenn's ranking!](http://www.forbes.com/2008/05/19/billionaires-harvard-education-biz-billies-cx_af_0519billieu_slide_4.html)) and spend your 30s sipping cocktails on rooftop terraces.

We are providing you with code that makes it very easy to search Twitter for keywords and grab the ones you want, but we encourage you to play around with the code and extend it. We will be using [tweepy](http://pythonhosted.org/tweepy/html/index.html), which, like all python packages, is hosted on github, is well documented, and has a cutesy name involving 'py'. 	

1. Download and install tweepy from [github](https://github.com/tweepy/tweepy). If you have never installed code from github before, its very just. Just open a terminal and run the following commands:

<ul>
<li><code>$ git clone https://github.com/tweepy/tweepy.git</code>
<li><code>$ cd tweepy</code>
<li><code>$ sudo python setup.py install</code>
<li>type pas$word123, or whichever other unhackable password you are using.
</ul>

2. Download our [script](../../../assignments/ccb-scraper.py) for pulling data from Twitter using tweepy. (Courtesy of [Ryan Cotterell](https://github.com/ryancotterell), guru of all things python).

3. To run the script in the command line:
<ul>
<li><code>$ python get_tweets.py [n] keyword1 [keyword2 ... keywordn]</code></li>
</ul>
- where <code>n</code> is (optionally) the maximum number of tweets to grab and keywords are the words you want to search for. You must give at least one keyword. If you leave out the <code>n</code> parameter, you will continue to get tweets in a stream until you kill the program.

4. Collect 1000 tweets which reference a company of your choice.

<ul>
<li><code>$ python get_tweets.py 1000 Apple > apple_tweets.txt </code></li>
</ul>

5. Grab a random sample of 100 tweets and manually label them for sentiment (positive, negative, or neutral). You will use your own labels later to check that Turkers are doing their work well (or at least as well as you are).

<ul>
<li><code>$ cat apple_tweets.txt | shuf | head -100 > labeled_apple_tweets.txt </code></li>
</ul>





