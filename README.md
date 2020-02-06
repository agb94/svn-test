# svn-test
```console
foo@bar:~$ svn co --depth empty https://github.com/agb94/svn-test
Checked out revision 1.
foo@bar:~$ cd svn-test/
foo@bar:~$ ls
foo@bar:~$ svn up trunk
Updating 'trunk':
A    trunk
A    trunk/README.md
Updated to revision 1.
foo@bar:~$ vim trunk/README.md
foo@bar:~$ svn commit -m 'Add hi! to README.md' --username=[email] --password=[password]
Sending        trunk/README.md
Transmitting file data .done
Committing transaction...
Committed revision 2.
```
