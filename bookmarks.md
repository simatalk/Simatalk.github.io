# Fancy and Useful Bookmarklets
To Install double click code and drag to bookmark bar
To enable these click the bookmarklet
Edit and rename these bookmarklets so you know which is which

## [Home](https://simatalk.github.io)

## Adblock
To disable refresh page


javascript:var st = confirm("strict adblocker?"); if(st){var invisible = document.createElement("style"); invisible.innerHTML = "iframe{display:none} embed{display:none} object{display:none} frame{display:none}"; document.body.appendChild(invisible); setInterval(function(){var embeds = document.querySelectorAll("iframe, embed, frame, object"); for(i = 0; i < embeds.length; i++){embeds[i].remove()}}, 500)} else{var adblock = document.createElement("style"); adblock.innerHTML = "[src*=adserver] {display: none; } [src*=adlinks] {display: none;} [src*=adtech] {display:none;} [id*=google_ads] { display: none; } [src*=doubleclick.net] { display:none;} [src*=googlead] { display: none; } [href*=googlead] { display:none;} [src*=googlesyndication] { display: none;} [src*=ads.] { display: none; } [src*=.ad] {display: none; } [src*=ad.] {display:none;} [src*=adsmart] { display:none;}"; document.body.appendChild(adblock)} if(st){var elements = document.body.querySelectorAll("*"); for(i2 = 0; i2 < elements.length; i2++){if(elements[i2].id.includes("google_ads_iframe")){elements[i2].remove()}}} var x = document.getElementsByClassName("video-stream html5-main-video")[0]; function videoblock() { if(x.src.includes("pltype=adhost")) { x.currentTime = 999999999; }} setInterval(videoblock, 10)


## Inspect Element


For Inspect: 


javascript:document.body.contentEditable = 'true'; document.designMode='on'; void 0


For no Inspect: 


javascript:document.body.contentEditable = 'false'; document.designMode='on'; void 0


For Inspect WITH OPTIONS (different from upper two):


javascript:(function () {var script=document.createElement('script');script.src='https://x-ray-goggles.mouse.org/webxray.js';script.className='webxray';script.setAttribute('data-lang','en-US');script.setAttribute('data-baseuri','https://x-ray-goggles.mouse.org');document.body.appendChild(script);}())


## Developer Console


javascript:(function()%7B(function() %7Bvar x %3D document.createElement("script")%3Bx.src %3D "https%3A%2F%2Fcdn.jsdelivr.net%2Fgh%2FSnowLord7%2Fdevconsole%40master%2Fmain.js"%3Bx.onload %3D alert("Loaded Developer Console!")%3Bdocument.head.appendChild(x)%3B%7D)()%7D)()


## Snake Mod


javascript: req = new XMLHttpRequest(); req.open('GET', 'https://raw.githubusercontent.com/DarkSnakeGang/GoogleSnakeCustomMenuStuff/main/custom.js'); req.onload = function() { eval(this.responseText + 'snake.more_menu();'); }; req.send();


## Disable Adblock Blocker
To disable refresh page


