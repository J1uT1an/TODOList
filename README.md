## 基于 TS4.1 + React17 + AntD4 + Koa2 + MongoDB 实现的 TodoList 全栈应用

![image](https://user-images.githubusercontent.com/36991862/114294191-69457700-9acf-11eb-9a27-ebe78825d171.png)

### 应用特点

- 前后端均用 TypeScript 编写
- 接口统一遵循 RESTful 风格
- 实现服务端的优雅错误处理
- 实现了前后端分离

### 技术栈

- 语言
  - TypeScript（赋予 JS 强类型语言的特性）
- 前端
  - React（当下最流行的前端框架）
  - Axios（处理 HTTP 请求）
  - Ant-Design（阿里开源的 UI 语言框架）
  - React-Router（处理页面路由）
  - Redux（数据状态管理）
  - Redux-Saga（处理异步 Action）
- 后端
  - Koa（基于 Node.js 平台的下一代 web 开发框架）
  - Mongoose（内置数据验证， 查询构建，业务逻辑钩子等，开箱即用）

### 本地运行

```bash
# clone
git clone https://github.com/B2D1/TodoList.git
```
### 启动后端项目
```bash
cd /TodoList/server

# 推荐使用yarn依赖
yarn

# 启动后端服务，监听本地 5000 端口，请自行下载 MongoDB，并开启数据库服务
yarn start
```
### 启动前端项目
```bash
cd /TodoList

yarn

# 启动 react 项目
yarn start

# 会报错，因为 Browserslist 中的依赖已经更新了 Browserslist: caniuse-lite is outdated. Please run: npx browserslist@latest --update-db
# 因为Browserslist / caniuse-lite 存在于yarn.lock中，版本已经被控制死了
# 升级Browserslist包即可
npx browserslist@latest --update-db
```

```bash
# 如果还没解决，可执行如下两个命令
rm -rf node_modules   // 删除node_modules包
yarn cache clean  // 清空yarn的缓存

#启动项目
npm run dev
```

### 遇到问题的建议：
#### 遇到问题一定要看清错误提示
不要自己瞎折腾，比如：
- 删除node_module包，反复重新安装；
- 换其他的安装方式 npm ,cnpm等；
- 强制执行npm run dev, 看到一堆未安装的包，然后一次安装
未定位清除问题，瞎猜太浪费时间了