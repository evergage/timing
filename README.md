
This tool provides a timing breakdown of your page load, including Evergage network requests. Install by dragging the following link to your toolbar.

[Evergage Timing Bookmarklet](javascript:(function() {if(!window.__profiler||window.__profiler.scriptLoaded!==true){var d=document,h=d.getElementsByTagName(%27head%27)[0],s=d.createElement(%27script%27),l=d.createElement(%27div%27),c=function(){if(l){d.body.removeChild(l);};window.__profiler=window.__profiler||new __Profiler();window.__profiler.init();__profiler.scriptLoaded=true;},t=new Date();s.type=%27text/javascript%27;l.style.cssText=%27z-index:999;position:fixed;top:10px;left:10px;display:inline;width:auto;font-size:14px;line-height:1.5em;font-family:Helvetica,Calibri,Arial,sans-serif;text-shadow:none;padding:3px 10px 0;background:#FFFDF2;box-shadow:0%200%200%203px%20rgba(0,0,0,.25),0%200%205px%205px%20rgba(0,0,0,.25);%20border-radius:1px%27;l.innerHTML=%27Just%20a%20moment%27;s.src=(window.location.protocol%20%3D%3D%20%22https%3A%22%20%3F%20%22https%3A%22%20%3A%20%22http%3A%22)%2B%27//evergage.github.io/timing/profiler.js%27;s.onload=c;s.onreadystatechange=function(){console.log(arguments);if(this.readyState==%27loaded%27){c()}};d.body.appendChild(l);h.appendChild(s);}%20else%20if(window.__profiler%20instanceof%20__Profiler){window.__profiler.init()}})();)


Breaking Down onLoad
====================

This script has a form of bookmarklet and uses [Navigation Timing object](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/NavigationTiming/Overview.html) to present timing of different phases of loading the page by a browser. It measures everything from triggering the action (hitting enter on url bar, refreshing page or clicking a link/button) to the moment when site is fully loaded.

It is a visual presentation of the content of `performance.timing` object.

Adding it to your bookmarks allows you to analyze performance of every request you'd like to check out.

So far Navigation Timing API works in Firefox 7+, Chrome and IE 9+ 

Check out how it works here - http://evergage.github.com/timing/

More resources:

* [HTML5 Rocks - Measuring Page Load Speed with Navigation Timing](http://www.html5rocks.com/en/tutorials/webperformance/basics/)
* [MSDN - performanceTiming Object](http://msdn.microsoft.com/en-us/library/ff975075)
* [My description of performance.timing properties based on all of the above](info.html)