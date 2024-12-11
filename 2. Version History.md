# Version History

### Commit structure
1. Commit - metadata
2. Tree - trackes the names and locations of files and directories in the repo
3. Blob - Binary Large Object - compressed snapshot of a file's contents

### Viewing a repository's history
git log

### Limiting the view of a repo's history
git log -2
git log -2 filename.txt

### Comparing files

| Command                          | Function                                               |
|----------------------------------|-------------------------------------------------------|
| `git diff report.md`             | Show changes between unstaged file and the latest commit |
| `git diff --staged report.md`    | Show changes between staged file and the latest commit |
| `git diff 35f4b4d 186398f`       | Show changes between two commits using commit hashes   |
| `git diff HEAD~1 HEAD~2`         | Show changes between two commits using HEAD syntax 


### Restoring and Reverting files

| Command                                | Function                                              |
|----------------------------------------|------------------------------------------------------|
| `git revert HEAD`                      | Revert all files from a given commit                |
| `git revert HEAD --no-edit`            | Revert without opening a text editor               |
| `git revert HEAD -n`                   | Revert without making a new commit                 |
| `git checkout HEAD~1 -- report.md`     | Revert a single file from the previous commit       |
| `git restore --staged report.md`       | Remove a single file from the staging area          |
| `git restore --staged`                 | Remove all files from the staging area             |
