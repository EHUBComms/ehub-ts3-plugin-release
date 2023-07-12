# TS3 plugin

Installation:

Check which Team Speak version you have (32bit or 64bit).
Download both .exe and .zip files. If you have TeamSpeak 32bit - download x86.exe and x86.zip, if 64bit - x64.exe and x64.zip files.
Copy AudioRecordingUpload_x64.dll or AudioRecordingUpload_x86.dll and AudioRecordingUpload.ini into the ts3 client plugins folder.
Copy the other dlls into the main 'TeamSpeak 3 Client' directory.
Replace the plugins\AudioRecordingUpload.ini file with the one sent in this message.

Usage:

You can tell if the plugin is successfully loaded by the client, if once you connect to a ts server, the window title of the client shows a message, that the plugin got initialized. Start a voice recording or a multitrack recording. Once the recording get stopped, the plugin shows a popup and asks if the recorded wav files should get compressed to mp3 and uploaded to the AWS S3 bucket.

Compression conversation and upload percentage status will be shown in the ts3 client window title bar. Also if an error appears or on success, the status is always shown in the window title bar.

For more details (eg. on errors), you can open the ts3 client log.

The plugin listens on TCP port 3000 for incoming GSI event payloads. To enable csgo events sending to the plugin, copy the "gamestate_integration_AudioRecordingUpload.cfg" file into your

C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg

folder.

The gamestate integration does load automatically and sends the ingame round start event to the ts3 plugin, which logs the timestamps and uploads the logfile to S3 too.
# ehub-ts3-plugin-release
