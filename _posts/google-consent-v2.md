---
title: "Google Consent V2"
excerpt: "Starting March 2024 (allegedly), Google is to require Consent Mode for everyone who has a website or app that will be collecting data for audience building or remarketing with Google Advertising services."
coverImage: "/assets/blog/google-consent-v2/lego-handshake.jpg"
date: "2020-03-16T05:35:07.322Z"
author:
  name: Alan Esquivel
  picture: "/assets/blog/authors/alanesquivel.jpg"
ogImage:
  url: "/assets/blog/google-consent-v2/lego-handshake.jpg"
---

## What is Consent Mode Anyways?

In a nutshell, Consent Mode is primarily about collecting additional data points from users who did not grant consent to their personal data and browser storage accessed for data collection. This way of collecting data is based on not having access to personal data, so it won't show up in Google Services, but instead a random set of identifiers would be used instead.

This won't show up directly in Google though, it will go through a [modeling process](https://support.google.com/analytics/answer/11161109?hl=en), so when users don't grant consent, events are not associated with a persistent user identifier. If Analytics collects 10 page view events, it can’t observe and report whether that’s 10 users or 1 user. Instead, Analytics applies machine learning to estimate the behavior of those users based on the behavior of similar users who do accept analytics cookies or equivalent app identifiers. 

## The two modes in Consent Mode

### Basic Consent Mode

This means that Consent Mode is active on the page or app, but all of Google's tags are prevented from firing and collecting any data until consent is granted. Which means if the user never grants permission, Google wouldn't recieve any data from this user. This is what you see more of today and most tutorials online show you how to set it up this way.

## Advanced Consent Mode 

This is what Google wants you to do instead, since it means collecting data from consenting users and non-consenting users alike, using data from non-consenting users anonymously. 

## How to Implement

This answer is pretty dependent on your setup and what CMP your are using (if you are using one). But a good starting point is going to the people who have put this in place, [Google](https://developers.google.com/tag-platform/security/guides/consent?consentmode=advanced)! They have the most information about the setup and also, have their official partners listed.

Configuring consent management is a lot of work. This is by design, as consent needs to be deliberately integrated and engineered, as there are legal consequences for ignoring the granularity of what user choice actually is.

With these new consent settings in GTM, thankfully it’s no longer the Google Tag Manager admin who has to do the bulk of the work, but the vendors and CMP that have to update their systems to provide the functionality needed to support their clients utilizing Consent Mode.

Photo by [Pawel Czerwinski](https://unsplash.com/@pawel_czerwinski?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) on [Unsplash](https://unsplash.com/photos/3-children-in-white-and-blue-shirts-IuQBc3aM5Sw?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash)
  