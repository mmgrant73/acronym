[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)
# Acronym:

### What is it?
Acronym is a custom web component.  It is a text box that holds an acronym.  When a mouse is over the element, it will expand and show the meaning of the acronym.  When the mouse is no longer over the element, it will contact to just show the acronym again.
For example, NASA will expand to National Aeronautics and Space Administration.

![Alt text](https://mmgrant73.github.io/acronym.png?raw=true "Image-Acronym")

[Click here for Demo](https://mmgrant73.github.io/acronym/acronym.html) 

### How to use it?
It is quite easy to use it on your webpage. Just follow the below steps:

1. Include the link to the script file that holds the this custom web component (progress-circle.js) near the bottom of 
   the body section of your webpage.  See below
   
```
    <script src="./acronym.js"></script>
```

2.  Then use the custom element tags on your webpage.

```
    <x-acronym type="vertical" innerstyle="box-shadow: 6px 6px 3px grey; text-shadow: 0 0 3px #FF0000;">
        National Aeronautics and Space Administration
    </x-acronym>
```

Note: The inner text of this custom element will be used to set the acronym.  It will take the first letter of each word
and that will display in the text box.  When expanded the whole text will be shown.
That is all you have to do to use this custom element.  There is an example HTML page (acronym.html) that shows how to use it.

```
    <!DOCTYPE html>
    <html>
      <head>
        <title>Acronym Web Component</title>
        <script>
            function acronymclick(){
                alert("click event has been triggered!!");
            }
        </script>
      </head>
      
      <body>
      
        <h1>This is a template of the web component "acronym"</h1>
        <x-acronym type="vertical" onclick="acronymclick()" innerstyle="box-shadow: 6px 6px 3px grey; text-shadow: 0 0 3px #FF0000; background-color: Beige; border-radius: 15px; border: 3px solid black;">
            Matthew Monroe Grant
        </x-acronym>

        <script src="./acronym.js"></script>

      </body>
      
    </html>
```

### There are only three properties (2 attributes and the innerText) that you can use to customize this element.

1. innerText - The first letter of each word will be used for the acronym and when expanded the whole text will be shown
2. type - Is how this custom element will be displayed there are two options (horizontal or veritical)
3. innerstyle - this attibutes allows you to set the style for the text box (see example to see how this is used)

### To Do:
1. Add a way to ignore words in the innerText that you don't want to add to the acronym.
Maybe by using Upper and Lowercase to determine which to ignore.
For example: National Aeronautics and Space Administration - "and" will be ignored and the acronym will be NASA
2. Fix it so that one can use text-align: center.  See note below

Note: That each of these attributes have defaults values but you need to a least set the innerText.
Also, don't use 'text-align: center' for this element as it mess up the spacing.  
Instead use a wrapper div with 'margin: auto', if you want to center the element
