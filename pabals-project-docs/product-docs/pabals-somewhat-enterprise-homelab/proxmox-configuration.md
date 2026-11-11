---
description: What do I use on a day-to-day basis?
---

# Proxmox configuration

### What can one use Proxmox for?

Proxmox is a Type-1 Hypervisor, meaning that it runs directly onto the hardware of your computer. So instead of having to deal with a limited amount of resources taken from a main OS like Windows, or Linux Mint and using VirtualBox/VMware/virt-manager, I use Proxmox to create VMs and containers of whatever I desire.

Here are some uses for Proxmox in the homelabbing community:

Media hosting with Plex/Jellyfin.

SIEMs and honeypot for security monitoring with Wazuh and Grafana.

Hosting your own website using Nginx and cloudflared (pabal.dev)

Your own cloud photo storage via Immich.

If you could not tell, most of these uses are purely to avoid using proprietary/big tech applicatons such as Google Drive, Netflix, Spotify, et cetera, but homelabbing itself can be a great pathway for understanding enterprise infrastructure since you get the chance to build one and understand how to navigate/troubleshoot said infrastructure while having some fun/real use for it.

### My specific VMs/containers

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Above is an image VMs/containers, 101 (docker-host) runs Docker containers for MySQL & PHP, both of which are used for my laptop website (head to https://pabal.dev/ for more).&#x20;

103 (opnsense) runs OPNsense to make my Layer-2 TP link SG108E work on a RoaS (Router on a Stick) configuration since my router/mesh routers do not have VLAN capability, and to separate traffic from the rest of the devices in my home network.

"Why isn't the Wazuh VM running?" Because it takes a lot of RAM, and I don't use it often. As of right now (November 10, 2026), I only have one homelab node, I plan to get more in order to get rid of this resource issue, but for now, I think I have a solid setup.
