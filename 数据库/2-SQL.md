# SQL
## 笔试真题
小猿开展暑期课程，如下哪些sql语句能查询出参加了暑期课（表A）但是没有参加夏令营（表B）的学生呢？
表A：A
| id    |
| ----- |
| 10001 |
| 10003 |
| ... |
表B：
| id    |
| ----- |
| 10002 |
| 10003 |
| ... |

A. select user.* from A left outer join B on A.id=B.id where B.id is null
B.select user.* from A join B on A.id=B.id where B.id is null
C. select user.* from A right outer join B on A.id=B.id where B.id is null
D. select user.* from A inner join B on A.id=B.id where B.id is null