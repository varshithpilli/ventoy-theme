# Custom Theme for Bootable USB using Ventoy
A repo containing my custom theme I made/modified for my ventoyUSB.

## Steps
- Install Ventoy on your USB [Install](https://www.ventoy.net/en/doc_start.html)
- Navigate to your USB Partition named __Ventoy__
- Clone this repo and rename it to __ventoy__
- Paste it in the above mentioned partition along side your .iso files

## Modifications
### Background Image
- Navigate to the __ventoy__ folder you just pasted.
- Find the subfolder named __theme__.
- You can delete the current *background_ventoy.png* and replace it with your own image.

### Select Box
- In the same folder, replace the *select_c.png*.

You could tweak everything on the ventoy page by replacing the .png files. I used [Canva](https://www.canva.com/) to make my custom .png files.

## Theme.txt
* The theme.txt is more similar to the .css file.
* Important things to note is that the modifications in spacing or colours of __+ boot_menu__ block would be dont to the main bootable list menu in ventoy
* In my theme I have disabled the icons, but you can add them with just a bit of research.
* The __+ hbox__ blocks are for the modifications of the controls in the bottom of the ventoy screen. Apart from the spacing and colours, I do not recommend messing with them as it would be difficult to debug them once lost.

## ventoy.json
* This file's main purpose is to give an alias for the images on your USB.
<pre> <code>
```
"menu_alias": [
        {
            "image": "/EndeavourOS_Mercury-2025.02.08.iso",
            "alias": "Endeavour"
        },
        {
            "image": "/kali-linux-2024.1-live-amd64.iso",
            "alias": "Kali"
        },
        {
            "image": "/Win11_24H2_EnglishInternational_x64.iso",
            "alias": "Windows"
        },
        {
            "image": "/ubuntu-24.04-desktop-amd64.iso",
            "alias": "Ubuntu"
        }
    ]
```
</code> </pre>
* you could modify the above mentioned block of code from *ventoy.json* to fit your needs and accessibility.
* Note that in the image key, the file name should be preceeded by '/' and should also include the file extension.