# deleteTempFileInDir
删除一个目录下，最后修改时间早于hour小时前的文件。文件名词要求 47个字符以上， 文件后缀长度大于等于40


**example**:  
    

    deleteTempFileInDir  -dir=/data/tempdir/   -hour=5  >> /tmp/deleteTempFileResult.txt
    
result example:

       save  StorageSize:  34123412 Bytes,   delete file number:   23
       total file is 59, now  is Saturday, 24-Oct-15  11:30:30 CSt, gams is over.




   
#/deleteTempFileInFiles  
删除 在一个目录下且文件名已经保存在本文件中的， 修改时间超过-hour= 小时的。文件名词要求 47个字符以上，且 文件后缀长度大于等于40

如：cat /data/test/readme  |  xargs -i -t  ./deleteTempFileInFiles  -dir=/data/test -filename={}  -hour=2

其中：  cat /data/test/readme    如下，一行一个文件名称
ddddddddddddddddd
ddddddddddddddddddd
dddddddddddddddd
me
me2
 234.123412341234123412341234123412341234123412341234
 234.1234123412341234123412341234123412341234123412342
 234.12341234123412341234123412341234123412341234123423
 234.123412341234123412341234123412341234123412341234
    
