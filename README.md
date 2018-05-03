# webBug
[![Build Status](https://travis-ci.org/DKXXXL/webBug.svg?branch=master)](https://travis-ci.org/DKXXXL/webBug)

A web crawler.

## Compile
git clone & stack build is enough

## Usage
Create file "history", "queue", "nextweb" & "rule" in same directory where the executable locates.

file "queue" is a text file, in which there are lines of http website waiting to be crawled.

file "nextweb" and "rule" is of lines of codes in syntax:

`[WebSitePattern]:::[Next1stPattern]>>>>[Next1stWebSitePattern]>>>> ...`

where *WebSitePattern* is the regular expression of current website to match, and all the string in the content of that website that pass all the regular expression patterns followed by *:::* will be added to *queue* and *output* according to file *nextweb* and *rule* correspondingly.

file "history" will contain all the website the program won't explore anymore.