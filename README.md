# GPG for GMail #

![logo.png](http://people.ubuntu.com/~l3on/goopg/logo-50perc.png)

**WARN**: This is an alpha version.

### *What you can do:* ###

* Recruit alpha-testers:

 * requirements: must be developers (or something like that)
 * how: send to l3on@ubuntu.com the github account request


### Wath you cannot do: ###

* Share the code for now, it will be realased when ready


### What you should do: ###

* Spread screenshots about GMail is going to get new extension


# Deps #

```bash
sudo apt-get install node-less python-googleapi python-gflags python-xdg python-gnupg
```

# Build the css #
```bash
cd app/lib
make
cd -
```

# Install in Chrome #
* Open [chrome://extensions](chrome://extensions) in the browser
* Click on "Developer mode"
* Then click on "Load unpackage extension" and select the dir `app`

# Update the app ID #
Once extension is installed, get the `NEW_ID` extension in chrome://extension and run:
```bash
NEW_ID=the_id_you_found
OLD_ID=ppopiamobkilibbniemlecehjmbfbjjp
sed s/$OLD_ID/$NEW_ID/ -i app/goopg-web-extension-id.js host/com.leoiannacone.goopg.json
```

# Install the host

If you use chromium:
```bash
cd host
bash install.sh
cd -
```

If you use chrome:
```bash
cd host
bash install.sh google-chrome
cd -
```

Open http://gmail.com
