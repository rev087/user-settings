# user-settings

__user-settings__ is a simple way to manage user settings for your command-line Node application. Settings are stored as a file in the user's home directory and all methods are synchronous for simplicity.

## Usage

You specify the filename to store and retrieve

```js
// If ~/.myAppSettings doesn't exist, it's created
var settings = require('user-settings').file('.myAppSettings');

// Storing user settings
settings.set('username', 'rev087');

// Retrieving user settings
var username = settings.get('username');

// Unsetting
settings.unset('username');

```

## Home directory location

The home directory used for Unix systems is `process.env.HOME` and `process.env.USERPROFILE` for Windows.