# Eclipse_CC
Eclipse CORE | Character Creation documentation

1. Put `Eclipse_Core` && `Eclipse_CC` in your resource directory
2. Add ensure in your `server.cfg`


| Command | Description |
| --- | --- |
| `ensure eclipse_Core` | You must ensure this resource the first |
| `ensure eclipse_CC` | just add it ;/ |

3. MySql settings (resources\eclipse_Core\config\database.json)


  ![1](https://user-images.githubusercontent.com/36680471/114997401-759f4a80-9ea8-11eb-8b81-ba096d1c6e6b.PNG)
  
4. Turn on Mysql 
5. Load dump database in your mysql client  
[dump.zip](https://github.com/douglasprod/Eclipse_CC/files/6323759/dump.zip)
6. Change NUI language in `resources\eclipse_CC\config\config.json`. You can choose EN(English) and RU(Russian), for now

![image](https://user-images.githubusercontent.com/36680471/114999878-ea738400-9eaa-11eb-8f45-7a1fcdf928db.png)

7. Start your server
8. Enjoy!



`API`
You can try doesn't use Eclipse Core and connect CharacterCreation for your framework(vRP, Esx, etc..)

| ServerEvent | Data | Description |
| --- | --- | --- |
| `ECLIPSE:CreateCharacter`| string, string | This event triggered when you create your character. You get CharacterData https://pastebin.com/uD4EUVC5 and CharacterCloth https://pastebin.com/Npe1MEnK. You need diserialize(decode) it on server-side  |
| `ECLIPSE:LoadCharacter` | int | It triggered when you choose character. It sends character id |
| `ECLIPSE:LoadCharactersList` | - | It triggered when you first spawn. You need make array with CharacterInfo https://pastebin.com/jEm4wrBM and CharacterData(for spawn ped) https://pastebin.com/uD4EUVC5 and than you need trigger client event `ECLIPSE:StartCharactersCreation` |

| ClientEvent | Data | Description |
| --- | --- | --- |
| `ECLIPSE:StartCharactersCreation`| string, string | This event you need triggered when you want start character select. You need send two array. CharacterInfo https://pastebin.com/jEm4wrBM and CharacterData(for spawn ped). Correct example: ECLIPSE:StartCharactersCreation(charactersInfo, charactersData) |


For more question and works, help write in Discord. https://discord.gg/8nXR6rfB2C
