---
title: Week 38 Documentation
---
Week 2 of our project, backlog items have started being resolved.

This week we explored the GCP Metadata Service and how a VM can use a Service Account to authenticate with other GCP services. We also moved from static SSH keys in metadata to OS Login and IAM to improve control and traceability of SSH access.

We also set up Headscale on the jump server as a self-hosted control server for our private Tailscale network. We then installed Tailscale on the jump server so it could connect to the Headscale network as a node.

Each team member then installed Tailscale on their own computer/WSL and connected to the same Headscale server. This created a private overlay network where the team's devices can communicate using private Tailscale IP addresses instead of relying on public IP addresses.

We then set up a second primary instance and adjusted firewall rules to access it with SSH only through the jumpserver using SNAT. We also tried hosting a webserver, turning off SNAT and adjusting firewall rules so we can reach it.

Added Spectres IP address to tailscales route so we could access spectre through the jumpserver.

Configured split dns in headscale. And configured jump host as a DNS proxy, and installed dnsmask.

Finally tailscale policies were established along with some fake employee users.  
  

  
  
Throughout the week we had some problems with authorisation and logging into the jumphost. Two team members had problems with the tailscale on their computer disconnecting from their headscale users. We had to solve this by creating a new headscale/tailscale user and removing the old ones.

After finishing our group work for the week we decided we can work on backlog items to fill the time and harden the infrastructure before next week.

among us

sussy amug us
