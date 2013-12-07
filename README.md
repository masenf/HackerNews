Hacker News
==========

![Screenshot of the app](http://i.imgur.com/XxS04KP.png)

An open source Hacker News client for Android phones & tablets. 

This fork of Hacker News adds 'Read later' functionality and story caching. Since I don't always have a solid network connection when I have downtime, caching captivating stories and comments beforehand is a valuable feature.

# How to build

**You'll need 4 jar files (or a more recent version):**

- [bugsense-3.5.jar](https://www.bugsense.com/docs)
- [commons-lang3-3.1.jar](http://commons.apache.org/lang/download_lang.cgi)
- [gson-2.2.2.jar](http://code.google.com/p/google-gson/)
- [jsoup-1.7.2.jar](http://jsoup.org/)

Create a "libs" folder at the project root and add these jars to it.

**Additionally, you'll need two of my library projects:**

- [HoloTheme](https://github.com/bishopmatthew/HoloTheme)
- [DatabaseUtils](https://github.com/bishopmatthew/DatabaseUtils)

HoloTheme is a collection of useful code I share between projects. Some of it is oriented towards using Holo-themed widgets on Android 2.1+. It requires the Android support library be put in the "libs" directory.

DatabaseUtils is a really simple ORM that uses reflection to do CRUD operations on objects that extends SqlObject. 

Clone both repositories, and then import them into eclipse. Then add them as library projects to HackerNews.

**Finally, you will need to either put the API key for your own [Bugsense](http://www.bugsense.com/) account** into `res/strings.xml` as `bugsense_api_key`, or **remove the `BugSenseHandler.initAndStartSession()` call** in [SlideoutMenuActivity](https://github.com/bishopmatthew/HackerNews/blob/master/src/com/airlocksoftware/hackernews/activity/SlideoutMenuActivity.java#L65)

# Design Overview

I've outlined the design in in [this wiki article](https://github.com/bishopmatthew/HackerNews/wiki/Design-Overview). This might also be helpful if you're interested in writing Android apps.

# How to help

If you tackle any of the issues on the tracker, that would be great! I've added a few enhancements there with a pretty detailed description of what needs to be done.

# License

The MIT License (MIT)
Copyright (c) 2013 Matthew Bishop

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


The code will be here later today, for now you can use issues for bug reports or feature requests.
