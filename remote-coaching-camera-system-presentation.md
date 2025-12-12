---
marp: true
title: Remote Coaching Camera System
theme: gaia
paginate: true
inlineSVG: true
style: |
    .columns {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 1rem;
    }
---

# Remote Coaching Camera System

---

# Problem

My daughter shoots competitive archery and we recently started with a coach who is resides in Statesboro, GA. She meets with the coach roughly once a week over video chat on her phone and sometimes while shooting we need to move the tripod around so the coach can see her stance.

I wondered what would be the best way to provide various angles to the coach during practice?

---

# Research

Claude and I had a thinking session that consisted of

* What hardware could be used?
* How would the cameras be positioned and mounted?
* How would the streams be shared?

---

# Initial prompt

> I have an archery range in my backyard and want to setup cameras on the archery for training sessions, id like to have a camera on the left, right and back of the archer, i want to be able to send a link to the trainer for them to view the session, i currently only have trees around the shooting box, can you provide a plan for the positioning, cameras and tech setup

---

# Solution (current)

Claude and I went back and forth on on the hardware and software stack, but ultimately landed on:

* Reolink RLC-820a (3x cameras)
* Reolink RLA-PS1 (unmanaged poe switch)
* Joilcan AH75 camera tripods
* 3x 100ft cat6 cable
* Frigate NVR

---

# Why Reolink cameras?

* No cloud requirement, can be local only
* 4K
* RTSP
* Outdoor rated
* POE

---

# Why tripods?

* Mobile
* Better control over placement and positioning
* Perfect for trials

---

# Why Frigate NVR?

* Best looking open source camera streaming/recording tool
* Does what I need in the first phase
* Uses [go2rtc](https://github.com/AlexxIT/go2rtc)

---

#  Gotchas

* Camera's base doesnt mount to a tripod (3d printer for the win!)
* Proxying through Cloudflare means broken streaming

---

# Setup

* See diagram

---

# Future

This setup hasn't been used in production just yet (next month), so I don't want to get ahead of myself. However, if this works out, I have ideas which may take me into writing my own remote coaching platform, who knows.

---

# What have I learned?

* Cloudflare proxy limitations
* Camera streaming
* Web streaming
