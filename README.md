Html 2 Pdf
=============

This is a pdf creation plugin for Phonegap 3.3.0 / Cordova 3.3.1 supporting Android (>=2.3.3) and iOS(>=6.0).

This plugin supporting UTF-8 (Thai font).
It creates a pdf from the given html and stores it on the device.

There is one method:

* create(html, filePath, successCallback, errorCallback)

Installation
======
You may use phonegap CLI as follows:

<pre>
➜ phonegap local plugin add https://github.com/phopkrit/cordova-plugin-html2pdf.git
[phonegap] adding the plugin: https://github.com/phopkrit/cordova-plugin-html2pdf.git
[phonegap] successfully added the plugin
</pre>

This Plugin requires iText.jar to be added to your project. Here is the last open source version (4.2.0) of it:    

 * GitHub: https://github.com/ymasory/iText-4.2.0
 * Download .jar:: https://github.com/ymasory/iText-4.2.0/downloads  
  
It has been confirmed to work with cordova 3.3.0+

Usage
====
Ionic/angularJS Example
<pre>
{
        //get source from HTML element with jqLite
        var source = angular.element(document.querySelector('#id')).html();

        var success = function(status) {
            alert('Message: ' + status);
        }

        var error = function(status) {
            alert('Error: ' + status);
        }

        if(Platform.isAndroid){
            window.html2pdf.create(source,"test.pdf", success, error);
        } 
        
        if (Platform.isIOS){
            window.html2pdf.create(source,"~/Documents/test.pdf", success, error);
        }
}
</pre>
