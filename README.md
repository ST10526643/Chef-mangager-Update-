# Chef's Menu Manager

An Expo Router and React Native app for managing a restaurant menu. Menu items
are shared between screens in the app's in-memory menu context.

## Features

- Add, edit and delete dishes with name, description, course and price.
- Search by dish name and filter by Starter, Main Course or Dessert.
- View live totals, average price in rand and item counts by course.
- Validate required fields, prices and duplicate dish names before saving.

Menu data is held in memory and resets when the app is restarted; no backend or
database is configured.

## Run on an Android emulator

1. Install dependencies once with `npm install`.
2. Start an Android emulator from Android Studio and wait for it to finish booting.
3. Run `npm run android` from the project folder. Alternatively, run `npm start`
   and press `a` in the Expo terminal to open the app on the emulator.

## Manual feature checks

1. Add a dish for each course using valid names, descriptions and prices.
2. Try saving a blank form, an invalid/zero price and a duplicate dish name;
   verify each attempt displays a helpful message.
3. Search for part of a dish name, choose a course, and confirm both filters
   apply together. Clear the filters and confirm all dishes return.
4. Edit a dish's details and verify the menu and statistics update immediately.
   Try renaming it to another dish's name and confirm the duplicate is rejected.
5. Delete a dish, cancel the first confirmation, then confirm deletion and
   verify the item disappears.
6. Check the item total, average price and all three course counts before and
   after edits/deletions. Delete all dishes to verify the empty-menu state and
   the `R0.00` average are handled.

## Validation commands

- `npx tsc --noEmit` checks the TypeScript project.
- `npm run lint` runs the Expo ESLint configuration.
- `npx expo export --platform android` builds the Android JavaScript bundle.
