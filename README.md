# sfm-patches

## [dirargs](sfm-dirargs-0.3.1.diff)

The **dirargs** patch adds two optional arguments that allow you to specify the
starting location of the left and right pane respectively.

## [sort-ignoredot](sort-ignoredot/sfm-sort-ignoredot-0.3.1.diff)
Adds an option to ignore the leading dot character in 'dotfiles' when sorting them.

## [symlinks](sfm-symlinks-0.4.diff)

* hide symlinks (resolved full name) from files list
* show full symlink name on bottom status line when actual symlink selected

## [dragon](sfm-dragon.diff)
Add a keybind that create a window with selected files to drap and drop on a gui app.
* Requires [dragon](https://github.com/mwh/dragon)

## [nerdicons](sfm-nerdicons.diff)
Add files and folders icons.
* Requires a [Nerd Font](https://www.nerdfonts.com/font-downloads) patched font

Note: go to that part of <i>sfm.c</i> code to fix main folders icons (downloads, pictures...)
``` c
if(strcmp(ex, "own") == 0)  /* downloads */
    icon = " ";
else if(strcmp(ex, "oc") == 0) /* documents */
    icon = " ";
else if(strcmp(ex, "us") == 0) /* music */
    icon = "ﱘ ";
else if(strcmp(ex, "ic") == 0) /* pictures */
    icon = " ";
else if(strcmp(ex, "id") == 0) /* videos */
    icon = " ";
else if(strcmp(ex, "ext") == 0) /* nextcloud */
    icon = " ";
else if(strcmp(ex, "stea") == 0) /* steam */
    icon = " ";
else
    icon = " "; /* default folder */
    /* Uncomment to get the folders "extensions"
     * then change above (comment again after) */
    //icon = ex; /* debug */
```

