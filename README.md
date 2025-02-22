## Minimalistic rEFInd theme

[rEFInd](http://www.rodsbooks.com/refind/) is an easy to use boot manager for UEFI
based systems. This is a brand new theme created by using the rEFInd-minimal theme as a base.

![preview](https://github.com/user-attachments/assets/fc6bc3b0-418e-4172-acd8-0895ab49026c)

### Usage

1. Locate your refind EFI directory. This is commonly `/boot/efi/EFI/refind`
   though it will depend on where you mount your ESP and where rEFInd is
   installed. `fdisk -l` and `mount` may help.

2. Create a folder called `themes` inside it, if it doesn't already exist

3. Clone this repository into the `themes` directory.

4. To enable the theme add `include themes/rEFInd-afterdark/theme.conf` at the end of
   `refind.conf`.

Here's an example menuentry configuration (from the screenshot)

```nginx
menuentry "Arch Linux" {
    icon /EFI/refind/themes/rEFInd-afterdark/icons/os_arch.png
    loader vmlinuz-linux
    initrd initramfs-linux.img
    options "rw root=UUID=dfb2919d-ff78-48db-a8a7-23f7542c343a loglevel=3"
}

menuentry "Windows" {
    icon /EFI/refind/thrEFrEFInd-afterdarkal/icons/os_win.png
    loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
    icon /EFI/refirEFIndrEFInd-afterdarkimal/icons/os_mac.png
    loader /EFI/Apple/Boot/bootmgfw.efi
}
```

Entries that are autodetected should also show the proper icons.

### Background sizes

If you find the background looks blurry it may be due to the included wallpaper
being an incorrect resolution for your monitor. You can download the [SVG version](https://drive.google.com/file/d/1a_E6PZNcs0do9KOtvJWEADW00dnHQ-tS/view?usp=sharing) of the background, resize it as appropriate, and replace the
`background.png`.

You can of course also choose your own background!

### Attribution

The OS icons are from [Lightness for burg][icons] by [SWOriginal][icon-author].  

The new OS icons are reworked from the [Wikimedia Commons](https://commons.wikimedia.org/wiki/Main_Page) of the respective OSes.

 

The new function icons are from the [Lucide Icons](lucide.dev) icon pack.

[icons]: http://sworiginal.deviantart.com/art/Lightness-for-burg-181461810

[icon-author]: http://sworiginal.deviantart.com/
