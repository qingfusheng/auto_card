# 四川大学每日健康报自动提交平台

![image](image.jpg)

## 平台介绍

1. 本平台是适用于SCU微服务川大健康每日报自动打卡的平台
2. 本平台会保存用户密码（本来想用Cookie的但是不太靠谱）
3. 本平台不保存用户其他信息，信息总是来自于前一天的打卡
4. 如果需要修改打卡数据，请手动打卡一次即可更新打卡信息

## 安装方法

1. PHP(版本>7.0)+Nginx/Apache

2. Python(版本>3.6) 环境：

   - json
   - logging
   - smtplib
   - requests

3. 添加计划任务：（9代表每天九点执行一次）

   ```
   0 0 9 * * ? python3 -u server.py >>runlog.log
   ```

   

## 注意事项

1. 使用自动打卡必须要前一天有打卡记录，否则不会成功（正常情况都有）
2. 撤销打卡的时候会输入学号会删掉对应学号的全部打卡信息，无需多次

## 特别鸣谢

Python脚本在@awei的基础上改良而成

#ADD_Attention
- This is a project copyed from [皮卡的代码站](https://code.52pika.cn)

