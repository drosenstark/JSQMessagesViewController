[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)

### JSQMessagesViewController ###
[Carthage](https://github.com/Carthage/Carthage) support for https://github.com/jessesquires/JSQMessagesViewController.

The dependencies [JSQMessagesViewController](https://github.com/jessesquires/JSQMessagesViewController) and [JSQSystemSoundPlayer](https://github.com/jessesquires/JSQSystemSoundPlayer) are added as git subtree modules. This allows us to easily pull in newer changes to JSQMessagesViewController.

### Usage ###
Add ```github "hemantasapkota/JSQMessagesViewController"``` to your ```cart``` file.
Execute ```carthage update```

For usage in Swift, don't forget to add ```#import <JSQMessages/JSQMessages.h>``` to your bridging header file.

### Update Dependencies ###

You might want to update the dependencies to pull in newer changes. To do so:

```
git subtree pull --prefix JSQMessagesViewController https://github.com/jessesquires/JSQMessagesViewController master --squash

git subtree pull --prefix JSQSystemSoundPlayer https://github.com/jessesquires/JSQSystemSoundPlayer master --squash
```

### Dan Says

When I tried to update the dependencies using `git subtree pull` it overwrote the containing directory. So the brute force solution to this is to delete the and then add them. Then you can pull them. So:

```
rm -rf JSQMessagesViewController
# now commit all, then add
git subtree add --prefix JSQMessagesViewController https://github.com/jessesquires/JSQMessagesViewController master --squash
# Now the pull will work!
git subtree pull --prefix JSQMessagesViewController https://github.com/jessesquires/JSQMessagesViewController master --squash

rm -rf JSQSystemSoundPlayer
# now commit all, then add
git subtree add --prefix JSQSystemSoundPlayer https://github.com/jessesquires/JSQSystemSoundPlayer master --squash
git subtree pull --prefix JSQSystemSoundPlayer https://github.com/jessesquires/JSQSystemSoundPlayer master --squash
```
