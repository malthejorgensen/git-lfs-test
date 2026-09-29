git-lfs-test
============
Repository to test Git LFS.

How this repo was created
-------------------------

    # Create 50 MB file
    dd if=/dev/zero of=large-file.bin bs=1m count=50 && ls -lh large-file.bin && stat -f '%z bytes' large-file.bin

    git lfs install  # Install Git LFS into this repository (use `git lfs install --skip-repo` if you have custom git hooks)
    git lfs track "large-file.bin"  # Add `large-file.bin` as a Git LFS file
    git add .gitattributes large-file.bin  # Stage in preparation for commit
    git commit -m "Add large file using Git LFS"


**NOTE:** If you have custom git hooks, you want to manually add the Git LFS hook scripts
to your own hook file, and then run `git lfs install --skip-repo` instead of
`git lfs install`.
