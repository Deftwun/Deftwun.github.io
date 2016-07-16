---
title:"Clover Sites Video Background"
layout:post
date:   2016-07-15 5:00:00
published: true
---
# How do you get a video background on Clover Sites

##Convert to Gif
Currently the only way to get a video background with Clover Sites is by converting your video to a gif. This may be the best & cleanest solution. But may be a problem if you have large video.

There is another solution though, although its more of a work-around:

##Custom code
1. Once your in the editor, click  'ADVANCED MODE' at the top-left of the screen.
2. Then click on 'Design Settings'.
3. Scroll down until you see  a box labeled 'CUSTOM <HEAD> CODE'.
4. Paste in code below. (make sure to change videoURL)

###Paste
```javascript
<script src="https://code.jquery.com/jquery-3.1.0.slim.min.js"></script>
<script>
(function() {

  window.$ = window.$c;

  $(document).on('page:load', function(e) {

  	//Change this..
    var videoURL = 'http://your-video-url.mp4';

    // .. and this if needed
    var videoPages = ['','home'];

    var href = window.location.href;
    var page = href.substr(href.lastIndexOf('/') + 1);

    if (visiblePages.indexOf(page) > -1){

      console.log("Loading custom-video-bg: " + videoURL);

      var video = $('<video ></video>',{
          id:'custom-video-bg',
          src:videoURL,
          muted:true,
          loop:true,
          autoplay:true,
          controls:false
        })

        .css({
          position:'absolute',
          width:'100%',
          top:0,left:0,
        })

        .appendTo($('body'));

      console.log("custom-video-bg appended.");
    }
  });
})();
</script>
```

###Note:
You'll also want to make sure the section image is removed, invisible, or has identical aspect ratio of your video.

It's certainly not perfect, as the video is overlaying _everything_ when viewed in the editor. But it looks fine in preview mode and when live.
