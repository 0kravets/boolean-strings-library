# boolean-strings-library
# Let's start

While you're reading this text everything has already changed :). A new network appeared, a new search engine has been created, and new boolean operator's been invented.<br>
That is what I love about **talent sourcing**, every day you have anything new to learn and discover.<br> 
Here are a few reasons why I decided to create this rep:
<ol>
  <li>That is fun to use (so-to-say) the main tool of R&D teams;</li>
  <li>That definitely helps to understand how it works;</li>
  <li>Boolean strings are the sort of technical art for me;</li>
  <li>There're so many new undiscovered sources we can learn together and share our best-working x-ray strings for them.</li>
</ol>

 Hope to see your brilliant examples as well! 

# Table of Contents

- [Boolean operators and basic rules](#boolean-operators-and-basic-rules)
  - [AND](#and)
  - [OR](#or)
  - [NOT](#not)
  - [Asterisk](#asterisk)
  - [Parenthesis](#parenthesis)
  - [Quotation Marks](#quotation-marks)
  - [Wildcard](#wildcard)
- [Strings library](#strings-library)
  - [Before we start](#before-we-start)
  - [CODERWALL](#coderwall)
  - [CRUNCHBASE](#crunchbase)
  - [KAGGLE](#kaggle)

# Boolean operators and basic rules

## AND

**Combining multiple terms**

For example, if you’re looking for a Sysadmin who has experience with Linux and is from Israel, the basic string will look like this:

`Sysadmin AND Linux AND Israel`

It means that all keywords must be presented in the resulting records.<br>
Google automatically interprets a space between words as AND, which means you don’t have to type AND, but not every search engine or database does this.<br>
On some databases, you can meet (**&**) instead.<br>
AND operator has precedence in search over OR and NOT.

## OR

**Getting results that contain either of the terms**

For example, if you’re looking for a Sysadmin from Israel who has experience with Linux or Sysadmin from Israel who has experience with Windows, your basic string will look like this:

`Sysadmin AND (Linux OR Windows) AND Israel`

It’s a good operator to use if your keywords have synonyms or common spellings.<br>
On some search engines (such as Google) you can use (|) instead, but it doesn’t work everywhere. Pay attention that you don’t need to put a space between | and terms:

`Sysadmin (Linux|Windows) Israel`

OR operator has precedence in search over NOT.

## NOT

**Excluding certain terms**

For example, if you’re looking for a Sysadmin but not a Manager:

`Sysadmin AND Israel NOT Manager`

Google no longer recognizes NOT, you can use (-) instead:

`Sysadmin -Manager -Cat`

## Asterisk

**Root word search**

Asterisk can broaden your search by including various word endings:

`manag*` = manager, managing, managerial, managed, managing, managers, and so on.

It doesn’t work on every search engine, for example, Linkedin doesn’t use (*).

## Parenthesis

This is essential for complex strings to organize the keywords. Parenthesis will show the search engine that statements inside are separate conditions:

`Sysadmin AND (Linux OR Windows) AND Israel`

`(Sysadmin OR “IT specialist”) AND (Israel OR Cyprus) AND (Linux OR Windows)`

The simple string `Sysadmin AND (Linux OR Windows)` can be written in different ways but will show the same idea:

`Sysadmin (Linux AND Windows)`

`(Sysadmin AND Linux) OR (Sysadmin AND Windows)`

`(Sysadmin Linux)|(Sysadmin Windows)`

Parenthesis has the highest precedence.

## Quotation Marks

**Searching for the exact word or phrase** 

If you add (””) to a single word it will prevent Google from word-stemming it to other options (synonyms or spelling), if you surround a phrase it will search for an exact phrase.

`Sysadmin OR “IT Specialist”`

Using Quotation Marks correctly can give you shorter strings and better results:

`“(Java OR Scala OR Python) (developer OR engineer OR programmer)”` = 

`(“Java developer” OR “Java engineer” OR “Java programmer” OR ”Scala developer” OR “Scala engineer” OR “Scala programmer” OR “Python developer” OR “Python engineer” OR “Python programmer”)`

## Wildcard

**replacing any character in a term**

`Angular?js` = Angularjs or Angular.js

# Strings library

## Before we start

We will create a list of creative boolean strings for unconventional sources when traditional sourcing methods don't work. <br>
But firstly make sure, that you're sick and tired of searching the basics (ATS, databases, CRMs, and LinkedIn) because the basic strategies have the higher ROI at the end. <br> 
Now, let's start

## CODERWALL

What is Coderwall?<br> 
Coderwall is a digital portfolio platform for programmers. Pulls data from Github, Bitbucket, and StackOverflow to form a digital portfolio. Users can earn badges by collaborating on projects and participating in competitions.<br> 
It is a developer community used by nearly half a million developers each month to learn and share programming tips.<br> 

**Website** coderwall.com<br> 

The structure of the platform is really simple
- after coderwall.com/ goes nickname of a user coderwall.com/hannamantana
- on the page users could fill in their name, picture, current job title, and company, write a short summary about themselves, their interests and skills, and even leave links to other social accounts:
<img width="1301" alt="coderwall" src="https://github.com/0kravets/boolean-strings-library/assets/133959902/588e90d3-0a2b-4452-8253-372eef63476b">

A basic boolean string for this type of website structure will look pretty simple:

`site:coderwall.com "Java Developer”`

I would recommend adding the additional word **profile** to exclude all the forum conversation threads and see profile pages. <br>
Plus, I wouldn't use any keywords for "developer, development, developing, etc." as it really decreases the amount of results, and to be honest, this is a platform for coders, programmers, and developers, we know that in advance. <br>

`site:coderwall.com profile Node.js`

**Downsides**

- it is difficult to break it by location, so be prepared to look through people from all over the world
- unfortunately, there no many new profiles created over the last few years, basically ROI will be very low, but you always can find a gem, someone who left any clues for you, where to find them now  

## CRUNCHBASE

Yes, the leading provider of private-company prospecting and research solutions. 75 million users—including salespeople, entrepreneurs, investors, and market researchers use it, so there is a high chance to find who we're looking for.<br>

**Website** crunchbase.com<br>

The structure of the platform is pretty simple, we're more interested in subscribed people:
- this part will be: crunchbase.com/person/someones name
- on the page, you can see CB rank (see most active people), Location (if it's been filled), Region, linked for other networks, short summary, and even job history and education

A basic boolean string will look like this:

`site:crunchbase.com/person CTO Poland`

**Downsides**

- unfortunately, you need to buy a subscription to open more than 10 pages a day, and at first glance, there is no way to avoid it, so if you're lucky to have a corporate subscription, use it
- it is possible to start your free trial

There is a helpful way to use these 10 pages a day, as an additional source of finding new people on the Internet, using Google's (I use Google as a browser) "Tool" and just filtering new pages (aka new/changed profiles) or last activities on pages, by "Past 24 hours", "Past week" etc. It looks like a good way to search for new Founders and C-level in your area.

## KAGGLE

It is the world's largest online data science & machine learning practitioners community.<br>

**Website** kaggle.com<br>

The website has a clear structure, you can search through Competitions (kaggle.com/competitions) or Code (kaggle.com/code) but people's pages have the address of kaggle.com/yourname, so we need to break it by using profile's attribute and not to search through the discussion pages like kaggle.com/getting-started/.<br>

I will use “joined * ago” phrase to jump into people's pages, as these words clearly identify personal pages. 

`site:kaggle.com “joined * ago” “poland”`

**Downsides**

- not everyone mentions locations so it is difficult to say if people in your location really us it. I hardly believe that in Israel only 700 people are using Kaggle
- you will see in results links for the same person a few times (so not even 700, ah?), actually the more person contribute to the conversations the higher chances that you will see their profile not only once

It is a nice tool especially if you hire gems from the data science scene. It can help to understand what these people like and which trends they follow. If you're allowed to hire globally, or remote people I would definitely recommend checking "User Rankings" and finding the best of the best. And please read more about the ranking system https://www.kaggle.com/rankings because it will help you to understand people's profiles better.
