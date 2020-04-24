##使MYSQL可以远程访问
1.修改数据库安全模式，解除安全模式
```
SET SQL_SAFE_UPDATES = 0;
```
2.修改MYSQL数据库USER表中ROOT的HOST值
```$xslt
use mysql;
update user set host = "%" where user = "root";
```
3.修改数据库安全模式，恢复安全模式
```
SET SQL_SAFE_UPDATES = 1;
```