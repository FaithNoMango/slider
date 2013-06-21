FaithNoMango Jquery Slider (which is actually a fader)
======================================================

Included Files:
---------------
<table>
  <tr><th>Description</th><th>File</th></tr>
  <tr><td>Example usage:</td><td>example.htm</td></tr>
  <tr><td>CSS:</td><td>css/slider.css</td></tr>
  <tr><td>Javascript:</td><td>js/slider.js</td></tr>
  <tr><td>Left Image:</td><td>slider_images/slider_left.png</td></tr>
  <tr><td>Left Image (Over):</td><td>slider_ images/slider_left2.png</td></tr>
  <tr><td>Right Image:</td><td>slider_images/slider_right.png</td></tr>
  <tr><td>Right Image (Over):</td><td>vslider_images/slider_right2.png</td></tr>
</table>

How to use it:
--------------

Unzip the files to your htdocs folder on your web server. 

Inside your html document, in the head section, include the css file (before the javascript):
```
<link rel="stylesheet" type="text/css" media="screen" href="css/slider.css" />
```
Next, inside your html document's head section, include the jquery javascript source file:
```
<script type="text/javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script> 
```
Also include the slider javascript source file: 
```
<script type="text/javascript" src="js/slider.js"></script> 
```
Include this code next, and put your own values in to specify options: 
```
<script type="text/javascript">
$(function()
{
    var slider_properties = 
    {
        autoplay: true, 
        auto_speed: 5000,
        fade_speed: 500,
        width: 640,
        height: 424
    };
    $('#slider').begin(slider_properties);
});
</script> 
```
Note that:
----------

- Autoplay can be true or false, depending on whether you want the slider to autoplay
- Auto_speed is the speed at which the image changes during autoplay; note that 5000 = 5 seconds
- Fade_speed is the speed at which the images fade in/out; 500 = half a second
- Width is the width of the slider; the images inside the slider will be this width
- Height is the height of the slider; the images inside the slider will be of slightly less tall than this

Finally, in your html, include this code:
-----------------------------------------
```
<div id="slider">
    <div id="slider_img">
        <img src="images/my_first_slider_image.jpg">
        <img src="images/my_second_slider_image.jpg">
        <img src="images/my_third_slider_image.jpg">
        <img src="images/my_fourth_slider_image.jpg">
    </div>
    <div id="slider_left">
        <a href="#">
            <img src="slider_images/slider_left.png" id="sl">
            <img src="slider_images/slider_left2.png" id="sl2">
        </a>
    </div>
    <div id="slider_bips">
    </div>
    <div id="slider_right">
        <a href="#">
            <img src="slider_images/slider_right.png" id="sr">
            <img src="slider_images/slider_right2.png" id="sr2">
        </a>
    </div>
</div>
```
Note that:
----------

Replace the contents of div#slider_img with the locations of the images you want to display in the slider

Supported Browsers:
-------------------

Works in Internet Explorer 9 & 10, Chrome 27.0.1453.110 m, Firefox 21.0, and Safari 5.1.7. 
To support older versions of Internet Explorer, consider using html5shiv.js.