Forward your server's chat to your DIscord server using Webhooks.

Psystec's Discord: discord. /EyRgFdA

## Features

* Global Chat forward.
* Team Chat forward.
* Notifies when a player connects or disconnects.
* Chat format can be customized.
* You can Enable/Disable Discord metions in Rust chat.
* Can configure the discord chat to show the players steam icon.
* Ignore messages containing banned words being sent to the discord.

## Permissions
 
To reload the config file with a console command you will need `chattodiscord.admin`

## Console Commands

- `chattodiscord` -- Displays the commands.
- `chattodiscord loadconfig` -- Loads the config file, handy for if you make changes in the config file.

## Configuration
*  If you don't want to display the clients steam icon if discord leave the `SteamApiKey` empty.
*  If you don't want to display GLOBAL chats, leave the `GlobalChatWebhook` empty.
*  If you don't want to display TEAM chats, leave the `TeamChatWebhook` empty.
*  If you don't want to display player connections in chats, leave the `ConnectionWebhook` empty.
 
```json
{
  "SteamApiKey": "https://steamcommunity.com/dev/apikey",
  "GlobalChatWebhook": "",
  "TeamChatWebhook": "",
  "ConnectionWebhook": "",
  "AllowMentions": false,
  "AllowSpecialCharacters": true,
  "GlobalChatFormat": "[{time}] [**GLOBAL**] **{username}**: `{message}`",
  "TeamChatFormat": "[{time}] [**TEAM**] **{username}**: `{message}`",
  "ConnectionFormat": "[{time}] **{username}**: {connectionstatus}",
  "DateFormat": "yyyy-MM-dd HH:mm:ss",
  "FilterBadWords": [ "badword1", "badword2" ]
}
```
## Message Placeholders

- `{time}` -- Displays the time using the DateFormat setting in the config file.
- `{username}` -- Displays the client's steam username.
- `{userid}` -- Displays the client's steam id.
- `{connectionstatus}` -- Displays the client's connection status (Connected/Disconnected) (ConnectionFormat).
- `{message}` -- Displays the client's RUST message (ChatFormats).

## Localization

 ```json
{
  "Connected": "Connected",
  "Disconnected": "Disconnected",
  "NoPermission": "You do not have permission to use this command.",
  "FileLoaded": "File loaded.",
  "cmdCommand": "COMMAND",
  "cmdDescription": "DESCRIPTION",
  "cmdReload": "Reads the config file.",
}
```

## Discord Notifications

Add the SteamApiKey to allow the plugin to display the player's steam profile icon as the Webhook's icon.
Key can be generated here: [https://steamcommunity.com/dev/apikey](https://steamcommunity.com/dev/apikey)

## Examples

- Discord Chat:

![](https://i.imgur.com/c29oSex.png)