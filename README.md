# Lab8-Starter

Harvir Ghuman

## How are graceful degradation and service workers related?

Graceful degradation and service workers are fundamentally connected because a service worker acts as a performance enhancement that gracefully steps out of the way if a user's environment cannot support it.Service workers are standalone scripts that run in the background completely outside your main web application. This separation allows your app to load quickly while the service worker handles slow background tasks like network interception and local caching.

When a user with a modern browser visits your site, the service worker takes control to save assets and serve data even when there is no internet connection. However, if a user has an older browser that does not support service workers, your code uses feature detection to check for support first. If support is missing, the registration block is simply ignored. The application does not crash or break. Instead, it gracefully degrades to a traditional network setup where every request goes directly to the live internet.