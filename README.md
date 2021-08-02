# rsyncBackupper

A small script that uses rsync to snapshot directories on a remote machine.

Should work on most Linux distros. I have used it with Debian, Ubuntu and Arch.

May work with macOS although I have only tested with older versions and there may be some permissions issues.

## Usage

- Download rsyncBackupScript.sh or clone the repo
- Create a copy and modify the variables with source and destination details
- Test the script works
- Schedule to run regularly with cron, systemd or whatever you use for scheduling

## What it Does
 - Uses rsync to copy the files across from the source into the `snapshot_dir`
 - Old version of modified or deleted files get moved into `temp_dir` 
 - Compresses the `temp_dir` as a backup of the old files
 - Deletes any of these compressed backups that are older than 30 days


## Planned Improvements
 - Make the 30 day limit variable
 - Error messages to stderr

