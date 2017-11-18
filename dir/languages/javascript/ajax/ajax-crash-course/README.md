# AJAX Crash Course (Vanilla JavaScript)
**Author**: [Traversy Media](https://www.youtube.com/user/TechGuyWeb)  
**URL**: [Video](https://youtu.be/82hnvUYY6QA)  
**Duration**: 01:09:42  
**Donate to Author**: [Patreon](https://www.patreon.com/traversymedia)  

## Table Of Contents
1. [What is AJAX](#what-is-ajax) (00:57)
1. [Diagram How it works](#diagram-how-it-works) (01:59)
1. [Basic idea of the web](#basic-idea-of-the-web) (00:00)
1. [With AJAX...](#with-ajax) (00:00)
1. [XmlHttpRequest (xhr) Object](#xmlhttprequest-xhr-object) (04:07)
1. [Libraries and Other Methods](#libraries-and-other-methods) (05:06)
1. [Get A Text File](#Get A Text File)
## +


## What is AJAX
1. Asynchronous JavaScript & XML
   Its not a language, framework or a library. A set of web technologies to send and receive data from a web client to a server asynchronously.

   Its all done behind the scenes without having to reload the web page.

   XML is rarely used anymore. jQuery has taken its place. Will be working with JSON more so than XML.

1. Set of web technologies
1. Send & receive data asynchronously
1. Does not interfere with current web page
1. JSON has replaced XML for the most part



## Diagram: How it works
![Layout](https://raw.github.com/elwoodberry/education/master/_img/diagrams/ajax-crash-course__001.png)

## Basic idea of the web
[SERVER] > Common request & Response > [CLIENT]

1. You click (make a request) a link on a website.
1. A common request is sent to the server.
1. A common response is returned to the client(browser).
1. You request everything and you get everything.

## With AJAX...
[SERVER] > XmlHttpRequest > AJAX Engine > JS Call > [CLIENT]

1. Allows you to make the call to the server asynchronously in the background without having to reload the page.
1. Request is made with JavaScript or a library.
1. Response is returned in XML/JSON format
1. Request is made using the 'XmlHttpRequest' object.

## XmlHttpRequest (xhr) Object

1. API in the form of an object
   It has properties and methods attached to it.

1. Provided by the browser's JS environment
1. Methods transfer data between client/server
1. Can be used with other protocols then HTTP
1. Can work with data other than XML(JSON, plain text)


## Libraries and Other Methods
1. [jQuery](https://jquery.com/) - DOM manipulation library
1. [Axios](https://www.axios.com/) - Slim library
1. [SuperAgent](https://github.com/visionmedia/superagent) - Slim library
1. [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) - Baked into your favorite browser
1. [Prototype](http://prototypejs.org/) - Library
1. [Node HTTP](https://nodejs.org/api/http.html) - Node HTTP server

## Get A Text File
1. Create an HTML File
1. Add A Button
    ```
    button(id="button" class="btn btn-primary btn-lg" role="button") Get Text File!  
    ```
1. Add an event listener for a click on that button.
    ```
    document.getElementById('button').addEventListener('click', loadText);
    ```
1. Create a 'load text' function.
    ```
    function loadText(){

    }
    ```
1. **Test**: Console log the click
    ```
    console.log('Test The Click');
    ```
1. Create 'sample-text__00001.txt'
1. Create 'xhr' for XmlHttpRequest Object
    ```
    const xhr = new XMLHttpRequest();
    ```
    * **Make** The Request  
    * **Type** of Request  
    * **URL** of Request
1. Open Function
    Parameters (type, url/file, async)
    ```
    xhr.open('GET', 'sample-text__00001.txt', true);
    ```

1. Onload Function
    ```
    xhr.onload = function(){
      // Check for status of the response
      if(this.status == 200)
    }

    // Sends request
    xhr.send();
    ```
    status
    * HTTP Statuses
    * 200: "OK"
    * 403: "Forbidden"
    * 404: "Not Found"

1. OnReadyStateChange Function