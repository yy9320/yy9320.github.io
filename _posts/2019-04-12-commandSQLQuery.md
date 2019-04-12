# command라인에서 sql 파일 실행

## 먼저 mysql 에 커멘드로 접속한다.

```bash
$ mysql –u username –p schema

$ mysql > source /bin/test.sql
```
위와 같이 mysql > source 하고 sql파일을 실행하게 되면 sql파일을 실행해서 쿼리가 돌아간다.
여러개의 쿼리를 한번에 실행하고 싶을때 유용하게 쓰일것으로 예상된다.

```bash
$ mysql > source test.sql  

$ mysql > \. /bin/test.sql

```
> mysql > source test.sql 이건 같은 위치에 있을때 이렇게 실행할 수 있다.
> mysql > \. /bin/test.sql 이렇게 하면 바로 실행된다.

**다음과같이 하면 바로 실행**

```bash 
$ mysql -u username -p schema < /bin/test.sql 하게 되면 바로 실행 


