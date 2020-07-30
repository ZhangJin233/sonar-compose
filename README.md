# sonar-compose

创建sonarqube+mysql环境

- sonarqube：8.4

- mysql：5.7.31
注意事项：
- volumes 中docker路径的问题，如果你的docker-》Preferences-》file sharing 中没有opt、tmp 文件目录，可以改成相应本地已有的，详细查看：



使用docker compose创建成功后，在浏览器中输入：localhost:9000

使用admin 登陆，密码：admin

下载项目需要的插件 administration-》Plugins


在ide（如intelliJ) 中下载SonarLint,

Preferences -》tools -》SonarLint
- 选择sonarqube  
- 输入sonarqube 所在的主机地址，如果是本机启动的docker 就是 http://localhost:9000
- authentocation type 中选择 login/password  Token
- 点击create token 跳转到 sonarqube 中创建token 输入Name 点击Generate  copy Token
- Token 填写 sonarqube中创建的 token，连接完成

在 intelliJ-》 Analyze 选择 Analyze All files 
开始进行代码检查✌️