# Eatery Picker

A Toronto food-and-drinks picker that saves its lists and recent picks in this browser using `localStorage`. There is no sign-in, Supabase project, or online database setup. All four categories start empty.

## Use the app

Open `index.html` in a modern browser and add places to each category. Your lists and up to ten most recent picks per category persist in that browser on that device, including after closing and reopening the page.

**Local storage limitations:** Data does not sync to another device or another browser. Clearing this site's browser data or switching browsers/devices can remove or hide the saved list. Anyone using the same browser profile can see or change it. The app does not upload the list to a database. Browser extensions or the hosting platform may have their own separate data practices.

If you previously saved places in Supabase, this local version does not import or delete that old online data. It remains in your Supabase project until you remove it there.

## Test checklist

- [ ] Add a place and reload the page; confirm it remains saved in the same browser.
- [ ] Confirm an empty category shows the friendly prompt and cannot select a nonexistent place.
- [ ] Add a name, then try the same name with different capitalization and extra spaces in that category; confirm it is rejected. Confirm the same name is allowed in another category.
- [ ] Edit a place, then delete it and confirm the browser asks first.
- [ ] Add several entries and pick repeatedly. Confirm results come from the selected category, “Avoid the previous pick” skips the prior name when possible, and history uses Toronto-local time.
- [ ] Make more than ten picks in one category; confirm only its ten newest remain. Delete a previously picked place and confirm its historical name remains.
- [ ] Turn on your device's reduced-motion preference and confirm a pick reveals without the cycling animation.
