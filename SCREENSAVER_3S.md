# Screensaver 3s / 锁屏 3 秒

## 中文

这个仓库是 [decentespresso/streamline-js](https://github.com/decentespresso/streamline-js) 的公开 fork，只改锁屏：

- 屏保解锁从单击改为按住 3 秒。
- 按压点周围显示进度环，3 秒填满。
- 提前松手、拖动超过约 28px，或第二根手指介入，都会取消解锁。
- 其余功能与上游一致。

自动跟随：`.github/workflows/sync-upstream.yml` 每 6 小时合并一次 `upstream/main`，运行 `npm test` 后推送。上游改了同一段代码导致冲突时，工作流会失败并停下，等人工解决。上游 `skin-manifest.json` 的版本变化时，工作流会自动打一个日期版本的 tag，由仓库原有的 release workflow 构建可安装的 zip。

## English

This is a public fork of [decentespresso/streamline-js](https://github.com/decentespresso/streamline-js) with one behavior change:

- The screensaver unlocks with a 3-second press-and-hold instead of a tap.
- A progress ring fills around the press point over those three seconds.
- Releasing early, dragging about 28 px, or a second pointer cancels the unlock.
- Everything else matches upstream.

Auto-follow: `.github/workflows/sync-upstream.yml` merges `upstream/main` every 6 hours, runs `npm test`, and pushes only when the merge is clean and the tests pass. If upstream changes the same code, the workflow stops on the conflict for a manual fix. When upstream's `skin-manifest.json` version changes, the workflow tags a date-based release, and the repository's existing release workflow builds the installable zip.
