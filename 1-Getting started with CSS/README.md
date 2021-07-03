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