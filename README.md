# HTML

### Switches to connect devices

In essence, the communication is pretty intuitive. Clients send messages to servers requesting data, and servers respond with the required data, but how is this data transferred? The answer requires defining the structure of the Internet first.

The Internet comprises of devices known as switches that facilitate the connection of each device to every other device on the network. The devices themselves are referred to as end-systems, and which is essentially just a fancy term for the computer you’re using to access this webpage right now!

End-systems are connected to switches through links and all of the switches are, in turn, connected to each other, thus ensuring that every end-system on the Internet is implicitly connected to every other end-system.

switches facilitate the communication between any two end-systems by forwarding packets along the path that they know exists between the packet source and destination. So basically, switches store pre-determined paths between end-systems and forwards packets among them.

### Routers

A commonly heard term when it comes to networks is routers. Routers have the same function as switches per se in that they also connect end systems to the rest of the web. However, routers are actually very different from switches since they have the additional capability of allowing lookups for destination addresses and determining the shortest or the least busy path from the source of a packet to its destination. Routers are, therefore, a more powerful version of switches and the Internet comprises of a mix of both routers and switches that facilitate the transfer of data between end-systems.

### Data packets

Now that we have established how the Internet is structured to ensure connectivity let’s talk about how data is actually transported across the network. This is done by dividing the data, which is just a set of bits, that needs to be transferred into several smaller chunks of bits known as packets and then sending each packet to its destination independently. The reason for this is that you cannot always send large amounts of data in a single packet because it is highly likely that data in large packets get corrupted on the path from its source to its destination due to a bit flip during transmissions. It is, therefore, more efficient and reliable to send multiple smaller packets.

### TCP

The primarily used protocol for communication between a web application and a browser is referred to as the Transmission Control Protocol (TCP)

TCP is a transport layer protocol that takes the responsibility of transmitting data and ensures reliable data transfer between clients and servers across the web. The way TCP does this is by adding additional information to data packets that allow for packet authentication and by allowing the exchange of acknowledgment messages between the client and server to confirm data transmissions.

The TCP protocol starts with a 3-way handshake. The handshake allows both ends (server and client) to initiate and maintain several TCP connections at once.

---

### HTTP & HTTPS

We have just learned that clients and servers communicate with each other by initiating TCP connections and then sending messages to one another. Now, we will look into exactly how these messages are structured.

HyperText Transfer Protocol, commonly referred to as HTTP, is an application layer protocol that dictates how the messages a client and server exchange on the web are structured as well as how they are exchanged. The client program and server program talk to each other by exchanging HTTP messages, and the benefit of HTTP is that it ensures messages are being delivered intact and in time.

This may seem ambiguous, but the high-level idea is that HTTP is built on top of TCP and creating an HTTP server for your web application basically just means that you are creating a server that clients create TCP connections with for reliable data transfer. In simple terms, HTTP is the means through which you can make sure your application is using TCP to transmit messages from clients to the server and vice versa. So basically, when you enter a URL in your browser, what actually happens is that an HTTP command gets sent to the server hosting the application to fetch and transmit the requested web page through TCP.

 HTTPS is an acronym for HyperText Transfer Protocol Secure, and it is basically just the secure version of HTTP. What this means is that communications between the browser and the hosting server are encrypted so that no third parties on the network can access information that is not intended to be shared.
---

### Ports

So far, we have discussed both the transport layer protocol as well as the application layer protocol that ensures efficient communication between end-systems on the web. But, where exactly do the messages these protocols allow end-systems to go? Ports are the endpoints of the communication between clients and servers. That is to say; ports are where messages from the network arrive on an end-system

We briefly discussed sockets earlier and talked about how they are the gateways to processes; sockets are opened on ports in order to allow processes to send and receive messages. Ports are designated by numbers, and all ports below 1024 are associated with a specific protocol each by default. The port number for HTTP, for instance, is 80, and what this means is that any messages you send or receive on the web come in to and leave your machine on a socket at port 80. Ports above 1024 are open ports available to programmers to use for any process they want to communicate with a network. They can build sockets on these ports and define the structure and type of messages this socket can cater to through socket programming. Socket programming is an aspect of Computer Networks that is beyond the scope of this discussion, but it is a highly useful skill to get under your belt and should definitely be looked into if you are interested in the field.

### Table

* Header Tag


* Title 
> what show on tab

```
<head>
  <title></title>
</head>
```

* Meta
> This tag can be used in several ways but we're going to add in a couple of the most common ones that we want to include in every page.

