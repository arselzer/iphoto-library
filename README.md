# iPhoto Library Migration Information

## Status: not yet ready to use

## Why

iPhoto does not scale well if your collection of images gets too large and/or complex.
In my case, there are about 140 GB of images in iPhoto. While less than one third of them were RAW images,
more than 75% of the space taken up is due to RAW images. iPhoto does not offer convenient ways of dealing with these
problems. To extract all RAW photos, process them, reinsert/export them, it is needed to understand the internal
structure of the iPhoto Library.

iPhoto will also soon be discontinued by Apple and replaced. While the switch to the new application will probably be smooth, it
is safer to take the organization of the photos into your own hand, especially with the RAW copies imported as well.

## Location

The iPhoto library is located at `$HOME/Pictures/iPhoto\ Library` (Backslash added for convenience when copying).
This will resolve to something like `/Users/alex/iPhoto Library`.

Let's assume:
```bash
$ IPHOTO_LIBRARY=$HOME/Pictures/iPhoto\ Library
```

## Subdirectories

### Masters
Contains the photos as imported into iPhoto.
It containes the data needed for extraction of images.

`$IPHOTO_LIBRARY/Masters`

The subtree of images follows this structure:

`[year]/[month]/[day]/[year][month][day]-[some-number?]`

### Previews
Contains (only?) the JPEGs created from the RAW files.

`$IPHOTO_LIBRARY/Previews`

### Thumbnails
... Thumbnails of the images, which iPhoto displays while scrolling.

`$IPHOTO_LIBRARY/Thumbnails`

Here are the contents of my `iPhoto Library`:

![](https://github.com/AlexanderSelzer/iphoto-library/blob/master/iPhoto.jpg)
