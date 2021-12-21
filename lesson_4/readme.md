## Результат выполнения в консоле:
```ksammar@Ksammar-Laptop:~/LM/lesson_4$ kubectl run -t -i --rm --image postgres:10.13 test bash
If you don't see a command prompt, try pressing enter.
root@test:/# psql -h 172.17.0.3 -U testuser testdatabase
Password for user testuser: 
psql (10.13 (Debian 10.13-1.pgdg90+1))
Type "help" for help.

testdatabase=# CREATE TABLE testtable (testcolumn VARCHAR (50) );
CREATE TABLE
testdatabase=# \dt
           List of relations
 Schema |   Name    | Type  |  Owner   
--------+-----------+-------+----------
 public | testtable | table | testuser
(1 row)

testdatabase=# \q
root@test:/# \q
bash: q: command not found
root@test:/# exit
exit
Session ended, resume using 'kubectl attach test -c test -i -t' command when the pod is running
pod "test" deleted
ksammar@Ksammar-Laptop:~/LM/lesson_4$ 
```