# Chat Utility Mod (CUM)

This epic mod sends messages based on various in-game actions of you and other players!

## How To Use CUM
This mod has many convars, to get started open console and type `cum_` to see the list of available convars. To do something like enable kill messages, type and enter the following : `cum_kill_msgs_enabled 1` and if you want to change the default kill message, type `cum_kill_msgs "I killed @vn, they got rekt Xddddd"` This will make it where when you kill someone, it'll send the message "I killed (the name of the player you killed), they got rekt Xddddd" in chat. Any instances of @vn will be replaced with the victim name of the message type, and @an will be replaced with the attacker of the message type. If you do death messages and include @an in your message, it'll put the name of the person who killed you in place of it. For the responder, @sn is used for the message sender name. All of these proxies can be changed through convars such as `cum_victim_name_proxy`.

If you want to have multiple different messages that are randomly selected when you kill someone, simply put multiple messages in the convar `cum_kill_msgs` and separate them with a `|` character like this : `cum_kill_msgs "your first message|your second message|your third message"`

There are also different modes that you can use, for example with kill messages you can either use the random mode which is on by default, or by setting `cum_kill_msgs_mode 0` or you can use the list mode by setting `cum_kill_msgs_mode 1`, which will send your messages in the order they're put in the convar. For the responder there are 3 modes. Random mode which is on by default, or by setting `cum_responder_msgs_mode 0`, there's also list mode by setting `cum_responder_messages_mode 1` which is the same as the list mode for kill messaages, and there's also the copy-cat mode which sends the same message as the person it's responding to, it's `cum_responder_msgs_mode 2` You can also change what team it responds to using `cum_responder_team` when set to 0 it responds to both teams, when set to 1 it responds only to your team, when set to 2 it responds only to enemy team. You can also use the new "reading that" function added in CUM v1.4.0, which essentially responds to a message with a certain length with a specific message. To enable it you can use `cum_responder_reading_that_enabled 1` and to set the message you can use `cum_responder_reading_that_msg` also you can set the lenght required for it to respond with that message using `cum_responder_reading_that_length`, the default is 45

There are more settings for the responder which are listed below
- `cum_responder_whitelist` This convar current only takes 1 username of a player you want to target with the responder, in the future it may be able to take more than 1 player at a time.
- `cum_responder_msg_contains` Searches for a string in each message, and only responds if the message contains that string. It is not case sensitive.

Here's a huge tip for making message lists : If you put a blank message in your list like this `| |` then when the chat utility mod gets to that message it will not send a message. This can be used with the random message mode to create a chance of sending or not sending a message based on how many blank messages you put in the list

There's also a way to delay messages that are sent with the convar `cum_msg_delay` which influences all message types. The delay is in seconds (should be obvious lol)

There's also a typing based delay, added in CUM v1.5.0 to use it simply type `cum_typing_delay_enabled 1` and set the typing speed (in characters per second) with `cum_typing_speed`

If you really want to spam (which I do not recommened and may or may not put you at major risk for being banned/kicked from a server) then you can use the shapes feature that was introduced in version 1.1.0 of the CUM. The shapes feature can be accessed through the following convars
- `cum_kill_msgs_shape_enabled` : Sets whether or not the shapes feature for kill messages is enabled
- `cum_kill_msgs_shape` : changes the shape of the shapes feature for kill messages, 0 is a line and 1 is a sine wave
- `cum_death_msgs_shape_enabled` : Sets whether or not the shapes feature for death messages is enabled
- `cum_death_msgs_shape` : changes the shape of the shapes feature for death messages, 0 is a line and 1 is a sine wave
- `cum_suicide_msgs_shape_enabled` : Sets whether or not the shapes feature for suicide messages is enabled
- `cum_suicide_msgs_shape` : changes the shape of the shapes feature for suicide messages, 0 is a line and 1 is a sine wave

## List of all ConVars and their uses
- `cum_kill_msgs_enabled` : whether kill messages are on or not. 0 for off and 1 for on.
- `cum_kill_msgs_shape_enabled` : whether to use shapes with kill messages or not. 0 for off and 1 for on.
- `cum_kill_msgs_shape` : what shape to use for kill messages. 0 for a 15 message straight line, 1 for a sine wave.
- `cum_kill_msgs_mode` : what mode to use for kill messages. 0 for random message, 1 for list (in order from start to finish)
- `cum_death_msgs_enabled` : whether death messages are on or not. 0 for off and 1 for on.
- `cum_death_msgs_shape_enabled` : whether to use shapes with death messages or not. 0 for off and 1 for on.
- `cum_death_msgs_shape` : what shape to use for death messages. 0 for a 15 message straight line, 1 for a sine wave.
- `cum_suicide_msgs_enabled` : whether suicide messages are on or not. 0 for off and 1 for on.
- `cum_suicide_msgs_shape_enabled` : whether to use shapes with suicide messages or not. 0 for off and 1 for on.
- `cum_suicide_msgs_shape` : what shape to use for suicide messages. 0 for a 15 message straight line, 1 for a sine wave.
- `cum_msgs_splitter` : what character to use to split messages in message lists.
- `cum_shapes_spacing_time` : how much time (in seconds) should be between each message when using shapes.
- `cum_victim_name_proxy` : what string should be replaced with the victim name in messages.
- `cum_attacker_name_proxy` : what string should be replaced with the attacker name in messages.
- `cum_kill_msgs` : the kill message/messages to use.
- `cum_death_msgs` : the death message/messages to use.
- `cum_suicide_msgs` : the suicide message_messages to use.
- `cum_msg_delay` : the set message delay to use in seconds.
- `cum_responder_enabled` : whether responder messages are on or not. 0 for off and 1 for on.
- `cum_responder_msgs` : the responder message/messages to use.
- `cum_responder_msgs_mode` : what mode to use for responder messages. 0 for random, 1 for list (in order from start to finish), 2 for copy cat (sends the same message it's responding to back).
- `cum_responder_sender_name_proxy` : what string should be replaced with the sender name in responder messages.
- `cum_respodner_msg_contains` : if left blank, this will do nothing, but if it is changed the responder will only respond to messages containing the string in this ConVar
- `cum_responder_team` : what team to respond to, 0 for all teams, 1 for your team, 2 for enemy team.
- `cum_responder_whitelist` : Currently only works with 1 player name, if this convar is not blank the responder will only respond to messages sent by the username put in this ConVar.
- `cum_responder_self_reply` : whether the responder should reply to your messages. 0 for off and 1 for on.
- `cum_typing_delay_enabled` : whether messages should be sent with a delay based on a set typing speed (set in `cum_typing_speed`)
- `cum_typing_speed` : Typing speed for `cum_typing_delay_enabled` in characters per second.
- `cum_responder_reading_that_enabled` : whether to send "reading that" responder messages. If enabled a the responder will respond to messages over a certain length with a special message.
- `cum_responder_reading_that_length` : the required message length for the "reading that" feature to respond to the message
- `cum_responder_reading_that_msg` : message to send when using "reading that" feature
