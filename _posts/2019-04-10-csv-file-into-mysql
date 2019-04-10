리눅스에서 csv 파일 mysql 에 직접 추가하기 

- csv파일을 데이터 베이스에 import 할때, 오래 걸리는 시간적 이슈가 있다.

이에 오늘은 다른 바로 추가 할 수 있는 방법을 찾아보려고 한다.

먼저 데이터 베이스에 접속한다.
$ mysql -u username -p schema 
  db 직접 접근

LOAD DATA LOCAL INFILE '/home/yy/data/countryIP.csv' INTO TABLE tbl_countryip FIELDS ENCLOSED BY '"' TERMINATED BY ',' ESCAPED BY '"' LINES TERMINATED BY '\n';

위와 같은 소스를 올리게 되면 /home/yy/data/countryIP.csv 파일을 직접 가지고와서 tbl_countyip 라는 테이블에 넣는데 “ 이거 사이에 있고 컬럼의 구분은 “,” 컴마로 되어있다는 의미 , lines terminsted 는 \n  =  한 줄 띄우는 lf로 한줄을 구분한다는 의미이다 
위와 같이 넣을 수 있는 파일은 한 컬럼들이 “ 로 시작해서 “ 로 끝나는 것들만 가능한데 만약 이게 되지 않고 그냥 구분되어 있다고 하면 enclosed by를 지우면 된다.

또한, 만약 lf 이지 않고 crlf인 경우에는 노트패드에서 lf 로 변경후 사용해도 되고 
TERMINATED BY '\n\r'을 하게 되면 crlf를 처리 할 수 있다.
