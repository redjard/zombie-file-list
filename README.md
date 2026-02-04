# zombie-file-list
Lists Linux files that are still opened in a process but were deleted. These "zombie files" use up space and inodes but are hard to find.

I wrote this because my /tmp tmpfs was taking up 32GB of ram despite the files inside summing to only 3MB.

Usage:
```
zombie-file-list <path to filesystem>
```

Note:
- This command is designed to be run on filesystem roots, not paths in general.
- Sizes are apparent sizes, e.g. on ext4 the actual sizes are rounded up to the next 4KiB
