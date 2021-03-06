# More things to know

## Reference into shell scripting
[write-shell-scripts](https://learn.adafruit.com/an-illustrated-guide-to-shell-magic-typing-less-and-doing-more/write-shell-scripts)

[standard-i-o-pipes](https://learn.adafruit.com/basic-shell-magic/standard-i-o-pipes)

## How to create a copy of your PI's image

Say you spend a lot of time and you have everything setup as you would like it. Nothing need to change, but you want to replicate it every where. Here is how to do it.

In Terminal, enter the following command to create a disc image (.dmg) of your SD Card in your home directory.
```bash
sudo dd if=/dev/disk1 of=~/SDCardBackup.dmg
 ```
Wait until the SD card has been completely read; the command does not show any feedback, so wait for the command prompt to reappear in the terminal window once it is complete.

Now if your need an exact copy, you can restore it exactly how it was.
You have two options:

1. You could use the ballena software we describe in the [README.md](./README.md) to write the image to a new card.
2. If you want to practice your terminal chops, you could follow the next steps


Before you can write to the card you have to 'unmount' it so that the operating system does not try to write to it at the same time.  Use the following in the Terminal:
```bash
diskutil unmountDisk /dev/disk1
```
Then use the this to write the image back to the SD card:
```bash
sudo dd if=~/SDCardBackup.dmg of=/dev/disk1
```
Once it has finished writing the image to the SD card, you can remove it from your Mac using:
```bash
sudo diskutil eject /dev/rdisk3
```

[more info on how to do it in other operating systems](https://thepihut.com/blogs/raspberry-pi-tutorials/17789160-backing-up-and-restoring-your-raspberry-pis-sd-card)
[OOP in python]("https://python-textbok.readthedocs.io/en/1.0/Variables_and_Scope.html")

## Cloning from your machine
1 make sure your computer has ssh enabled. you can change this from system preferences > remote login
2 git

```
git clone usr@computer.local:path/to/repo/.git
```
add upstream or pistream if you will, 

so that both can receive and pull
```
git config receive.denyCurrentBranch ignore

```
[ref](https://stackoverflow.com/questions/3221859/cannot-push-into-git-repository)



## Qucik Links
- [sharing internet over usb](https://stevegrunwell.com/blog/raspberry-pi-zero-share-internet/)
- [battery charger](https://electronics.stackexchange.com/questions/298453/understanding-lipo-charging-protection-circuit)
- [chilli](https://www.allrecipes.com/recipe/238386/raspberry-habanero-jam/)
- [3d model of rapberry](https://grabcad.com/library/raspberry-pi-zero-w-board-1)
