<?php

// Set the following for your database installation
// Copy or rename this file to .htconfig.php

$db_host = 'localhost';
$db_port = 0;
$db_user = '__DB_USER__';
$db_pass = '__DB_PWD__';
$db_data = '__DB_NAME__';
$db_type = 0; // an integer. 0 or unset for mysql, 1 for postgres

/*
 * Notice: Many of the following settings will be available in the admin panel 
 * after a successful site install. Once they are set in the admin panel, they
 * are stored in the DB - and the DB setting will over-ride any corresponding
 * setting in this file
 *
 * The command-line tool util/config is able to query and set the DB items 
 * directly if for some reason the admin panel is not available and a system
 * setting requires modification. 
 *
 */ 


// Choose a legal default timezone. If you are unsure, use "America/Los_Angeles".
// It can be changed later and only applies to timestamps for anonymous viewers.

App::$config['system']['timezone'] = '__TIMEZONE__';

// What is your site url? DO NOT ADD A TRAILING SLASH!

App::$config['system']['baseurl'] = 'https://__DOMAIN__';
App::$config['system']['sitename'] = "YunoHost Streams";
App::$config['system']['location_hash'] = '__RANDOM_STRING__';

// These lines set additional security headers to be sent with all responses
// You may wish to set transport_security_header to 0 if your server already sends
// this header. content_security_policy may need to be disabled if you wish to
// run the piwik analytics plugin or include other offsite resources on a page

App::$config['system']['transport_security_header'] = 1;
App::$config['system']['content_security_policy'] = 1;
App::$config['system']['ssl_cookie_protection'] = 1;

// Your choices are REGISTER_OPEN, REGISTER_APPROVE, or REGISTER_CLOSED.
// Be certain to create your own personal account before setting 
// REGISTER_CLOSED. 'register_text' (if set) will be displayed prominently on 
// the registration page. REGISTER_APPROVE requires you set 'admin_email'
// to the email address of an already registered person who can authorise
// and/or approve/deny the request.

App::$config['system']['register_policy'] = REGISTER_OPEN;
App::$config['system']['register_text'] = '';
App::$config['system']['admin_email'] = '__EMAIL__';

// Recommend you leave this set to 1. Set to 0 to let people register without 
// proving they own the email address they register with.

App::$config['system']['verify_email'] = 0;

// Site access restrictions. By default we will create private sites.
// Your choices are ACCESS_PRIVATE, ACCESS_PAID, ACCESS_TIERED, and ACCESS_FREE.
// If you leave REGISTER_OPEN above, anybody may register on your
// site, however your site will not be listed anywhere as an open
// registration  hub. We will use the system access policy (below) 
// to determine whether or not to list your site in the directory 
// as an open hub where anybody may create accounts. Your choice of 
// paid, tiered, or free determines how these listings will be presented.  

App::$config['system']['access_policy'] = ACCESS_PRIVATE;

// This software has a focus on online safety and user privacy. The default
// channel configuration is a restricted role where all posts are private to
// your connections and one needs to change the audience manually in order to
// create a public post ('social_restricted'). You might want to instead
// change this to post publicly by default, and require a manual change to
// restrict the audience to only your connections. To do that, change this
// to 'social'.  
    
App::$config['system']['default_permissions_role'] = 'social_restricted';

// This setting affects the quality of the site directory and friend suggestions.
// It controls how many "friends of friends" to import into your site from connections
// that are made on this site. Every digit increase can have a dramatic effect on disk
// and database use depending on the size of your site and the number of connections that
// have been made. If set to 100 or more and you have more than a dozen local accounts,
// each with a modest number of connections, your directory could ultimately discover most
// of the known fediverse, or tens of millions of entries.
// The default setting of 10 will provide you with a very well connected fediverse instance
// with an interesting and well-rounded directory, and provide good quality friend suggestions.
// You might wish to reduce this or change it to 0 if resource use is a concern.
// The quality of your directory and friend suggestions will decrease accordingly. If you
// raise it, it is recommend that you raise it incrementally and not make large or sudden
// jumps, as this could quickly mushroom into millions or tens of millions of new
// directory records.

App::$config['system']['max_imported_follow'] = __MAX_IMPORTED_FOLLOW__; 

// If you operate a public site, you might wish that people are directed
// to a "sellpage" where you can describe for features or policies or service plans in depth.
// This must be an absolute URL beginning with http:// or https:// .

App::$config['system']['sellpage'] = '';

// Maximum size of an imported message, 0 is unlimited

App::$config['system']['max_import_size'] = 200000;

// Location of PHP command line processor

App::$config['system']['php_path'] = '/usr/bin/php__PHP_VERSION__';

// Configure how we communicate with directory servers.
// Deprecated. Please do not change.
App::$config['system']['directory_mode']  = DIRECTORY_MODE_NORMAL;

// default system theme
App::$config['system']['theme'] = 'fresh';

// Allow local test environments with unverified SSL certs using Lando
App::$config['system']['ssl_exceptions'] = 'lndo.site';


// PHP error logging setup
// Before doing this ensure that the webserver has permission
// to create and write to php.log in the top level web directory,
// or change the name (below) to a file/path where this is allowed.

ini_set('display_errors', '0');

// Uncomment the following lines to turn on PHP error logging.
error_reporting(E_ERROR | E_PARSE ); 
ini_set('error_log','php.log'); 
ini_set('log_errors','1');

// Extra settings stored in the app data dir (Service Classes, PHPMailer...)
include '__DATA_DIR__/extra_conf.php';
