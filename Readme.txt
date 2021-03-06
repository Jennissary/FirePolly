Table of Contents:
Disclaimers
Features
Prerequisites
Setup File Instructions
Optional setup steps
Contact information and feedback

Disclaimers: 
Amazon Polly TTS voices are only free for the first year. After that, it converts to a pay-as-you-go model, charging per 1 million characters used.
Having a bot account logged in to Firebot is highly recommended for this setup. The TTS will ignore chat messages from your linked bot account, meaning bot responses and timers will not be read unless you add them as a separate event. By default, Firebot will chat as your username if you do not have a bot account logged in. 
Longer chat messages may have a pause after them which is longer than actually required. 
Chat messages containing only a command may be spoken over by the next chat message. 
Chat messages containing a URL or ampersand symbol will be skipped. 

Features: 
1. Global limit of 5 emotes per chat message. Messages with more than 5 will not read via TTS, and will time out repeat offenders, (up to 10 minutes for more than 10 emote spam messages). 
2. Commands available to streamer and moderators to control the TTS speech rate and volume. Use the command !speechrate, followed by a space, and a number between 1 and 200. Use the command !speechvolume, followed by a space, and a number between 1 and 100. Use these commands without any numbers to see what the current rate and volume are. The speech rate and volume are a global setting for all Amazon Polly effects included in this setup. 
3. Voice sample commands. Streamer and moderators can use the command !voicesample, followed by masculine, feminine, or the name of any Polly English voice, to hear a brief sample of each. 
4. Set voice commands, available to all viewers. Viewers can use the command !setvoice, followed by the name of the Polly English voice they would like their chat messages to be read in. 
5. Set Cooldown command. Streamer and moderators can use the command !setcooldown, followed by a space, then a number. That number will be the time, in minutes, viewers must wait before they can change the Amazon Polly voice which reads their chat messages. 
6. A separate set of effects for viewer customized voices for chat messages, or a single voice for all chat messages. These can be switched on or off in the Events menu, and the single voice can be set to a different audio device if you do not want your stream to hear all chat messages. 
7. A !stop command, which will immediately cut off any speech that is currently being read, and clear the TTS queue. This command can also be triggered from a stream deck. This is useful for messages which are excessively long, unsafe, or malicious in nature. 


Prerequisites, (do these before importing the setup file):
1. Create an Amazon Web Services account, and import to Firebot. Follow all steps at the following webpage: https://github.com/crowbartools/Firebot/wiki/Amazon-Polly-Integration
2. In Firebot's settings, go to advanced, and find the Persist Custom Variables drop-down menu. Set this to "on". This will ensure your preferred speech rate and volume are preserved whenever Firebot is restarted.
3. In Firebot's Settings, go to General, and find the Sound Output Device drop-down menu. All Polly TTS will be routed to this output device, so ensure it is a device your stream can hear if you wish. Individual events can be routed to a different device if you choose. 
4. In Firebot's Moderation Menu, go to Emote/Emoji limit, and find the switch to enable this feature. Set the max per message limit to 5, and do not populate response text. This setup already includes custom response text for viewers who exceed the 5 emote limit.
5. Restart Firebot.

Setup File Instructions: 
1. Download and extract the zipped folder for the plugin. Its location does not matter, and can be deleted later.
2. Optional: Save the sound files "Good tone zapsplat" and "Bad tone zapsplat" to a location which will not change. Refer to optional setup steps 5 through 11 for their usage. All other files in the setup folder can be deleted once setup is complete.
3. Open Firebot, and go to the settings menu. Under "Setups", select the button called "Import Setup". Select the button "Choose File". Browse for the folder you extracted in Step 1, and open the file titled "Amazon Polly Firebot Setup". Select the button Import Setup. 
4. Navigate to the Events menu, then find the Event Set titled Text to speech Polly. This is where the bulk of this setup occurs. Browse the events in this set, to see the standard events that come built into the setup. Generic chat messages and TTS responses are built in for the following Twitch events: Follow, Host, Raid, Channel Reward Redemption, Sub, Cheer, Gift Sub. Feel free to customize the chat and TTS responses, and add sound effects or animations as alerts! The Cheer event, for example, has a couple of fun conditional effects which you can revise or remove. Remember that the chat message effect and the TTS effect in these events will not match by default; you need to revise each one separately. 

