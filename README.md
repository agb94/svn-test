# svn-test
1. 일단, github에서 새로운 repository 생성

2. 해당 repo를 clone 해옴
```console
foo@bar:~$ svn co --depth empty https://github.com/user/repo
Checked out revision 1.
foo@bar:~$ cd svn-test/
``` 
약, private 레포라면 여기서 Auth 에러(Authentication realm: <https://github.com:443> GitHub)가 날 것이다.
그럴 땐 다음과 같이 이메일과 비밀번호를 주면 됨
```console
foo@bar:~$ svn co --depth empty https://github.com/user/repo --username=[깃헙이메일] --password=[깃헙비밀번호]
Checked out revision 1.
foo@bar:~$ cd svn-test/ 
``` 

3. Trunk 브랜치 가져오기
```console
foo@bar:~$ cd svn-test/
foo@bar:~$ ls
foo@bar:~$ svn up trunk
Updating 'trunk':
A    trunk
A    trunk/README.md
Updated to revision 1.
```

[여기](https://help.github.com/en/github/importing-your-projects-to-github/support-for-subversion-clients)에 보면 

> The Subversion bridge maps trunk to the Git HEAD branch (which is usually master).

라고 되어있다. 
이제 저걸 trunk로 가지고 작업을 하면 된다.

4. 커밋 예시

```console
foo@bar:~$ vim trunk/README.md
foo@bar:~$ svn commit -m 'Add hi! to README.md' --username=[email] --password=[password]
Sending        trunk/README.md
Transmitting file data .done
Committing transaction...
Committed revision 2.
```
