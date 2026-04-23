# node-pointer-compression-builds

#### Adding a new patch

```bash
$ cd node-src
$ vim some/code/file.cc
$ git commit
$ ../script/git-export-patches -o ../patches
```

> [!NOTE]
> `git-export-patches` ignores any uncommitted files, so you must create a commit if you want your changes to be exported. The subject line of the commit message will be used to derive the patch file name, and the body of the commit message should include the reason for the patch's existence.

Re-exporting patches will sometimes cause shasums in unrelated patches to change. This is generally harmless and can be ignored (but go ahead and add those changes to your PR, it'll stop them from showing up for other people).
