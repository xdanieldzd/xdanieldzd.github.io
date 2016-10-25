---
layout: post
title:  "Apple PowerBook 3400c"
date:   2016-10-25 23:50:00 +0200
categories: tech
---
I had mentioned this particular system in my previous post, with the prospect of writing one specifically about it -- and here we are. This here will be a summary of my recent experience with the [Apple PowerBook 3400c/200](https://en.wikipedia.org/wiki/PowerBook_3400c), a 1997 vintage PowerPC-based Macintosh laptop.

I acquired my particular specimen at a flea market some seven or so years ago, and for rather cheap at that, if I recall -- it might've been for as little as 10€. After I originally got it, I messed around with it a bit, with Mac OS 9, with networking it to my PC at the time, and then promptly lost interest in it again. In part because I didn't have much software for it, and in part because OS 9 just wasn't very enjoyable and ran rather sluggishly on this system. That was then, but let's now fast-forward to December 2015.

I am not sure what exactly came over me, but I felt like doing something with my bundle of Macs, the iMac G3 and this PowerBook in particular. So, I fished the PowerBook out of storage and took stock of what I had:

* Apple PowerBook 3400c
* 200 MHz PowerPC 603ev
* 32 MB RAM (16 MB on-board + 16 MB expansion)
* 20 GB Toshiba HDD
* 20x CD-ROM drive
* 12.1" LCD (800x600, 32k colors)
* Mac OS 9.0.4 (International English)

It also had various issues, very few of which I have fixed so far, including wobbly hinges -- thanks to the system's metal frame actually being cracked -- and a dead PRAM battery. It also has the usual scratches, some dead or stuck pixels and the like, which are kind of unlikely to ever get fixed.

Starting out, I backed up the few files I wanted to keep, before getting ready to format the hard disk. Now, the only real link to the outside world that the system has by itself is the standard RJ45 ethernet connector -- and while this sounds great in theory, Mac OS isn't capable of ex. accessing Windows' shared folders without extra software, nor is the opposite true. So what was my lazy man's solution? Hack together a file upload script in PHP, start Apache and PHP on my PC (as part of [XAMPP](https://www.apachefriends.org/index.html)), and use the Mac's Internet Explorer 5 to "upload" the files to the PC, one by one! This worked alright but wasn't a great solution, as the files lost their Macintosh-specific properties, and it would have been cumbersome to use with more than just a couple of files.

With the files backed up, I started collecting software from various sources -- specifically, various "abandonware" sites and the Internet Archive, but also some CDs I had lying around. Once I had the basics together, I went ahead and booted the system from a German Mac OS 8.5 CD, formatted the hard disk and installed the OS. Another hour or so later, I had the OS updated to version 8.6, and some software to allow the Mac to access Windows shares installed. Then came more software, general tools, some things I wanted to try to, etc. via the network.

And here comes the point where this old machine genuinely impressed me -- that is, for the first time. I got SoundJam MP, a media player which was later purchased by Apple and apparently served as the base for iTunes. I had seen fail0verflow's marcan on Twitter [use this program](https://twitter.com/marcan42/status/661182193767612416) on a [Twentieth Anniversary Macintosh](https://en.wikipedia.org/wiki/Twentieth_Anniversary_Macintosh), which was a 1997 limited edition system roughly comparable to my PowerBook in terms of specs -- but with, for example, a 50 MHz faster CPU --, to stream AnimeNFO Radio over the internet, and I wanted to try that, too.

Imagine that! Streaming 192 kbps MP3 audio, from the internet, over a 10 Mbit ethernet connection, to an almost twenty years old, 200 MHz laptop! Such a dumb idea, right?

But it worked. And _almost_ flawlessly, too. The sound occasionally cuts out for half a second or so, but it doesn't happen very often and is just something I'll ascribe to classic Mac OS' cooperative multitasking, which seems like a plausible explanation to me. I also tried the same with 320 kbps MP3 files stored on my PC, accessed via the local network, and this worked just as well. I am not sure if I'm exaggerating this achievement, but it seemed to me, at least at the time, that any computer below, say, 1 GHz is no longer capable of anything media-related anymore -- let alone something with a mere 200 MHz, decoding compressed audio coming in via ethernet, at these bitrates, and so on.

As for the second time that this system impressed me -- it was when I unplugged the power supply to see how much juice the battery still had left. I started SoundJam MP and the AnimeNFO Radio stream and let it run, periodically glancing over at the screen to check what Mac OS reported regarding the battery's status. Slowly but surely, the battery indicators dropped; the bars showing the charge level, as well as the timer showing the approximate remaining runtime...

_"Slowly"_ being the keyword here. I ended up plugging the power back in when the OS reported roughly one minute of charge left, which happened _73 minutes_ after starting playback. On a stock Apple battery, presumably also from 1997 or maybe a few years younger, if it had ever been replaced. But even if it is from 2000 or so, this machine still lasts a whole lot longer on battery than my current, temporary PC laptop does -- a Dell Latitude C640 from 2003 or thereabouts, which lasts for less than 10 minutes --, and longer than what my former laptop managed before it died -- an Asus X5DAB-SX070V from 2009, which had a completely dead battery by 2014. And again, during the whole 73 minutes, it was doing the streaming radio spiel. This was the point where this ancient laptop impressed me more than it should've had any right to.

Since then, the system has received an Orinoco 16-bit PCMCIA wireless LAN card, which I found for a rather low price on eBay and works quite well overall, although it does not seem to support any encryption standards beyond WEP. For this reason, I'm running an old wireless router set to WEP -- and, crucially, with MAC address filtering enabled, so as to only allow specific devices onto the network -- as a bridge for this and other, similarly old devices, to the main network and internet. Of course, listening to streaming radio also works wirelessly, and while I haven't done any measurements regarding how much additional battery drain the wireless LAN card causes, it doesn't appear to be too dramatic.

In conclusion, this little machine has become my "Macintosh troubleshooter", so to speak, as it was quite helpful in bringing up other Macs again, such as my iMac G3 350 or (temporarily) my Power Macintosh 4400/200. I would fetch drivers and software on my PC, share them with the PowerBook, extract or otherwise prepare them there if necessary, and then access them from the Mac in question to get the files. There's still some fixes I want to attempt eventually, such as replacing the dead PRAM battery, as well as possibly mend the broken chassis somehow, but overall, I'm happy with how this old, scratched flea market find turned out.
