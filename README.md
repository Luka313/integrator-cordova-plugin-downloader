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
Create download request. For more info on parameter use refer to [`DownloadRequest`](https://developer.android.com/reference/android/app/DownloadManager.Request).

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
		subPath: '' //Path within the external directory, including the destination filename
	},
	//Set the local destination to a path within the application's public external storage directory
	destinationInExternalPublicDir: {
		dirType: '',
		subPath: '' //Path within the external directory, including the destination filename
	},
	//Set the local destination for the downloaded file.
	destinationUri: '',
	//Additional HTTP headers to be included with the download request.
	headers: [{header: 'Authorization', value: 'Bearer iaksjfd89aklfdlkasdjf'}]
};
```
Starts download and returns location uri on completion

```javascript

cordova.plugins.Downloader.download(request,
		(location) => { alert('File is downloaded at' + location) },
		(err) => { alert(err)})
```

## Credits and License ##

Based on Emil Bay's [`cordova-plugin-android-downloadmanager`](https://github.com/emilbayes/cordova-plugin-android-downloadmanager) 


