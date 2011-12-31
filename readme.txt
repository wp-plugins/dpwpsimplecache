=== dpwpsimplecache ===
Contributors: danpai
Donate link: http://danilopaissan.net/blog/
Tags: cache, session
Requires at least: 2.5
Tested up to: 3.3
Stable tag: 0.1

D(ifferent)P(lace) Simple Cache is a WordPress plugin to implement a simple cache of objects at session level.

== Description ==

D(ifferent)P(lace) Simple Cache is a WordPress plugin to implement a simple cache of objects at session level.

dpwpsimplecache provides a global variable $dpcache, which is an instantiation of the class DP_Cache already set up to talk to the $_SESSION. Always use the global $dpcache variable. (Remember to globalize $dpcache before using it in any custom functions.)

Insert object;

	`$dpcache->set($key,$object);`
	
Get object:

	`$object = $dpcache->set($key);`
	
Count objects:

	`$dpcache->get_statistics();`
	
Get all objects:

	`$dpcache->get_all_values();`
	
Test if an object exist:

	`$dpcache->contais($key);`
	
Delete all objects:

	`$dpcache->flush();`
	
Prints human-readable information about all objects:

	`$dpcache->inspect();`
	
Delete an object:

	`$dpcache->delete($key);`
	
At any time, through the administrative page, you can:

* see all objects in the current user cache
* delete all objects in the current user cache

You can find the latest release on [GitHub](https://github.com/danpai/dpwpsimplecache)

== Installation ==

Copy the folder dpwpsimplecache and its content into `your-blog/wp-content/plugins`

== Frequently Asked Questions ==

No FAQ at this time.

== Changelog ==
= 0.1 =
* This version is quite stable but it can be used as long as you know what you are doing.