### 项目目录结构

- src
  - api 用于存放所有请求接口封装的函数
  - asssets 存放一些静态资源
  - components 存放一些公共组件
  - config 导入项目中的组件, 图标 和 路由表
  - layouts 定义了一些布局组件
  - pages 定义了项目中具体路由组件
  - redux 定义了项目中 redux 管理状态的代码(其他 pages 也有可能有 redux.但是这个 redux 相当于最外层的.store 和根 reducer 都在这里)
  - utils 封装一些工具函数 request.js 是真正发送请求的文件, 里面封装了 axios

### 如何项目添加一个组件,并可以访问到这个组件

1. 定义组件 需要在哪个模块下显示,就定义在哪个模块里面 pages/edu/test
2. 在 config/asyncComps.js 中引入 test 组件,并且集中导出
3. 在权限管理,菜单管理中,根据模块分级,添加 test
4. 在权限管理,角色管理中,给当前用户添加权限,就可以看到了
