# Faceless

Faceless is where you can talk freely. Share messages with your friends and the whole world.

## Preview ([Android](https://www.delight.im/get/faceless))

Main screen | Message details | Adding messages
:-------------------------:|:-------------------------:|:-------------------------:
<img src="Graphics/Screenshots/Version 2.9.0/01 Main.png?raw=true" alt="01 Main" width="200" /> | <img src="Graphics/Screenshots/Version 2.9.0/02 Details.png?raw=true" alt="02 Details" width="200" /> | <img src="Graphics/Screenshots/Version 2.9.0/03 Add.png?raw=true" alt="03 Add" width="200" />

## Download

 * Android: [Google Play](https://www.delight.im/get/faceless) or [GitHub](Releases/Android/Latest.apk?raw=true)

## Installation

### Android

 1. Rename `Android/src/im/delight/faceless/ConfigExample.java` to `Android/src/im/delight/faceless/Config.java` and replace all occurrences of `REPLACE_THIS_WITH_VALUE` with a proper configuration value for your setup
 2. Add the following dependencies as library projects:
    * [Android-Countries](https://github.com/delight-im/Android-Countries)
	* [Android-Time](https://github.com/delight-im/Android-Time)
	* [ActionBar-PullToRefresh](https://github.com/chrisbanes/ActionBar-PullToRefresh) with [SmoothProgressBar](https://github.com/castorflex/SmoothProgressBar)

### Server

 1. Set up a web server with Apache + PHP + MySQL
 2. Set up a Twilio account and register an SMS-enabled phone number POSTing to the public URL of `Server/htdocs/internal/sms_verify.php`
 3. Rename `Server/config.example.php` to `Server/config.php` and replace all occurrences of `REPLACE_THIS_WITH_VALUE` with a proper configuration value for your setup
 4. Set up cron jobs for `htdocs/workers/dispatcher.php`, `htdocs/workers/score_updater.php` and `htdocs/workers/cleaner.php`
 5. Enable `mod_rewrite` for the Apache web server

## Security

 * [Disclose bugs and vulnerabilities](https://www.delight.im/security/faceless) or read more about [security](SECURITY.md).

### Data center locations

 * Apache/PHP: Europe (AWS `eu-west-1` region)
 * MySQL: Europe (AWS `eu-west-1` region)

## Translations

 * Help translate by visiting [Faceless on Localize](https://www.localize.im/v/36)
 * View the full [list of translators](TRANSLATORS.md)

## Known issues

### Android

 * The app cannot be installed on devices without telephony features (e.g. tablets). This is because (a) the app is optimized for phones and (b) users would have to enter their phone number manually, otherwise, and (c) the app curently can run on a single device only.

### Twilio

 * "At the receiving end of SMS messages, Twilio cannot guarantee that every international SMS message sent to us will be received in your SMS log. Twilio accepts these messages, however it is the responsibility of the sending phone number carrier to deliver the SMS message to our network. I'd particularly recommend using our UK mobile numbers or Swedish mobile numbers. These numbers have been pretty successful at receiving SMS from other countries. There are two other things you should be aware of which affect the delivery of inbound international SMS: not all users will have plans which support international SMS, and international roaming might make the phone unable to send or receive SMS. If your users are primarily travelers, it's very likely that you will see issues of this type." (Lauren Buchsbaum from Twilio)

## Similar services

 * [Secret](http://www.secret.ly/)
 * [Whisper](http://whisper.sh/)
 * [Yik Yak](http://yikyakapp.com/)
 * [Experience Project](http://www.experienceproject.com/)
 * [PostSecret](http://postsecret.com/)

## License

```
Copyright (C) 2014 www.delight.im <info@delight.im>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see {http://www.gnu.org/licenses/}.
```