
### 欢迎 Star ，您的Star是对我的鼓励！

### 前提
配置nginx,多个前端项目部署在同一个域名下

### 实现过程
> #### 1.二级项目在vue.config.js中设置 publicPath: '/new/',
> #### 2.在路由index.js中设置   base:'/new/',
> #### 3.在index.html中加入<meta base=/new/>
> #### 4.nginx.conf中server 
> ####     location / {
> ####            root   D:/Application/nginx-1.12.2/html/dist;
> ####            index  index.html index.htm;
> ####			try_files $uri $uri/ /index.html;
> ####        }
> ####	   location /student/ {
> ####           root   D:/Application/nginx-1.12.2/html/dist/student;
> ####           index  index.html index.htm;
> ####			try_files $uri $uri/ /index.html;
> ####       }

