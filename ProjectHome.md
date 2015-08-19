> Openduckbill is a simple command line backup tool for Linux, which is capable of monitoring the files/directories marked for backups for any changes and transferring these changes either to a local backup directory or a remote NFS exported partition or to a remote ssh server using the very common, rsync command.

> As a backup tool, openduckbill can operate in any one of the modes mentioned below:

  * Maintain an exact copy of the source at the backup destination
  * Maintain current and previous version of the source at the backup destination

**Features**

  * Supports recursive and non-recursive backup of files/directories
  * Does filesystem monitoring
    * Openduckbill uses pyinotify for filesystem monitoring.
    * Any directory marked for backup, will be monitored for changes, and the changes will be synced to the backup destination regularly.
  * Three different modes of backup. Supports backup to
    * Local directory
    * NFS mount
    * SSH server (using rsync over ssh)
  * Include/exclude files/directories from backup
    * Supports including/excluding files/directories from backup using pattern matches
  * Supports maintaining current and previous versions of files at backup destination.
  * In NFS backup mode, the NFS partition is auto mounted.
  * Ability to remove files/directories which are not part of backup schedule from backup partition. (Currently this feature supported only in LOCAL and NFS backup modes.)
  * Uses YAML based config file
    * Easy to read and modify
  * Uses GUI dialog box to display critical information
  * Has built-in logging system
  * Daemon mode and Non-daemon mode
  * Extensive DEBUG info mode
  * Fully client side application
    * Minimal (or no) configuration required on server

[More details here](http://code.google.com/p/openduckbill/wiki/OpenduckbillReadme)