# Partitioning and Formatting a Disk Drive in Windows

On Windows systems, a common practice is to use one primary partition that contains the operating system, applications, and user data. The drive letter C: is mostly used to identify this partition. Other partitions are created on the hard disk for specialized functions, like storing data of a specific type. It's also common practice to assign partition letter names in order, creating disk partition D:, E:, F:, and so on.

In this lab, you'll see how this is done by partitioning an extra disk attached to the system into two partitions of 1GB and 9GB each.

# Partitioning a disk using control panel

Windows provides tools for disk management through the GUI. Among many other administrative tasks, the Control Panel in Windows also enables users to manage storage devices attached to the system.

Go ahead and open Control Panel by clicking on the Start button and selecting Control Panel.


![alt text](9_MJObGlZX17OqmcOmj7nnxnqdSFWck22bBdCw1v9_s=.png)

While in Control Panel, navigate to System and Security, then Administrative Tools.

![alt text](XhDfPG_HFwzXPWoAKG6zyOyBY693ldDf7Ku4AYjVpBI=.png)

![alt text](R+fLlikA0W9f9B6ibIqzZaAD9mzhl9Y5sWIsDzGJDkg=.png)

In the Administrative Tools window, double click on Computer Management.

![alt text](pOQKuNhRnSDvvf_9vaRLsaxwYOs1XNfwMChXwixo6vI=.png)

![alt text](HGZ0vtNyNKqqvpQhS3sauXgj8HLauyATBKsX7uhoIBE=.png)

From here, you can manage different services in your Windows system, including storage, task manager, etc. Since we're interested in managing disks, on the left panel, under Storage, select Disk Management.

![alt text](+vDgCcPN+6zqZ7uL1Baba38179YCwfnfbXQ34_SYGWg=.png)

You'll notice that your system has access to two disks, one of which contains unallocated space, and is labeled "Offline". You'll create partitions on this disk.

Note: Throughout this lab, please ignore the 100 MB partitions named EFI System Partition. Those are used to load the operating system during system boot up.


To enable partitioning, the disk will first need to be mounted on the system. Right click on the left part of the disk and select Online.

![alt text](Jiju8mGmC0n6NmEM4tWNPLEzSCPpnns04JdP6xogezY=.png)

The disk will be mounted and automatically assigned the letter D:. You'll further divide this disk into two partitions.



![alt text](gBubZ427tR5E0oEi_9ys3+HhYaOCMlY63XoBeHTlLkY=.png)

Since the space is already allocated to the disk D:, you'll need to first shrink it before a new partition can be created. Right click on the disk and select Shrink Volume.

![alt text](dFHp2qtroij8oadJz7UWXBWEXhklUkDaQNoo+0vE7e0=.png)

Control Panel will present you with a dialogue where you'll enter the size to shrink the disk. Enter 20,480MB to partition the disk into two partitions of 30GB and 20GB each. Click Shrink.


![alt text](hPfcw619agvgO4RVEl5EeyUMft0HEeap7I641uwfL1I=.png)

The disk will be shrunk, and the additional 20GB space will be shown as unallocated.

![alt text](zCRqF75p0TXZqX8cizA9AbvyIQcPdNpar4zHsFocvnU=.png)


On this unallocated space, you'll create a new partition of 20GB in size. Right click on it and select New Simple Volume.


![alt text](PfeT9uTNdui4rhUym0BvN6FicZW9_bYy61+BME+kuFA=.png)


Control Panel will present you with a partition creation dialogue. Click Next.



![alt text](CA5okW7z22rgEI65Foo9CQ2vbZXOjBRqbK5DyWSL1mY=.png)


A size specification dialogue will be presented, where you'll enter the size of the partition you want to create. Create a partition that takes up all the remaining space by accepting the default value in this dialogue. Then, click Next.

![alt text](LMCdAfUPMcOIS_blRE3I4_fHW0DPcHnySqE6ZY9k4X8=.png)

In the next section of the wizard, ensure the drive letter is set to E. Click Next.


![alt text](m_uLfxRUmUkRLT5aq4waChn4aHTxj5IUBXg0qYQ3LUg=.png)

In the next section of the wizard, you'll select the file format that the partition should be made up of. You'll also need to provide the label of the partition. You can provide any name you'd like, or use the default name. Leave the default partition selected, and click Next.


![alt text](C9+Yig5UjtJOASSVXdnqnocUSQRqyLy_kzC8VS9SD54=.png)

The last section of the wizard will be presented. Ensure the Drive letter or path is set to "E:", then click Finish.

![alt text](V6z5WRQIM3cJ_3M4sKMgVKUadUBoUyiymnJ5oLXF_9g=.png)

The disk partitioning will be carried out, and the resulting disk configuration will be updated. The second disk now consists of two partitions: D: and E: of 30GB and 20GB, respectively.


![alt text](DT72qtatclj1xOxFshyn03NplQ84pczxp_My36FHxGg=.png)

# Formatting a partition

Next, you'll format a partition to a different file format.

Caution!
Formatting a partition is destructive, and will erase all data on the partition. Not good! Remember to always backup your data before modifying partitions on a live system.

To format the partition E: to a different file format, right click on it, and select Format.

![alt text](QbK11DY5a6QXuoe6tz97H5B7Fliiw0IOKpAoHa+JRA8=.png)

Control Panel will present you with a file system formatting dialogue. In the file format drop down list, select FAT32, then click OK.

![alt text](k3KVsbvwJz5uGh0EH0rV10AwskYu5ZBm2IsaNkI5vVQ=.png)

![alt text](ixJkqE77cI0rFby1PgBRm7esrqw1Ewxib6taedX99Uc=.png)


A confirmation alert with a warning will be presented. To proceed with the formatting, click OK.


![alt text](N1Y8nXN6q2X7IRDEUm7lcdI4KqQ329jUF+5aUjObxZ8=.png)

The partition will be formatted to the selected file system type, and the final disk configuration will be shown.

![alt text](3yUN+8LSpAxuxnynL1ZOIWh4u02Vdi0ijTbzIja1EiI=.png)

That's it! You've successfully partitioned and formatted a disk in a Windows system.

# Conclusion
In this lab, you've gone through the process of creating partitions and formatting them to specific file systems on a Windows system. Great work! The skills you've gained here are a crucial part of your IT Support Specialist toolbox.