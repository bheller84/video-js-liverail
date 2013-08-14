LiveRail for VideoJS
====================

Here's an integration for VideoJS that adds advertising from LiveRail.

There are two different versions of the source code here: one is more up-to-date (but still about a year old) and it also has the custom Vidcaster fullscreen menu built-in. This displays a menu in the middle of the video when the fullscreen button is clicked, which then gives the viewer the option to enter Flash's fullscreen mode. We developed this because HTML5 fullscreen mode was non-ideal or non-existent in certain browsers so it makes for a good fallback. The other copy of the source code is a little older and it doesn't have the fullscreen menu, but it's even more out of date.

To send data to LiveRail, include the following JavaScript in your page source before the player is initialized. I forget what `OVERLAY_PILL = 0` does but that should probably stay just in case, and the others are hopefully self-explanatory. For more information about where these end up in LiveRail, refer to the LiveRail developer documentation.

    VideoJS.options.flash.flashVars = {
      LR_PUBLISHER_ID: "[LiveRail Publisher ID goes here]",
      LR_VIDEO_ID: "[Your video ID for LiveRail goes here]",
      LR_TAGS: "[Optional, comma-separated list of tags]",
      LR_LAYOUT_SKIN_MESSAGE: "Advertisement - Your video will begin in {COUNTDOWN} seconds.",
      LR_LAYOUT_OVERLAY_PILL: "0"
    };

Credit for this goes to Tanel Teemusk (LiveRail integration / fullscreen menu) and Dan Connor (fullscreen menu).