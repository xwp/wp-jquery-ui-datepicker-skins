jQuery UI datepicker skins for WordPress
=============================

A collection of jQuery UI datepicker skins to match the admin color schemes available in WordPress.

To preview the skins, visit http://x-team.github.io/wp-jquery-ui-datepicker-skins/.

This project includes CSS/LESS/Sass for the following prepackaged WordPress admin color schemes:
* Default
* Light
* Blue
* Coffee
* Ectoplasm
* Midnight
* Ocean
* Sunrise

![Comparison Image](https://raw.githubusercontent.com/x-team/wp-jquery-ui-datepicker-skins/master/assets/comparison.png)

##Usage

###Initial Setup

Be sure to enqueue WordPress' prepackaged jQuery UI CSS file using ````wp_enqueue_style( 'jquery-ui' )```` and the related javascript files using ````wp_enqueue_script( 'jquery' )```` and ````wp_enqueue_script( 'jquery-ui-datepicker' )````.

Help with configuring jQuery UI's Datepicker can be found at http://jqueryui.com/datepicker/.

###Using the CSS file

To include the WP jQuery Datepicker stylesheet, simply copy the CSS file located at ````css/datepicker.css```` to your project and enqueue it using the ````admin_enqueue_scripts```` WordPress action hook.

###Generating Custom LESS Styles

1.  Copy and rename one of the  .less files in ````less/schemes/```` (e.g., blue.less).

2.  Fill in the variables at the top of the file with your desired class name and colors.

3.  In ````less/datepicker.less```` import your newly-created .less scheme file.

4.  Compile your LESS and enqueue your new CSS file.

###Generating Custom Sass Styles

1.  Copy and rename one of the  .scss files in ````sass/schemes/```` (e.g., blue.scss).

2.  Fill in the variables at the top of the file with your desired class name and colors.

3.  In ````sass/datepicker.scss```` import your newly-created .scss scheme file.

4.  Compile your Sass and enqueue your new CSS file.

##Credits

Developed for the <a href="http://wordpress.org">WordPress Community</a> by the Superheroes <a href="http://x-team.com/wordpress">X-Team</a>.





