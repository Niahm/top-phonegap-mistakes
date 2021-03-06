## Cordova Browser Platform ##
Date: 2015-10-10<br>
Last Update: 2016-01-20

This blog post is to collate what little information is available for the badly name `browser platform`. The intent of this platform is to allow testing on a webbrowser with the plugins, and in theory make minimumal changes when deployed to an actual mobile device.

In theory, you can develop with your favorite browser, and fine tune on your mobile device. However, in practice, this is one of the worst documented elements of the Cordova system. This is evidence by by it's omittance from the *[Cordova Platform Guide](http://cordova.apache.org/docs/en/latest/guide/platforms/index.html)*, and the lack of any pertinent information in the github [README.md](https://github.com/apache/cordova-browser) file. There is scatter information in the plugins, but tonight this is all i have energy for.

- <a href=#plugins>Plugins</a>
- <a href=#releases>Releases</a>
- <a href=#articles>Articles</a>
- <a href=#references>References</a>


### <a name=plugins>Plugins</a> ###

The state of third-party plugins with `browser platform` is unknown &ndash; as of the *last update*. However, some improvements are noted in *cordova-lib* for their availability.

 plugin             | supported | date supported     |  [issues reported](https://issues.apache.org/jira/browse/CB-8012?jql=project%20%3D%20CB%20AND%20issuetype%20%3D%20Bug%20AND%20status%20%3D%20Open%20AND%20resolution%20%3D%20Unresolved%20AND%20component%20%3D%20Browser%20ORDER%20BY%20priority%20DESC%2C%20summary%20ASC%2C%20updatedDate%20DESC)
--------------------|-----------|--------------------|-----------------
battery             |    yes    | August 13th, 2015  |
camera              |    yes    | September 24, 2014 |  [CB-10139](https://issues.apache.org/jira/browse/CB-10139) [CB-9780](https://issues.apache.org/jira/browse/CB-9780)
console             |    yes    | always available   |
contacts            |    no     |  -                 |
device              |    yes    | September 22, 2014 |
device motion       |    yes    | September 22, 2014 |
device orientation  |    yes    | September 22, 2014 |
dialogs             |    yes    | February 10, 2015  |
filesystem          |    yes    | April 21, 2015     | [CB-9832](https://issues.apache.org/jira/browse/CB-9832)
file transfer       |    yes    | April 21, 2015     |
geolocation         |    no     |  -                 |
globalization       |    yes    | April 21, 2015     |
inappbrowser        |    yes    | April 21, 2015     |
media               |    yes    | April 21, 2015     |
media capture       |    yes    | April 21, 2015     |
network information |    yes    | September 22, 2014 |
splashscreen        |    yes    | April 21, 2015     |
statusbar           |    yes    | November 24, 2015  |
vibration           |    yes    | November 24, 2015  |
whitelist           |    no     |  -                 |
legacy whitelist    |    no     |  -                 |


### <a name=releases>Releases</a> ###

There are only three (3) release for *browser platform*, 4.1.0, 4.0.0, and 3.6.0.

#### 4.1.0 ####

- [Cordova Browser 4.1.0](http://cordova.apache.org/announcements/2016/03/04/cordova-browser-4.1.0.html)

    - [CB-10755](https://issues.apache.org/jira/browse/CB-10788) Updated checked in node_modules
    - [CB-10650](https://issues.apache.org/jira/browse/CB-10650) Non-index content.src causes Splashscreen to be not displayed on browser
    - [CB-9836](https://issues.apache.org/jira/browse/CB-9836) Add .gitattributes to prevent CRLF line endings in repos
    - [CB-9669](https://issues.apache.org/jira/browse/CB-9669) Browser exec should have more failsafes
    - Update to use new 'express' implementation of cordova-serve.
    - [CB-9658](https://issues.apache.org/jira/browse/CB-9658) Improve 'cordova run browser' when browser not installed.
    - [CB-9654](https://issues.apache.org/jira/browse/CB-9654) 'cordova run browser' -> duplicate 'CTRL + C' messages.

#### 4.0.0 ####

- [Tools Release: September 9th, 2015](https://cordova.apache.org/news/2015/09/09/tools-release.html)

    - [Cordova Browser ~4.0.0](https://github.com/apache/cordova-browser/blob/master/RELEASENOTES.md#400-aug-13-2015)
    - pinned browser@~4.0.0, windows@~4.1.0, blackberry10@~3.8.0, webos@~3.7.0 (cordova-lib)
    - [CB-9549](https://issues.apache.org/jira/browse/CB-9549) Removes excess JS files from browserified app
    - [CB-9505](https://issues.apache.org/jira/browse/CB-9505) Correct plugin modules loading within browserify flow. This closes #126 (cordova-js)

#### 3.6.0 ####

- [Apache Cordova CLI 4.0 Release](https://cordova.apache.org/announcements/2014/10/16/cordova-4.html) - 16 Oct 2014

> We have also released Cordova-Browser 3.6.0, (...) - Initial support for Cordova-Browser platform. (...)

> **New Platform: Cordova Browser**

> We have just released Browser as a platform. Add it to your projects with cordova platform add browser. This feature is intended for development purposes. We are working on adding browser support to our core plugins. Ray Camden has put together detailed blog post outlining which plugins we currently support at

> **What's new in Cordova-Browser**

>    - Update JS snapshot to version 3.6.0
>    - added initial Windows run support
>    - No longer need to kill Chrome for macOS
>    - added create.bat for Windows support


### <a name=articles>Articles</a> ###

* *The Cordova Browser Platform* - 2016-03-22
* http://www.raymondcamden.com/2016/03/22/the-cordova-browser-platform/

* *Quick tip for Cordova and the Browser platform &ndash; Setting a custom port* -  October 22, 2015
* http://www.raymondcamden.com/2015/10/22/quick-tip-for-cordova-and-the-browser-platform

* *Browser as a platform for your PhoneGap/Cordova apps* - September 24, 2014
* http://www.raymondcamden.com/2014/9/24/Browser-as-a-platform-for-your-PhoneGapCordova-apps

> Working with a limited number of plugins as of 
 - Camera
 - Device
 - Device Motion (Accelerometer)
 - Device Orientation (Compass)
 - Network Information

### <a name=reference>References</a> ###

#### Mention of *browser platform* Blog by Blog ####
other than pinned 

- [Plugins Release](https://cordova.apache.org/news/2015/11/24/plugins-release.html) - 24 Nov 2015
    - [CB-9426](https://issues.apache.org/jira/browse/CB-9426) Fix exception when using device motion plugin on browser platform.
    - [CB-9426](https://issues.apache.org/jira/browse/CB-9426) Fix exception when using device orientation plugin on browser platform
    - override resolveLocalFileSystemURL by webkitResolveLocalFileSystemURL for browser platform add .project into git ignore list
    - [CB-9167](https://issues.apache.org/jira/browse/CB-9167) Fix crash on browser window close 
    - [CB-7965](https://issues.apache.org/jira/browse/CB-7965) Add cordova-plugin-statusbar support for browser platform
    - Fixed browser platform to pass tests and combined tests (plugin:vibration - no issue number)
    - Removed call to add proxy and renamed browser file (plugin:vibration - no issue number)
    - [CB-7966](https://issues.apache.org/jira/browse/CB-7966) Add cordova-plugin-vibration support for browser platform

- [Tools Release: November 6th, 2015](https://cordova.apache.org/news/2015/11/06/tools-release.html) - 06 Nov 2015
    - [CB-9587](https://issues.apache.org/jira/browse/CB-9587) Check if browser platform added properly before creating parser.
    - [CB-9604](https://issues.apache.org/jira/browse/CB-9604) Fix error adding browser platform with PlatformApi polyfill.

- [Tools Release: August 13th, 2015](https://cordova.apache.org/news/2015/08/13/tools-release.html)
    - Browserify flag for adding plugins at build time vs run time has all tests passings. Please try it out via --browserify. EX. cordova run android --browserify.
    - [CB-9420](https://issues.apache.org/jira/browse/CB-9420) Fixes malformed require calls in browserify bundle. This closes #270
    - [CB-9429](https://issues.apache.org/jira/browse/CB-9429) Enables jsdom/browser tests for browserify.
    - Fixed issues with data transforms when using browserify (cordova-js)
    - [CB-7953](https://issues.apache.org/jira/browse/CB-7953) Add cordova-plugin-battery-status support for browser platform

- [Tools Release: June 10, 2015](https://cordova.apache.org/news/2015/06/10/tools-release.html)
    - [CB-8441](https://issues.apache.org/jira/browse/CB-8441) cordova prepare --browserify now supports 3rd party plugins to build your cordova.js at run time! Try it out!
    - [CB-8965](https://issues.apache.org/jira/browse/CB-8965) copy platform specific js into platform_www when adding new platforms for browserify workflow
    - [CB-6865](https://issues.apache.org/jira/browse/CB-6865) added browserify support for plugins with any id (cordova-js)
    - updated browserify dependency to 10.1.3 (cordova-js)

- [Tools Release: April 21, 2015](https://cordova.apache.org/news/2015/04/21/tools-release.html)
    - [CB-8223](https://issues.apache.org/jira/browse/CB-8223) Adds configparser module for exposing config.xml in the Browser platform (cordova-js)

- [Plugins Release and Moving plugins to npm: April 21, 2015](https://cordova.apache.org/announcements/2015/04/21/plugins-release-and-move-to-npm.html)
    - [CB-7964](https://issues.apache.org/jira/browse/CB-7964) browser Add support (plugin:splashscreen)
    - [CB-7956](https://issues.apache.org/jira/browse/CB-7956) Browser Add support (plugin:file)
    - [CB-7957](https://issues.apache.org/jira/browse/CB-7957) Browser Add support (plugin:file-transfer)
    - [CB-8683](https://issues.apache.org/jira/browse/CB-8683) Updated tizen and Browser specific references of old id to new id (globalization)
    - [CB-7960](https://issues.apache.org/jira/browse/CB-7960) Browser Add support (plugin:globalization)
    - [CB-7961](https://issues.apache.org/jira/browse/CB-7961) Browser Add support (plugin:inappbrowser)
    - [CB-8432](https://issues.apache.org/jira/browse/CB-8432) Correct styles for Browser wrapper to display it correctly on some pages (inappbrowser)
    - [CB-8683](https://issues.apache.org/jira/browse/CB-8683) Updated WP and Browser specific references of old id to new id (inappbrowser)
    - [CB-7962](https://issues.apache.org/jira/browse/CB-7962) Adds Browser platform support (plugin:media)
    - [CB-7963](https://issues.apache.org/jira/browse/CB-7963) Browser Add support (plugin:media-capture)
    - [CB-8185](https://issues.apache.org/jira/browse/CB-8185) Use navigator.onLine as connection information source on Browser platform (network-information)
    - [CB-7964](https://issues.apache.org/jira/browse/CB-7964) browser Add support (plugin:splashscreen)

- [Tools Release: March 02, 2015](https://cordova.apache.org/news/2015/03/02/tools-release.html)
    - [CB-8472](https://issues.apache.org/jira/browse/CB-8472) Can't find config.xml error installing browser platform after plugin (cordova-lib)
    - [CB-8223](https://issues.apache.org/jira/browse/CB-8223) Expose config.xml in the Browser platform (cordova-lib)

- [Plugins Release: February 10, 2015](https://cordova.apache.org/news/2015/02/10/plugins-release.html)
    - browser: Fixed a bug that caused an "cannot call method of undefined" error if the browser's user agent wasn't recognized (plugin:device - no issue number)
    - [CB-7955](https://issues.apache.org/jira/browse/CB-7955) Add support "browser" platform (plugin:dialogs)

- [Tools Release: January 09, 2015](https://cordova.apache.org/news/2015/01/09/tools-release.html)
    - [CB-8158](https://issues.apache.org/jira/browse/CB-8158) Added hasModule check to browserify code (cordova-lib)
    - browserify: updated require to use symbollist (cordova-lib)

- [Plugins Release: December 9, 2014](https://cordova.apache.org/news/2014/12/09/plugins-release.html)
    - Browser Changing device.platform to always report the platform as "browser". (plugin:device - no issue number)

- [Apache Cordova CLI 4.0 Release](https://cordova.apache.org/announcements/2014/10/16/cordova-4.html)
    - computeCommitId for browserify workflow fixed to handle cli and non cli workflows (cordova-lib)
    - [CB-7219](https://issues.apache.org/jira/browse/CB-7219) prepare-browserify now supports commitId and platformVersion for cordovajs (cordova-lib)
    - Added tests for browser platform (cordova-lib)

- [Plugins Release: September 22, 2014](https://cordova.apache.org/news/2014/09/22/plugins-release.html)
    - Added plugin support for the browser (plugin:device)
    - Added support for the browser (plugin:device motion)
    - Updated doc for browser (plugin:device motion)
    - Add support for the browser (plugin:device orientation)
    - Updated docs for browser (plugin:device orientation)
    - Added support for the browser (plugin:network information)
