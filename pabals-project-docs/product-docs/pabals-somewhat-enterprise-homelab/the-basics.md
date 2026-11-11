---
description: Picking out hardware, software I'm using, the literal building blocks.
---

# The basics

### Hardware

I would like to preface that I already have some hardware within my current set up. I have a gaming PC (Ryzen 5 3600,  RTX 2060, 32GB DDR4 RAM) with two monitors (Acer XV240Y, BenQ GW2283).&#x20;

However, I wanted to have a separate PC to actually tinker around, as everyone does when they think of a homelab.

### Enter, the humble used mini PC

What better place would one look for a mini PC in this literally-every-pc-part crisis?

Facebook Marketplace.

<figure><img src="../.gitbook/assets/Screenshot 2026-10-05 213556.png" alt=""><figcaption></figcaption></figure>

I specifically had mini PCs such as the Optiplex or ThinkCentre Minis because they do not draw up a lot of power, obviously they're small, and they can fit amongst other things that would make up the size of my ATX sized behemoth of a gaming PC. This specific PC had an i7-6700T and 16GB of RAM, but no SSD and no WiFi card :(

I already had an SSD, but this is where the buying my switch had to come in.

### Enter, the \*\*MANAGED\*\* switch.

I made the mistake of buying a TP-Link SG105. An unmanaged swtich that only served as an ethernet splitter. I wanted to buy a swtich mainly because I did not have enough ethernet ports for my Deco X15 Mesh Router in my room (which acts as an access point for my ISP router), so I resorted to this.

<figure><img src="../.gitbook/assets/IMG_8686 (1).jpg" alt="" width="563"><figcaption></figcaption></figure>

I learned through an Instagram Reel that managed switches are genuinely superior, especially with the idea of configuring VLANS. So, I purchased it's older brother, the SG108E. Beautiful, aint it?&#x20;



<figure><img src="../.gitbook/assets/IMG_8687 (2).jpg" alt=""><figcaption></figcaption></figure>

### Enter, the OS.

What should I run on this machine? Arch? Mint? Proxmox.

Proxmox is a hypervisor that directly installs into my hardware. The reason I did not want to get a distro is because distros often take around 2-3GB of ram for idle use, which is not ideal if I want to spin up multiple containers/VMs. Proxmox also has capability for VM snapshots, so if anything breaks, I can roll back to a working state.

Oh, and last but not least, I can access everything from my gaming PC, how convenient.

### So.. what's next?

(As of Oct 7, 2026) Getting the physical part was quite easy. But now I have to get my networking right by configuring my managed switch to make sure the traffic is separated from my home.
