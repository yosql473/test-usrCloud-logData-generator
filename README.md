# test-usrCloud-logData-generator  XX云日志模拟器

## 日志产生位置
  默认在 `/tmp/logs` 下，需要该目录存在与权限通常。

## 日志格式
 
  轮询:  
    
    INFO  cn.simulator.data.UpDownDataSimulator -下行数据流 - 类型:服务器轮询下发，目标设备:00016907000000000063，data:xxxxxxxxxxx
    
    INFO  cn.simulator.data.UpDownDataSimulator -上行数据流 - 类型:设备轮询上报，目标设备:00016907000000000063，data:xxxxxxxxxxx
  
  手动查询数据点:
    
    INFO  cn.simulator.data.UpDownDataSimulator -下行数据流 - 类型:服务器手动查询，目标设备:00016907000000000069，data:xxxxxxxxxxx
    
    INFO  cn.simulator.data.UpDownDataSimulator -上行数据流 - 类型:设备单独上报，目标设备:00016907000000000069，data:xxxxxxxxxxx
  
  设备主动上报:
    
    INFO  cn.simulator.data.UpDownDataSimulator -上行数据流 - 类型:设备主动上报，目标设备:00016907000000000066，data:xxxxxxxxxxx

## 快速开始

1.创建目录 `/tmp/logs` 如果已经有的话确保这个目录没有在使用当中
  
  chmod -p /tmp/logs
  
2.赋予权限

  sudo chmod 777 -R /tmp/logs/
  
3.运行程序

  java -jar data_generator.jar
  
  或者
  
  nohup java -jar data_generator.jar &
  
  需要长期运行可以不产生 nohup.out 文件:
  
  nohup java -jar data_generator.jar & >/dev/null 2>&1
 
