>When someone first visits your website, their browser downloads the HTML of the current page plus the linked CSS file. Then when they navigate to another page, their browser only needs to download the HTML of that page; the CSS file is cached, so it does not need to be downloaded again. Since browsers cache the external stylesheet, your pages load faster.

### Section 1.1: External Stylesheet   
An external CSS stylesheet can be applied to any number of HTML documents by placing a <link> element in each HTML document.  

The attribute rel of the <link> tag has to be set to "stylesheet", and the href attribute to the relative or absolute path to the stylesheet. While using relative URL paths is generally considered good practice, absolute paths can be used, too. In HTML5 the type attribute can be omitted.  

It is recommended that the <link> tag be placed in the HTML file's <head> tag so that the styles are loaded before the elements they style. Otherwise, users will see a flash of unstyled content.

#### Example   
**hello-world.html**
```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <link rel="stylesheet" type="text/css" href="style.css">
</head>

<body>
    <h1>Hello world!</h1>
    <p>I ♥ CSS</p>
</body>

</html>
```
**style.css**
```
h1 {
    color: green;
    text-decoration: underline; 
}
p {
    font-size: 25px;
    font-family: 'Trebuchet MS', sans-serif;
}
```
Make sure you include the correct path to your CSS file in the href. If the CSS file is in the same folder as your HTML file then no path is required (like the example above) but if it's saved in a folder, then specify it like this href="foldername/style.css".  
```
<link rel="stylesheet" type="text/css" href="foldername/style.css">
```
External stylesheets are considered the best way to handle your CSS. There's a very simple reason for this: when
you're managing a site of, say, 100 pages, all controlled by a single stylesheet, and you want to change your link colors from blue to green, it's a lot easier to make the change in your CSS file and let the changes "cascade" throughout all 100 pages than it is to go into 100 separate pages and make the same change 100 times. Again, if you want to completely change the look of your website, you only need to update this one file.   
You can load as many CSS files in your HTML page as needed.
```
 <link rel="stylesheet" type="text/css" href="main.css"> <link rel="stylesheet" type="text/css" href="override.css">
```
CSS rules are applied with some basic rules, and order does matter. For example, if you have a main.css file with some code in it:
```
p.green { color: #00FF00; }
```
All your paragraphs with the 'green' class will be written in light green, but you can override this with another .css file just by including it after main.css. You can have override.css with the following code follow main.css, for example:   
```
p.green { color: #006600; }
```
Now all your paragraphs with the 'green' class will be written in darker green rather than light green.
### Section 1.2: Internal Styles    
CSS enclosed in <style></style> tags within an HTML document functions like an external stylesheet, except that it lives in the HTML document it styles instead of in a separate file, and therefore can only be applied to the document in which it lives. Note that this element must be inside the <head> element for HTML validation (though it will work in all current browsers if placed in body).
***hello-world.html**  
```
<head>
    <style>
        h1 {
            color: green;
            text-decoration: underline;
        }

        p {
            font-size: 25px;
            font-family: 'Trebuchet MS', sans-serif;
        }
    </style>
</head>

<body>
    <h1>Hello world!</h1>
    <p>I ♥ CSS</p>
</body>
```
