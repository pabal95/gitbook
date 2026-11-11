---
description: Configuring my SG108E to work with incompatible routers.
---

# Figuring out networking

### Network Topology

Everything in my homelab comes from my mesh router that acts as an Access Point (since my router is far from my room)

Here's my physical port layout in a nice table.

<table data-header-hidden><thead><tr><th width="93"></th><th></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Port</strong></td><td><strong>Connected Device</strong></td><td><strong>Switch Mode</strong></td><td><strong>Purpose</strong></td></tr><tr><td>Port 1</td><td>TP-Link Deco Mesh Node</td><td>Access / Untagged (VLAN 1)</td><td>Uplink connection back to the mesh router, local LAN, and internet access.</td></tr><tr><td>Port 2</td><td>Gaming PC</td><td>Access / Untagged (VLAN 1)</td><td>Primary desktop rig on the local LAN with direct gigabit throughput.</td></tr><tr><td>Port 3</td><td>ThinkCentre M910q (Proxmox Host)</td><td>Trunk / 802.1Q Tagged (or PVID 1)</td><td>Dedicated host uplink carrying management traffic and isolated VM/container networks.</td></tr><tr><td>Ports 4–8</td><td>Available Expansion</td><td>Unassigned / Default</td><td>Reserved for hardware expansion, test rigs, or additional nodes.</td></tr></tbody></table>

VLAN 1 (Untagged - Default LAN): Manages standard household traffic and provides the uplink gateway back to my primary ISP router.

VLAN 10 (Tagged - For my Gaming PC): Dedicated exclusively for the Proxmox VE web GUI, SSH host access, and secure switch administration. Access is restricted to trusted local machines.

VLAN 20 (Tagged - homelab stuff): Isolated environment housing the Ubuntu VM and Docker containers, ensuring experimental workloads cannot interact with or compromise the hypervisor host.