```
<head>
    <title>The Name of Our Page</title>
    <!-- define the character encoding. -->
    <meta charset="UTF-8">
    <!-- gives the browser information about dimension and scaling. It's useful as we start to create responsive sites. -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

```


---

* **Body Tag**

* HTML Attributes
> HTML attributes provide additional information about an HTML element. Attributes can be considered as properties of the element. An element may have a single attribute, many attributes, or no attributes at all. There are no spaces between the attribute name, = sign, and the attribute value.

```
<h2 title="This is a subheading">Hello, World!</h2>
<tagName attribute_name="attribute_value" style="color:blue"></tagName>
```


* link
> An anchor which creates a hyperlink to things like other HTML pages, files, email addresses, and more
* Email Addresses (mailto:someone@educative.io)
* Phone Numbers (tel:+18004444444)
* Documents/Files (Give the URL of the file instead of a web page)
* Another different location on the same web page the browser is currently on

An absolute URL provides all the information necessary for a browser with an internet connection to reach the desired address. Furthermore, an absolute URL will not change its destination if used on different devices/browsers.

```
<a href="https://google.com">Go to Google</a>
```

Relative URLs provide less information than absolute URLs and generally refer to pages on the same domain. Relative URLs are useful when you start to deal with multiple web pages on your site, and want a way to navigate between them.

quick example of a directory named website with:

* a main index.html page
* an about section, named about.html
* a nested directory named blogPosts, with three article HTML files named:
  * article1.html
  * article2.html
  * article3.html

> how would we navigate back to the index.html page if we are in the blogPost directory? We can accomplish this by indicating the path to the file is one direct level up, like so: ../index.html.

```
<a href="about.html">About</a>
<a href="blogPost/article2.html">Article 2</a>

<html>
 <head>
   <title>Exercise 4</title>
 </head>
 <body>
     <a href="blogPost/about.html">About</a>
 </body>
</html>
```


```
<p></p>
```

```
<h1></h6>
<p></p>
```

* img 
```
<img src="" alt="" >
```

* break line 
> used to create a line break on our page. You can think of it like hitting enter in a word document. It will force the content to drop down a line.
```
<br>
```

* List
> Ordered List - We create an ordered list using the <ol> tag. This is the parent element and will have any number of <li> list items inside.

```
<body>
    <ol>
        <li>Item One</li>
        <li>Item Two</li>
        <li>Item Three</li>
    </ol>
</body>
```

> Unordered List - We create an unordered list using the <ul> tag. Once again this will be filled with any number of <li> list items.

```
<body>
    <ul>
        <li>Item One</li>
        <li>Item Two</li>
        <li>Item Three</li>
    </ul>
</body>
```

---

* **Table**


```
<table>
    <tr>
        <th>First Name</th>
        <th>Last Name</th>
    </tr>
    <tr>
        <td>Lebron</td>
        <td>James</td>
    <tr>
</table>
```


* Table Row

> Table row is defined by the <tr> tag

```
<table>
    <tr> </tr> 
</table>
```

* Table Data Cell/Point

> A table data/cell is defined with the <td> tag. Listing multiple <td> elements one after the other will create columns within a table row.

```
<table>
  <tr>
    <td>Name 1</td>
    <td>Note 1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>Name 2</td>
    <td>Note 2</td>
    <td>2</td>
  </tr>
</table>
```
* Table Header

> To designate a heading for a column or row of cells use table header element <th>. By default, table headings are bold and centered.

```
<tr>
  <th>First column header</th>
  <th>Second column header</th>
  <th>Third column header</th>
</tr>
```



* Table Caption

> To add a heading for a table use a caption element <caption>. The <caption> element must be inserted immediately after the <table> element.

```
<table>
  <caption>Heading of the table</caption>
  ...
</table>
```
* Examples

```
    <table>
      <caption>Jan 1st - Feb 14th</caption>
      <tr><th>Expenses</th><th>Cost</th></tr>
      <tr><td>Fuel costs</td><td>6000 BDG</td></tr>
      <tr><td>Hotel</td><td>1500 BDG</td></tr>
      <tr><td>Fun</td><td>900 BDG</td></tr>
      <tr><td>Food</td><td>500 BDG</td></tr>
    </table>
```

---

### Form

To add a form to a page, use the <form> element, which identifies where on the page control elements will appear.

```
<form action="/login" method="POST">
</form>
```

An HTML form contains form elements. Form elements are different types of input elements, like text fields, checkboxes, radio buttons, submit buttons, and more.

> type attribute is what allows us to tell HTML what type of input we want to use. The second attribute name will be used to identify the information that the user types in

> added an id attribute to our input tag. In order for our label to work correctly the id of our input needs to match the for attribute on the label. In our example both are given the value of "id-first-name".

