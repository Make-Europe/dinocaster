# Farcaster Frames Poll app

A Frame lets you turn any cast into an interactive app. 

This example lets you create a poll and have users vote on it. The FrameAction is authenticated against a hub so the votes cannot be spoofed (if `HUB_URL` is provided), and the results are stored in a redis database. 

Here is an updated and complete overview and related documentation:  
[https://docs.farcaster.xyz/learn/what-is-farcaster/frames/](https://docs.farcaster.xyz/learn/what-is-farcaster/frames/)


## Demo

- [https://fc-polls.vercel.app/](https://fc-polls.vercel.app/)


## Setup
- After deploying your repo to Vercel...
- Create a `kv` database `https://vercel.com/<name>/<project>/stores`
- Set the `KV` prefix url's for the new `kv` database
- Navigate to env variables: https://vercel.com/gregan/fc-links-vote/settings/environment-variables
- If you're doing something production facing w/ trusted data, set the `HUB_URL` environment variable to a production hub's public ip address port 2283 ref: https://docs.farcaster.xyz/reference/frames/spec#frame-signature-packet
- Set the `HOST` env variable to your public facing url or domain, ie; `https://<project>.vercel.app/`
