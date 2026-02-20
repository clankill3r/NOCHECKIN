# @NOCHECKIN
A pre-commit hook that prevents from commiting if the text **nocheckin** is present in any of the staged files.

Special thanks to [ElpieKay](https://stackoverflow.com/users/6330106/elpiekay) who did all the hard work. Also thanks to 
[jthill](https://stackoverflow.com/users/1290731/jthill) for a slight improvement.

The original question and source can be found here:
https://stackoverflow.com/a/59133674/1022707


The reason I make a repository out of this is so people can watch it and will be notified if anyone will post an issue. Since so far this has not been heavily tested.


#### Changelog

```
V5:
- @ prefix no longer required, and search is not case insensitive.
V4:
- added "--diff-filter=d" to fix problem with deleted files.
V3:
- All filenames containing @NOCHECKIN are listed now instead of only the first one.

V2:
- Not a single file is commited now when @NOCHECKIN is present (before it would commit the files that did not have an @NOCHECKIN).

V1:
- initial
```

#### Usage

This `pre-commit` file should be placed inside `.git/hooks`.

Make sure the `pre-commit` file has the permisions to be executed!
E.g. `chmod +x pre-commit` on OSX.

#### Notes
For those interested, it also works with [Fork](https://git-fork.com/).
![](fork_source_control.png)

