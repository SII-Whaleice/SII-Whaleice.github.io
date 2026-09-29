# 维护论文列表

论文集中在 `_data/publications.yml`（JSON 写法也是合法 YAML）。页面自动按
分为图文论文、纯文字论文两组，图文组在前，两组内部均按 `order` 从大到小排序。Jingyu Li 位列前三位作者的论文显示图片，其余条目以圆点列表显示题目链接、作者和加粗的会议/期刊名称，不保留图片占位或图片列。
作者列表用英文逗号加空格分隔；`Jingyu Li`（含星号标记）会自动加粗。

## 添加论文

复制一条已有记录，修改 `title`、`url`、`authors`、`venue`、`year` 和 `order`。
`code` 没有时填空字符串。当前 `order` 格式为
`发表年份-arXiv编号前四位-arXiv编号后五位`，先按发表年份、再按预印本先后排序。
没有 arXiv 编号的旧条目暂放同年末尾，精确顺序可在核对日期后调整。

## 放入图片

1. 把图片放到 `images/`，例如 `images/metis.png`。
2. 将对应论文的 `"image": ""` 改成 `"image": "images/metis.png"`。
3. 图片未配置时显示占位框。桌面图片区域宽 180px，手机宽 160px。
   图片使用 `object-fit: contain`，保持比例，不裁切。

新增论文后，自动根据作者列表中的位置决定是否显示图片，与论文在页面中的位置无关。
共同一作的星号不改变作者列表中的实际位置。无需编辑页面 HTML。

当前需要图片的 12 篇论文（括号内为 Jingyu Li 的作者位置）：

- Metis（1）：`images/metis.png`
- MCNav（1）：`images/mcnav.png`
- Uni-World VLA（3）：`images/uni-world-vla.png`
- SGDrive（1）：`images/sgdrive.png`
- GeoTeacher（1）：`images/geoteacher.png`
- Perception in Plan / VeteranAD（2）：`images/veteranad.png`
- ImagiDrive（1）：`images/imagidrive.png`
- UniMotion（3）：`images/unimotion.png`
- Future-Aware End-to-End Driving / SeerDrive（3）：`images/seerdrive.png`
- RealEngine（3）：`images/realengine.png`
- DDS3D（1）：`images/dds3d.png`
- SOOD（3）：`images/sood.png`

路径为建议文件名；填写对应记录的 `image` 字段后才显示图片。暂时保留占位框。
MiCEval、Ground Segmentation、A Simple Vision Transformer 中作者位置为第四，
因此显示圆点、标题链接、作者及加粗的会议/期刊名称。

UniMotion 的 arXiv 页面标注为 NeurIPS 2025，因此按会议年份归入 2025，
虽然预印本在 2026 年 1 月上传。Metis、MCNav 和 Uni-World VLA 暂标为 arXiv 2026。
