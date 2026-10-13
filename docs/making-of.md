# 制作思路与提示词

参考材料是一张官方纸偶展开图，以及两张正面、一张背面的折叠实物照片。制作目标是让纸偶动起来，同时保留那个「表情特别严肃，身体却方方正正」的反差。

## 造型约束

- 立方体纸盒头，写实印刷面孔，深色头发、浓眉和短胡须。
- 深蓝灰制服、胸前三角标记、红棕色袖带和方块靴子。
- 武器始终握在角色自身的右手；正面看时位于画面左侧。
- 保留纸面纹理和折痕，身体与四肢采用纸盒结构。
- 动作保持克制，不加入漂浮符号、速度线、发光或地面阴影。

## 基础造型提示词

```text
Create one full-body Dylan Faden pet based on the supplied Control Resonant
papercraft references. Preserve the rigid cubic paper head, printed realistic
face, dark swept-back hair, heavy eyebrows, gray-blue eyes and short beard.
Keep the cuboid dark blue-gray utility tunic, brass triangle on anatomical
left chest, red-brown sleeve bands and black block boots. Anatomical RIGHT
hand holds a narrow charcoal blade down beside the body, attached to the fist.
Preserve folded paper edges and recognizable printed likeness. One centered
complete figure on pure cyan #00FFFF. No scenery, text, shadows, glow, guide
marks or detached effects. Keep cyan out of the character.
```

## 动作提示

每种动作单独生成一条横向帧序列，并附上基础造型、参考图与相应的排布指南。

| 动作 | 帧数 | 关键要求 |
| --- | ---: | --- |
| 待机 | 6 | 轻微呼吸与眨眼，双脚基本站稳 |
| 向右跑 | 8 | 侧身向画面右侧，前后脚交替 |
| 向左跑 | 8 | 单独生成，保持武器手别和服装标记 |
| 挥手 | 4 | 空闲左手抬起、摆动、放下 |
| 小跳 | 5 | 轻微起跳、腾空、落回原位，身体比例固定 |
| 受挫 | 8 | 低头、垂肩、恢复 |
| 等待 | 6 | 左手掌心向上，像是在等一个答复 |
| 工作 | 6 | 站定摸下巴、皱眉、点头思考 |
| 检查 | 6 | 倾身、歪头、眯眼检查 |

## 视线方向

身体、脚和持握武器的位置保持稳定。纸盒头通过俯仰与左右转动看向目标，印刷面部跟着盒面转动。抬头时露出下巴与盒子底面，低头时露出更多头顶。

先确定上、右、下、左四个方向，再制作两组连续的八帧视线。角度从正上方开始顺时针计算，相邻方向相隔 22.5°。

## 处理与检查

生成图经过连通区域分帧、背景移除、整行动作比例与基线对齐，再组装成 v2 图集。最后进行一次边缘去色，并从最终图集生成本仓库的所有动画预览。

已检查 73 个必需单元格、15 个透明空白单元格、状态含义、跳跃落点、身体位置和视线方向。此仓库提供最终素材、格式说明和制作提示；生成过程不保证每次产生完全相同的像素。
