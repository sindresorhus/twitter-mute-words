# Twitter Mute Words [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> Inspiration for words to mute on Twitter

Twitter supports [muting tweets](https://twitter.com/settings/muted_keywords) with specific words from your timeline.

Note that Twitter limits it to 100 entries, so pick the ones most important to you.

Contributions welcome, but it should be generally useful and not offensive. The list is lowercase and alphabetically sorted.


## Politics

```
#alternativefact
#alternativefacts
@realdonaldtrump
attorney general
bomb
bombs
brexit
climate change
comey
congress
conspiracy
constitutional
conway
corbyn
court order
david duke
detention
diplomat
diplomatic
election
fbi
federal agencies
federal agency
government
governments
handcuffs
hate
hatred
immigration
inauguration
isis
ivanka
legislation
nazi
nazis
obama
pentagon
political
politician
politicians
politics
president
protest
protesting
protestor
protestors
protests
putin
religion
religious
republican
republicans
sean spicer
senate
senator
senators
sjw
steve bannon
supreme court
tax dollars
taxes
terrorist
terrorists
trump
war
white house
```


## Sports

```
football
soccer
```


## Other

```
fake news
kardashian
snapchat
stock market
```

## Automated Entry via Hacky JavaScript

There doesn't appear to be an official API for adding a list of muted keywords, so the following JavaScript can be ran on the [muted keywords page](https://twitter.com/settings/muted_keywords).

```javascript
// Replace with your list...
var itemList = [
  'foo',
  'bar',
  'baz'
];

var iterator = 0;

var interval = setInterval(function() {
  if (itemList.length === iterator) {
    alert('done!');
    clearInterval(interval);
  } else {
    openDialog();
    setTimeout(function() {
      enterText(itemList[iterator]);
      iterator++;
      setTimeout(function() {
        pressAdd();
      }, 1000);
    }, 2000);
  }
}, 4000); // Extra second is padded on to give the UI
          // a chance to close down the modal.


function openDialog() {
  jQuery('.MutedKeywordsActions-openDialogButton').click()
}

function enterText(text) {
  jQuery('.MutedKeywordsAddItemForm-row > div div').focus();
  jQuery('.MutedKeywordsAddItemForm-row > div div').text(text);
}

function pressAdd() {
  jQuery('.MutedKeywordsAddItemForm-button').click();
}
```

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
