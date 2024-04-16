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
  <li><a href="/home">Home</a></li>
  <li><a href="/about">About</a></li>
  <li><a href="/contact">Contact</a></li>
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
