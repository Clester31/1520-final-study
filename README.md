# Final Exam Preparation

## Q1: What is HTML used for?
HTML is used to present the structure of a document, such as what/where text should be displayed or where images should be placed
```HTML
<!DOCTYPE html>
<html>
<head> </head>
<body> </body>
</html>
```

## Q2: Explain in words how we can use Unordered lists to create navigation bars. Include the command to have 3 list items per row.
Unordered lists allow us to group links within a single element that we can style to achieve our desired layout
```HTML
<ul>
  <li style=”float: left width: 30%”><a href="/home">Home</a></li>
  <li style=”float: left width: 30%”><a href="/about">About</a></li>
  <li style=”float: left width: 30%”><a href="/contact">Contact</a></li>
</ul>
```

## Q3: How to create a product information that contains an image, description and price using list items?
```HTML
<ul>
  <li><img src="image.url"></li>
  >li>Item Description Here</li>
  <li>Price: $15</li>
</ul>
```

## Q4: What is the main difference between an inline tag and a block tag in HTML?
Inline: An inline element does not start on a new line, it only takes up as much width as necessary
```HTML
<span>Inline</span>
```
Block: Always starts on a new line, and the browser automatically adds some space (margin) before and after the element
```HTML
<p>Block</p>
<div>
  <p>Div</p>
</div>
```

## Q5: How to have a set of radio buttons grouped, so that if you click in one all the other ones are deselected automatically?
```HTML
<form action="/action_page.php">
  <p>Please select your favorite Web language:</p>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
  <input type="submit" value="Submit">
</form>
```

## Q6: What is the difference between IDs and Classes in HTML?
id allows you to target a specific instance of an element
```HTML
<!-- ids should be unique on a page -->
<span id="A"></span>
<span id="B"></span>
```
class allows you to target a group of elements
```HTML
<!-- classes can repeat -->
<div class="custom">Element 1</div>
<div class="custom">Element 2</div>
```

## Q7: What is CSS used for?
CSS is used to style and format the layout of HTML elements on web pages

## Q8: What is the general structure of a CSS command
```CSS
element {
  property: value;
}
```

## Q9: How to set the background color to blue of all H1 tags in a given page using CSS?
```CSS
h1 {
  background-color: blue;
}
```

## Q10: How to select an HTML tag using its ID
```CSS
#id {
  property: value;
}
```

## Q11: How to select an HTML tag using its ID
```CSS
.class {
  property: value;
}
```

## Q12: What is responsive web design?
An approach to web design that aims to make web pages render well on a variety of devices and window or screen sizes from minimum to maximum display size to ensure usability and satisfaction

## Q13: Give an example of how to make list items go from 3 items per row to 1 item per row going from a monitor to a smartphone screen
```CSS
/* For monitors */
@media only screen and (min-width: 768px) {
  .list-item {
    width: 33.33%; /* Display 3 items per row */
  }
}

/* For smartphones */
@media only screen and (max-width: 767px) {
  .list-item {
    width: 100%; /* Display 1 item per row */
  }
}
```

## Q14: What is javascript used for?
By themselves, HTML and CSS can provide a description of the structure and presentation of a document to the browser (static). We need to present a dynamic application to the user via the browser. To do this, we'll need programs that can be fetched from the web and run within the browser

## Q15: Create a small function is JavaScript that computes how much a customer should tip the waitress based on two parameters: dinner price and waitress kindness (an integer from 1 through 3, representing 10%, 15%, and 20%, respectively)
```JavaScript
function calculateTip(price, kindness) {
  if(kindness === 1) {
    price += (price * 0.1);
  } else if (kindness === 2) {
    price += (price * 0.15);
  } else {
    price += (price * 0.2);
  }
}
```

## Q16: How to create an object in javascript using JSON?
```JavaScript
{
  "smartphones": [
    {
      "id": "1",
      "brand": "Google Pixel 5a",
      "price": "$299.99",
      "screen": "6.34 in",
      "pixels": "1080 x 2400",
      "resolution": "415 PPI",
      "storage": "128 GB",
      "ram": "6 GB",
      "battery": "4680 mAh",
      "weight": "6.46 ounces"
    },
  [
}
```

