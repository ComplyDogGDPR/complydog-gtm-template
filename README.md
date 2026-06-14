# ComplyDog Consent Mode Template for Google Tag Manager

A Google Tag Manager custom template that loads the ComplyDog cookie consent banner and wires up Google Consent Mode v2 inside GTM. It sets consent defaults before any other tag runs and updates consent signals automatically based on the visitor's banner choices.

## Setup

1. Add the **ComplyDog Consent Mode** tag to your container from the Community Template Gallery.
2. Enter your ComplyDog **Campaign ID**, found in your ComplyDog dashboard.
3. Set the tag to fire on the **Consent Initialization - All Pages** trigger. This ensures consent defaults are set before any other tag runs.

## What it does

On load, the template sets all consent signals to `denied` by default (with `security_storage` granted), then updates the following signals based on the user's choices in the ComplyDog banner:

- `ad_storage`
- `ad_user_data`
- `ad_personalization`
- `analytics_storage`
- `functionality_storage`
- `personalization_storage`

This keeps tracking and advertising tags compliant until the visitor grants consent, and propagates their preferences to Google Consent Mode v2 in real time.

## Requirements

A ComplyDog account and an active campaign.
