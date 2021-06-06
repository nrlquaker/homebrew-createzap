# brew-createzap

A `brew` [external command](https://github.com/Homebrew/brew/blob/master/docs/External-Commands.md) that generates [zap stanza](https://docs.brew.sh/Cask-Cookbook#stanza-zap). It scans common places for leftover files, such as:

```sh
~/Library/Application Support
~/Library/Application Support/com.apple.sharedfilelist/com.apple.LSSharedFileList.ApplicationRecentDocuments
~/Library/Caches
~/Library/Containers
~/Library/Preferences
/Library/Application Support
/Library/Preferences
...
```

## Installation

```sh
brew tap nrlquaker/createzap
```

## Usage

`brew createzap flux`

Output:

```ruby
zap trash: [
  "~/Library/Application Support/Flux",
  "~/Library/Caches/org.herf.Flux",
  "~/Library/Containers/com.justgetflux.flux",
  "~/Library/Cookies/org.herf.Flux.binarycookies",
  "~/Library/Preferences/org.herf.Flux.plist",
]
```
