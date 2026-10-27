# Homeward

Homeward is a pet adoption website. It connects animal shelters with families looking to adopt.

This repository holds the whole website. It is a plain static site: there are no frameworks, no build step, and nothing to install. The files here are exactly what visitors receive.

## Live site

- Main site for adopters: https://homeward-bev.pages.dev
- Page for shelters: https://homeward-bev.pages.dev/shelters/

## What each file is

| File | What it does |
|---|---|
| `index.html` | The main page for people looking to adopt. Includes the pet browser, the match quiz, and the shelter dashboard preview. |
| `shelters/index.html` | The page for shelters, explaining what Homeward offers them and how to join the pilot. |
| `assets/styles.css` | The look shared by both pages: colors, fonts, and basic spacing. Change a color here and it changes on both pages. |
| `data/pets.json` | The list of pets shown on the main page: names, photos, breeds, ages, traits, and stories. Edit this file to add, remove, or update a pet. |
| `_redirects` | Sends old links to the new addresses. Anyone visiting `/homeward.html` lands on the main page, and anyone visiting `/homeward_shelters.html` lands on the shelters page. |
| `README.md` | This guide. |

Styles that only one page uses live inside that page, in its `<style>` section.

## How changes get published

1. Make changes on a separate branch, not directly on `main`.
2. Open a pull request on GitHub so the changes can be reviewed.
3. Merge the pull request into `main`.
4. Cloudflare Pages notices the merge and publishes the new version automatically, usually within a minute or two. There is nothing else to run or upload.

If something looks wrong after publishing, the previous version can be restored from the Cloudflare Pages dashboard.

## Editing the pet list

Each pet in `data/pets.json` is one block between `{` and `}`. Copy an existing pet, change the details, and give it a new `id` number that no other pet uses. Keep the commas and quotation marks exactly as they appear in the other entries, or the main page will show "We couldn't load the pets right now" instead of the pets.

## Writing rule: no em dashes

Do not use the em dash anywhere on the site, including page text, pet stories, page titles, and this README. The em dash is the long dash, about as wide as the letter M, that writers often use to break up a sentence. Use a period, colon, or comma instead, or the word "including" when introducing a list.

For example, instead of joining two thoughts with a long dash, write "Olive is calm, and ready for a home." or "Olive is calm. She is ready for a home."
