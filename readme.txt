=== XHTML Content Negotiation for Wordpress ===
Contributors: solarissmoke
Tags: xhtml, MIME, content-type, application/xhtml+xml
Requires at least: 2.0.2
Tested up to: 3.1
Stable tag: trunk

A plugin to serve Wordpress content using the application/xhtml+xml MIME type

== Description ==

A plugin to allow Wordpress to serve content using the application/xhtml+xml MIME type, based on the client's HTTP ACCEPT request. It also takes into account the q-values of the request, in compliance with [RFC2616 HTTP/1.1](http://tools.ietf.org/html/rfc2616#page-100). The plugin also handles clients that don't supply an ACCEPT header (e.g., the W3C Validator).

The plugin detects IE6 and above and serves content as text/html, because IE doesn't follow the HTTP 1.1 requirement and can't parse application/xhtml+xml anyway.

**Note: if you use this plugin, you MUST ensure that your theme uses the XHTML doctype declaration. If you use anything else (including the HTML5 doctype, `<!doctype html>`), many browsers will render your document as an XML tree.**

If you come across any bugs or have suggestions, please contact me at [rayofsolaris.net](http://rayofsolaris.net).

== Installation ==

1. Upload `plugin-name.php` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

You can find a list of FAQs [here](http://rayofsolaris.net/code/?p=xhtml-content-negotiation-for-wordpress#faq)

== Changelog ==

= 1.4 =
* Fixed a bug where some q-values were parsed incorrectly.
* Inserted class wrapper

= 1.3 =
* Fixed a bug from version 1.2 that caused a PHP "unknown modifier" warning (thanks to [Matt](http://www.balancedlifeministry.org/)).

= 1.2 =
* Added a check for MS Pocket IE, which would otherwise have been served XHTML
* Restructured some code for readability and extensibility (thanks to [Craig Loftus](http://craigloftus.net/))

= 1.1 =
* There was no catch-all return if the q-value evaluation was inconclusive - fixed
* Tidied up some code for readability

= 1.0 =
* First version