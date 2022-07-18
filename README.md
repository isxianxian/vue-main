- 代码的目录结构
  -  benchmarks：做性能测试
  - dist：打包后的目录文件
  -  examples：官方的例子
  -  flow：类型检测（和ts功能一样，但现在没人使用了）
  -  packages：一些写好的包（vue源码中包含了week）
  -  scripts：打包脚本
  -  src：源码目录
      - compiler：专门用作模板编译的
      - core：核心代码
      - platforms
      - server：服务端渲染有关
      - sfc：解析单文件组件
      - shared：模块之间的共享属性和方法

- 通过package.json 找到打包入口
- 打包入口：
  - src\platforms\web\entry-runtime-with-compiler.js 
  - src\platforms\web\entry-runtime.js （两个入口文件的区别是，带有compiler的会重写$mount函数，将template转化为render函数，使用区别是啥了）
  