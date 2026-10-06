# 论文图片来源

当前页面的 9 篇论文各展示 3 个预览面板，共使用 27 个不同的图像文件，不再展示单张背景示意图或重绘示意图。GUA 使用完整实验总览，以及梯度方向对比图中两组不同方程的原始子面板。

每篇论文的整个预览区统一为 **4:3**，采用“上方完整主图 + 下方并排的两个结果面板”。主图通常为方法架构；GUA 改用比例更合适的完整实验总览。通过 `--method-ratio` 记录原始主图的宽高比，上方区域随该比例确定高度，不裁掉主图内容；下方用 `object-fit: cover` 等比填满剩余区域，可能裁去结果图边缘，适合快速预览而非读取数值。图像文件不拉伸、不重绘、不改动实验结果或颜色；完整内容点击 Paper 或预览图进入原文查看。

## 已核验 PDF 的截图

以下 PDF 均验证了 PDF 文件头、页数以及论文标题，并对截图所在页面进行了目视核对。截图仅裁去页边、正文和图注，未改动结果、坐标轴或颜色；页面以图片替代文本简要预览，详细图注可在链接到的原文中阅读。PDF 页码从 1 起算。

| 论文 / 来源 | 图片 | 原文位置 |
| --- | --- | --- |
| [PG-SR](https://arxiv.org/abs/2602.13021) | `pgsr-method.png`、`pgsr-ood.png`、`pgsr-priors.png` | 图 2 / 第 3 页、图 4 和图 5 / 第 7 页 |
| [GUA](https://arxiv.org/abs/2609.01558) | `gua-performance-overview.png`、`gua-schrodinger-directions.png`、`gua-burgers-directions.png` | 完整图 3 / 第 7 页；图 11 的 Schrödinger、Burgers 两组 Adam / GUA 梯度方向子面板 / 第 35 页 |
| [ICL-Mesh](https://ojs.aaai.org/index.php/AAAI/article/view/39920) | `icl-mesh-quality-preview.png`、`icl-mesh-method.png`、`icl-mesh-refinement.png` | 图 4 中 ICL-Mesh 与高质量参考网格及色标 / 第 5 页、图 3 / 第 3 页、图 5 / 第 6 页 |
| [PI-MeshONet](https://doi.org/10.1016/j.knosys.2025.115054) | `pi-meshonet-method.png`、`pi-meshonet-airfoil-quality.png`、`pi-meshonet-refinement-detail.png` | 图 2 / 第 3 页、图 15(b) 和图 16 的上排加密对比 / 第 10 页 |
| [MeshONet](https://doi.org/10.1016/j.neunet.2026.108746) | `meshonet-method-published.png`、`meshonet-airfoil-published.png`、`meshonet-refinement-preview.png` | 正式版本图 3 / 第 4 页、图 13(b) / 第 8 页、图 22 的 200×200 与 400×400 完整相邻加密面板 / 第 10 页 |
| [DSNO](https://doi.org/10.1109/IJCNN64981.2025.11228931) | `dsno-darcy.png`、`dsno-method.png`、`dsno-burgers.png` | 图 7 / 第 6 页、图 1 / 第 3 页、图 5 / 第 6 页 |
| [PGONet](https://doi.org/10.1063/5.0258420) | `pgonet-method.png`、`pgonet-boundary.png`、`pgonet-obstacles.png` | 图 3 / 第 3 页、图 10 / 第 15 页、图 11 / 第 15 页 |

DSNO 原文为用户工作目录中的 `Dual-Spectral_Neural_Operator_for_Solving_Partial_Differential_Equations.pdf`，共 8 页。已用原文截图替换页面上的 `dsno-overview.svg`；旧文件未删除。

PI-MeshONet 原文为用户工作目录中的 `PI-MeshONet-camera copy.pdf`，共 14 页，首页 DOI 为 `10.1016/j.knosys.2025.115054`。方法图由 `tools/extract_pi_meshonet_figures.py` 提取；这次从图 15 只选取 (b) 的质量比较，从图 16 选取 100×100 和 200×200 两个相邻加密面板，避免预览被压成细条或落在上下图的空隙。方法图采用 `(45, 66, 550, 341)` 的 PDF 截图范围；新结果的坐标见下表。旧的背景示意图和整张实验截图保留，但不再引用。

MeshONet 改为用户提供的正式版本 `1-s2.0-S089360802600208X-main.pdf`，共 11 页，首页标题和 DOI 已核对。作者名单按该正式 PDF 首页补齐为 Jing Xiao、Xinhai Chen、Jiaming Peng、Qinglin Wang、Jie Liu，不将 ResMetaMesh 中的 Qingling Wang 拼写套用到此篇。旧的 arXiv 版本图片仍保留。名称相近的 `PI-MeshONet-camera.pdf` 实际也属于 MeshONet，不用于 PI-MeshONet。

ICL-Mesh 与 MeshONet 的下排改为按选定子图的宽高比分配两列宽度，而不是强制等宽。ICL-Mesh 保留图 4 的 ICL-Mesh 与 High Quality Mesh 两列、三种测试几何及原始色标；MeshONet 保留图 22 的两个完整相邻加密面板，并仅裁去方法图外侧空白。外框仍统一为 4:3，上方方法图完整展示，下排等比填充；这样大幅减少浏览器对完整面板的二次裁切，不重排或重绘原始实验图。

新增 PDF 截图由 `tools/refresh_publication_previews.py` 以 3 倍渲染生成，坐标为 `(左, 上, 右, 下)`，单位 pt：

| 文件 | PDF 页 | 截图范围 |
| --- | --- | --- |
| `pgsr-ood.png` | 7 | `(55, 67, 290, 223)` |
| `pgsr-priors.png` | 7 | `(307, 67, 542, 223)` |
| `gua-performance-overview.png` | 7 | `(106, 81, 505, 275)` |
| `gua-schrodinger-directions.png` | 35 | `(313, 141, 480, 218)` |
| `gua-burgers-directions.png` | 35 | `(313, 232, 480, 309)` |
| `icl-mesh-quality-preview.png` | 5 | `(398, 54, 559, 220)` |
| `pi-meshonet-airfoil-quality.png` | 10 | `(309, 288, 556, 373)` |
| `pi-meshonet-refinement-detail.png` | 10 | `(343, 433, 522, 502)` |
| `meshonet-method-published.png` | 4 | `(62, 57, 534, 319)` |
| `meshonet-airfoil-published.png` | 8 | `(52, 310, 275, 381)` |
| `meshonet-refinement-published.png` | 10 | `(312, 313, 554, 355)` |
| `meshonet-refinement-preview.png` | 10 | `(312, 313, 403, 354)` |

GUA 原方法图的宽高比约 3.88:1，在统一 4:3 拼图区中过于细长，导致下方结果区过高、柱状图两侧被裁。现从本地 `papers/2609.01558.pdf` 重新提取完整图 3（1197×582，约 2.06:1），搭配图 11 两组更新方向对比；下排结果区比例约 1.96:1，与两张原始子面板的 2.17:1 更接近。来源图内的图例、方法名、坐标轴及箭头均保留在提取文件中；网页下排仍可能轻裁边缘刻度。旧三图保留但不再引用。仅更新此篇可运行 `python tools/refresh_publication_previews.py --pdf-source papers/2609.01558.pdf`，无需下载其他论文图片。

用户当前预览中的三张新图均加载失败，而本地文件和本地 HTTP 测试正常；该预览环境的具体失败原因尚未核实。为消除这一篇对新增文件路径的依赖，三张 PNG 现按原始字节以 `data:image/png;base64,...` 内嵌到 `index.html`，`data-source` 保留对应来源路径。三个源文件仍保留，合计约 109 KB；Base64 编码使 HTML 增加约 145 KB，不改变图像像素或科学内容。即使图片目录不可访问，这三张图也可随 HTML 显示。重新提取后须同步更新内嵌内容；`tools/embed_gua_previews.py` 生成供 `apply_patch` 使用的修改补丁，不自行写入 HTML；`python -X utf8 tools/embed_gua_previews.py --check` 可验证内嵌字节与源文件一致。

## 出版社公开图片

这些文件通过出版社公开图片接口获得，按 PII 核对所属论文并目视核对图内内容。未取得这两篇完整 PDF，正文页面返回 403，因此不将 `gr` 资源编号冒充已核实的正文图号，也不补写无法读取的原文图注。以下文件保留接口返回的原始 JPEG 字节，只由浏览器缩放预览。

| 论文 | 文件 / 内容 | 出版社图片来源 |
| --- | --- | --- |
| [ResMetaMesh](https://doi.org/10.1016/j.cagd.2026.102585) | `resmetamesh-method.jpg`：预训练、硬约束、LoRA 微调架构 | [gr2](https://ars.els-cdn.com/content/image/1-s2.0-S0167839626000798-gr2_lrg.jpg) |
| ResMetaMesh | `resmetamesh-spanner.jpg`：扳手几何的网格质量对比 | [gr3](https://ars.els-cdn.com/content/image/1-s2.0-S0167839626000798-gr3_lrg.jpg) |
| ResMetaMesh | `resmetamesh-disc.jpg`：多孔圆盘的网格质量对比 | [gr4](https://ars.els-cdn.com/content/image/1-s2.0-S0167839626000798-gr4_lrg.jpg) |
| [LDNO](https://doi.org/10.1016/j.neucom.2026.134745) | `ldno-method.jpg`：液态层、LSTM 和自适应交叉注意力融合架构 | [gr3](https://ars.els-cdn.com/content/image/1-s2.0-S0925231226021430-gr3_lrg.jpg) |
| LDNO | `ldno-field-slices.jpg`：标量场 Truth / Prediction 和时间切片对比 | [gr7](https://ars.els-cdn.com/content/image/1-s2.0-S0925231226021430-gr7_lrg.jpg) |
| LDNO | `ldno-field-errors.jpg`：不同初始条件下的 Truth / Prediction / Error 场图 | [gr8](https://ars.els-cdn.com/content/image/1-s2.0-S0925231226021430-gr8_lrg.jpg) |

此前使用的 `resmetamesh-graphical-abstract.jpg` 和 `ldno-graphical-abstract.jpg` 实际是方法背景/基础概念图片，不是合适的完整方法架构，现已换下。新增公开图片也由 `tools/refresh_publication_previews.py` 下载。

ResMetaMesh 的整张实验图含八个几何面板，在缩略图中容易过密。页面实际使用 `resmetamesh-spanner-preview.jpg`（来自 gr3，原始像素范围 `(1180, 540, 2361, 1049)`，选取下排 Latent / Full 结果）和 `resmetamesh-disc-preview.jpg`（来自 gr4，范围 `(0, 690, 2361, 1313)`，选取下排对比）。两图从保留的原始 JPEG 裁取，以标准 RGB JPEG 编码，最长边不超过 1600 像素；只作裁切、缩放和有损压缩，未重绘科学内容。可运行 `python tools/refresh_publication_previews.py --publisher-details-only` 从本地原图重新生成，无需联网。

此前的两个 `*-detail.png` 保留但不再引用。用户截图中的两个 PNG 加载失败，本地文件可正常解码，因此尚不能确定其预览环境中的失败原因；换用新文件名的 JPEG，并在加载失败时回退到对应完整本地 JPEG。发布网站时须同步上传这四个 JPEG 资源（两张预览、两张备用原图），不能只更新 HTML。

## PGONet 作者录用稿原图

PGONet 原文为用户提供的 `POF25-AR-001011.pdf`，共 18 页；首页标题为 *A Physics-Informed Generative Adversarial Network for Advancing Solutions in Ocean Acoustics*，DOI 为 `10.1063/5.0258420`。这是作者录用稿，不冒充出版社排版版本。通过 `tools/extract_pgonet_figures.py` 以 3 倍 PDF 渲染，截取图 3 的整体架构、图 10 的压力释放边界检测、图 11 的多障碍物检测。坐标（左、上、右、下，单位 pt）分别为 `(172, 444, 544, 569)`、`(167, 149, 541, 350)`、`(168, 394, 546, 598)`；只去掉页边、稿件水印侧栏、正文和独立图注，保留图内标注、坐标轴和实验结果。

主页上方的方法图按原始 1116:375 比例完整展示，下方两张实验图等比覆盖，整个外框与其他论文一样为 4:3。旧文件 `pgonet-architecture.svg` 保留但不再引用，“方法示意图（重绘）”标注已移除。

旧版未再引用的图片保留，便于恢复。图片版权归原作者或出版社所有；将页面公开发布前，请确认个人主页使用权限，尤其是出版社版本的图像。
