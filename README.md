# test-usrCloud-logData-generator
# XX云日志模拟产生程序 - 日志系统测试专用

## 使用教程

1.创建目录 `/tmp/logs` 如果已经有的话确保这个目录没有在使用当中
  
  chmod -p /tmp/logs
  
2.赋予权限

  sudo chmod 777 /tmp/logs/
  
3.运行程序

  java -jar data_generator.jar
  
  或者
  
  nohup java -jar data_generator.jar &
  
  需要长期运行可以不产生 nohup.out 文件:
  
  nohup java -jar data_generator.jar & >/dev/null 2>&1
 
