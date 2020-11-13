### Install Node envirments:
[reference:](https://github.com/nodesource/distributions/blob/master/README.md)

```
curl -sL https://deb.nodesource.com/setup_15.x | sudo -E bash -
sudo apt-get install -y nodejs
```
#### 安装vuejs，创建工程
```
sudo npm install @vue/cli -g
sudo npm install prettier -g
```

#### vue脚手架创建工程
```
vue create frontend
cd frontend
```
#### vue add 的是plugin
```
vue add router
vue add vuex
vue add vuetify
```
#### 安装开发组件
```
npm install material-design-icons-iconfont -D
npm install @fortawesome/fontawesome-free -D
# 导入后即可使用
import "@fortawesome/fontawesome-free/css/all.css"
import "material-design-icons-iconfont/dist/material-design-icons.css"
```