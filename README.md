# Kindle Clock

This is a minimal Kindle clock page that shows a large digital clock and date.

It is intended for GitHub Pages. Put `index.html` at the repository root and publish GitHub Pages from the `main` branch root.

To force a manual UTC offset, edit the top of the script in `index.html`:

```javascript
var USE_MANUAL_OFFSET = true;
var MANUAL_UTC_OFFSET_HOURS = 2;
```

Use `MANUAL_UTC_OFFSET_HOURS = 2` for Denmark summer time, UTC+2.

The page also shows a Chinese lunar date.

Use the `Settings` link on the page to save a note and a manually entered weather line in the Kindle browser. The saved text is stored locally in the browser.

You can also set default text in `index.html`:

```javascript
var CUSTOM_MESSAGE = "Your message here";
var WEATHER_TEXT = "Copenhagen: 12C, cloudy";
```

Leave either value as an empty string to hide that line.
