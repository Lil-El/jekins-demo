hello

在仓库添加webhook设置，
1.在Jenkins中生成token
2.在webhook填写 url:   http://Jenkins用户名:xxxxxxxxxxxxxxxx@IP地址:8080/generic-webhook-trigger/invoke

构建只选择master分支：
在构建-执行shell：添加脚本（查看可选环境变量），shell脚本填写if语句，判断${git branch}为 origin/Master时，再去操作（删除原build文件夹，npm install等）
