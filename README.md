# brew-createzap

A `brew` [external command](https://github.com/Homebrew/brew/blob/master/docs/External-Commands.md) that generates [zap stanza](https://docs.brew.sh/Cask-Cookbook#stanza-zap).

## Installation

```sh
brew tap nrlquaker/createzap
```

## Usage

```sh
brew createzap flux
```

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
