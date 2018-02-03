# CMB2 Field Type: Font Awesome
#### Font Awesome Icon Selector for CMB2

## Description
Font Awesome icon selector for powerful custom metabox generator [CMB2](https://github.com/WebDevStudios/CMB2 "Custom Metaboxes and Fields for WordPress 2")

You can use as field type in CMB2 function file. Add a new field, set type to `faiconselect` and add font awesome icons to options (look Usage for examples). Plugin uses [jQuery Font Picker](https://codeb.it/fonticonpicker/) for creating a icon selector. 

### ScreenShot
![Image](screen1.png?raw=true)

## Usage

include `iconselect.php` to your cmb2 function file. Alternatively download this repo and put files into `wp-content/plugins/` directory. When you enable plugin, you can use field type in CMB2.

Use `faiconselect` for type. For Example;

```php
$cmb->add_field( array(
    'name' => __( 'Select Font Awesome Icon', 'cmb' ),
    'id'   => $prefix . 'iconselect',
    'desc' => 'Select Font Awesome icon',
    'type' => 'faiconselect',
    'options' => array(
	'fa fa-facebook' => 'fa fa-facebook',
	'fa fa-500px'  	 => 'fa fa-500px',
	'fa fa-twitter'	 => 'fa fa-twitter'
    )
) );
  ```
  After that jQuery Font Picker plugin handle the select. 
  
  Aslo you can use predefined array for Font Awesome. I created a function with this addon to use in `options_cb`. Function called as `returnFaPre`.
  
```php
$cmb->add_field( array(
    'name' => __( 'Select Font Awesome Icon', 'cmb' ),
    'id'   => $prefix . 'iconselect',
    'desc' => 'Select Font Awesome icon',
    'type' => 'faiconselect',
    'options_cb' => 'returnFaPre'
) );
  ```
  That's All for now :) Contributions are welcome
  
