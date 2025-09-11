+++
date = '2025-09-08T21:52:51+01:00'
draft = false
title = 'Porting my Minecraft world from PlayStation 4 Edition to Java'
+++
Like most people of my age, I used to play a lot of Minecraft during Primary and Secondary school.

Minecraft was very popular in my friend group, but we never got to play all together on the same world as we were split between PS3 owners and Xbox 360 owners for many years.

Though by 2017 we all had moved from PS3/360 to PS4, so we started a new multiplayer Creative mode world and over the next few years, we spent *a lot* of time playing on this world. My PlayStation 4 account reached over 2600 hours played on just Minecraft alone.

![Minecraft1](/images/Minecraft2000hours.png)

![Minecraft1](/images/Minecraft1.png)

In December 2019, Minecraft on console recieved a major update. This update promised to be a huge upgrade for Minecraft's current console editions at the time, bringing a new engine, crossplatform multiplayer, online multiplayer servers and 1:1 version parity across all platforms.

In reality, this was not a simple update, but rather a total migration into a different version of the game entirely, updating from 'Minecraft: PlayStation 4 Edition' by 4J Studios and being replaced with simply 'Minecraft', known as 'Bedrock Edition' on PC and developed by Mojang and Xbox.

> **DISCLAIMER:** When I talk about different Minecraft "versions", I'm referring to different releases of the game, such as PlayStation 3 Edition, Java Edition, etc. I'm not referring to different patch updates for the same release of Minecraft, such as Java 1.8 to Java 1.9.

From here onwards, I'm going to be reffering to Minecraft: PlayStation 4 Edition as 'Legacy Edition' and I will be referring to the new version as 'Bedrock Edition' as I believe these are the official terms for each version.

As this was a different version of the game, old save files were incompatible. The new version provided an in-game tool to convert your worlds from Legacy Edition to Bedrock Edition, but it wasn't perfect.

**Issues with Bedrock's world converter**

One of the biggest issues is that The End is handled completely differently between Legacy and Bedrock. Bedrock's End works much like Java Edition, in which The End works like its own seperate dimension, just like the normal world and the Nether.

In Legacy, The End is not it's own explorable dimension, instead it functions as a simple boss arena for the Ender Dragon with invisible walls that stop players from leaving the island. Coverting worlds from Legacy to Bedrock would cause the chunks around these invisible walls to be replaced with new chunks as the game tries to expand the playable space in The End.

One of the key landmarks in our world was a city that somebody had built on the End Island. Converting would cause any parts of the city near the invisible walls to get deleted and replaced by newly generated chunks.

![MinecraftEndCity](/images/MinecraftEndCity.png)

Any kind of special tile would be reset to their default states, so fences, doors, signs, etc. There were some smaller issues such as signs losing their text, or chests losing their inventories. It was annoying and nobody wanted to go through the hassle of manually replacing every broken special tile on the map.

![MinecraftBrokenFence](/images/MinecraftBrokenFence.png)

Unrelated to any issues with the world converter specifically, we also quickly discovered that Bedrock to felt really bad to play on compared to Legacy Edition. Everything was much slower and clunkier to control with worse menus, more major glitches, and much worse game performance.

With these issues, we decided that we were not going to convert the world to Bedrock and would stay on Legacy instead. Even though Bedrock Edition did replace the Legacy Edition application, there was a button on the title screen to revert back to playing Legeacy Edition if you paid for it before December 2019. 

**Discovering the Legacy4J mod for Java Edition**

In early 2024, the button to access Legacy Edition disappeared from my Minecraft title screen. I believe this happens when PSN cannot verify that you owned Minecraft before the update. 

I tried everything to fix it, but nothing worked. I tried to ask PlayStation support for help, but I was told they couldn't help me as the game was published by Microsoft. I tried to ask Microsoft support for help and they told me they couldn't help me as it was an issue with my PlayStation account. In the end, I didnt get anywhere and gave up.

I did not want to convert my world to Bedrock Edition as (even when ignoring the issues with the world converter) I just genuinely dislike playing on Bedrock Edition. I could've started playing Minecraft on Java Edition, but I didn't want to do that either as I would be without the world I spent 2000+ hours on and I did not feel like starting from scratch.

