<a href="https://nodei.co/npm/images-for-discord"><img src="https://nodei.co/npm/images-for-discord.png?downloads=true&downloadRank=true&stars=true"></a>

# images-for-discord

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

You can download it from <a href="https://www.npmjs.com/image-for-discord">npmjs</a>.

```cli
npm i image-for-discord
```

# Configuration

The first step is to import the module in your code.

```js
const Ifd = require("image-for-discord");
```

Then you have to request your image and send it as an attachement.

```js
// Import the discord.js library.
const Discord = require("discord.js")
// Create a new discord.js client.
const bot = new Discord.Client()

const Ifd = require("image-for-discord");
> You can also destructure to avoid repeating Ifd.

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
        let img = await new Ifd.Delete().getImage(avatar)
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

- ``new Ifd.Blur().getImage(`<Avatar>`, `<Level(Number)>`);``

![Blur](https://cdn.discordapp.com/avatars/769652460011782144/18b416ba0a9460d8d64f5e5a8e02842b.webp?size=1024)

- ``new Ifd.Gay().getImage(`<Avatar>`);``

![Gay](https://some-random-api.ml/canvas/gay?avatar=https://cdn.discordapp.com/avatars/769652460011782144/18b416ba0a9460d8d64f5e5a8e02842b.png)

- ``new Ifd.Greyscale().getImage(`<Avatar>`);``

![Greyscale](https://media.discordapp.net/attachments/814510581260353596/815969527623319603/hola.png)

- ``new Ifd.Invert().getImage(`<Avatar>`);``

![Invert](https://cdn.discordapp.com/attachments/814510581260353596/815969767751024700/hola.png)

- ``new Ifd.Sepia().getImage(`<Avatar>`);``

![Sepia](https://cdn.discordapp.com/attachments/814510581260353596/815970030592196678/hola.png)


## Gifs

- ``new Ifd.Blink().getImage(`<Avatar>`, `<Avatar2>`.....);``

> You can add as many images as you want 

![Blink](https://imgur.com/JjUXmRU.gif)

- ``new Ifd.Triggered().getImage(`<Avatar>`);``

![Triggered](https://cdn.discordapp.com/attachments/814510581260353596/815978006605725716/triggered.gif)


## Montage

- ``new Ifd.Ad().getImage(`<Avatar>`);``

![Ad](https://cdn.discordapp.com/attachments/814510581260353596/815978169324142603/hola.png)

- ``new Ifd.Affect().getImage(`<Avatar>`);``

![Affect](https://cdn.discordapp.com/attachments/814510581260353596/815978741409775666/hola.png)

- ``new Ifd.Batslap().getImage(`<Avatar>`, `<Avatar2>`);``

![Batslap](https://vacefron.nl/api/batmanslap?text1=bruh&text2=Don%27t%20Be%20Gay&batman=https://cdn.discordapp.com/avatars/769652460011782144/18b416ba0a9460d8d64f5e5a8e02842b.png&robin=https://cdn.discordapp.com/avatars/807319206814416987/f79b434ace897b4ea23aee5e1708e881.png)

- ``new Ifd.Beautiful().getImage(`<Avatar>`);``

![Beautiful](https://cdn.discordapp.com/attachments/814510581260353596/815979089873207296/hola.png)

- ``new Ifd.Bed().getImage(`<Avatar>`, `<Avatar2>`);``

![Bed](https://imgur.com/b1idSnr.png)

- ``new Ifd.Bobross().getImage(`<Avatar>`);``

![Bobross](https://cdn.discordapp.com/attachments/814510581260353596/815982432850804736/delete.png)

- ``new Ifd.ConfusedStonk().getImage(`<Avatar>`);``

![ConfusedStonk](https://cdn.discordapp.com/attachments/814510581260353596/815982639999352832/delete.png)

- ``new Ifd.Delete().getImage(`<Avatar>`);``

![Delete](https://cdn.discordapp.com/attachments/814510581260353596/815983031575511060/delete.png)

- ``new Ifd.DiscordBlack().getImage(`<Avatar>`)``

![DiscordBlack](https://cdn.discordapp.com/attachments/814510581260353596/815983178808033290/delete.png)

- ``new Ifd.DiscordBlue().getImage(`<Avatar>`)``

![DiscordBlue](https://cdn.discordapp.com/attachments/814510581260353596/815984236044615770/delete.png)

- ``new Ifd.DoubleStonk().getImage(`<Avatar`, `<Avatar2>`)``

![DoubleStonk](https://imgur.com/HbuuUC6.png)

- ``new Ifd.Facepalm().getImage(`<Avatar>`);``

![Facepalm](https://cdn.discordapp.com/attachments/814510581260353596/815984428277825657/delete.png)

- ``new Ifd.Hitler().getImage(`<Avatar>`);``

![Hitler](https://cdn.discordapp.com/attachments/814510581260353596/815984677520932914/delete.png)

- ``new Ifd.Jail().getImage(`<Avatar>`);``

![Jail](https://cdn.discordapp.com/attachments/814510581260353596/815984817992761374/delete.png)

- ``new Ifd.Karaba().getImage(`<Avatar>`);``

![Karaba](https://cdn.discordapp.com/attachments/814510581260353596/815986386686443520/delete.png)

- ``new Ifd.Kiss().getImage(`<Avatar>`, `<Avatar2>`);``

![Kiss](https://imgur.com/sSoCAeH.png)

- ``new Ifd.LisaPresentation().getImage(`<Text>`);``

![LisaPresentation](https://cdn.discordapp.com/attachments/814510581260353596/815988457863249920/delete.png)

> Limited to 300char

(Thanks to sιмση ℓεcℓεяε#5765)
- ``new Ifd.Mms().getImage(`<Avatar>`);``

![MMS](https://cdn.discordapp.com/attachments/814510581260353596/815989620449345616/delete.png)

- ``new Ifd.NotStonk().getImage(`<Avatar>`);``

![NotStonk](https://cdn.discordapp.com/attachments/814510581260353596/816003451057864734/delete.png)

- ``new Ifd.Podium().getImage(`<Avatar1>, <Avatar2>, <Avatar2>, <Name1>, <Name2>, <Name3>`);``

![Podium](https://imgur.com/bQoKf0a.png)

- ``new Ifd.Poutine().getImage(`<Avatar>`);``

![Poutine](https://cdn.discordapp.com/attachments/814510581260353596/816003255125147648/delete.png)

- ``new Ifd.Rip().getImage(`<Avatar>`);``

![RIP](https://cdn.discordapp.com/attachments/814510581260353596/815999485788422156/delete.png)

- ``new Ifd.Spank().getImage(`<Avatar>`, `<Avatar2>`);``

![Spank](https://imgur.com/25gq0es.png)

- ``new Ifd.Stonk().getImage(`<Avatar>`);``

![Stonk](https://cdn.discordapp.com/attachments/814510581260353596/816002911053152286/delete.png)

- ``new Ifd.Tatoo().getImage(`<Avatar>`)``

![Tatoo](https://cdn.discordapp.com/attachments/814510581260353596/816002752215384094/delete.png)

- ``new Ifd.Thomas().getImage(`<Avatar>`);``

![Thomas](https://cdn.discordapp.com/attachments/814510581260353596/816002598414974986/delete.png)

- ``new Ifd.Trash().getImage(`<Avatar>`);``

![Trash](https://cdn.discordapp.com/attachments/814510581260353596/816002438367805510/delete.png)

- ``new Ifd.Wanted().getImage(`<Avatar>`, `<Currency>`);``

> Currency ($, €, ...)

![Wanted]()


## Utils

- ``new Ifd.Circle().getImage(`<Avatar>`);``

![Circle](https://cdn.discordapp.com/attachments/814510581260353596/816000975176990720/delete.png)

- ``new Ifd.Color().getImage(`<Color>`);``

> An hex color is needed, like "#FF0000"

![Color](https://imgur.com/40tMwfe.png)
