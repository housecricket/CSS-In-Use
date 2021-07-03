### Section 1.1: External Stylesheet   
An external CSS stylesheet can be applied to any number of HTML documents by placing a <link> element in each HTML document.  

The attribute rel of the <link> tag has to be set to "stylesheet", and the href attribute to the relative or absolute path to the stylesheet. While using relative URL paths is generally considered good practice, absolute paths can be used, too. In HTML5 the type attribute can be omitted.  

It is recommended that the <link> tag be placed in the HTML file's <head> tag so that the styles are loaded before the elements they style. Otherwise, users will see a flash of unstyled content.