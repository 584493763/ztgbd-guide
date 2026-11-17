# ZtGBD 使用教程

面向全球疾病负担（Global Burden of Disease, GBD）数据的 R 函数集合 `ZtGBD` 的操作手册，覆盖数据读取与整理、率指标计算、趋势与预测建模、健康不平等测度以及结果图形化五个环节。

## 在线阅读

<https://584493763.github.io/ztgbd-guide/>

页面左侧为函数级目录，可直接跳转到具体函数。

## 内容范围

| 章节 | 内容 | 涉及函数 |
|---|---|---|
| 1 | 包体结构与运行环境 | 依赖、授权、可选组件 |
| 2 | 数据准备与筛选 | a1.GBDread、a2.GBDFactor、a3.GBDfilter |
| 3 | 率与趋势指标 | b1.ASR、b2.ASRrei、b3.EAPC |
| 4 | 三线表输出 | b4.GBDtable、b5.GBDtable2 |
| 5 | 描述性图形 | c1–c5 |
| 6 | 地理分布制图 | d1.Mapquantile、d2.Map |
| 7 | 年龄-时期-队列模型 | e1.APC、e2.plotAPC |
| 8 | Joinpoint 回归 | f1.Joinpoint、f2/f3 |
| 9 | 疾病负担分解 | g1.decomposition、g2.plotDecom |
| 10 | 趋势预测 | h1–h5 |
| 11 | 前沿分析 | i1.Frontier、i2.plotFrontier |
| 12 | 健康不平等 | j1.GBDInequality、j2/j3 |
| 13 | SDI 与风险因素 | k1–k4 |
| 14 | 质量照护指数 | m1.GBDQCI |
| 15 | 结果导出 | l1.GBDsave |
| 16 | 常见问题 | 加载、筛选、渲染、路径 |

## 版本与环境

- ZtGBD 3.1.3
- R 4.5.1（Windows x64）
- 文档内全部图形由对应脚本实际运行产生，未作后期修饰

## 关于示例数据

文档中的示例数据按 GBD Results Tool 导出表的结构模拟生成：人口字段取自 GBD 2021 估计值，年龄别率按年龄、年份与社会发展指数的结构设定，**数值仅用于演示函数行为，不代表真实流行病学估计**。实际分析时以官方下载数据替换即可，函数调用方式不变。

## 本地查看

仓库为纯静态页面，克隆后直接打开 `index.html` 即可；若需与线上一致，可在仓库根目录启动任意静态服务器：

```bash
python -m http.server 8000
```

## 目录结构

```
ztgbd-guide/
├── index.html          教程正文（单页，含目录锚点）
├── README.md
├── .nojekyll           禁用 Jekyll 构建
└── assets/
    └── fig/            23 张示例图形
```