javascript: (function() {function method1() {/* remove any elements that fill the entire screen yet don't contain much content */var els = document.querySelectorAll('body *');var wW = window.innerWidth * 0.8;var wH = window.innerHeight * 0.8;var bigs = [];/* tag DOM with first_try marker */var bod = document.querySelector('body');bod.style = 'overflow:auto!important';att = document.createAttribute('class');att.value = 'deblock_first_try';bod.setAttributeNode(att);/* check size of all elements */for (var i = 0, il = els.length; i < il; i++) {var s = window.getComputedStyle(els[i]);var w = els[i].offsetWidth;var h = els[i].offsetHeight;/* remove any scroll disabling styles */if (s.getPropertyValue('overflow') == 'hidden') {els[i].style = 'overflow:auto!important';}/* save big elements to an array */if (w >= wW && h >= wH) {bigs[bigs.length] = els[i];}}bigs.sort(function(a,b){return b.innerHTML.length - a.innerHTML.length;});var p = 0.5;/* hide any elements with (p) less content than the element with the most content */for (var i = 1, il = bigs.length; i < il; i++) {if(bigs[i].innerHTML.length < bigs[0].innerHTML.length * p) {bigs[i].style = 'display:none!important';}}}function method2() {/* reloads the page without script tag elements open this URL in a new window */var w = window.open(location.href,'_blank');w.addEventListener('DOMContentLoaded', function(){/* as soon as that page loads... */var html = w.document.querySelector('html').cloneNode(true);var els = html.querySelectorAll('script');/* strip out all script tag elements before they change the DOM */for(var i=0, il=els.length; i<il; i++) {els[i].parentNode.removeChild(els[i]);}var html = html.innerHTML;/* copy and paste that page's DOM to this page, then close it */document.querySelector('html').innerHTML = html;addButtons();w.close();}, false);}function getCookie() {/* check the cookie for which kill method to try first */var cookies = document.cookie.split(';');for(var i=0, il = cookies.length; i<il; i++) {var c = cookies[i];if (c.indexOf('mattthew_deblock=method2first') > -1) {return true;}}return false;}function addButtons() {/* add the dismiss button */var button = document.createElement('div');button.innerHTML = 'DISMISS&nbsp;ME';var att = document.createAttribute('style');att.value = 'position:fixed; top:10px; right:10px; display:inline-block; padding:4px 8px; border-radius:4px; z-index:999999; color:white; font-family:sans-serif; font-size:14px; box-shadow:0px 4px 4px rgba(0,0,0,0.4), 0px 0px 4px rgba(0,0,0,0.4); cursor:pointer; background-color:red;';button.setAttributeNode(att);att = document.createAttribute('class');att.value = 'mattthew_deblock_button';button.setAttributeNode(att);var bod = document.querySelector('body');button.addEventListener('click', function(){/* remove all deblock buttons from the DOM */var el = document.querySelectorAll('.mattthew_deblock_button');el[0].parentNode.removeChild(el[0]);el[1].parentNode.removeChild(el[1]);});bod.appendChild(button);/* add the try again button */button = document.createElement('div');button.innerHTML = '&nbsp;TRY&nbsp;AGAIN&nbsp;';att = document.createAttribute('style');att.value = 'position:fixed; top:54px; right:10px; display:inline-block; padding:4px 8px; border-radius:4px; z-index:999999; color:white; font-family:sans-serif; font-size:14px; box-shadow:0px 4px 4px rgba(0,0,0,0.4), 0px 0px 4px rgba(0,0,0,0.4); cursor:pointer; background-color:blue;';button.setAttributeNode(att);att = document.createAttribute('class');att.value = 'mattthew_deblock_button';button.setAttributeNode(att);var bod = document.querySelector('body');button.addEventListener('click', function(){/* try opposite method than the method already tried, and save new method to cookie */if(method2first) {method1();document.cookie = 'mattthew_deblock=method1first; expires=' + exdate.toUTCString();} else {method2();document.cookie = 'mattthew_deblock=method2first; expires=' + exdate.toUTCString();}});bod.appendChild(button);}/* call functions */var exdate = new Date();exdate.setDate(exdate.getDate() + 365);if(!document.querySelector('.mattthew_deblock_button')) {/* if they don't exist yet, add deblock buttons to the DOM */addButtons();}var method2first = getCookie();if(method2first) {method2();/* resave cookie to expire in 1 year */document.cookie = 'mattthew_deblock=method2first; expires=' + exdate.toUTCString();} else {method1();}})();


## Translate Page
No more Spanish or French


javascript:(function(){var a=window.getSelection(),b='';if(a!=''){a='text='+encodeURIComponent(a)}else{a='u='+encodeURIComponent(location.href);b='translate'};window.open('https://translate.google.com/'+b+'?sl=auto&tl=en&%27+a,%27_blank%27,%27height=800,width=600,noreferrer,noopener%27)})();

## [Cookie Pop](https://raw.githubusercontent.com/simatalk/home/gh-pages/cookiepop.txt)
