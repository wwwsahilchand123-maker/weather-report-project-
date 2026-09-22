# WeatherNova Privacy Behavior

## Location access
WeatherNova should request browser geolocation only after the user selects My Location. City search remains available for users who do not want to share precise location.

## Data handling
- Treat precise coordinates as sensitive.
- Do not persist coordinates unless a feature explicitly requires it.
- Do not send coordinates to services unrelated to the selected weather or map feature.
- Prefer city-level data when precise coordinates are unnecessary.
- Explain location permission usage in the UI.

## Failure behavior
If geolocation is denied, unavailable, or times out, keep the dashboard usable, show a clear message, offer city search as the fallback, and do not repeatedly request permission without a user action.

## Verification checklist
Test granted, denied, dismissed, and unavailable permission states. Verify that precise coordinates do not appear in visible logs or error messages.