# Flast
Cross-platform browser based on Chromium.

## How to build
Run these in Bash:
```bash
pushd app
  FEEDBACK_SEND_URL="<Feedback send URL>" GOOGLE_API_KEY="<Google API key>" node ./setConfig.js
popd
npm run package  # Wait about 20min.
```

Or(maybe POSIX compatible):
```sh
cd app
FEEDBACK_SEND_URL="<Feedback send URL>" GOOGLE_API_KEY="<Google API key>" node ./setConfig.js
cd -
npm run package  # Wait about 20min.
```

If something wrong, try `npm run build` instead of `npm run package`

## EACCES: permission denied, stat '~/.config/flast/Users/<UUID>/Themes/Black.json'
Run this: `chmod +x '~/.config/flast/Users/<UUID>/Themes`

## Error: Cannot find module './Config.json'
Run this: `cd app && FEEDBACK_SEND_URL="<Feedback send URL>" GOOGLE_API_KEY="<Google API key>" node ./setConfig.js && cd -`
And rebuild Flast.
