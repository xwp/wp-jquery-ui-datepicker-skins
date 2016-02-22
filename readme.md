jQuery UI Datepicker Skins for WordPress
=============================

A collection of jQuery UI datepicker skins to match the admin color schemes available in WordPress.

To preview the skins, visit http://xwp.github.io/wp-jquery-ui-datepicker-skins/.

This project includes CSS/LESS/Sass for the following prepackaged WordPress admin color schemes:
* Default
* Light
* Blue
* Coffee
* Ectoplasm
* Midnight
* Ocean
* Sunrise

![Comparison Image](https://raw.githubusercontent.com/xwp/wp-jquery-ui-datepicker-skins/master/assets/comparison.png)

##Usage

###Initial Setup

Be sure to enqueue [the jQuery UI base CSS file](https://ajax.googleapis.com/ajax/libs/jqueryui/1.11.1/themes/smoothness/jquery-ui.min.css) with your own ````wp_enqueue_style()```` call, and the related javascript files using ````wp_enqueue_script( 'jquery' )```` and ````wp_enqueue_script( 'jquery-ui-datepicker' )````.

Help with configuring jQuery UI's Datepicker can be found at http://jqueryui.com/datepicker/.

###Using the CSS file

To include the WP jQuery Datepicker stylesheet, simply copy the CSS file located at ````css/datepicker.css```` to your project and enqueue it using the ````admin_enqueue_scripts```` WordPress action hook.


###Complete Example

```php
function myplugin_enqueue_scripts() {
	wp_register_script(
		'myplugin-js',
		plugins_url( 'javascript/myplugin.js', __FILE__ ),
		array( 'jquery', 'jquery-ui-datepicker' ),
		$myplugin_version,
		true
	);

	// Can remove this when #18909-core is committed
	wp_register_style(
		'jquery-ui',
		plugins_url( 'css/jquery-ui.min.css', __FILE__ ),
		array(),
		'1.11.1'
	);

	// https://github.com/x-team/wp-jquery-ui-datepicker-skins
	wp_register_style(
		'wp-datepicker-skins',
		plugins_url( 'css/datepicker.css', __FILE__ ),
		array( 'jquery-ui' ),
		'1712f05a1c6a76ef0ac0b0a9bf79224e52e461ab'
	);

	wp_register_style(
		'myplugin-css',
		plugins_url( 'css/myplugin.css', __FILE__ ),
		array( 'wp-datepicker-skins' ),
		$myplugin_version
	);

	wp_enqueue_script( 'myplugin-js' );
	wp_enqueue_style( 'myplugin-css' );
}
add_action( 'admin_enqueue_scripts',  'myplugin_enqueue_scripts' );
```

###Generating Custom LESS Styles

1.  Copy and rename one of the  .less files in ````less/schemes/```` (e.g., blue.less).

2.  Fill in the variables at the top of the file with your desired class name and colors.

3.  In ````less/datepicker.less```` @import your newly-created .less scheme file.

4.  Compile your LESS and enqueue your new CSS file.

###Generating Custom Sass Styles

1.  Copy and rename one of the  .scss files in ````sass/schemes/```` (e.g., blue.scss).

2.  Fill in the variables at the top of the file with your desired class name and colors.

3.  In ````sass/datepicker.scss```` @import your newly-created .scss scheme file.

4.  Compile your Sass and enqueue your new CSS file.

##Credits

Developed for the <a href="http://wordpress.org">WordPress Community</a> by the Superheroes at <a href="https://xwp.co">XWP</a>.



