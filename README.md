# Build
1. `git clone https://github.com/RSATom/HelloJanusAudiobridge.git && cd HelloJanusAudiobridge`
2. `npm install && cordova prepare ios --debug`
3. `open ./platforms/ios/HelloJanusAudiobridge.xcworkspace`
4. Configure signing in project properties
5. Build with Xcode or from command line with `cordova build ios`

# Crash issue with iosrtc v8.0
1. Run application.
2. Press `Start` button inside application
3. Enter any nickname and press `Join the room`
4. Profit! - Crash with `Swift runtime failure: Unexpectedly found nil while unwrapping an Optional value` at https://github.com/cordova-rtc/cordova-plugin-iosrtc/blob/91cccc5660f79babbbb889697bc60b5fd4936316/src/PluginRTCPeerConnection.swift#L397 on `pluginRTCRtpTransceiver!` unwrap
