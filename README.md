Example
============
![PRSpy Widget Example](widget-example.png?raw=true "PRSpy Widget Example")

Standalone Version
============
* Copy `standalone/prspy/` into the root directory of your site.
* Configure the widget settings in `standalone/index.php`.
```js
// refresh interval of widget in ms
var interval = 30000;
// you can list more than one, e.g. ["[3dAC]", "[KSK]"];
var clantags = ["[KSK]"];
// show clantag in popup before name (values: true, false)
var showtag = false;
// prspy data url
var prspydata = '/prspy/serverdata.php';
```
* Copy the distinguished sections of `standalone/index.php` into your corresponding template page.

Joomla Module
============
* Run `make.bat` to import web files from standalone version. This is necessary to avoid duplicate files in version control which have to be adjusted twice during changes.
* Copy `joomla_module/mod_prspy` into the `modules/` folder of your Joomla! installation.
* Acitvate and configure the settings in the administration backend.
Tested with Joomla!-Version 2.5.24.

![PRSpy Widget Joomla Settings](joomla-backend.png?raw=true "PRSpy Widget Joomla Settings")

Wordpress Plugin
============
* Run `make.bat` to import web files from standalone version.
* Copy `wordpress_plugin/prspy-widget` into the `wp-content/plugins/` folder of your Wordpress installation.
* Acitvate and configure the settings in the administration backend.
Tested with Wordpress Version 4.0.

Settings
============
* *Clantags* (`[KSK],[3dAC],...`) defines the clantag(s) which will be filtered.
* *Show clantags* (`true`, `false`) defines wether clantags are shown before names or not.
* *Interval* (`ms`) defines the refresh interval of the PRSpy widget in milliseconds.
* *PRSpy data url* (`prspy/serverdata.php`) defines a relative or absolute URL to PRSpy JSON data.
The file `serverdata.php` retrieves *http://www.realitymod.com/prspy/json/serverdata.json?#time()#* and deliver it from the same domain. It avoids blocking messages like unsafe script by different browsers.

Libraries (included)
============
* [jQuery 1.11.1](https://jquery.com/download/)
* [jQuery Cookie 1.4.1](https://plugins.jquery.com/cookie/)

Links
============
[Realitymod.com forum thread (only for server administrators)](http://www.realitymod.com/forum/f109-pr-bf2-sa-private-forums/105484-clan-members-currently-playing-prspy-2.html)


Contributors
============
Original Concept: [3dAC] blip2  
Joomla Module and Flags/Scores: [KSK] wenzul
