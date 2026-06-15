---
title: "Trustless Notes"
publishDate: 2026-06-15
description: "A Zero Knowledge Notes App made with Nextjs and Supabase."
tags: ["nextjs", "supabase", "cryptography"]
# updatedDate: "2026-06-15"
---

Most online note taking apps perform only server-side encryption, meaning they can decrypt and read the text anytime they want. Like having to comply with law enforcement, scanning for censorship, etc.

## Inspiration

I was always fascinated by [protectedtext.com](https://protectedtext.com), it was a very intersting concept to me, "**Trustless Security**".
They mention their goal is to always fight for privacy, [protectedtext/helpusfight](https://www.protectedtext.com/site/helpusfight). Their code is open source, but I never got around to reading it, the flow was very clear on their site, you go to any url of the form `proctectedtext.com/<ANYTHING>`, and if it's a first time visit they ask you to set a password and on subsequent vists, I believe they just try decrypting the text in browser and since they use AES, it throws an error if wrong key is used for decryption. Also, of course if we forget our password, the content is unrecoverable.

So, I wanted to expand on this idea for a project in my Network Programming and Security Course.

## My Extension

I liked the idea so to kill 2 birds with one stone, I expanded on it for my course, [Trustless Notes](https://github.com/Mystery-Coder/trustless-notes).
(Credits to my friends, [Srinidhi](https://github.com/SRINIDHI3628) and [Suraj](https://github.com/Suraj132004)). I had a simple approach in mind, when the user signs up, use their password for encrypting everything, then as I learnt more by chatting with Claude (I find this a really great way of exploring ideas), I got to know about Password Based Key Derivation Function (PBDKF2), which is made specifically for this process. So the simple flow is while signing up instead of storing the hash of the user's password, generate random bytes called sentinel and use the key derived from their password (PBDKF2) to encrypt it. Then, on login instead of hashing thier input, we can just try decrypting the encrypted sentinel, if it throws an error we know it's the wrong password. I wanted the platform to be a bit more general purpose like a notes app, all the notes in one place but only you can decrypt them and I also wanted image attachments in notes.

## What I learned

I understood Nextjs wayy more in depth, where exactly is it safe to run server side code, how API routes actually work, when to use them, server actions, etc. Nextjs is really great when you don't really need a dedicated backend and are using something like Supabase. I also got to explore Web Browser APIs, they have so much support, this project needed only Web Crypto API which was a standard officially declared since 2017, but the browser APIs have been growing, WebGPU, WebSerial are ones which I found interesting. The database and blob storage experience with Supabase is very good, but it is very abstracted (well, it is a Backend as a Service). Row Level Security in Supabase is something I still need to understand more in depth.
