### DEFINITION
jQiery is a small, lightweight, fast JavaScript library designed to simplify HTML DOM tree traversal and manipulation, as well as event handling, CSS animations and AJAX.

AJAX (Asynchronous JavaScript transfer) is a set of web-development techniques that uses various web technologies on the client-side to create asynchronous web applications. By decoupling the data interchange layer from the presentation layer, Ajax allows web pages and, by extension, web applications, to change content dynamically without the need to reload the entire page. AJAX is not a programming language, rather a concept.

## The Document Ready Event
$(document).ready(
    function(){
        //all jQuery methods go here
    }
)

or,

$(function(){
    //jQuery methods go here
})

This is to prevent the jQuery code from running before the document is ready (finished loading). It is a good practice to wait for the document to be fully loaded and ready before working on it. 

## SELECTORS
The jQuery syntax is such that it can select HTML elements and perform some action on the element.
Basic syntax for jQuery selector:
$(selector).action()

The $ sign is used to define/access the jQuery
A (selector) is used to point/reference at an HTML element you want to make some changes to.
A action() is performed on the selected element.

1. $(this).hide()  -> hides the current element
2. $("p").hide() -> hides all <p> elements
3. $(".test").hide() -> hides all elements with class="test"
4. $("#test").hide() -> hides the element with id="test"

### Commonly used selectors cheatsheet:
1. Element selectors: $("p") , $("button") 
2. #id selector: $("#idName")
3. .class selector: $(".test")
4. All element selectors: $(*)
5. Current HTML element selector: $(this)
6. HTML element selector with specific class: $("p:intro") <p class="intro"></p>
7. First HTML element selector: $("p:first")
8. Anchor element with target as blank(opens in another tab): $("a[target = '__blank']")

## EVENTS
An event represents the precise moment when something happens
In jQuery, most DOM events have an equivalent jQuery method. For example, to assign a click event to all paragraphs on a page:
$("p").click(
    function(){
        //action when the event fires
    }
)
Example,
When a click event fires, hide the paragraph element.
$("p").click(
    function(){
        $(this).hide();
    }
);

$("p").dblclick(
    function(){
        $(this).hide();
    }
)

### Common event methods:
hide(), toggle(), 

## jQuery AJAX
AJAX is the art of exchanging data with a server, and updating parts of a web page without reloading the whole page. It is a programming practice to load the data in the background and display it on the webpage, without reloading the whole page.

With jQuery AJAX methods, you can request text, HTML, XML, JSON from any remote server using both HTTP GET and HTTP POST and you can load the external data directly into the selected HTML.

Note: jQuery makes AJAX code easier because it makes it browser-independent.

### AJAX methods:
#### 1. jQuery load() method:
$(selector).load(URL, data, callback);
The load() method loads data from a server and puts the returned data into the selected element.
URL = the URL you wish to load.
data = set of querystring to be sent along with the request.
callback = The callback function to be executed after the action function load() is completed.

-------------------------------------------------------
$.ajax() v/s $.get()
in the ajax .ajax action method we can specify the method of request to be sent.
however, in get() we can send only get requests. 
--------------------------------------------------------

