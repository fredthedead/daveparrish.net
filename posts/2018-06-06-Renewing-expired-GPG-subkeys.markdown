---
title: Renewing expired GPG subkeys
date: 2018-06-06 11:08:00
---

After starting the [Plasma desktop](https://www.kde.org/plasma-desktop), I noticed that [KDE Wallet software](https://utils.kde.org/projects/kwalletmanager/) was not decrypting my secrets anymore even after putting in my passphrase correctly. The reason is because my [GPG](https://wiki.archlinux.org/index.php/GnuPG) subkeys had expired! I choose to extend the expiration date of my keys but I could have also [rotated the expired keys](https://wiki.archlinux.org/index.php/GnuPG#Rotating_subkeys).

The reason my keys expired in the first place is because I followed the advice from [another blog](https://sungo.wtf/2016/11/23/gpg-strong-keys-rotation-and-keybase.html) on how to securely manage GPG keys. I had decided to let my main public key expire after a few years and the subkeys to expire after six months. When they expired I needed to first extend the expiration using [help from StackExchange](https://unix.stackexchange.com/a/177310/55139). While fairly straight forward now that I have done it, I related to this quote going through the process. ["Is it any wonder GnuPG has never taken off for the masses..."](https://unix.stackexchange.com/questions/177291/how-to-renew-an-expired-keypair-with-gpg#comment753809_177310)

After extending the expiration date, the next task is to distribute the newly signed public keys so that others can still decrypt and verify your messanges created with GPG.
In my case, I have have my keys posted on my website, on [Keybase](https://keybase.io/daveparrish) and also used by a variety of other services such as [Github](https://help.github.com/articles/signing-commits-with-gpg/) and [Facebook](https://www.facebook.com/notes/protect-the-graph/securing-email-communications-from-facebook/1611941762379302).
Currently I have only updated my keys on Keybase, but I will be updating the other locations next.
For Github, [my future commits should not be marked as "Verified"](https://help.github.com/articles/updating-an-expired-gpg-key/) because my public key is expired, but I wasn't able to verify this behavior myself.
I'm not sure what Facebook will do with an expired key.
