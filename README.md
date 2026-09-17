# Olwande Akoth: Professional Profile

A one-page profile site for Olwande Akoth, Social Impact Advocate, PR and Communications Professional, Programs Manager, Eco-Fashion Designer, and Digital Creator based in Nairobi, Kenya. Built as a narrative, with photos and copy woven together to tell her story, from her Social Impact and Corporate CVs plus photos from her community programme work.

## View it live

Primary: https://atindahhillary.github.io/olwande-Akoth/

Mirror: https://olwande-akoth-atindlets.vercel.app/

Both publish from the main branch. GitHub Pages deploys from main, root folder.

## View it locally

No build step or server needed. Open index.html directly, or drag it into any browser.

## Structure

index.html is the site itself, with all CSS and JS inline and no dependencies except a Google Fonts link.

images holds the photos used throughout the story and in the career timeline.

videos holds the self-hosted video clips and their poster frames.

api/chat.js is a Vercel serverless function that powers Olie, the on-site assistant.

## Setting up Olie (the assistant)

Olie calls a real language model through the api/chat.js serverless function, which only runs on Vercel. To turn it on:

1. In the Vercel project (olwande-akoth), go to Settings > Environment Variables.
2. Add a variable named `ANTHROPIC_API_KEY` with your Anthropic API key as the value.
3. Redeploy (or push a commit) so the function picks up the new variable.

Without that key set, or on the GitHub Pages copy of the site (which cannot run server code at all), Olie automatically falls back to a scripted quick-reply guide instead of failing silently. This means the live AI version only ever runs on the Vercel mirror, and any usage there draws on your own Anthropic API key and billing.