On a random night in March 2025, during a call with my friends, I was complaining about how much I miss "old" console Minecraft and how I stopped playing the game because of Bedrock Edition. Poyoraz suggested that I try the [Legacy4J](https://modrinth.com/mod/legacy4j/versions) mod for Java Edition.

![MinecraftLegacy4J1](/images/MinecraftLegacy4J1.png)

After testing out the mod, I was stunned. It was a 1:1 perfect recreation down to every tiny detail, every UI menu, even the player's movement physics were adjusted to feel just like Legacy Edition.

I immediately fell back in love with Minecraft again thanks to this mod, Poyraz said I sounded like the happiest person in the world during that call. ^ ^;

During this same call, I then proposed the idea of trying to find a way to recover my old PS4 creative world.

**Converting the world from Legacy Edition to Java Edition**

Converting Minecraft worlds between different versions is something I had looked into before, but never attempted. When discussing the idea in call, Poyoraz suggested that I try using [je2be](https://je2be.app/), an online tool for converting worlds between Minecraft versions.

![MinecraftJe2BeAPP](/images/MinecraftJe2BeAPP.png)

If our world was on PS3, conversion would've been easy, I would've been able to export the save file to USB and then convert the PS3 game data into a Java world using je2be with no extra steps. But unforunately converting from PS4 (Legacy) save files are not supported, I believe its because exported PS4 save files are encrypted.

However, Bedrock IS supported, so it looked like it would be possible to convert the world from Legacy Edition to Bedrock using the in-game conversion tools, and then from Bedrock to Java using je2be.

But exported save files from PS4 are still encrypted, how do you get around this? Well, I found a trick a few years prior that would be helpful.

In 2022, I found a Touhou themed map that was made for PC. I wanted to find a way to bring this world to the PS4 version so that I could play it with my friends and my research led me to find about a trick with Minecraft Realms. Minecraft Realms is a service that lets you to upload your Minecraft world to a online server and access it from any other device that supports Bedrock Edition. 

I could download the Bedrock version of the map, take a free trial of Realms, upload it to a Realm, then download the map on PS4 then cancel the trial. That sounded perfect, but when I tried to create the Realm I was having issues with my Microsoft account and gave up (subtle foreshadowing).

Theoretically, this same method should work in reverse for bringing PS4 worlds to Java. If I could convert our PS4 world to Bedrock, then it be possible to create a Realm on the PS4 and then connect to it on PC. From there I could download the world from the Realm and convert that Bedrock data into Java data with je2be.

![MinecraftPlan](/images/MinecraftPlan.png)

With the plan sorted out, the first thing I had to do was convert the world from PlayStation 4 Edition to Bedrock Edition. This was very simple as Bedrock Edition has a built in conversion tool to bring over your older save files to the new game that I mentioned prior.

Conversion took a while, but that was to be expected as the world was very large. I must compliment Bedrock for having more efficiant world file sizes, our 7GB PS4 world data was compressed down to about 300MB during the conversion.

![Minecraft7GB](/images/Minecraft7GB.png)
![Minecraft7GB](/images/MinecraftAfter.png)

After converting the world to Bedrock, the next step was to upload it to Realms, which is typically a paid service but I just used the free trial (and then forgot to cancel it anyways... rip €4).

This is where everything started to go wrong. Even though I was playing Bedrock on PlayStation 4, you need an Xbox account to use online features such as Realms. 

I don't have an Xbox, but I did have an Xbox account that I used to play the Halo Master Chief Collection a few years before. I tried to log into Minecraft using that Xbox account but I got this error message: 

> This Microsoft account is already associated with PlayStation. You cant use a Microsoft account that is already associated with PlayStation.

To me that reads as "oh okay, I must've linked this Microsoft to a PlayStation before, I'll make a new Microsoft then". I tried using a newly created Microsoft account but got the same error. 

So I made a brand new email with no connections to anything, used that email to make a new Microsoft with no connections to anything, used that Microsoft to make a new Xbox with no connections to anything. This way there should be no association to PlayStation at all as these are all brand new accounts... right? But when I used that Xbox to log in to Minecraft Bedrock PS4, I got the same error. 

After some frustration, it turns out there is a typo in the error message, and its supposed to say: 

> This PlayStation account is already associated with Microsoft. You cant use a PlayStation account that is already associated with Microsoft.

It's a small difference in words, but it completely changes the meaning. I was under the impression that the issue was with the Microsoft account, rather than the PlayStation account. To fix the issue all I had to do was find the Microsoft account that I had originally linked to the PSN account back in 2022, but it was still really frustrating that I wasted so much time creating new accounts and emails just because of a typo in an error message.

Yes it is my fault that I didn't keep good track of which Xbox accounts I had already used, but also I only play on PS4 and don't own an Xbox, I don't think it was crazy to assume that paying attention to an Xbox account was unnecessary for me.

After that headache, I finally had access to the Realms free trial, but uploading the world took forever. The world was only 312MB but the upload was going to take around 2 hours, it seems Realms just has really slow servers.

Because I was going to be waiting a while, I went to download Bedrock on PC in preparation for later steps, but when I tried to download it from the Minecraft Launcher it told me my launcher was outdated. This wasn't a surprise, I rarely use my PC for games so I had likely just downloaded Minecraft years ago and then never opened it again.

![MinecraftLauncher](/images/MinecraftLauncher.png)

When trying to download the new Minecraft Launcher, it took me to the Microsoft Store. I've never used the Microsoft Store before this, but I heard it was terrible. In my experi would not even work no matter what I tried. 

At first, it would not let me choose the install path for the download, the box was just blank so I could not click the install button. 

![MinecraftLauncher2](/images/MinecraftLauncher2.png)

When I fixed that issue, it would just say my internet was not connected whenever I tried to download the Minecraft Launcher. Eventually I couldn't even check the Minecraft Launcher in my library as it just said "Error" even though it could still see that I owned both Java and Bedrock (for Windows).

![MinecraftLauncher3](/images/MinecraftLauncher3.png)
![MinecraftStoreError](/images/MinecraftStoreError.png)

We tried to troubleshoot it for about an hour but it was not working at all.

I got so desperate that I gave my Microsoft account details to Michael, so that he could log into my account on his PC to download the world then send it back to me through an email. And of course when Michael tried it, it worked first try for him.

Michael logged into Bedrock on his PC with my account, downloaded the world from the Realm and then emailed it back to me.

With the world converted to Bedrock, the last step was to convert from Bedrock to Java using je2be, which was a simple one button process but the conversion speed was extremely slow.

I could not stay awake any longer, so I went to bed but left my computer on streaming the conversion process to a Discord call so that Michael could supervise the world conversion and wake me up if anything went wrong. 

![Minecraftje2be2](/images/Minecraftje2be2.png)

After a long struggle with Microsoft's account systems and a roughly 3.5 hour long wait for je2be, the conversion process had finished and our world was ready to be opened in Java. The entire process ended up taking around 7 hours, with the large majority of it being spent on messing aroung with Microsoft accounts and wating for je2be to finish converting.

**Final Results**

![MinecraftLegacy4J2](/images/MinecraftLegacy4J2.png)

After converting the world between 3 completely different versions of Minecraft, I was expecting there to be some major issues or corruptions with the world but everything turned out almost entirely fine.

The issues with Bedrock's converter were still present, special tiles became corrupted, mostly doors and signs. Some of these corruptions were quite interesting, such as doors being made up of 2 bottom half tiles, and armor stands that were wearing iron door textures on their heads.

![MinecraftBuggedDoor](/images/MinecraftBuggedDoor.png)

![MinecraftIronDoorHead](/images/MinecraftIronDoorHead.png)

One of the funniest issues was that the gamerules were reset to default. TNT Explodes had been disabled for years but once we opened the world in Java it was renabled which caused a cat that had been sitting on a TNT pressure plate for about 6 years to immediately blow up as TNT was finally able to detonate.

![alt text](/images/MinecraftMorgana.png)

Outside of these specific cases, I couldn't find any other issues with the world. Bedrock's converter was causing the same issues it always has been since 2019, but je2be seemingly worked flawlessly, I couldn't find any issues that weren't caused by Bedrock's converter specifically.

**Conclusion**

I repeated this conversion process 2 more times to bring over a few other worlds, the first being my Survival world where I earned all of Minecraft's achivements on PS4, and then another being the same but on the PS3.

These worlds are pretty basic and empty, as I don't care much for Suvival I only used these worlds to unlock all of achivements in the game, but I still wanted to preserve them anyways.

![alt text](/images/MinecraftSurvival1.png)

![alt text](/images/MinecraftSurvival2.png)

The conversion process was a lot quicker this time around as I wasn't wasting time with Microsoft's account systems. je2be also converted the worlds much quicker as they were significantly smaller.

As for the old multiplayer Creative world, I downloaded a cute shader pack to make the game look pretty (even if it causes my computer to only run at 20FPS...) and opened the world for my friends to join in.

It would be impossible for me to showcase everything in our world due to how absurdly large it is, but I'll showcase a few pictures.

![alt text](/images/MinecraftBuilds1.png)

![alt text](/images/MinecraftBuilds6.png)

![alt text](/images/MinecraftNetherBase2.png)

In the end, I'm very happy I was able to figure out a way to preserve my old Creative map. I don't play Minecraft or video games in general as much anymore, but it's still very nice to play on this map and build together with friends from time to time.

I don't have much else to say, it's my first time writing such a post like this so I hope it was easily readable. ^ ^;
Thanks for reading.

**Special thanks**

[Poyoraz](https://www.tumblr.com/poyoraz), for introducing me to the Legacy4J mod. Without my love for that mod, this project never would've happened.

[Michael](https://x.com/Toaster21029), for downloading my worlds onto your PC and emailing them to me when I couldn't download Microsoft's broken launcher on my own PC.