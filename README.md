# DB
DB관련학습


외래키 추가 방법
```
ALTER TABLE tb_goodanswer
ADD CONSTRAINT quseq2   <-외래키지정이름이다.
FOREIGN KEY (quseq)
REFERENCES tb_question (seq) ON DELETE CASCADE ON UPDATE CASCADE;;
```

외래키 확인
```
select * from information_schema.table_constraints where table_name = 'tb_goodanswer';   //외래키 확인
select * from information_schema.table_constraints where constraint_schema = 'selfin';
```

외래키 삭제
```
alter table tb_goodanswer drop foreign key quseq2;   // 외래키 이름을 지정해서 삭제
```

외래키 오류 확인(그런데 나온적이 없다) SHOW ENGINE INNODB STATUS


