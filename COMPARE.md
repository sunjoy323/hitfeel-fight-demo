# 原文终版 vs Demo 对照

对照图：`/workspace/hitfeel-demo/compare.png`

## 本轮修复 / 优化
- **对战失灵根因**：`const AT_L` 拼写错误（应为 `ATK_L`）。轻拳或 AI 轻拳一出手就抛 `ATK_L is not defined`，整局 `requestAnimationFrame` 中断 → 手机上表现为「按不动」。
- 模式按钮：避免 `touchstart preventDefault` 吞掉 click；`bindTap` 兼容触屏。
- 操作区：更大按钮、`z-index`、短屏缩小 canvas；pointer capture，去掉 iOS 误触的 `pointerleave` 清键。
- 跳跃/出拳意图提到状态机前面，不被 attack/hurt early-return 吃掉。
- 视觉：更肉的体型、更狠蓄力/冲拳、受击挤压更强、射线不规则 + 轻胶片颗粒/暗角。

## 仍有差距
- 原文手绘闪光的脏感与接触形变仍略强于 Canvas 近似。
