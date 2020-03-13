# Streaming on YouTube with OBS

# Why

YouTube streaming is suitable for our needs as it allows restricted streams. These are streams that essentially private unless you have the URL for it.

YouTube streaming support next to real-time high quality streaming that records each stream once it's been broadcast.

## What doesn't streaming on YouTube let you do?

* Two way communication. Two-way will need to be done via some other means.  The streamer could enable a hangouts OR zero that gives immediate feedback to the group.


## Prerequisites (do this at least 24 hours before your first stream)

To be able to stream on youtube, you need a youtube account that's enabled for streaming.

* Go to [https://www.youtube.com/live_dashboard_splash](https://www.youtube.com/live_dashboard_splash)
* Choose "Get Started"
* Verify your account. To do this you'll need to provide a mobile number that will allow Google to send you a verification code. Sometimes you'll need to enter it twice. 
* Once that's been authorised, you'll need to wait 24 hours before YouTube will allow you to stream. **please don't do this setup on the same day that you need to broadcast as that will be too late.**


# OBS

OBS is relaiable software for creating high quality live streams. It works with most major platforms including YouTube and Twitch. We will use it with YouTube.

## Install OBS

* `brew cask install obs` will install OBS. If you'd rather do it manually, there's a mac installer on the official OBS website.
* Launch OBS
* First time it's run, it will try to configure for your needs. Follow this process. Don't configure too many things yourself, as we will override this config shortly anyway.
* Import the settings provided `Profile` > `Import`.
* **Change the streamer key** Settings > Stream > Stream Key and repace it with YOUR streamer key from YouTube.


## Before Streaming
In no particular order, you'll need to check all of the following settings:

* **Settings** > **Output** > **Video Bitrate** `4500 Kbps`
* **Settings** > **Video** > **Base (Canvas) Resolution**: `1920x1080`
* **Settings** > **Video** > **Output (Scaled) Resolution**: `1920x1080`
* **Settings** > **Advanced** > **Network** > Dynamically change bitrate to manage congestion (Beta): ✅


### How to use it

* Setup your stream on youtube with the following:
  * go to [https://studio.youtube.com/](https://studio.youtube.com/)
  * Choose Create (top right)
  * Go live
  * Create a New Stream
  * Give your stream a title eg "G18 Lesson on JS Arrays"
  * Make it Unlisted
  * Add a description if you want
  * Add
  * This will take you to the stream admin screen.
  * Copy the stream key into your stream key in OBS (Settings > Stream > Stream Key
  * Under **Stream Latency** set it to **Ultra low-latency**
  * Now switch over to OBS and choose **Start Streaming**
  * Over on the stream admin page wait a minute or so for the OBS feed to connect to YouTube. You'll see the feed on the preview.
  * If it all looks good you can now GO LIVE
