# FairyGUI-cocoscreator

A flexible UI framework for Cocos Creator, working with the FREE professional Game UI Editor: FairyGUI Editor.

Official website: [www.fairygui.com](https://www.fairygui.com)

# 关于版本
* master 适用于CocosCreator 2.4或更新的版本
* ccc2.1-2.3 适用于CocosCreator 2.1-2.3版本
* ccc2.0 适用于CocosCreator 2.0版本
* 不支持CocosCreator 1.x版本

# 目录结构
* source fairygui的源码
* demo 例子工程,可用CocosCreator直接打开
  * UIProject UI 工程,可以FairyGUI编辑器打开

# 获取fairygui库
如果你只是想添加或者更新fairygui库到你的项目,那么下载以下文件即可:
* bin/fairygui.js
* bin/fairygui.d.ts

# 编译源码
使用VSC打开source目录,执行gulp build任务.

# License
MIT


# 关于编译源码
安装npm

安装gulp
```
npm install gulp-cli -g
npm install gulp -D
gulp --help
```

安装依赖
```
npm install
```

安装rollup
```
npm install rollup
```

执行编译
```
gulp build
```

# 适配cocos creator 3.8

1. RenderComponent -> UIRenderer
2. director.getTotalTime() -> game.totalTime
3. view.getCanvasSize() -> screen.windowSize
4. View.instance.getCanvasSize() -> screen.windowSize
5. spine
6. GTextField 修复位置偏移


# 引入creator工程

  将fairygui.mjs放到asset/lib/目录下

  将fairygui.d.ts放到temp/目录下


  // 修复creator编辑器报错

  项目-项目设置-脚本-Import Map

  // 要重启Creator
  import-map.json
  ```
{
  "imports": {
    "fairygui-cc": "./assets/lib/fairygui.mjs"
  }
}
  ```


  代码中引入
  ```
import * as fgui from "fairygui-cc";

fgui.GRoot.create();
  ```


```
RollupError: You must specify "output.file" or "output.dir" for the build.
```

# PS:
  1. fgui的字距功能在cocos creator中不支持