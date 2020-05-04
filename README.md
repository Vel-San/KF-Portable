- [KF-PORTABLE](#kf-portable)
  - [What is included](#what-is-included)
    - [Vanilla Changes](#vanilla-changes)
    - [Mutator Changes](#mutator-changes)
  - [Usage](#usage)
    - [Server Success Validation](#server-success-validation)
  - [FAQ](#faq)

# KF-PORTABLE

A pre-configured, Whitelisted *dedicated-server* **/System** directory for Killing Floor 1

This guide assumes that you are already familiar with setting up a dedicated server via '**steamCMD**', if not, then you can simply contact me using the following:

- [Steam](https://steamcommunity.com/id/Vel-San/)
- Discord: **.Vel-San.#7468**
- [Twitter](https://twitter.com/Vel__San)

## What is included

This directory is tailored according to my own taste of mutators, which is **Whitelisted** if run as a *dedicated* server.
I did not change any settings of the actual game, just edited things like:

### Vanilla Changes

- Server Name (Can be changed to what you want)
- VAC Secured
- Edited parameters to allow downloading of Muts as compressed
- Changed the NAT value
- Changed default launch options of the server (Can be Changed to what you want)
- Added my own FTP server to FastDownloads

### Mutator Changes

I currently have 2 lists of mutators in my Steam Collections:

- Not-Whitelisted, Minimal must-have muts that will improve player experience (Affects gameplay in several ways)
  - [Found Here](https://steamcommunity.com/sharedfiles/filedetails/?id=1913521033)
- Whitelisted, Minimal must-have muts that do not affect your gameplay, rather just imrpove Quality of the game
  - [Found Here](https://steamcommunity.com/sharedfiles/filedetails/?id=1490172785)

Below, you can see the currently installed (**And configured**) mods if you are using this repo:

```text
ZedKillCount | Shows a detailed view of ZEDs killed after a wave is done

WeaponPickupMessage | Shows a message on weapon pickup, visible to all players

RgMsgMut | Shows a message when someone rages a Scrake or a Fleshpound

PatriarchScoreboard | Shows detailed view of Daddy Patty stats once you kill him, or he kills you

MedicAlert | Shows a message to the medic **ONLY** if someone needs healing

ESWWeightMut | Customize the inventory weight so you can buy more weapons

DouchebagFixer | Shows a message that someone is not grouped up, and kicks them if they don't gather

CountryTags | Shows country TAG next to names in ScoreBoard

KFARGChat | Shows a small Chat-icon if someone is typing something

KFDamagePopup | Shows damage popups when you hit a ZED

KFShareCash | Shares the cash of disconnected or players who crashed

ReloadOptionsMut | Enables you to interrupt a reload, very useful in emergency
```

All of these mutators are pre-configured for the optimal experience. If you want to manually change the values and configuration of them, you can find the original files here:
<!-- TODO -->
- [MEGA - Default Mutators](https://mega.nz/folder/YDoEmKiC#s6FGAtgh40-TvB4bHsLaMQ)
  - If you want to upload these files to your own FTP host, you have to use **Compresser.bat** to conver them into .uz2 format - you can find the bat also in **/System**

## Usage

Alright. So, assuming you already downloaded the **/System** directory from the repo and you have Killing Floor installed via steamCMD as a dedicated server.

- Navigate to your local KF-Dedicated Server directory
- Copy-Paste or Move the downloaded **/System** into your local **/System**
- Replace all files when prompted

Now we need to update the '*Vanilla*' Settings to what **YOU** want

- Open **Killingfloor.ini** with a file editor (Preferably *VSCode* or *NotePad++*)
- Press Cntrl+F (To Find a keyword)
- Search for 'Change_me' (Without the quotes)
  - Whenever you find a Change_me keyword, replace it when what you want :)!
- Now look for **KF_Server_Launcher.bat**
  - Right click and create a desktop shortcut for it

You are done! Launch Killing Floor from steam, once it loads, go to Open the newly created KF_Server_Launcher shortcut from your desktop. You should be able to view the server once it starts inside the game (Multiplayer > Lan)

You can join your own server, and if you have all ports properly forwarded in your router, anyone can join you!

### Server Success Validation

When you launch the shortcut, you should see something like the following:

![console_log](doc_images/console_log.png)

## FAQ

- What are the ports that need forwarding?

>7707 UDP/IP (Game Port)
>
>7708 UDP/IP (Query Port)
>
>7717 UDP/IP (GameSpy Query Port)
>
>28852 TCP/IP and UDP (Allows your Server to Connect to the Master Server Browser)
>
>8075 TCP/IP (Port set via ListenPort that your WebAdmin will run on)
>
>20560 UDP/IP (Steam Port)

- How do I access WebAdmin UI?
  - In your browser, launch
    ><http://127.0.0.1:8075/ServerAdmin/>

    And enter your credentials

- How do I edit the mutator configuration?
  - Hmm.. I haven't added this part to the documentation yet, but if i see demand i'll add it for sure

- Will you add more mutators?
  - If the mut is Whitelisted, feels like it imrpoves the game quality and doesn't affect the gameplay then yes; Ping me on Steam with your request!

- How can I remove all these mutators and play just vanilla?
  - That is already included in the config. When you launch a game and join it, just press ESC, then Vote for a Map and change the game mode to 'Pure Vanilla'

- How do I install KF in steamCMD as a dedicated server?
  - [Check this out](https://wiki.tripwireinteractive.com/index.php/Dedicated_Server_%28KillingFloor%29)

- Can I run AND play on the server?
  - Yep! Just launch Killing floor from steam first, then launch the Shortcut mentioned in the instructions above
