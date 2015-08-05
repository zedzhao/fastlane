<h3 align="center">
  <a href="https://github.com/KrauseFx/fastlane">
    <img src="assets/fastlane.png" width="150" />
    <br />
    fastlane
  </a>
</h3>
<p align="center">
  <a href="https://github.com/KrauseFx/deliver">deliver</a> &bull; 
  <a href="https://github.com/KrauseFx/snapshot">snapshot</a> &bull; 
  <a href="https://github.com/KrauseFx/frameit">frameit</a> &bull; 
  <a href="https://github.com/KrauseFx/PEM">PEM</a> &bull; 
  <a href="https://github.com/fastlane/sigh">sigh</a> &bull; 
  <a href="https://github.com/KrauseFx/produce">produce</a> &bull;
  <a href="https://github.com/KrauseFx/cert">cert</a> &bull;
  <a href="https://github.com/KrauseFx/codes">codes</a> &bull;
  <a href="https://github.com/fastlane/spaceship">spaceship</a> &bull;
  <a href="https://github.com/fastlane/pilot">pilot</a> &bull;
  <a href="https://github.com/fastlane/boarding">boarding</a>
</p>
-------

<p align="center">
    <img src="assets/gym.png">
</p>

gym
============

[![Twitter: @KauseFx](https://img.shields.io/badge/contact-@KrauseFx-blue.svg?style=flat)](https://twitter.com/KrauseFx)
[![License](http://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/fastlane/gym/blob/master/LICENSE)
[![Gem](https://img.shields.io/gem/v/gym.svg?style=flat)](http://rubygems.org/gems/gym)

###### Build your iOS app the right way

Get in contact with the developer on Twitter: [@KrauseFx](https://twitter.com/KrauseFx)

-------
<p align="center">
    <a href="#features">Features</a> &bull; 
    <a href="#installation">Installation</a> &bull; 
    <a href="#usage">Usage</a> &bull; 
    <a href="#resign">Resign</a> &bull; 
    <a href="#how-does-it-work">How does it work?</a> &bull; 
    <a href="#tips">Tips</a> &bull; 
    <a href="#need-help">Need help?</a>
</p>

-------

<h5 align="center"><code>gym</code> is part of <a href="https://fastlane.tools">fastlane</a>: connect all deployment tools into one streamlined workflow.</h5>

# What's gym?

`gym` is a drop-in replacement for [shenzhen](https://github.com/nomad/shenzhen), a tool for building your iOS apps.

[shenzhen](https://github.com/nomad/shenzhen) does both building and distributing iOS apps. Since we now all use [fastlane](https://fastlane.tools) for distributing it makes sense to have *one* tool dedicated for building your app. 

`gym` uses the latest and best APIs to build and sign your application which results in much faster build times compared to `shenzhen`

Advantages of `gym` compared to `shenzhen` and plain `xcodebuild`

- Around 30% faster build times
- Beautiful inline build output
- Easy and dynamic configuration using parameters, environment variables, manual inputs or using a `Gymfile`
- Built-in right into `fastlane`
- Generate both an `ipa` and a compressed `dSYM` file
- Manually trigger a build by only running `gym`, never remember any complicated `xcodebuild` commands again
- `gym` actively helps you resolve common issues like problems with Code Signing, wrongly configured projects and more
- Automatic verification of inputs, like the available schemes or project files

# Installation

This tool is still work in progress. You can already try it by cloning the repo and running

    sudo bundle install && sudo rake install

Make sure, you have the latest version of the Xcode command line tools installed:

    xcode-select --install

# Usage

    gym

That's all you need to build your application. If you want more control, here are some available parameters:

    gym --workspace "Example.xcworkspace" --scheme "AppName" --clean

For a list of all available parameters use

    gym --help

# Gymfile

Since you might want to manually trigger a new build but don't want to specify all the parameters every time, you can store your defaults in a so called `Gymfile`.

Run `gym init` to create a new configuration file which may contain data like this:

```ruby
scheme "Example"

sdk "9.0"

output_directory "./build"
```

# Tips
## [`fastlane`](https://fastlane.tools) Toolchain

- [`fastlane`](https://fastlane.tools): Connect all deployment tools into one streamlined workflow
- [`deliver`](https://github.com/KrauseFx/deliver): Upload screenshots, metadata and your app to the App Store
- [`snapshot`](https://github.com/KrauseFx/snapshot): Automate taking localized screenshots of your iOS app on every device
- [`frameit`](https://github.com/KrauseFx/frameit): Quickly put your screenshots into the right device frames
- [`PEM`](https://github.com/KrauseFx/pem): Automatically generate and renew your push notification profiles
- [`produce`](https://github.com/KrauseFx/produce): Create new iOS apps on iTunes Connect and Dev Portal using the command line
- [`cert`](https://github.com/KrauseFx/cert): Automatically create and maintain iOS code signing certificates
- [`codes`](https://github.com/KrauseFx/codes): Create promo codes for iOS Apps using the command line
- [`spaceship`](https://github.com/fastlane/spaceship): Ruby library to access the Apple Dev Center and iTunes Connect
- [`pilot`](https://github.com/fastlane/pilot): The best way to manage your TestFlight testers and builds from your terminal
- [`boarding`](https://github.com/fastlane/boarding): The easiest way to invite your TestFlight beta testers 

##### [Like this tool? Be the first to know about updates and new fastlane tools](https://tinyletter.com/krausefx)

## Use the 'Provisioning Quicklook plugin'
Download and install the [Provisioning Plugin](https://github.com/chockenberry/Provisioning).

# Need help?
- If there is a technical problem with `gym`, submit an issue.
- I'm available for contract work - drop me an email: gym@krausefx.com

# License
This project is licensed under the terms of the MIT license. See the LICENSE file.

> This project and all fastlane tools are in no way affiliated with Apple Inc. This project is open source under the MIT license, which means you have full access to the source code and can modify it to fit your own needs. All fastlane tools run on your own computer or server, so your credentials or other sensitive information will never leave your own computer. You are responsible for how you use fastlane tools.
