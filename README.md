# Attenuated Github

Github Oauth is cool. It enables a **github user** to share access to its account to a **third-party service**. This access is [scoped](https://developer.github.com/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/) (although the granularity cannot be negociated between the service and the user) and [revokable](https://help.github.com/en/articles/reviewing-your-authorized-applications-oauth)

However, the [available scopes](https://developer.github.com/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/) can sometimes be too coarse-grained for some purposes. For instance, you may want some Continuous Integration service to push some content to a specific branch (like `gh-pages`) of a specific repo. However, the way things are designed by Github, when the service setups oauth authentication, the minimum it can ask for is write access to all branches of all the user's public repositories.

(This isn't true of github apps)