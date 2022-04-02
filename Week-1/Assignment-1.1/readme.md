# Assignment 1.1

Hi! I'm **Goura Gopal Dalai**, student at Pesto! Please find my assignment in this document.
**When a user enters an URL in the browser, how does the browser fetch the desired result? Explain this with the below in mind and Demonstrate this by drawing a diagram for the same.**
1. What is the main functionality of the browser?
2. High Level Components of a browser
3. Rendering engine and its use
4. Parsers (HTML, CSS, etc)
5. Script Processors
6. Tree construction
7. Order of script processing
8. Layout and Painting


# Solution to Assignment 1.1

## When a user enters an URL in the browser, how does the browser fetch the desired result?

When a user types a website URL such as https://pesto.tech in the web browser, the following processes will happen behind the scenes:
1. Browser will try to find the IP address of the URL in the following way: 
**i.** The Browser will search for the website's DNS records in the local cache (browser's own cache). DNS is just like a phonebook having list of websites mapped to corresponding IP address.
**ii.** Secondly, if DNS not found in browser's cache, the browser will search the record in the Operating System Cache.
**iii.** If still not found, the browser will search in router cache.
**iv.** Then in ISP's cache - which should be the last hope for finding the requested URL.
**v.** If still not found - the DNS server will try to find the host server for the URL https://pesto.tech, and will return back to the browser in the same path it went. 
These requests are sent using small data packets that contain information such as the content of the request and the IP address it is destined for (IP address of the DNS recursor). These packets travel through multiple networking equipment between the client and the server before it reaches the correct DNS server. This equipment use routing tables to figure out which way is the fastest possible way for the packet to reach its’ destination. If these packets get lost, you’ll get a request failed error. Otherwise, they will reach the correct DNS server, grab the correct IP address, and come back to your browser. [Source](https://medium.com/@maneesha.wijesinghe1/what-happens-when-you-type-an-url-in-the-browser-and-press-enter-bb0aa2449c1a)
2. The browser initiates a TCP connection with the server.
3. The browser sends an HTTP request to the webserver.
4. The server handles the request received.
5. The server sends out an HTTP response.
6. The browser displays the HTML content.
![What happens when you type a URL in the web browser?](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-happens-when-you-type-a-url-in-the-web-browser-request-response-f68c0cb95019db02.jpg)
## What is the main functionality of the browser?

A web browser's primary function is to **render HTML**, the code that is used to design or “mark up” web pages. When a browser loads a web page, it processes the HTML, which may contain text, links, and references to images and other items like CSS and JavaScript functions.

## High Level Components of a browser

The browser's main components are:

1.  **The user interface**: this includes the address bar, back/forward button, bookmarking menu, etc. Every part of the browser display except the window where you see the requested page.
2.  **The browser engine**: marshals actions between the UI and the rendering engine.
3.  **The rendering engine** : responsible for displaying requested content. For example if the requested content is HTML, the rendering engine parses HTML and CSS, and displays the parsed content on the screen.
4.  **Networking**: for network calls such as HTTP requests, using different implementations for different platform behind a platform-independent interface.
5.  **UI backend**: used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. Underneath it uses operating system user interface methods.
6.  **JavaScript interpreter**. Used to parse and execute JavaScript code.
7.  **Data storage**. This is a persistence layer. The browser may need to save all sorts of data locally, such as cookies. Browsers also support storage mechanisms such as localStorage, IndexedDB, WebSQL and FileSystem.
![](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/layers.png)

## Rendering engine and its use

A rendering engine is software that draws text and images on the screen. The engine draws structured text from a document (often HTML), and formats it properly based on the given style declarations (often given in CSS). Examples of layout engines: Blink, Gecko, EdgeHTML, WebKit.

## Parsers (HTML, CSS, etc)

-   Parsing and Rendering turn the HTML content into a web page with colors and backgrounds and pictures.
-   **HTML Parsing:**  HTML Text -> Tokenization -> DOM Tree
-   **CSS Parsing:**  CSS Text -> Tokenization -> CSSOM Tree
-   DOM and CSSOM are merged to form a Render Tree
-   Render Tree has all the information required to mark and paint the screen.
-   Render Tree -> Layout -> Paint
-   The layout does the maths for placing the elements
-   Paint paints the elements with colors, backgrounds, shadows, etc.

## Script Processors


## Tree construction



## Order of script processing



## Layout and Painting



