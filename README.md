# Kindle Clock

This is a minimal Kindle clock page that shows a large digital clock and date.

It is intended for GitHub Pages. Put `index.html` at the repository root and publish GitHub Pages from the `main` branch root.

To force a manual UTC offset, edit the top of the script in `index.html`:

```javascript
var USE_MANUAL_OFFSET = true;
var MANUAL_UTC_OFFSET_HOURS = 2;
```

Use `MANUAL_UTC_OFFSET_HOURS = 2` for Denmark summer time, UTC+2.

The page also shows two smaller world clocks. Edit these values in `index.html` to change them:

```javascript
var WORLD_CLOCK_ONE_LABEL = "Beijing";
var WORLD_CLOCK_ONE_UTC_OFFSET_HOURS = 8;
var WORLD_CLOCK_TWO_LABEL = "Central America";
var WORLD_CLOCK_TWO_UTC_OFFSET_HOURS = -6;
```

The page also shows a Chinese lunar date.

Use the `Settings` link on the page to save a note and weather settings in the Kindle browser. The saved text is stored locally in the browser.

Some old Kindle browsers may not keep local browser storage after refresh. In that case, use `Save URL` in Settings and bookmark the updated URL. The note and weather location are stored after the `#` part of the URL.

For automatic weather, enter a location such as `Copenhagen` or `Aarhus, Denmark`. Weather data comes from Open-Meteo and does not require an API key. The page keeps the last weather result cached locally and refreshes it about every 30 minutes.

If automatic weather is unavailable, the manual weather fallback text can still be displayed.

For Lyngby near Copenhagen, entering `Lyngby` is treated as `Kongens Lyngby` to avoid matching other Danish places named Lyngby.

You can also set default text in `index.html`:

```javascript
var CUSTOM_MESSAGE = "Your message here";
var WEATHER_TEXT = "Copenhagen: 12C, cloudy";
var WEATHER_LOCATION = "Copenhagen";
```

Leave either value as an empty string to hide that line.
