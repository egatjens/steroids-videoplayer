# Android Video Player Plugin for Appgyver Steroids #

Adapt [macdonst VideoPlayer Plugin] (https://github.com/macdonst/VideoPlayer) to work on Android Appgyver Steroids Application.

The video player allows you to display videos from your Steroids application.

## Add the plugin to the  Build Service ##

[
  {"source":"https://github.com/egatjens/steroids-videoplayer.git"},
]

Reference: [Custom plugins for your app] (http://guides.appgyver.com/steroids/guides/cloud_services/plugin-config/)


## Using the plugin ##

The plugin creates the object `window.plugins.videoPlayer`.  To use, call the play() method:

<pre>
  /**
	* Display an intent to play the video.
    *
    * @param url           The url to play
    */
  play(url)
</pre>

Sample use:

    window.plugins.videoPlayer.play("http://path.to.my/video.mp4");
    window.plugins.videoPlayer.play("file:///path/to/my/video.mp4");
    window.plugins.videoPlayer.play("file:///android_asset/www/path/to/my/video.mp4");
    window.plugins.videoPlayer.play("https://www.youtube.com/watch?v=en_sVVjWFKk");

Note: When playing video from the assets folder, the video is first copied to internal storage with MODE_WORLD_READABLE.
