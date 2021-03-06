# Install

Kato works with [Sick Beard](http://sickbeard.com/install.html) ([binaries](http://sickbeard.hostingsociety.com/) also available) for tv shows and [CouchPotato](http://couchpotatoapp.com/) for movies. Both of these apps use [Sabnzbd](http://sabnzbd.org/) for downloading from usenet.

Requirements: Node, HandbrakeCLI & AtomicParsley

* Install Xcode
* Install Homebrew: `/usr/bin/ruby -e "$(curl -fsSL https://raw.github.com/gist/323731)"`
* Install node: `brew install node`
* Install [npm](http://npmjs.org/): `curl http://npmjs.org/install.sh | sh`
* Install AtomicParsley: `brew install atomicparsley`
* Install [HandbrakeCLI](http://handbrake.fr/downloads2.php)

# Todo

* cleanup updates
  * enable option for auto-cleanup after transcode and atomify
  * add lsof check to make sure not cleaning files currently being processed
* parse .nfo files using xml2js and remove sqlite queries
* Handle multi episode files (eg. "Green Lantern The Animated Series S01E01-02 Beware My Power.avi")
  * Include description for both episodes in the file
  * Update video "name" to include multi ep indicator (eg. "S01E01-02 Beware My Power"))
* Remove hardcoded list of shows with colons and generate dynamically?
  * maybe fetch all shows from Sick Beard and iterate through to create list of shows with colons?
* Vows tests
