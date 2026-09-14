# yotsuki-taylor.github.io

The root of this host, and it exists for one file.

`.well-known/assetlinks.json` is a Digital Asset Links statement. Android
fetches it when Broker Stars is installed and, if it names that app's package
and the certificate it was signed with, stops asking which app should open an
invitation link: `https://yotsuki-taylor.github.io/BrokerStars/?d=<code>` goes
straight into the game rather than into a browser.

It has to live **here**, at the root of the host, because that is the only
place Android looks. The game itself is a different repository
([BrokerStars](https://github.com/yotsuki-taylor/BrokerStars)) served from
`/BrokerStars/`, and a project page cannot put a file at the root.

`.nojekyll` is what stops GitHub Pages from discarding a folder whose name
begins with a dot.

The fingerprints are three: Google Play's signing certificate, which is what
anybody installing from the store gets; the upload key, for an APK handed round
directly; and the debug key, so a local build behaves like the real one. The
source of truth is `android/assetlinks.json` in the game's repository — change
it there and copy it here.
