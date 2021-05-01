# PAH
Press & Hold extensions for Mac

## Requirements

- macOS Sierra and higher
- active Press & Hold (by default)

## Installation

- Disable System [Integrity Protection](https://developer.apple.com/documentation/security/disabling_and_enabling_system_integrity_protection).
- Continue in [Recovery mode](https://support.apple.com/en-us/HT201314) or start it.
- Open Terminal.
- Unmount system volume with: `sudo mount -uw /`. Note: After reboot it will be mounted back automatically.
- Use cURL to replace the Keyboard plist files.
    - Original file is published here also with `-orig` in case you may need to restore it.
    - Backup the keyboard plist file(s) you want to replace.

cURL command (for `Keyboard-en.plist`):

```sh
cd /System/Library/Input Methods/PressAndHold.app/Contents/PlugIns/PAH_Extension.appex/Contents/Resources/ && curl -sS https://raw.githubusercontent.com/raisty/pah/master/Keyboard-en.plist -o Keyboard-en.plist
```

- Enable System [Integrity Protection](https://developer.apple.com/documentation/security/disabling_and_enabling_system_integrity_protection).

## Uninstall / Restore

You can replace current `keyboard plist` using your backup or "most common" plist located in this repo.

- Disable System [Integrity Protection](https://developer.apple.com/documentation/security/disabling_and_enabling_system_integrity_protection).
- Continue in [Recovery mode](https://support.apple.com/en-us/HT201314) or start it.
- Open Terminal.
- Unmount system volume with: `sudo mount -uw /`. Note: After reboot it will be mounted back automatically.
- Use cURL to replace the Keyboard plist files.

cURL command (for `Keyboard-en.plist`):

```sh
cd /System/Library/Input Methods/PressAndHold.app/Contents/PlugIns/PAH_Extension.appex/Contents/Resources/ && curl -sS https://raw.githubusercontent.com/raisty/pah/master/Keyboard-en-orig.plist -o Keyboard-en.plist
```

- Enable System [Integrity Protection](https://developer.apple.com/documentation/security/disabling_and_enabling_system_integrity_protection).

## Contribution

Feel free to distribute, copy, contribute, comment, change the content. Fork and comments welcome.

If you have idea how to improve another keyboard input feel free to share your setup.

We follow the macOS keyboard setup with the conjuction of [Compose table](https://help.ubuntu.com/community/GtkComposeTable) and most used [emoji symbols](https://emojipedia.org/).

## Disclaimer

Use at your own risk. This tool can modify your keyboard plist file(s). Consider create computer backup first.

## License

[WTFPL](LICENSE)

## Support

Consider supporting my work with [Bitcoin][btc], [Litecoin][ltc], [Ethereum][eth], or here on [Github][gh].

[btc]: https://pay.btc.horse#bitcoin:37iSWX4QdoayZXmuj13AExuhzSkfd7LuG6
[ltc]: https://pay.btc.horse#litecoin:M8bEQNPkZ66hoFGYJuMVntyjj9dmYo1wBf
[eth]: https://pay.btc.horse#ethereum:0x10c993039CC831A1fe8230ddd82A0A13625Dd43E
[gh]: https://github.com/sponsors/raisty
