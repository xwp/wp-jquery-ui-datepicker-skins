jQuery UI datepicker skins for WordPress
=============================

A collection of jQuery UI datepicker skins to match the admin color schemes available in WordPress.

Includes Datepicker styles for:
* Default
* Light
* Blue
* Coffee
* Ectoplasm
* Midnight
* Ocean
* Sunrise


##Usage

###Initial Setup

Be sure to enqueue WordPress' prepackaged jQuery UI CSS file using ````wp_enqueue_style( 'jquery-ui' )```` and the related javascript files using ````wp_enqueue_script( 'jquery' )```` and ````wp_enqueue_script( 'jquery-ui-datepicker' )````.

Help with configuring jQuery UI's Datepicker can be found at http://jqueryui.com/datepicker/.

###Using the CSS file

To include the WP jQuery Datepicker stylesheet in your project, simply copy the CSS file located at ````css/datepicker.css```` and enqueue it using the ````admin_enqueue_scripts```` WordPress action hook.

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





