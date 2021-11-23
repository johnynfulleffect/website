---
title: "My First PR Merged"
date: 2021-11-23T11:26:23-05:00
draft: false
---

Primarily a close source developer, it was nice to contribute to open source!

<!--more-->

Working as a software engineer and a systems architect, I submit PR's all day, every day, so the ***act*** of opening a PR and getting it merged is no big deal to me.  However, I have only worked on closed source projects up until today.  Feel free to check it out:

[Dell iDRAC Traefik configuration #93](https://github.com/techno-tim/techno-tim.github.io/pull/93)

I have been customizing (read: breaking and fixing) my HomeLab over the second half of 2021 and one of my lingering issues was allowing my Dell R720's Integrated Dell Remote Access Control (iDRAC) to be proxied behind my Traefik reverse proxy/ingress controller/load balancer.  

**Problem:** When loading the main system summary, javascript errors prevented the page from ever loading, as well as preventing the virtual console.

**Solution:** Remove headers that the rest of my services either require or allow them to be secure

- `X-Content-Type-Options: true`
- `Strict-Transport-Security` with the `preload` tag

The rest of the configuration was properly setting up routers and services in Traefik for a custom domain (details in PR)

Even tho this PR modifies a configuration file used in a demo, nothing going to mainstream, I still feel accomplished and happy that I figured out the issue and hopefully help someone else.
