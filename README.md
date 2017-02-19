# YoutubeVideo

A Javascript library to access the WebM (and other) streams for Youtube Videos.

Refactored code from:
https://github.com/endlesshack/youtube-video

## Usage

    var youtubeId = "Q4-MnX5PfO8";
    YoutubeVideo(youtubeId, function(video){
      console.log(video.title);
      var webm = video.getSource("video/webm", "medium");
      console.log("WebM: " + webm.url);
      var mp4 = video.getSource("video/mp4", "medium");
      console.log("MP4: " + mp4.url);

      $("<video controls='controls'/>").attr("src", webm.url).appendTo("body");
    });

