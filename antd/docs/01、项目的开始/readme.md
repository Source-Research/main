## 项目的开始

### 项目的启动
可以参考这里：                 
[https://github.com/ant-design/ant-design#%EF%B8%8F-development](https://github.com/ant-design/ant-design#%EF%B8%8F-development)

```bash
$ git clone git@github.com:ant-design/ant-design.git
$ cd ant-design
$ npm install
$ npm start
```

#### 项目 start 都做了些啥子
```json
{
  "scripts": {
    "start": "antd-tools run clean && cross-env NODE_ENV=development concurrently \"npm run color-less\" \"bisheng start -c ./site/bisheng.config.js\""
  }
}
```

**启动参数说明:**                         

模块 | 作用             
:-|:-                   
[antd-tools](https://github.com/ant-design/antd-tools)  | antd cli 工具封装，包含了打包、编译、发布、lint检测、api检测等
[cross-env](https://github.com/kentcdodds/cross-env) | 这个就没有啥好说的了，夸平台设置环境变量
[concurrently](https://github.com/open-cli-tools/concurrently) | Run commands concurrently. Like `npm run watch-js & npm run watch-less` but better.
[bisheng](https://github.com/benjycui/bisheng) | 让 markdown 文档转为 react 单页应用。没错，antd 的文档就是用的这个工具， 启动配置文件可见 `site/bisheng.config.js`


