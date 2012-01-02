=== dpwpsimplecache ===
Contributors: danpai
Donate link: http://danilopaissan.net/blog/
Tags: cache, session
Requires at least: 2.5
Tested up to: 3.3
Stable tag: 0.4

D(ifferent)P(lace) Simple Cache is a WordPress plugin to implement a simple cache of objects at session level.

== Description ==

D(ifferent)P(lace) Simple Cache is a WordPress plugin to implement a simple cache of objects at session level.

dpwpsimplecache provides a global variable $dpcache, which is an instantiation of the class DP_Cache already set up to talk to the $_SESSION. Always use the global $dpcache variable (Remember to globalize $dpcache before using it in any custom functions). 

If you don't want to track sessions into db set the $USE_DB_SESSION_MANAGER global variable to 0

	`global $USE_DB_SESSION_MANAGER;`
	`$USE_DB_SESSION_MANAGER = 0; // default 1`

Insert object;

	`$dpcache->set($key,$object);`
	
Get object:

	`$object = $dpcache->set($key);`
	
Count active users:

	`$count_users = $dpcache->get_sessions_number();`
	
Count objects in the current user's $_SESSION:

	`$dpcache->get_statistics();`
	
Get all objects in the current user's $_SESSION:

	`$dpcache->get_all_values();`
	
Test if an object exist in the current user's $_SESSION:

	`$dpcache->contais($key);`
	
Delete all objects. If the $all parameter is set to false the method delete only the current user's $_SESSION, if true truncate the entire table (default false):

	`$dpcache->flush();`
	
Prints human-readable information about all objects:

	`$dpcache->inspect();`
	
Delete an object in the current user's $_SESSION:

	`$dpcache->delete($key);`
	
Delete single session by ID:

	`$dpcache->invalidate_single_session($sessid);`
	
Prints the number of active sessions:

	`<?php echo dpscache_active_users(); ?>`
	
At any time, through the administrative page, you can:

* see all objects in the current user cache
* delete all objects in the current user cache
* force the deletion of all sessions
* force the deletion of a single session

You can find the latest release on [GitHub](https://github.com/danpai/dpwpsimplecache)

== Installation ==

Copy the folder dpwpsimplecache and its content into `your-blog/wp-content/plugins`

== Frequently Asked Questions ==

No FAQ at this time.

== Changelog ==
= 0.1 =
* This version is quite stable but it can be used as long as you know what you are doing.
= 0.2 =
* This version add a custom table for session management. It can be used as long as you know what you are doing.
= 0.3 =
* Fixed some minor errors
= 0.3.1 =
* Fixed some minor errors
= 0.3.2 =
* Fixed some minor errors
= 0.4 =
* Single session level management