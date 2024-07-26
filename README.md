# jQuery DOM Manipulation Project

## Overview

This project demonstrates basic DOM manipulation using jQuery. It covers various tasks such as adding classes, removing elements, changing styles dynamically, and handling events.

## Features

1. **Console Log on DOM Ready**: Logs a message when the DOM is fully loaded.
2. **Center Images**: Adds the class `image-center` to all images inside an `<article>` tag to center them.
3. **Remove Last Paragraph**: Removes the last paragraph in the article.
4. **Random Font Size for Title**: Sets the font size of the title to a random pixel size between 0 and 100.
5. **Add List Item**: Adds a new item to the list.
6. **Replace Aside Content**: Empties the `aside` and adds a paragraph apologizing for the list’s existence.
7. **Change Background Color**: Changes the background color of the body based on RGB values entered in input fields.
8. **Remove Image on Click**: Removes an image when it is clicked.

## Getting Started

### Prerequisites

- [jQuery](https://jquery.com/) - A fast, small, and feature-rich JavaScript library.

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/jquery-dom.git
    ```

2. Navigate to the project directory:
    ```sh
    cd jquery-dom
    ```

3. Open the `index.html` file in your web browser.

### Usage

Open `index.html` in your preferred web browser to see the following functionalities:

1. **Console Log**: Open the browser console (usually with `F12` or `Ctrl+Shift+I`) to see the "Let’s get ready to party with jQuery!" message.
2. **Centered Image**: The image inside the article will be centered.
3. **Removed Last Paragraph**: The last paragraph inside the article will be removed.
4. **Random Font Size for Title**: The title's font size will be set to a random value between 0 and 100 pixels.
5. **New List Item**: A new item saying "This is a new list item" will be added to the ordered list.
6. **Replaced Aside Content**: The content of the `aside` will be replaced with a paragraph apologizing for the list.
7. **Change Background Color**: Adjust the RGB input values to change the background color of the body.
8. **Remove Image on Click**: Click on the image to remove it from the DOM.

### Code Explanation

The main jQuery code is included in a `<script>` tag within the `index.html` file:

```html
<script>
  $(document).ready(function () {
    
    // 1. Log a message when the DOM is ready
    console.log("Let’s get ready to party with jQuery!");
    
    // 2. Add the class "image-center" to all images inside article
    $("article img").addClass("image-center");
    
    // 3. Remove the last paragraph in the article
    $("article p:last-child").remove();
    
    // 4. Set the font size of the title to be a random pixel size from 0 to 100
    $("#title").css("font-size", Math.random() * 100 + "px");
    
    // 5. Add an item to the list; it can say whatever you want
    $("ol").append("<li>This is a new list item</li>");
    
    // 6. Empty the aside and put a paragraph in it apologizing for the list’s existence
    $("aside").empty().append("<p>I apologize for the list’s existence</p>");
    
    // 7. Change the background color of the body based on input values
    $("input").on("input", function() {
      const red = $("input").eq(0).val();
      const green = $("input").eq(1).val();
      const blue = $("input").eq(2).val();
      $("body").css("background-color", `rgb(${red}, ${green}, ${blue})`);
    });
    
    // 8. Remove the image from the DOM when clicked
    $("img").on("click", function() {
      $(this).remove();
    });
  });
</script>