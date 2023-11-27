# Chat Utility Mod (CUM)

## Finally, a public update after more than a year!

This epic mod sends messages based on various in-game actions of you and other players!

## How To Use CUM
This mod has many convars, to get started open console and type `cum_` to see the list of available convars. To do something like enable kill messages, type and enter the following : `cum_kill_msgs_enabled 1` and if you want to change the default kill message, type `cum_kill_msgs "I killed @vn, they got rekt Xddddd"` This will make it where when you kill someone, it'll send the message "I killed (the name of the player you killed), they got rekt Xddddd" in chat. Any instances of @vn will be replaced with the victim name of the message type, and @an will be replaced with the attacker of the message type. If you do death messages and include @an in your message, it'll put the name of the person who killed you in place of it. For the responder, @sn is used for the message sender name. All of these proxies can be changed through convars such as `cum_victim_name_proxy`.

If you want to have multiple different messages that are randomly selected when you kill someone, simply put multiple messages in the convar `cum_kill_msgs` and separate them with a `|` character like this : `cum_kill_msgs "your first message|your second message|your third message"`

There are also different modes that you can use, for example with kill messages you can either use the random mode which is on by default, or by setting `cum_kill_msgs_mode 0` or you can use the list mode by setting `cum_kill_msgs_mode 1`, which will send your messages in the order they're put in the convar. For the responder there are 3 modes. Random mode which is on by default, or by setting `cum_responder_msgs_mode 0`, there's also list mode by setting `cum_responder_messages_mode 1` which is the same as the list mode for kill messaages, and there's also the copy-cat mode which sends the same message as the person it's responding to.

There are more settings for the responder which are listed below
- `cum_responder_whitelist` This convar current only takes 1 username of a player you want to target with the responder, in the future it may be able to take more than 1 player at a time.
- `cum_responder_msg_contains` Searches for a string in each message, and only responds if the message contains that string. It is not case sensitive.

Here's a huge tip for making message lists : If you put a blank message in your list like this `| |` then when the chat utility mod gets to that message it will not send a message. This can be used with the random message mode to create a chance of sending or not sending a message based on how many blank messages you put in the list

There's also a way to delay messages that are sent with the convar `cum_msg_delay` which influences all message types. The delay is in seconds (should be obvious lol)

If you really want to spam (which I do not recommened and may or may not put you at major risk for being banned/kicked from a server) then you can use the shapes feature that was introduced in version 1.1.0 of the CUM. The shapes feature can be accessed through the following convars
- `cum_kill_msgs_shape_enabled` : Sets whether or not the shapes feature for kill messages is enabled
- `cum_kill_msgs_shape` : changes the shape of the shapes feature for kill messages, 0 is a line and 1 is a sine wave
- `cum_death_msgs_shape_enabled` : Sets whether or not the shapes feature for death messages is enabled
- `cum_death_msgs_shape` : changes the shape of the shapes feature for death messages, 0 is a line and 1 is a sine wave
- `cum_suicide_msgs_shape_enabled` : Sets whether or not the shapes feature for suicide messages is enabled
- `cum_suicide_msgs_shape` : changes the shape of the shapes feature for suicide messages, 0 is a line and 1 is a sine wave
