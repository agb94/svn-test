# svn-test
```bash
$ svn co --depth empty https://github.com/agb94/svn-test
Checked out revision 1.
$ cd svn-test/
$ ls
$ svn up trunk
Updating 'trunk':
A    trunk
A    trunk/README.md
Updated to revision 1.
$ vim trunk/README.md
$ svn commit -m 'Add hi! to README.md' --username=[email] --password=[password]
Sending        trunk/README.md
Transmitting file data .done
Committing transaction...
Committed revision 2.
```
