## MySQL 5.7.25 version 실행 안됨 오류

mysql -u root -p 

```mysql
mysql -u root -p
password:******* 입력후
```

비밀번호 확실히 맞았는데도 에러날 경우

ERROR 2003 (HY000): Can't connect to MySQL server on 'localhost' (10061)

**-> 'localhost'(10061). 즉, 로컬에서 MySQL서버에 연결(접속)할 수 없음.**



**제어판 - 시스템 및 보안 - 관리도구 - 서비스**로 들어가서

MySQL이 존재 하는지 확인한다.

![MySQL서비스](https://user-images.githubusercontent.com/32161395/79579393-7de07080-8102-11ea-976b-aa93e5270137.png)

<br>

만약 존재할 경우 다시 시작하면된다.

**만약 존재하지 않을 경우**

관리자 권한으로 cmd창을 열고

실행하고자 하는 MySQL의 bin폴더 경로로 가서

ex) cd C:\Users\Teak\mysql-5.7.25-winx64\mysql-5.7.25-winx64\bin

mysqld --install 을 입력하면

Service successfully installed. 가 출력된다.

그 후 mysql을 접속하면 이상없이 잘 된다.