# 砼 · VI 编辑器 / Fair-Faced VI Studio

清水混凝土风格的 **LabVIEW 风格数据流图编辑器** —— 单文件 HTML,纯浏览器本地运行,零依赖、零上传。

**在线使用**:GitHub Pages 首页即是。

## 功能

- **程序框图编辑**:22 种节点(控件 / 指示器 / 常数 / 算术 / 比较 / 布尔 / 字符串 / For·While 结构框 / 注释便签),拖端子连线,LabVIEW 式类型着色,类型不匹配自动断线
- **前面板**:控件 / 指示器自动生成,可编辑控件值
- **运行求值**:数据流求值,结果写入指示器;结构框按几何包含迭代;错误列表可点击定位
- **导入 .vi(深挖,只读)**:按社区逆向成果解析 RSRC 容器、解压 zlib 区块,提取框图 / 前面板里的**文本线索**(标签、常量、子VI 路径,支持 GBK 中文),可一键转为画布注记
- **导入 / 导出 `.vidoc.json` 工程**:本工具的完整可再编辑格式
- **导出 SVG(带建筑图签)/ PNG**
- 撤销重做、复制、缩放平移、localStorage 自动续稿

## 边界(诚实声明)

`.vi` 是 NI 的专有二进制格式。本工具对它做到:读容器结构 + 解压区块 + 提取文本,**不做完整对象树解码,也不能写回 `.vi`**。可编辑内容以 `.vidoc.json` 工程承载。

格式细节参考了开源逆向项目 [pylabview](https://github.com/mefistotelis/pylabview)(MIT),内联 [pako](https://github.com/nodeca/pako) 做 zlib 解压。LabVIEW 是 National Instruments 的商标;本项目与 NI 无关,仅用于教学与草图。

## License

MIT
