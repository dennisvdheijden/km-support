---
layout: post
title: Featuring - Revenue Report
categories: tutorial
author: Lars Lofgren
summary: A introduction to our Revenue Report tab.
---
<div id="wistia_3f023d87a8" class="wistia-embed" data-video-width="640" data-video-height="400">&nbsp;</div>
<!--<div id="wistia_3f023d87a8" style="width:640px;height:400px;" data-video-width="640" data-video-height="400">&nbsp;</div>-->
<script charset="ISO-8859-1" src="http://fast.wistia.com/static/E-v1.js">
	
</script>

<script>

/** 
 * Helper function for loading KM trackable videos.
 * 
 * id     - The Wistia video ID
 * width  - The player width
 * height - The player height
 * name   - The name of the video. This can be anything and
    will be appended to the event logged in KM.
 */

function loadKMTrackableVideo (id, width, height, name) {
	wistiaEmbed = Wistia.embed(id, {
	  videoWidth: width,
	  videoHeight: height,
	  controlsVisibleOnLoad: true
	});

	// Begin binding KISSmetrics tracking
	wistiaEmbed.bind("play", function() {
		_kmq.push(['record', 'Played video - ' + name]);
	});

	wistiaEmbed.bind("pause", function() {
		_kmq.push(['record', 'Paused video - ' + name]);
	});

	wistiaEmbed.bind("end", function() {
		_kmq.push(['record', 'Finished video - ' + name]);
	});

}

loadKMTrackableVideo("3f023d87a8", 640, 400, "Blank Slate: Revenue Report");
</script>