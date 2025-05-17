# kdev-templatetools

For anyone on an Arch variant, by the way, I made an AUR package for both KDevelop app and KDevelop file service menu entries.

> yay -Ss kdev-templatetools

aur/kdev-templatetools 0.1.5-1 (+0 0.00) (Installed)
    KDevelop app and file utilities for building and installing your own templates.

The package is currently undocumented.  That will be corrected in the next few days.  In the mean time, it's pretty obvious.  Create a directory structure, probably by copying the contents of an existing template under one of the following two directories:

KDev App Templates - global - /usr/share/kdevappwizard/templates

KDev File Templates - global - /usr/share/kdevfiletemplates/templates

Unpack something that seems similar to your goal, manipulate it as you wish, then right click on the directory in Dolphin, select Actions -> Install as KDevelop <type> Template.

Don't forget to change the name of the directory and the name in the template file.

KDevelop will happily display two identically named templates and you'll have to guess which is yours.  If that happens: delete yours, correct any naming collisions, right click, and push the corrected template into place.

File templates update dynamically, so no need to restart KDevelop when you change or add file templates.

App templates do not update dynamically, so you'll need to restart KDevelop to pick up any changes.

I doubt I'm using the system as intended but I have a lot of file templates that could probably be snippets.  I prefer to use file templates as it's way faster and easier.  Perhaps I'm abusing this feature but KDevelop doesn't complain.

Happy coding!