Optional setup steps:
5. Add the subtle sound effect which plays whenever a new chat message comes in. This helps to know how many messages are queued to be read, while the TTS is still reading them. Navigate to the Events menu, then find the Event Set titled Text to speech Polly. Find the event titled "Chat - All stream Polly Voices", Select the drop-down ellipses menu, then select edit. 
6. Scroll down to the Effects section, then find the event titled "Play Sound". This is for the alert tone which plays immediately whenever a new chat message comes in. Select the drop-down ellipses menu called "open effect menu", then select edit. 
7. Find and select the button "Choose File", then navigate to the folder location where you saved the sound file "Good tone zapsplat". Select this sound file. 
Note: you can customize the volume and audio output device of this sound in this menu, or select another sound entirely. If you use the zapsplat sound, you must credit the website zapsplat somewhere in your channel info. 
8. Scroll to the bottom of the Play Sound Menu, then select the Save button. 
9. In this same Event menu, under the Effects section, find the effect titled "Conditional Effects". Select the drop-down ellipses menu called "open effect menu", then select edit. Find the Else If condition called "Emote spam moderation", then select it to expand. There should be an Effects section within this Else If effect. Find the effect at the bottom of the list titled "Play Sound". This is for the alert tone which plays if a chat message exceeds the 5 emote limit. 
10. Select the drop-down ellipses menu called "open effect menu", then select edit. Find and select the button "Choose File", then navigate to the folder location where you saved the sound file "Bad tone zapsplat". Select this sound file. 
Note: you can customize the volume and audio output device of this sound in this menu, or select another sound entirely. If you use the zapsplat sound, you must credit the website zapsplat somewhere in your channel info. 
11. Scroll to the bottom of the Play Sound Menu, then select the Save button. 
12. Customize your solo Polly voice, so that your stream can or cannot hear it. Navigate to the Event titled "Chat - Solo Polly voice" in the Text to Speech Polly Event Set. Ensure this is switched off whenever you have the "Chat - All Stream Polly voices" switched on. Enabling this event will perform the same things as the "All Stream Polly Voices", but will do so in only one voice. You can easily customize the audio output device to a different one than the Default. 
13. Link the Stop command to a Streamdeck button. In the Firebot menu Preset Effect Lists, find the item titled Stop. Select the drop-down ellipses menu, then select edit. At the bottom of this menu, expand the menu "How to Trigger from Streamdeck", then select it to expand. Follow the steps listed here. Currently, known streamdeck software is inaccessible with screen readers, and will likely require sighted assistance.
14. Add usernames to the list of ignored usernames for chat message events. Navigate to the Event titled "Chat - All stream polly voices" or "Chat - Solo Polly Voice" in the Text to Speech Polly Event Set. Select the drop-down ellipses menu, then select edit. Scroll down to the Effects section, then find the event titled "Conditional Effects". TSelect the drop-down ellipses menu called "open effect menu", then select edit. Select the "If" Condition called "Check that name is not bot and emotes less than 5", and select it to expand the menu. Above the effects area is a list of 2 conditions: an array length variable, and Username is not bot. Find the plus sign button called "add new condition". Select the drop-downs: Type (username), Comparator (is not). Enter your username in the "expected value" text field, or the username of any other bots you don't want read via this TTS.

Contact information and feedback:
If you have any further questions or need assistance, feel free to message Jennissary directly on Twitter, Twitch, or Discord (Jennissary#1090). You can also reach out to the Crowbar questions discord channel!