```
<input type="text" name="name">
<input type="date" name="birthday">
<input type="time" name="game-time">
<input type="email" name="email-address">
<input type="url" name="website">
<input type="number" name="cost">
<input type="tel" name="phone-number">
```

> To write a short hint that describes the expected value of an input field, use placeholder attribute. This hint is shown before the user enters a value.

```
<input placeholder="Your name" type="text" name="name">
```

> Another element that’s used to capture text-based data is the <textarea> element. The <textarea> element can accept larger passages of text than <input> element. Also, you can make <textarea> field resizeable.

```
<textarea name="comment">Add your comment here</textarea>
```

```
    <form>
      <h2>Leave your awesome comment</h2>
      <input name="myfriendname" placeholder="Your name">
      <input name="email-address" placeholder="Your email address">
      <textarea>Add your awesome comment here</textarea>
      <input type="submit" name="submit" value="Send">
    </form>
```

```
        <form>
            <label for="first-name">First Name</label>
            <input id="first-name" type="text" name="first_name">
            <br />

            <label for="last-name">Last Name</label>
            <input id="last-name" type="text" name="last_name">
            <br />

            <label for="user-email">Email</label>
            <input id="user-email" type="text" name="email">
            <br />

            <label for="user-password">Password</label>
            <input id="user-password" type="password" name="password">
            <br />

            <button>Register</button>
        </form>
```

<!-- Checkbox -->
<!-- Ctrl-D , Tab -->
```
        <form>
            <input id="id-one" type="checkbox" name="option-one">
            <label for="id-one">Option One</label>
            <input id="id-two" type="checkbox" name="option-two">
            <label for="id-two">Option two</label>
            <input id="id-three" type="checkbox" name="option-three">
            <label for="id-three">Option three</label>
        </form>
```

<!-- Radio -->
```
        <form>
            <input id="twenty-thirty" type="radio" name="age_group" value="20-30">
            <label for="twenty-thirty">20-30 Years Old</label>

            <input id="thirty-forty" type="radio" name="age_group" value="30-40">
            <label for="thirty-forty">30-40 Years Old</label>

        </form>
```

<!-- Drop Down -->
```
        <form>
            <label for="user-city">Select Your City</label>
            <select id="user-city" name="city">
                <option value="usa">USA</option>
                <option value="tokyo">Tokyo</option>
            </select>
        </form>
```

<!-- text area -->
       <form>
            <label for="user-message">Message</label>
            <textarea id="user-message" name="message" cols="30" rows="10">

            </textarea>
        </form>

---

* Div

---

# CSS

CSS rule-set consists of a selector and a declaration blocks:

* the selector which points to the HTML element you want to style

  * Selectors generally target an attribute value (id or class value) or type of element (<h1> or <p>)

  ```
  p { ... }
  h1 { … }
  ```
  * Selectors are classified by type, class, and id.

* the declaration block which contains one or more declarations separated by semicolons
 * Each declaration includes a CSS property name and a value, separated by a colon.

 ```
 p {
  color: blue;
  font-size: 32px;
}
 ```

 * class attribute

 ```
 <p class="brand">Sole Shoe Company</p>

 .brand {
}
 ```

 > multiple class attribute

 ```
 .green {
  color: green;
}
.bold {
  font-weight: bold;
}


<h1 class="green bold"> ... </h1>
 ```

 * id selector
 > to style HTML element uniquely, use id attribute 

 ```
 <h1 id="large-title"> ... </h1>

 #large-title {
}
 ```

* text styling & formatting

```
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

* background styling 

```
div {
  background-image: url("alert.png");
}
```

* styling tables

> To make a table look more attractive you need to style it. In order to specify table borders use the border property.

```
table, th, td {
  border: 1px solid black;
}
```

> The border-collapse property sets whether the table borders should be collapsed into a single border.

```
table {
  border-collapse: collapse;
}
```

> To change width and height of a table are use width and height properties.

```
table {
  width: 100%;
}

th {
  height: 50px;
}
```
> The text-align property sets the horizontal alignment (left, right, or center) of the content in the row <th> or column <td>.

By default, the content of row elements are center-aligned and the content of column elements are left-aligned

```
th {
  text-align: left;
}
```

> To change the vertical alignment (top, bottom, or middle) of the content in table rows and columns use the vertical-align property.

By default, the vertical alignment of the content is middle.

```
td {
  height: 50px;
  vertical-align: bottom;
}
```

* image

> To set positioning of image use the the float property.

```
img {
  float: left;
  max-width: 400px;
  margin-right: 10px;
}
```