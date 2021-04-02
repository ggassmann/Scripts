- DIALOG 0.1
Dialog is a script that makes chat a bit more fun and easier to parse. It is token-based, either using selected and targeted tokens or specific token IDs.

`!Dialog --id|token_id --to|token_id --type|type --message`

`--id|token_id`: Required. Specifies the speaker

`--to|token_id`: Optional. If a recipient is specified, the dialog becomes a whisper.

`--type|quote|whisper|emote|ooc`: Optional. This determines the style of the dialog box to display. If not used, the script assumes an in-character quote. Whisper doesn't actually do anything, but is included as an option for making it plain that a whisper is intended. specifying a --to|token_id automatically chooses the whisper style.

`--message`: anything placed after -- that does not match one of the other tags becomes the defacto message.

**Token Image:** Clicking on the token image will repeat the last configuration. If you sent an emote, it will send another emote, propting you for the content. If you sent a whisper, it will send a whisper to the person you were whispering to. In this way, two characters who have started a whispered conversation can keep it going by just clicking on their token image in chat.
**Button Line:** There is a line of buttons at the bottom of the dialog that you can use to change the type of dialog. This will also set the token image button to repeat the dialog type.
Note about whispers: because the API cannot issue a target command, you must initiate a whisper using a macro. Once it is established, you can use the token image button.

**Sample Macros**

**Basic quote:** !dialog --id|@{selected|token_id} --?{message|message}

**Start a whisper:** !dialog --id|@{selected|token_id} --@{target|token_id} --?{message|message}

`!dialog --help`: displays this help box.