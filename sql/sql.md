ELECT COUNT(1) FROM qhimg_images  GROUP BY uniq_key  

获得个数大于1的相应字段
SELECT uniq_key,COUNT(1),hotel_seq  from qhimg_images  GROUP BY uniq_key HAVING COUNT(1)>1
​

导出数据库表结构：
mysqldump -h host -d database -u username -p >rrx.sql
批量执行sql脚本：进入到mysql 然后
source 脚本


执行sql语句：mysql  
带列名
mysql -ujdb -h 192.168.110.110  -puE4dcyBe6Ah11GzZ -e"SELECT et.UUId,et.entryMobile,et.entryIdentity ,ei.entryBirthday from entry et,entry_info ei where et.UUId=ei.entryUuid" JDB>entry.sql
不带列名
mysql -ujdb -h 192.168.110.110  -puE4dcyBe6Ah11GzZ -N -e"SELECT et.UUId,et.entryMobile,et.entryIdentity ,ei.entryBirthday from entry et,entry_info ei where et.UUId=ei.entryUuid" JDB>entry.sql

