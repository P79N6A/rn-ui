# rn-ui
A base on React Native UI component library.


## 用法


## 项目结构

UI 库主要拆分为通用 UI 组件模块、业务 UI 组件模块。

这里使用 [Lerna](https://github.com/lerna/lerna) 一个Monorepo管理工具，用来管理不同业务 UI 组件。

这里参考babel设计规范： [Why is Babel a monorepo?](https://github.com/babel/babel/blob/master/doc/design/monorepo.md)

```tree
dist/                           # 构建后文件
build/                          # 构建相关
packages/
  └── xxx                       # 根据功能(语言？)划分不同组件库
      ├── common/               # 通用公共库
      ├── docs/                 # 文档容器(内嵌不同组件的API)
      ├── demo/                 # 直出页面
      ├── test/                 # 测试相关
      ├── components/           # UI组件        
      └── index.js              # 项目入口
```

- `components/` 结构


```tree
components/
    ├── style                   # 全局样式
        ├── theme               # 主题
        ├── mixins              # 混入
        └── style.scss          # 全局组件样式(使用scss语法)
    └── xxx                     # 组件名
        ├── test                # 组件用例
        ├── style.scss          # 组件样式(使用scss语法)
        ├── index.md            # 自动生成        
        └── index.ts            # 组件逻辑
```
