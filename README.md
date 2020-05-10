# Files for rickcogley.keybase.pub

This repo contains a simple one page site for [rickcogley.keybase.pub](https://rickcogley.keybase.pub). Every [keybase.io](https://keybase.io) user gets public and private folders via the "kbfs" system, and, if you deploy an `index.html` or `index.md` file, it will be rendered at your "myuser.keybase.pub" site. 

I'm editing this `index.html` file manually, and need only to sync it and any assets to my local keybase public folder, to get the files to be copied up into the keybase.io web server for display. I hacked the `pre-push` git hook in the local copy of my repo, to do a simple rsync between my local git folder and the kbfs public folder. 

```shell
rsync -rlOtcv --exclude '.git' /path/to/rickcogley.keybase.pub/ "/Volumes/Keybase (rcogley)/public/rickcogley/"
```

The trailing slash in the source directory, and the quotes around the target directory matter. 
