Android Downloader Cordova plugin
========

This plugin is designed to support downloading files using Android DownloadManager.


Installation
--------

```bash
cordova plugin add integrator-cordova-plugin-downloader
```

Usage
--------

```javascript

var request = {
	//Location of the resource to download
	uri: '',
	//Title of this download, to be displayed in notifications
    	title: '',
	//Description of this download, to be displayed in notifications
    	description: '',
	//This will override the content type declared in the server's response.
    	mimeType: '',
	//Set whether this download should be displayed in the system's Downloads UI. True by default
    	visibleInDownloadsUi: true,
	//Control when a system notification is posted by the download manager. 
    	notificationVisibility: 0,  
    	// Set the local destination to a path within the application's external files directory
	destinationInExternalFilesDir: {
		dirType: '',
		subPath: ''
	},
	//Set the local destination to a path within the application's public external storage directory
	destinationInExternalPublicDir: {
		dirType: '',
		subPath: ''
	},
	//Set the local destination for the downloaded file.
	destinationUri: '',
	//Additional HTTP headers to be included with the download request.
	headers: [{header: 'Authorization', value: 'Bearer iaksjfd89aklfdlkasdjf'}]
};

//Starts download and returns location uri on completion
cordova.plugins.Downloader.download(request, 
				    (location) => { alert('File is downloaded at' + location) }, 
				    (err) => { alert(err)})
```

## Credits and License ##

Based on Emil Bay's cordova-plugin-android-downloadmanager (<https://github.com/emilbayes/cordova-plugin-android-downloadmanager>) 


