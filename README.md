# 板材加工NC路径模拟器

从v1.1.23放弃了Three.js + three-bvh-csg的渲染方案，使用了更高效的Manifold WASM 布尔运算库，提高对异形切割，圆弧切割等复杂切割效果的完美展示。
在此提供在线版本，目前搭建在免费的cloudflare page上，如果打不开，你可以下载最新版本压缩包，使用远程调用版（单文件版远程加载JS库https://jsd.onmicrosoft.cn/npm/manifold-3d@3.5.1/manifold.js），如果不能正常使用可自行修改替换manifold.js镜像源，或者自行在本地搭建服务器使用。

临时在线使用，请访问：
https://ncraft.ixujun.dpdns.org/nc-simulator

包内文件结构：
根目录（Web 站点根 or 子目录）/

├── nc-simulator_local.html          ← 本地调用版，需要搭建服务环境
├── nc-simulator_online.html          ← （推荐）远程调用版，单文件打开即可使用，如果不能正常加载，请替换manifold.js的镜像源地址

└── manifold_local/

    ├── manifold.js            ← Manifold WASM 的 JS 加载器，只有本地搭建服务器时才使用
    └── manifold.wasm          ← Manifold WASM 二进制（布尔运算核心），只有本地搭建服务器时才使用

####其它可用的manifold.js镜像源地址：

- 官方CDN镜像原（国外使用，国内可能慢）：
    https://cdn.jsdelivr.net/npm/manifold-3d@3.5.1/manifold.js

- 国内可用 jsdelivr 镜像（推荐国内使用）：

```
https://jsd.onmicrosoft.cn/npm/manifold-3d@3.5.1/manifold.js
```

```
https://cdn.jsdmirror.cn/npm/manifold-3d@3.5.1/manifold.js
```
```
https://jsd.cdn.zzko.cn/npm/manifold-3d@3.5.1/manifold.js
```

#### 介绍
这是一个用于模拟全屋定制行业常用NC路径模拟器，除能直观查看NC加工路径的运行过程外，还可以模拟板材的切割和打孔效果，方便在生产过程中查找问题。

#### 软件特点
- 做全屋定制的老板都很穷，所以此软件完全免费
- 能模拟常用板材的加工效果，可以看到切割，打孔，开槽效果
- 可以设置刀具的直径，模拟效果更真实
- 增加了NC代码跟踪预览，方便排查问题



#### 安装教程

1.  不需要安装
2.  单html文件，直接浏览器打开即可
3.  也可部署到自己的web服务器

![输入图片说明](%E9%A2%84%E8%A7%88%E5%9B%BE.png)

