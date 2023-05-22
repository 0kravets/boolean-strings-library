# boolean-strings-library
<h1>Let's start</h1>

While you're reading this text everything has already changed :). New network appeared, new search engine has been created, new boolean operator's been invented.<br>
That is what I love about **talent sourcing**, everyday you have anything new to learn and discover.<br> 
Here are a few reasons why I decided to create this rep:
<ol>
  <li>That is fun to use (so-to-say) the main tool of R&D teams;</li>
  <li>That definately helps to understand how it works;</li>
  <li>Boolean strings are the sort of technical art for me;</li>
  <li>There're so many new undiscovered sources we can learn together and share our best-working x-ray strings for them.</li>
</ol>

 Hope to see your brilliant examples as well! 

<h1>Boolean operators and basic rules</h1>
<h2>AND</h2>

**Combining multiple terms**

For example, if you’re looking for a Sysadmin who has experience with Linux and is from Israel, the basic string will look like this:

`Sysadmin AND Linux AND Israel`

It means that all keywords must be presented in the resulting records.<br>
Google automatically interprets a space between words as AND, which means you don’t have to type AND, but not every search engine or database does this.<br>
On some databases, you can meet (**&**) instead.<br>
AND operator has precedence in search over OR and NOT.

<h2>OR</h2>

**Getting results that contain either of the terms**

For example, if you’re looking for a Sysadmin from Israel who has experience with Linux or Sysadmin from Israel who has experience with Windows, your basic string will look like this:

`Sysadmin AND (Linux OR Windows) AND Israel`

It’s a good operator to use if your keywords have synonyms or common spellings.<br>
On some search engines (such as Google) you can use (|) instead, but it doesn’t work everywhere. Pay attention that you don’t need to put a space between | and terms:

`Sysadmin (Linux|Windows) Israel`

OR operator has precedence in search over NOT.

<h2>NOT</h2>

**Excluding certain terms**

For example, if you’re looking for a Sysadmin but not a Manager:

`Sysadmin AND Israel NOT Manager`

Google no longer recognizes NOT, you can use (-) instead:

`Sysadmin -Manager -Cat`

<h2>* Asterisk</h2>

**Root word search**

Asterisk can broaden your search by including various word endings:

`manag*` = manager, managing, managerial, managed, managing, managers, and so on.

It doesn’t work on every search engine, for example, Linkedin doesn’t use (*).

<h2>() Parenthesis</h2>

This is essential for complex strings to organize the keywords. Parenthesis will show the search engine that statements inside are separate conditions:

`Sysadmin AND (Linux OR Windows) AND Israel`

`(Sysadmin OR “IT specialist”) AND (Israel OR Cyprus) AND (Linux OR Windows)`

The simple string `Sysadmin AND (Linux OR Windows)` can be written in different ways but will show the same idea:

`Sysadmin (Linux AND Windows)`

`(Sysadmin AND Linux) OR (Sysadmin AND Windows)`

`(Sysadmin Linux)|(Sysadmin Windows)`

Parenthesis has the highest precedence.

<h2>"" Quotation Marks</h2>

**Searching for the exact word or phrase** 

If you add (””) to a single word it will prevent Google from word-stemming it to other options (synonyms or spelling), if you surround a phrase it will search for an exact phrase.

`Sysadmin OR “IT Specialist”`

Using Quotation Marks correctly can give you shorter strings and better results:

`“(Java OR Scala OR Python) (developer OR engineer OR programmer)”` = 

`(“Java developer” OR “Java engineer” OR “Java programmer” OR ”Scala developer” OR “Scala engineer” OR “Scala programmer” OR “Python developer” OR “Python engineer” OR “Python programmer”)`

<h2>? Wildcard</h2>

**replacing any character in a term**

`Angular?js` = Angularjs or Angular.js
