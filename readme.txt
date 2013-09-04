=== Timber ===
Contributors: jarednova
Tags: template engine, templates, twig
Requires at least: 3.5
Stable tag: 0.12.0
Tested up to: 3.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Helps you create themes faster with sustainable code. With Timber, you write HTML using Mustache-like Templates http://timber.upstatement.com

== Description ==
Timber cleans-up your theme code so, for example, your php file can focus on being the data, while your twig/html file can focus 100% on the HTML and display.

Once Timber is installed and activated in your plugin directory, it gives any WordPress theme the ability to take advantage of the power of Twig and other Timber features.

### Looking for docs?
* **[Project Page](http://timber.upstatement.com)**
* [Timber Documentation](https://github.com/jarednova/timber/wiki/)
* [Twig Reference (from SensioLabs)](http://twig.sensiolabs.org/doc/templates.html)
_Twig is the template language powering Timber; if you need a little background on what a template language is, [Twig's homepage has an overview](http://twig.sensiolabs.org/)_
* **[Video Tutorials](https://github.com/jarednova/timber/wiki/Video-Tutorials)**
* [Overview / Getting Started Guide](https://github.com/jarednova/timber/wiki/getting-started)

#### What does it look like?
Nothing. Timber is meant for you to build a theme on. Like the [Starkers](https://github.com/viewportindustries/starkers) or [_s theme](https://github.com/Automattic/_s) it comes style-free, because you're the style expert. Instead, Timber handles the logic you need to make a kick-ass looking site.

#### Who is it good for?
Timber is great for any WordPress developer who cares about writing good, maintainable code. It helps teams of designers and developers working together. At [Upstatement](http://upstatement.com) we made Timber because not everyone knows the ins-and-outs of the_loop(), WordPress codex and PHP (nor should they). With Timber your best WordPress dev can focus on building the .php files with requests from WordPress and pass the data into .twig files. Once there, designers can easily mark-up data and build out a site's look-and-feel.

#### Want to read more?
* [Timber on WordPress.org](http://wordpress.org/plugins/timber-library/)
* [Timber Overview on WP Mayor](http://www.wpmayor.com/articles/timber-templating-language-wordpress/)
* ["What is WordPress Missing? A Template Language" on Torque](http://torquemag.io/what-is-wordpress-lacking-a-template-language/)



== Changelog ==

= 0.12.1 =
* A few fixes that catch issues with absolute vs. relative URLs in resize

= 0.12.0 =
* Pagination is refactored to be more intutitve, and well, better.
* Resize is also refactored to respect absolute vs. relative URLs
* Got rid of lots of old, bogus code.

= 0.11.0 =
* fixed load order of views so files inside of the child theme have priority over the parent theme.
* comment ordering respects the default set in WordPress
* added getting started screen
* misc bug fixes
* removed lots of old garbage, simplified file organization
* contributors for this release: @ysurian, @thisislawatts, @punkshui and @paulwilde

= 0.10.7 =
* more normalization of menus, users
* fixed bug in post.get_content (thanks @paulwilde)
* fixed bug in way menu items with children got their children (thanks @EloB)

= 0.10.6 =
* more normalization of comments
* Lots of cleanup of starter theme

= 0.10.5 =
* added theme URI to universal context

= 0.10.4 =
* Lots of code cleanup thanks to [Jakub](http://github.com/hsz)
* Added new function for bloginfo
* You can now hook into timber_context to filter the $context object
* Added Timber::get_terms to retrive lists of your blog's terms
* Added better support for translation
* Added filter for executing a function, ie {{'my_theme_function'|filter}}

= 0.10.3 =
* Corrected error with sidebar retrieval
* language_attributes are now avaiable as part of Timber::get_context(); payload.
* Upgraded to Twig 1.13.1

= 0.10.2 =
* added more aliases for easier coding (post.thumbnail instead of post.get_thumbnail, etc.)
* Garbage removal

= 0.10.1 =
* load_template for routing can now accept a query argument
* load_template will wait to load a template so that 'init' actions can fire.
* way more inline documentation
* print_a now includes the output of (most) methods in addition to properites.
* added lots of aliases so that things like .author will work the same as .get_author


== Installation ==

1. Activate the plugin through the 'Plugins' menu in WordPress
2. For an example, try modifying your home.php or index.php with something like this:

`
$context = array();
$context['message'] = 'Hello Timber!';
Timber::render('welcome.twig', $context);
`

Then create a subdirectory called `views` in your theme folder. The make this file: `views/welcome.twig`
`
{# welcome.twig #}
<div class="welcome">
	<h3>{{message}}</h3>
</div>
`

That's Timber!


== Frequently Asked Questions ==

= Can it be used in an existing theme? =

You bet! Watch these **[video tutorials](https://github.com/jarednova/timber/wiki/Video-Tutorials)** to see how.

= Support? =
Leave a [GitHub issue](https://github.com/jarednova/timber/issues?state=open) and I'll holler back.