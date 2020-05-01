# HTML

### Table

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
<form>Starting the form</form>
```

An HTML form contains form elements. Form elements are different types of input elements, like text fields, checkboxes, radio buttons, submit buttons, and more.

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