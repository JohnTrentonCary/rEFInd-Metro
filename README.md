## Metro rEFInd theme

[rEFInd](http://www.rodsbooks.com/refind/) is a simplistic boot manager for UEFI
based systems. This is a clean and minimal theme for it.

![screenshot](https://raw.githubusercontent.com/JohnTrentonCary/rEFInd-Metro/master/screenshot.png)

### Usage

 1. Locate your refind EFI directory. This is commonly `/boot/EFI/refind`
    though it will depend on where you mount your ESP and where rEFInd is
    installed. `fdisk -l` and `mount` may help.

 2. Create a folder called `themes` inside it, if it doesn't already exist

 3. Clone this repository into the `themes` directory.

 4. To enable the theme add `include themes/rEFInd-Metro/theme.conf` at the end of
    `refind.conf`.

Here's an example menuentry configuration

```nginx
menuentry "Ubuntu" {
	icon /EFI/refind/themes/rEFInd-Metro/icons/os_ubuntu.png
  TODO: Update here once I figure out what goes here
}

menuentry "Windows" {
	icon /EFI/refind/themes/rEFInd-Metro/icons/os_win.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
	icon /EFI/refind/themes/rEFInd-Metro/icons/os_mac.png
	loader /EFI/Apple/Boot/bootmgfw.efi
}
```

Entries that are autodetected should also show the proper icons.

### Planned Changes

Improve the quality of selection_big.png.

Add more OS icons such as Slackware, Ubuntugnome, Xubuntu, and other. (If anyone would like to improve the icons, please feel free to.)

Center reset.png

(Possibly) add a better font.

### Attribution

The almost all of the OS icons, as well as the background are from [Metro for burg][icons] by [LuxieBlack][icon-author].

Some of the icons are from [rEFInd-minimalist-black][other-icons] by
[Anders Fischer-Nielsen][other-icons-author] or are mofified versions of the default icons.

The rest of icons are from [icons8][https://icons8.com/]: [shutdown][https://icons8.com/icon/15896/Shutdown] and [restart][https://icons8.com/icon/16877/restart].

The layout to his README is based off of [rEFI-minimal][readme-base] by [Evan Purkhiser][readme-author]

[icons]: http://luxieblack.deviantart.com/art/Metro-burg-theme-336505408
[icon-author]: http://luxieblack.deviantart.com/

[padster]: https://github.com/theRealPadster
[other-icons]: https://github.com/andersfischernielsen/rEFInd-minimal-black

[readme-base]: https://github.com/EvanPurkhiser/rEFInd-minimal
[readme-author]: https://github.com/EvanPurkhiser
[other-icons-author]: https://github.com/andersfischernielsen
