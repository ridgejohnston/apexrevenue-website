# ApexRevenue.works — Website

Referral onboarding landing page for [Apex Revenue](https://apexrevenue.works) — the revenue intelligence browser extension for live streamers.

## Overview

This is the public-facing homepage for `apexrevenue.works`. It serves as a guided onboarding funnel for users referred via the Apex Revenue affiliate program.

## Features

- Auto-detects referral code from URL params (`?ref=`, `?code=`, `?r=`)
- 3-step onboarding: Install Extension → Create Account → Claim Referral
- One-click extension download + 4-slide interactive install guide overlay
- Affiliate referral tracking via AWS API Gateway

## Stack

- Vanilla HTML / CSS / JS — no framework dependencies
- Fonts: Bebas Neue + DM Sans + DM Mono (Google Fonts)
- Assets hosted on AWS S3 (`apex-revenue-downloads`)
- Referral submissions post to AWS API Gateway → Lambda

## Deploy

Drop `index.html` into any static host (Netlify, S3, Amplify, etc.).  
Update `API_ENDPOINT` in the script block with your AWS API Gateway URL.

## Referral URL Format

```
https://apexrevenue.works/?ref=AFFILIATE_USERNAME
https://apexrevenue.works/?ref=AFFILIATE_USERNAME&by=DISPLAY_NAME
```
