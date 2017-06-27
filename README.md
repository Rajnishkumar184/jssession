
### Offline Data Storage Technique

**Web Storage :** The Web Storage API provides mechanisms by which browsers can store key/value pairs.
**Web SQL Database :** The Web SQL Database API isn't actually part of the HTML5 specification but it is a separate specification which introduces a set of APIs to manipulate client-side databases using SQL.
**IndexedDB  :** Like Web Storage, it's a straightforward key-value mapping, but it supports indexes like those of relational databases, so searching objects matching a particular field is fast; you don't have to manually iterate through every object in the store.
**File Access**

#### Cookie:

An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to the user's web browser. The browser may store it and send it back with the next request to the same server. Typically, it's used to tell if two requests came from the same browser — keeping a user logged-in, for example. It remembers stateful information for the stateless HTTP protocol.

Cookies are mainly used for three purposes:

**Session management :** Logins, shopping carts, game scores, or anything else the server should remember

**Personalization :** User preferences, themes, and other settings

**Tracking :** Recording and analyzing user behavior


#### Web Storage


Html5 provides storage api that you can store large amounts of data, without this to affect the  performance of the web app.The Web Storage API provides mechanisms by which browsers can store key/value pairs.

LocalStorage
SessionStorage


**SessionStorage :**
sessionStorage maintains a separate storage area for each given origin that's available for the duration of the page session (as long as the browser is open)

**LocalStorage :** 
localStorage does the same thing, but persists even when the browser is closed and reopened

**_SessionStorage/LocalStorage Methods_**


setItem('key', 'value');  // Save data to Storage corresponding to key.

getItem('key');  // Get saved data from Storage

removeItem('key'); // Remove saved data from Storage

clear(); // Remove all saved data from Storage

````
For Example:

localStorage.colorSetting = '#a4509b';
localStorage['colorSetting'] = '#a4509b';
localStorage.setItem('colorSetting', '#a4509b’);
````

#### JSON (Javascript Object Notation)

JSON is data interchange format like XML it is used to pass data from one application to another from server to client or from client to server, etc.
The syntax of JSON was inspired by the JavaScript Object Literal notation, but there are differences between them.
In JSON all keys must be quoted, while in object literals this is not necessary.

````
For Example:

// JSON:
{ "foo": "bar" }

// Object literal:
{ foo: "bar” }
````

**Serializing and Deserializing Objects in JavaScript using JSON**

converting the javascript literal object to JSON string is known as serialisation  and converting JSON string to javascript literal object is known as deserialisation.

````
For Example :

var obj={name:’abc’};

var obj1=JSON.stringify(obj); // serialize javascript object to json string.

var obj2=JSON.parse(obj1);  // deserialize json object to javascript object.
````




##AJAX (Asynchronous Javascript And XML)

The two major features of AJAX allow you to do the following:

Make requests to the server without reloading the page
Receive and work with data from the server

The XMLHttpRequest object can be used to exchange data with a web server behind the scenes

**XMLHttpRequest Object Methods**

**_new XMLHttpRequest()_** -->	Creates a new XMLHttpRequest object
**_abort()_**	--> Cancels the current request
**_getAllResponseHeaders()_**	--> Returns header information
**_getResponseHeader()_**	--> Returns specific header information
**_open(method, url, async, user, psw)_**	--> Specifies the request

method: the request type GET or POST
url: the file location
async: true (asynchronous) or false (synchronous)
user: optional user name
psw: optional password

**_send()_**  --> Sends the request to the server, Used for GET requests
**_send(string)_** -->Sends the request to the server, Used for POST requests
**_setRequestHeader()_** -->Adds a label/value pair to the header to be sent


**XMLHttpRequest Object Properties**

**_onreadystatechange_** -->Defines a function to be called when the readyState property changes Holds the status of the XMLHttpRequest.
**_readyState_**	
0: request not initialized 
1: server connection established
2: request received 
3: processing request 
4: request finished and response is ready
**_responseText_**	--> Returns the response data as a string
**_responseXML_**	-->Returns the response data as XML data
**_status_**	--> Returns the status-number of a request
200: "OK"
403: "Forbidden"
404: "Not Found"

**_statusText_**	--> Returns the status-text (e.g. "OK" or "Not Found")



#### History API

The History interface allows to manipulate the browser session history, that is the pages visited in the tab or frame that the current page is loaded in.
The HTML5 history API gives you access to the browser navigation history via JavaScript. The HTML5 history API is really useful in single page web apps. A single page web app can use the HTML5 history API to make a certain state in the app "bookmarkable”.


The history object contains the following properties and functions - which comprise the history API:

__length__
__state__
__back()__
__forward()__
__go(index)__
__pushState(stateObject, title, url)__
__replaceState(stateObject, title, url)__



#### SPA(Single Page Application) 

Single Page Application(SPA) is a web application that fits on a single web page with dynamic actions without refreshing the page. Single Page Application interactions can be handle without reaching server. Single Page Application can improve performance in several ways like loading time, using AJAX, easy to navigate pages etc. End users will be more comfortable with Single Page Application, It is very easy to navigate to different page and filter content.

**Features of SPA**

History 
Modal
Ajax
Routing
Templating
Dom Manipulation

**Pros of SPA:**

1. No extra queries to the server to download pages. Single Page Application can improve performance in many ways, Single time file load each of HTML, CSS, JS.Only data is transmitted back and forth.
2. The development is simplified and streamlined. There is no need to write code to render pages on the server. It is much easier to get started because you can usually kick off development from a file file://URI, without using any server at all.
3. SPA can cache any local storage effectively. An application sends only one request, store all data, then it can use this data and works even offline.

**cons of SPA:**

1. Client must enable JavaScript, Single Page Application build with JavaScript, So JavaScript should be enabled in client browser. JavaScript enabled in all modern browsers by default. 
2. Security: Compare to traditional page Single Page Application is less secure due to Cross-site scripting (XSS). it enables attackers to inject client-side scripts into web application by other users.
3. Memory Leak: Memory leak in JavaScript can even cause powerful system to slow down.
