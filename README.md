# Tips for Mac
## 1. How to use external hard drive (NTFS) on Mac?
Terminal Operation:
```Java
// see the mode and mark the disk name as disk2s1
% mount | grep ntfs
/dev/disk2s1 on /Volumes/Untitled (ntfs, local, nodev, nosuid, read-only, noowners)
/dev/disk2s2 on /Volumes/Untitled 1 (ntfs, local, nodev, nosuid, read-only, noowners)
// unmount hard drive
% sudo umount /dev/disk2s1
% sudo umount /dev/disk2s2
// mount hard dirve on specific file
$ mkdir ~/Desktop/md1 ~/Desktop/md2 //create file
$ sudo mount_ntfs -o rw,nobrowse /dev/disk2s1 ~/Desktop/md1
$ sudo mount_ntfs -o rw,nobrowse /dev/disk2s2 ~/Desktop/md2
//over
```
## 2. How to get your file from the mac that won't boot?
- Got an Intel Mac? Use Target Disk Mode.
  - Connect the two computers with a FireWire or **Thunderbolt cable** (not your charge cable).
  - On the Mac you want to use as the disk in target disk mode, do one of the following:
       - If the computer is off, start it up while pressing and holding the T key.
       - If the computer is on, choose Apple menu > System Preferences, click Startup Disk, then click Target Disk Mode.
  - When the computer has started up, a disk icon appears on the desktop of the other computer
  - Transfer files by dragging them to and from the disk.
  - Eject the disk by dragging its icon to the Trash.
  - While you drag, the Trash icon changes to an Eject icon.
  - On the Mac you used as a disk, push the power button to shut it down, then disconnect the cable.
- Got an Apple Silicon Mac? Use Mac Sharing Mode.
