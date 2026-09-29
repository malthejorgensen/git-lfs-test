git-lfs-test
============
Repository to test Git LFS.

How this repo was created
-------------------------

    # Create 50 MB file
    dd if=/dev/zero of=large-file.bin bs=1m count=50 && ls -lh large-file.bin && stat -f '%z bytes' large-file.bin

