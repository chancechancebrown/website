---
title: "Using a GoPro as a Webcam"
date: 2022-03-10T11:31:12-05:00
draft: False
tags:
- Interviews 
- Streaming
---

I have always been picky about the quality of video and audio. During the pandemic, this issue became paramount when dealing with interviews and streaming. Your laptop webcam will suffice for the most part, and you can pick up some decent webcams for less than $100 these days, but none of these will blow you away and will also suffer from third-party software. Professional Twitch/Youtube streamers these days typically have a DSLR setup that gives top-notch video quality, but with the caveat that they can a) get a lot of money from their platform and/or b) write this off as a business expense. Most of us do not have this luxury, but might have something much cheaper like a GoPro lying around - [here's mine.](https://gopro.com/en/us/shop/cameras/hero9-black/CHDHX-901-master.html) I'll give you a run down on what you need to use this particular camera as a webcam.


1. [GoPro HERO9 Black](https://gopro.com/en/us/shop/cameras/hero9-black/CHDHX-901-master.html)
2. [GoPro Media Mod](https://gopro.com/en/us/shop/mounts-accessories/camera-media-mod/ADFMD-001.html)
3. [HDMI Capture Card](https://www.amazon.com/gp/product/B088HBRM7T)
4. [Mini HDMI to HDMI](https://www.amazon.com/gp/product/B08DK4LVYX)
5. [Some mount/arm for your desk](https://www.amazon.com/gp/product/B094N6W6SP)
6. [OBS Studio](https://obsproject.com)
7. [OBS Virtualcam](https://obsproject.com/forum/resources/obs-virtualcam.949)
8. [NVIDIA Broadcast](https://www.nvidia.com/en-us/geforce/broadcasting/broadcast-app/)*

*Optional


I do find it sort of obnoxious that the GoPro HERO8+ removed the HDMI out port so that you need the media mod to access that functionality. I recommend this route because the GoPro Webcam software is terribly buggy and gives an obnoxious splash screen each time you start it up.<img 
    style="display: block; 
           margin-left: auto;
           margin-right: auto;
           width: 100%;"
    src="../../images/OIP.jpg" 
    alt="GoPro Splash">
</img>  I did not like joining a video call and the person on the other end had to stare at that screen until my face appeared. This method also had the disadvantage of trying to charge your camera while streaming video, which if you do not have modern USB ports could be an issue. 

The setup is pretty straight forward, you plug your HDMI cable into your capture card into the top port of the media mod, your charger into the USB-C port, and you are mostly done. <img 
    style="display: block; 
           margin-left: auto;
           margin-right: auto;
           width: 100%;"
    src="../../images/media-mod-ports.png" 
    alt="GoPro Splash">
</img>

As far as capture settings go, mine are pretty standard:

- RES|FPS: 1080|60
- Lens: Narrow
- HyperSmooth: Off
- Hindsight: Off

PROTUNE:

- Bit Rate: High
- Shutter: 1/60
- White Balance: Auto
- ISO Min: 800
- ISO Max: 1600
- Sharpness: High
- Color: GoPro

Also, don't forget to go into the general settings and turn the auto power off to Never or else you'll have to touch the camera every 15 minutes before it shuts down. (I learned this during an interview where my video kept disconnecting, embarrassing)
YMMV on these, so feel free to tweak at your behest. Once in OBS, add a **Video Capture Device** to your sources, and give it whatever name you deem necessary. The device should show up as **USB Video** or similar (depending on what device you chose) when choosing the source, but after that, the bulk of the work is done. To enable the virtual camera go to **Tools** -> **VirtualCam** then select your output device name. On the main screen, just click **Start Virtual Camera** and your device should be good to go. 

Optionally, you can add some post-processing into the mix, and for that I choose NVIDIA Broadcast. The two effects I choose are **Background Blur** and **Auto frame**. Background blur is nice because you don't have to worry as much about your messy office or giving away your surroundings. Auto frame tracks your face and allows you to move around without worrying about going out of frame as well as zooms in such that you are the sole subject of the frame. 

It took quite a bit of trial and error to get to a stable video capture source, but it is well worth it. I have received multiple compliments in my interviews because of the video quality, which directly translates to a better impression. On the same hand, you should definitely look into getting a quality microphone even if video quality isn't that important to you. Personally, I've used a simple [Blue Yeti](https://www.bluemic.com/en-us/products/yeti/) for years now and never had a problem. If you are using NVIDIA Broadcast, you can add noise removal effects to even further up your interview game.