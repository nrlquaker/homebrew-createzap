# homebrew-createzap

A `brew cask` [external command](https://github.com/caskroom/homebrew-cask/blob/22009279693c55d7eb00f0b85b8b2f8b062fcd21/doc/hacking.md#external-commands) that generates [zap stanza](https://github.com/caskroom/homebrew-cask/blob/b9e51323b5593e2b46ef4f45c163e5fe25101079/doc/cask_language_reference/stanzas/zap.md). It scans common places for leftover files, such as:

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

`brew cask createzap flux`

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
