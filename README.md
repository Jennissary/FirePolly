# FirebotPollyTTSvoices (aka FirePolly)
Firebot setup files and instructions for having Amazon Polly TTS voices read Twitch chat
This Firebot setup will read all chat messages and basic Twitch events via an Amazon Polly neural Text To Speech voice of your choice. It can also read messages for both you and your stream to hear, and allow viewers to pick which voice is used to read their chat messages. 

Features include:
- A "solo" TTS voice, which reads only to the audio device of your choice, in the the default voice for the setup you download. 
- An "all" set of TTS voices, which allows viewers to set the voice which reads their own chat messages. 
- Commands available to the streamer and moderators, which customize the speech speed, speech volume, and the cooldown period for viewers to change their TTS voices. 
- Commands which preview all available masculine voices, all available feminine voices, and each individual voice.
- A limit of 5 emotes per chat message. Messages with more than 5 emotes will be deleted, not read to TTS, and repeat offenders will be timed out for increasingly long periods.
- A subtle sound effect for when each new chat message comes in, to help know how many are queued while the TTS is still reading.

Recordings of available voices are on Jennissary's Github page. Select a voice name that you want to be your default voice, and download the zipped folder with that voice name. The default voice will read confirmations of commands in the setup, all basic Twitch channel events, chat messages in the "Solo" voice event, and chat messages in the "All" voice event who have not assigned a voice for themselves.

Each zipped folder includes: 
- A firebot Setup import file.
- A "Good tone" alert sound file.
- A "Bad tone" alert sound file.
- A "Read me" text file, in plain text and HTML, with setup instructions.
- "About this setup" file (this file), in plain text and HTML.
