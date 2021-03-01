<a href="https://nodei.co/npm/discord-image-generation/"><img src="https://nodei.co/npm/discord-image-generation.png?downloads=true&downloadRank=true&stars=true"></a>

# discord-image-generation

A powerfull module that allow you to generate awesome images.

# Bugs and glitches

Feel free to report all bugs and glitches by creating an issue in the <a href="https://github.com/Mr-KayJayDee/discord-image-generation/issues">issue section.</a>

A correct and understandable issue contains : 
- Steps to reproduce 
- Code that summonned the error
- The complete error

You can also join me on my <a href="https://discord.gg/Uqd2sQP">discord server.</a>

<a href="https://discord.gg/Uqd2sQP"><img src="https://discord.com/api/guilds/527836578912010251/widget.png" alt="Amandine support server"/></a>

# Download

You can download it from <a href="https://www.npmjs.com/package/discord-image-generation">npmjs</a>.

```cli
npm i discord-image-generation
```

# Configuration

The first step is to import the module in your code.

```js
const DIG = require("discord-image-generation");
```

Then you have to request your image and send it as an attachement.

```js
// Import the discord.js library.
const Discord = require("discord.js")
// Create a new discord.js client.
const bot = new Discord.Client()

const DIG = require("discord-image-generation");
> You can also destructure to avoid repeating DIG.

// Listen to the ready event
bot.on("ready", () => {
    console.log("ok");  
})

// Listen to the message event
bot.on("message", async (message) => {
    if (message.content === "*delete") {
        // Get the avatarUrl of the user
        let avatar = message.author.displayAvatarURL({ dynamic: false, format: 'png' });
        // Make the image
        let img = await new DIG.Delete().getImage(avatar)
        // Add the image as an attachement
        let attach = new Discord.MessageAttachment(img, "delete.png");;
        message.channel.send(attach)
    }
})

// Log in to the bot
bot.login("super_secret_token")
````

# Available images


## Filters

- ``new DIG.Blur().getImage(`<Avatar>`, `<Level(Number)>`);``

![Blur](https://cdn.discordapp.com/avatars/769652460011782144/18b416ba0a9460d8d64f5e5a8e02842b.webp?size=1024)

- ``new DIG.Gay().getImage(`<Avatar>`);``

![Gay](https://some-random-api.ml/canvas/gay?avatar=https://cdn.discordapp.com/avatars/769652460011782144/18b416ba0a9460d8d64f5e5a8e02842b.png)

- ``new DIG.Greyscale().getImage(`<Avatar>`);``

![Greyscale](https://media.discordapp.net/attachments/814510581260353596/815969527623319603/hola.png)

- ``new DIG.Invert().getImage(`<Avatar>`);``

![Invert](https://cdn.discordapp.com/attachments/814510581260353596/815969767751024700/hola.png)

- ``new DIG.Sepia().getImage(`<Avatar>`);``

![Sepia](https://cdn.discordapp.com/attachments/814510581260353596/815970030592196678/hola.png)


## Gifs

- ``new DIG.Blink().getImage(`<Avatar>`, `<Avatar2>`.....);``

> You can add as many images as you want 

![Blink](https://imgur.com/JjUXmRU.gif)

- ``new DIG.Triggered().getImage(`<Avatar>`);``

![Triggered](https://cdn.discordapp.com/attachments/814510581260353596/815978006605725716/triggered.gif)


## Montage

- ``new DIG.Ad().getImage(`<Avatar>`);``

![Ad](https://cdn.discordapp.com/attachments/814510581260353596/815978169324142603/hola.png)

- ``new DIG.Affect().getImage(`<Avatar>`);``

![Affect](https://cdn.discordapp.com/attachments/814510581260353596/815978741409775666/hola.png)

- ``new DIG.Batslap().getImage(`<Avatar>`, `<Avatar2>`);``

![Batslap](https://vacefron.nl/api/batmanslap?text1=bruh&text2=Don%27t%20Be%20Gay&batman=https://cdn.discordapp.com/avatars/769652460011782144/18b416ba0a9460d8d64f5e5a8e02842b.png&robin=https://cdn.discordapp.com/avatars/807319206814416987/f79b434ace897b4ea23aee5e1708e881.png)

- ``new DIG.Beautiful().getImage(`<Avatar>`);``

![Beautiful](https://cdn.discordapp.com/attachments/814510581260353596/815979089873207296/hola.png)

- ``new DIG.Bed().getImage(`<Avatar>`, `<Avatar2>`);``

![Bed](https://imgur.com/b1idSnr.png)

- ``new DIG.Bobross().getImage(`<Avatar>`);``

![Bobross](https://cdn.discordapp.com/attachments/814510581260353596/815982432850804736/delete.png)

- ``new DIG.ConfusedStonk().getImage(`<Avatar>`);``

![ConfusedStonk](https://cdn.discordapp.com/attachments/814510581260353596/815982639999352832/delete.png)

- ``new DIG.Delete().getImage(`<Avatar>`);``

![Delete](https://cdn.discordapp.com/attachments/814510581260353596/815983031575511060/delete.png)

- ``new DIG.DiscordBlack().getImage(`<Avatar>`)``

![DiscordBlack](https://cdn.discordapp.com/attachments/814510581260353596/815983178808033290/delete.png)

- ``new DIG.DiscordBlue().getImage(`<Avatar>`)``

![DiscordBlue](https://cdn.discordapp.com/attachments/814510581260353596/815984236044615770/delete.png)

- ``new DIG.DoubleStonk().getImage(`<Avatar`, `<Avatar2>`)``

![DoubleStonk](https://imgur.com/HbuuUC6.png)

- ``new DIG.Facepalm().getImage(`<Avatar>`);``

![Facepalm](https://cdn.discordapp.com/attachments/814510581260353596/815984428277825657/delete.png)

- ``new DIG.Hitler().getImage(`<Avatar>`);``

![Hitler](https://cdn.discordapp.com/attachments/814510581260353596/815984677520932914/delete.png)

- ``new DIG.Jail().getImage(`<Avatar>`);``

![Jail](https://cdn.discordapp.com/attachments/814510581260353596/815984817992761374/delete.png)

- ``new DIG.Karaba().getImage(`<Avatar>`);``

![Karaba](https://cdn.discordapp.com/attachments/814510581260353596/815986386686443520/delete.png)

- ``new DIG.Kiss().getImage(`<Avatar>`, `<Avatar2>`);``

![Kiss](https://imgur.com/sSoCAeH.png)

- ``new DIG.LisaPresentation().getImage(`<Text>`);``

![LisaPresentation](https://cdn.discordapp.com/attachments/814510581260353596/815988457863249920/delete.png)

> Limited to 300char

(Thanks to sιмση ℓεcℓεяε#5765)
- ``new DIG.Mms().getImage(`<Avatar>`);``

![MMS](https://cdn.discordapp.com/attachments/814510581260353596/815989620449345616/delete.png)

- ``new DIG.NotStonk().getImage(`<Avatar>`);``

![NotStonk](https://cdn.discordapp.com/attachments/814510581260353596/816003451057864734/delete.png)

- ``new DIG.Podium().getImage(`<Avatar1>, <Avatar2>, <Avatar2>, <Name1>, <Name2>, <Name3>`);``

![Podium](https://imgur.com/bQoKf0a.png)

- ``new DIG.Poutine().getImage(`<Avatar>`);``

![Poutine](https://cdn.discordapp.com/attachments/814510581260353596/816003255125147648/delete.png)

- ``new DIG.Rip().getImage(`<Avatar>`);``

![RIP](https://cdn.discordapp.com/attachments/814510581260353596/815999485788422156/delete.png)

- ``new DIG.Spank().getImage(`<Avatar>`, `<Avatar2>`);``

![Spank](https://imgur.com/25gq0es.png)

- ``new DIG.Stonk().getImage(`<Avatar>`);``

![Stonk](https://cdn.discordapp.com/attachments/814510581260353596/816002911053152286/delete.png)

- ``new DIG.Tatoo().getImage(`<Avatar>`)``

![Tatoo](https://cdn.discordapp.com/attachments/814510581260353596/816002752215384094/delete.png)

- ``new DIG.Thomas().getImage(`<Avatar>`);``

![Thomas](https://cdn.discordapp.com/attachments/814510581260353596/816002598414974986/delete.png)

- ``new DIG.Trash().getImage(`<Avatar>`);``

![Trash](https://cdn.discordapp.com/attachments/814510581260353596/816002438367805510/delete.png)

- ``new DIG.Wanted().getImage(`<Avatar>`, `<Currency>`);``

> Currency ($, €, ...)

![Wanted]()


## Utils

- ``new DIG.Circle().getImage(`<Avatar>`);``

![Circle](https://cdn.discordapp.com/attachments/814510581260353596/816000975176990720/delete.png)

- ``new DIG.Color().getImage(`<Color>`);``

> An hex color is needed, like "#FF0000"

![Color](https://imgur.com/40tMwfe.png)

# Changelog 

## v1.4.7
- Improved Blink() generation, now supports adding an insane amount of images ^^

## v1.4.5
- Added Karaba()
- Fixed some errors returns that were not the same

## v1.4.0
- Added DiscordBlack() and DiscordBlue()
- Added ESLint and fixed all problems
- Use of the function file in LisaPresentation() instead of an in file function

## v1.3.9
- Edited links in README
- Bumped jimp from 0.14.0 to 0.16.1

## v1.3.8
- Edited the Rip() image
- Fixed the Spank() colors

## v1.3.4
- Added bobross()

## v1.3.2
- Added Stonk()
- Added NotStonk()
- Added DoubleStonk()
- Added ConfusedStonk()

## v1.2.12
- Optimized src/index.js (thanks to https://github.com/Pyrojs)

## v1.2.9
- Added Podium()
- Added Ad()
- Added Poutine()
- Fixed Wanted()
- Bumped jimp from ^0.13.0 to ^0.14.0

## v1.1.5
- Added LisaPresentation

## v1.1.2
- Fixed invalid path
- Moved assets folder 

## v1.0.0
- Changed the full structure
    - Sorted all files in folders
    - Sorted all files in the README
- Fixed new Wanted() text bug
- Added new Blink()
- Added a timeout options for new Triggered()
- Fixed the triggered example not animated
- Added some keywords
- Bumped jimp from ^0.12.1 to ^0.13.0
- Added workflow to auto publish to npm and github packages on push


## v0.1.14
- Updated .thomas() example

## v0.1.13
- Added example for .tatoo()
- Fixed the litle hole at the top of the users pic on .thomas()

## v0.1.12
- Saved all examples to imgur

## v0.1.11
- Added .tatoo()
- Updated JSDoc

## v0.1.9
- Added options for the wanted.
    - The base image has been updated
    - There is now a random price diplayed
    - You can now configure a currency
- Added .thomas()#   I m a g e - F o r - D i s c o r d  
 