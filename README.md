# **Conduit**

A communications consolidation app for Android - A single feed for your messages and alerts.

</div>

Conduit pulls messages and notifications from your communication apps into a single place, so you can action them quickly without app hopping, see a chronological timeline of when things came in, and search past communications and notifcations from one spot.

This repo hosts the releases and updates for the app. I have another repo which is the actually app code. 

> Conduit is on-device by design. It does not use APIs from the communication apps it supports. Instead, it relies on the notifications those apps post.

### Screenshots

### Features

- Combine messages and notifications from supported channels into a single place
- Todo Mode to filter out everything except unread to quickly action
- Dock with unread badges
  - Change Dock Size
  - Change scroll-ability indicator
- Custom views 
  - Custom views allow you to narrow down to just specific apps while in that view
  - Filter out all apps other than the ones included in the view from the app dock
  - Set a custom view as the default view for Conduit
- Search across all messages and notifications for supported channels
- Action notifications quickly, with each channel's own notification action chips available inside Conduit
  - Because of this, you may be able to customize the action buttons on the channels notifications depending on if the app supports it
- Block or hide notifications by matching on title, body content, or both
- Customizable:
- Swipe actions on message and notification entries
  - Swipe left, swipe right 
- Theme options
  - Dark/Light
  - AMOLED black
    - With or without monochrome icons
- Selectable App Icon
  - Dark, Blue, Manila, Legacy (Legacy looks awful but it was one of the first app icons)

### Supported Channels (Feel free to request more!)

- Google Messages
- Gmail
- Spark Email
- Outlook
- Snapchat
- LinkedIn
- Instagram
- System Phone (Google / Samsung Dialer)
- Truecaller
- Telegram
- Telegram X
- Reddit
- Steam
- Steam Chat
- Facebook
- Facebook Messenger
- Twitter (X)
- Microsoft Teams
- Airbnb

### How Updates Work

Releases are built and tested locally on my Pixel 10 Pro, with a Titan Slim as a secondary test device. Once a build is ready to publish, the APK is pushed to this repo.

Inside the app, a background worker checks the GitHub API for a newer version tag on an interval you can configure in Settings. If an update exists, an Update Available button appears to the left of the Conduit title at the top of the main page. Tapping it hands off to Android's native DownloadManager, which quietly downloads the APK in the background (posts a notifcation) and then triggers the standard Android package installer prompt.

### Why I built "Conduit"

Back in the day I used a Blackberry as my primary device - loved the focus it had on quickly getting through your comms and combining things into a single hub. Eventually, moved around different smart phones (always Android!) and then Blackberry came out out with the Blackberry Priv which I loved despite its faults. The standout feature for me was the Blackberry Hub. Once again, was able to get everything in one place and quickly move through items. Plus customize the view I was using to get through comms. I know that Blackberry still has that in some form with Inbox but I wanted to take a fundamentally different approach with keeping everything on device without APIs needed to pick up messages and comms. I also wanted even more customization.

<script type='text/javascript' src='https://storage.ko-fi.com/cdn/widget/Widget_2.js'></script><script type='text/javascript'>kofiwidget2.init('Tip me on Ko-fi!', '#72a4f2', 'P3Z22652K9');kofiwidget2.draw();</script> 
