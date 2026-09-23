# Weather Data Handling

## Request flow
1. Validate the requested location before sending it to a weather provider.
2. Use the provider's documented units and response fields.
3. Handle missing or stale weather fields without breaking the UI.
4. Display the time associated with the forecast or observation.

## Privacy
Location data should be requested only when needed. Avoid logging precise coordinates or retaining location history unless the application explicitly requires it.

## API failures
The UI should distinguish between invalid locations, rate limits, network failures, and unavailable provider data. Do not present cached or partial data as a fresh observation.

## User experience
Show a clear loading state, a useful error message, and a retry path when a weather request fails.
