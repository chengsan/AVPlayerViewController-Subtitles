<p align="center" >
<img src="https://raw.github.com/mhergon/AVPlayerViewController-Subtitles/master/assets/logo.png" alt="Logo" title="Logo" width=250>
</p>

![issues](https://img.shields.io/github/issues/mhergon/AVPlayerViewController-Subtitles.svg)
&emsp;
![stars](https://img.shields.io/github/stars/mhergon/AVPlayerViewController-Subtitles.svg)
&emsp;
![license](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)


AVPlayerViewController-Subtitles is a library to display subtitles on iOS. It's built as a Swift extension and it's very easy to integrate.

## How To Get Started

### Installation with CocoaPods

```ruby
platform :ios, '8.0'
pod "AVPlayerViewController-Subtitles"
```

### Manually installation

[Download](https://github.com/mhergon/MPMoviePlayerController-Subtitles/raw/master/MPMoviePlayerController-Subtitles.swift) (right-click) and add to your project.

### Requirements

| Version | Language  | Minimum iOS Target  |
|:--------------------:|:---------------------------:|:---------------------------:|
|          1.x         |            Swift            |            iOS 8            |


### Usage


```swift
import AVPlayerViewControllerSubtitles
```

```swift
// Video file
let videoFile = NSBundle.mainBundle().pathForResource("trailer_720p", ofType: "mov")

// Subtitle file
let subtitleFile = NSBundle.mainBundle().pathForResource("trailer_720p", ofType: "srt")
let subtitleURL = NSURL(fileURLWithPath: subtitleFile!)

// Movie player
let moviePlayer = AVPlayerViewController()
moviePlayer.player = AVPlayer(URL: NSURL(fileURLWithPath: videoFile!))
presentViewController(moviePlayer, animated: true, completion: nil)

// Add subtitles
moviePlayer.addSubtitles().open(file: subtitleURL)
moviePlayer.addSubtitles().open(file: subtitleURL, encoding: NSUTF8StringEncoding) // optional

// Change text properties (optional)
moviePlayer.subtitleLabel?.textColor = UIColor.redColor()

// Play
moviePlayer.player?.play()
```

## Screenshot
<p align="center" >
<img src="https://raw.github.com/mhergon/AVPlayerViewController-Subtitles/master/assets/screenshot.png" alt="Screenshoot" title="Screenshoot">
</p>

## Contact

- [Linkedin][2]
- [Twitter][3] (@mhergon)

[2]: https://es.linkedin.com/in/marchervera
[3]: http://twitter.com/mhergon "Marc Hervera"

## License

Licensed under Apache License v2.0.
<br>
Copyright 2015-2016 Marc Hervera.