## Q17: What is the DOM used for?
DOM stands for Document Object Model and is used to represent the structure of HTML documents as tree-like structures, where each node corresponds to an element, attribute, or pieces of text in the document. Allows for dynamic manipulation of web pages.

## Q18: how to get the DOM refernce of a given single HTML tag?
document.getElementById(id) or document.querySelector(element/id)

## Q19: how to get the DOM refernce of a given Multiple HTML tag?
document.querySelectorAll(element)

## Q20: How would you change the text of a specific H1 tag in your page with JavaScript/DOM
```JavaScript
let text = document.getElementById('h1tag');
text.textContent = "new text here"
```

## Q21: How would you change the color of a given H1 tag when clicking a button on the webpage? Explain the whole process of getting the reference, adding an event listener and creating the function that will change the background color
```JavaScript
let text = document.getElementById('h1tag');
let b = document.getElementById('bmyButton');

b.addEventListener('click', changeColor);

function changeColor() {
  text.style.color = 'red';
}
```

## Q22: What are the three types of web storage discussed in class? Give examples of how to use each one and also describe the differences among them
1. Local Storage
  * If you close the browser or get another TAB (session) the stored data will still be available
2. Session Storage
  * Storage that is only available during the session in which the webpage is open. If the page is closed, then the data will be lost  
3. Cookies
  * Data stored on a user's device by a web browser that is used to remember information about session state across multiple requests to a website. Only used when we need to send some info to the web server

## Q23: What is the purpose of having/using web storage?
To allow web applications to store data locally within a user's browser.

## Q24: What is the difference between client and host?
Client: Any device which requests something on a server
Host: Any device which sends or recieves traffic

# Q25: What is the genreal structure of the OSI model?
1. Physical - Transporting bits
2. Data Link - Interaction with the wire
3. Network - Addressing scheme (IP address)
4. Transport - Service to service / addressing scheme (ports)
5. Session 
6. Presentation
7. Application

# Q26: What does HTTP stand for?
Hypertext Transfer Protocol

# Q27: Given 5 types of HTTP requests that we have learned in class, what they are used for, and which ones require us to send data to the server.
1. GET - Retrieves data from the server
2. POST - submit data to the server
3. PUT - Update data already on the server (whole dataset must be provided)
4. PATCH - Update data already on the server (partial dataset may be provided)
5. DELETE - Deletes data from the server

# Q28: What is fetch command used for? Why do we say that fetch and “then” are promises?
The fetch command is used in JavaScript to make network requests (HTTP requests) to servers and fetch resources such as JSON data, HTML, images, etc. Fetch and Then are promises. Fetch will return a promise representing the completion or faailure of a newtork request. we then use then() when we have a success

# Q29: What can the postman app be used for?
Postman can be used to test and use HTTP request to either send or retrieve data

# Q30: What is Flask used for?
Flask is a python web framework that makes it easy to create a fully-featured web application. It is essentially our backend and provides tools, libraries, and patterns to simplify the creation of web application by handling tasks such as routing, HTTP request handing, and template rendering

# Q31: How to create a route, such as /about in a Flask program, that makes your web browser to display “Hello Banana” in H1 format?

```python
from flask import Flask

app = Flask(__name__)

@app.route("/about")
def about():
    return '<h1>Hello Banana</h1>'

if __name__ == "__main__":
    app.run()
```

# Q32: How would you reroute a customer from one page to another?
return redirect(url_for("def_name))

# Q33: How to render a full page from an html file in a Flask program?
return render_template("page.html")

# Q34: How to pass information to a html file, such as a link to a lougout page, via render_template method?
return render_template("page.html, logout_link=logout_link")

# Q35 What is a virtual environment used for
Virtual environments allow you to have all your project configurations part of your project, not the VS code environment

# Q37 What is AJAX used for?
AJAX stands for Asynchronous JavaScript and XML. It is used to send and retrieve data from a web server asynchronously without interfering with the display and behavior of the existing page

# Q38 How to save information that the user has previously been logged to avoid the need to redirect the user to the login page again?

# Q39 How to create a model in Flask? How to access it when needed?


