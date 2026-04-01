# 修改记录

## 2026-03-23

- GoBackToSleep: 修复待机唤醒一次后功能失效的问题，系统唤醒时自动重建 EventLogWatcher 订阅
- GoBackToSleep: 修复切换开关导致程序卡死的死锁问题，将 watcher Dispose 和 SendMessage 移至后台线程
- 修改文件：`HandheldCompanion/Platforms/Misc/WindowsPlatform.cs`

## 2026-03-20

- GoBackToSleep: 合法唤醒（电源键/指纹）后增加 2 秒 grace window，忽略伴生的 Joystick/Other 等 507 事件，修复指纹解锁时屏幕闪烁问题
- GoBackToSleep: 增加调试日志，记录 wake reason 原始码、映射结果及 resleep 决策
- 修改文件：`HandheldCompanion/Platforms/Misc/WindowsPlatform.cs`

## 2026-03-16

- 将指纹解锁(Reason=44)加入 GoBackToSleep 允许唤醒范围，指纹唤醒不再被送回睡眠
- 修改文件：`HandheldCompanion/Platforms/Misc/WindowsPlatform.cs`
