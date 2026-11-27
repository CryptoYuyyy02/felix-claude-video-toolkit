# Felix 的 Muse 做视频工具包

> 网上「Muse 做视频必备 20 个仓库」的清单我全实测了一遍，最后真正值得装的只有 3 组。这个仓库就是那 3 组 + 我的实测结论和取舍方法。

作者：Felix（@Feljoy_ix）｜实测日期：2026-11-27

## 为什么有这个仓库

清单类帖子的问题是：不查重、不实测、大小库混着列。

20 个仓库里，11 个我早就在用（Remotion、GSAP、FFmpeg、Three.js 等），6 个只是代码库、写项目时现引就行，真正的新增只有下面 3 组。这个仓库只收这 3 组，而且每个都过了三关：源码审计、和现有工具查重、真跑通一个例子。

## 内容

| 技能 | 管什么 | 上游 | 星数（2026-11-27 实读） |
|---|---|---|---|
| `skills/motion-design-skill/` | 动效导演层：节奏、缓动、编排、迪士尼 12 条动画原则 | LottieFiles/motion-design-skill | 3,760 |
| `skills/anatomy-skill/` | 等距结构图、产品爆炸拆解视图 | wheresryan22/anatomy + annnguyentt/anatomy-reveal-skill | 29,406 / 158 |
| `skills/openverse-media/` | 免 Key 搜免费音效、环境音、音乐、图片（可筛可商用授权） | WordPress/openverse 的公共 API | 824 |

每个技能目录里的 `SKILL.md` 是我按自己工具箱重写的版本：只留实测有用的部分，写清了和同类工具的分工、定版数值与已知坑，不是上游原文搬运。

## 怎么用

把 `skills/` 下的目录整个放进你的 Agent 技能目录（如 `~/.claude/skills/` 或你所用 Agent 的 custom-skills 目录），重启会话即可。具体触发词和用法见每个 `SKILL.md` 开头。

## Demo

`demo/kitchen-comedy-final.mp4`：照清单原帖的钩子视频复刻的同款厨房喜剧短片，40 秒，4 段 AI 视频拼接，胖厨师全程真动、零静图拼接。

## 实测报告

20 个仓库的逐个裁决、审计结论和坑，见 `docs/实测报告.md`。先说三个最容易踩的：

1. anatomy 的爆炸揭晓支线还差一个 puppeteer-core 依赖，没装之前只能算半通
2. librosa 别全量装，白占约 490MB
3. 大库（Remotion / GSAP / FFmpeg 等）别当技能装，写项目时现引

## 授权

- 本仓库的原创内容（重写版技能、实测报告、README、demo 视频）以 MIT 协议开源，见 `LICENSE`
- 三个上游仓库均为 MIT 协议，其版权与原文许可证完整保留在 `upstream-licenses/`，署名见 `NOTICE.md`
- Openverse 搜到的每条素材有各自的 CC 授权，使用前按技能里的纪律核对，BY 类必须署名
