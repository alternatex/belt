Belt
=========

###Interoperability library for script inclusion within titanium desktop sdk >= 1.2.0 

**aiming to make things easier**

<a href="https://github.com/alternatex/belt/">Go to Github</a> or 
<a href="https://github.com/alternatex/belt/tarball/master">Download the master tgz</a>
 
Example
----------------

**ftp-client**
<pre><code>
&lt;script type="text/javascript" src="lib/belt.js">&lt;/script>

&lt;script type="text/javascript"&gt;
	// fetch required
	Belt('ftp', {
		classNamespace: '\\util\\', 
		classPath: 'ftp.php',
		instantiate: false
	});
			 
	// setup connection credentials	
	var ftpOptions = {instanceArgs: {
		host: 'ftp.host.tld',
		user:'user',
		pass:'pass'
	}};
			
	// create js instance o php bridgy bridge
	var ftp = Belt("ftp", ftpOptions);

	// open connection
	ftp.open();
			
	// transfer
	ftp.upload("/path/to/local/file", "/path/to/remote/file");
	ftp.upload("/path/to/remote/file", "/path/to/local/file1");
			
	// close connection
	ftp.close();		
&lt;/script>
</code></pre>

Known-Issues
----------------
0.0.2:
==============
* restricted referencing (see v.0.0.3 kroll re-run)
* not thread-safe

Roadmap
----------------
Version 0.0.3:
================
* kroll direct fnc call optimization - w/o turn-around inclusion by step - callback object transformation seems to work now - go "native" > as it's far from optimal right now

Further Reading
----------------

Release Candidates
================
[1.2.0 RC 1](http://developer.appcelerator.com/blog/2011/05/create-and-distribute-apps-through-the-mac-app-store-with-titanium-desktop-sdk-1-2-release-candidate-1.html
[1.2.0 RC 2](http://developer.appcelerator.com/blog/2011/06/introducing-titanium-desktop-sdk-1-2-release-candidate-2.html
[1.2.0 RC 3](http://developer.appcelerator.com/blog/2011/08/introducing-titanium-desktop-sdk-1-2-release-candidate-3.html
[1.2.0 RC 4](http://developer.appcelerator.com/blog/2011/09/introducing-titanium-desktop-sdk-1-2-release-candidate-4.html

Miscellaneous
================
[Release Notes](http://developer.appcelerator.com/doc/desktop/release_notes
