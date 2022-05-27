# react-testing-starter-main

Following tutorial https://www.youtube.com/watch?v=OVNjsIto9xM

Thanks to team Cypress for this real world demo app ❤️

<a href="https://github.com/cypress-io/cypress-realworld-app">Original repo</a>

# Development

https://www.youtube.com/watch?v=OVNjsIto9xM

This needs folder needs to contain a `.git` folder.

https://linguinecode.com/post/how-to-fix-m1-mac-puppeteer-chromium-arm64-bug

On Mac M1, need to install chromium separately and not with npm / yarn

```sh
brew install chromium
.
==> Installing Cask chromium
==> Moving App 'Chromium.app' to '/Applications/Chromium.app'
==> Linking Binary 'chromium.wrapper.sh' to '/opt/homebrew/bin/chromium'
🍺  chromium was successfully installed!
.
which chromium
.
/opt/homebrew/bin/chromium
```

Homebrew applies “quarantine” attribute to downloaded files, need to clear it.

```sh
xattr -cr $(which chromium)
xattr -cr /Applications/Chromium.app
```

Might need to go to `System Preferences` > `Security & Privacy` > `General` tab, and select `Open Anyway`.

https://www.reddit.com/r/MacOS/comments/q9d772/homebrew_chromium_is_damaged_and_cant_be_openend/

Add to `.bash_profile`

```sh
export PUPPETEER_SKIP_CHROMIUM_DOWNLOAD=true
export PUPPETEER_EXECUTABLE_PATH=`which chromium`
```

```sh
npm install -g yarn
yarn install && yarn dev
```
