# FPS Zombie Survival Demo

基于 Unity 开发的第一人称僵尸生存射击 Demo，围绕玩家移动、武器射击、物品拾取、僵尸 AI、波次生成、HUD 展示与死亡结算构建完整玩法闭环。

## 项目概览

- 项目类型：Unity 第一人称射击 / 僵尸生存 Demo
- 开发方向：Unity 客户端开发、玩法系统、AI 状态机、UI 交互
- 主要场景：`Assets/Scenes/MainMenu.unity`、`Assets/Scenes/SampleScene.unity`
https://github.com/user-attachments/assets/e51a0302-3941-46b3-a2f9-9ab5ad13bfa1
## 技术栈

- Unity
- C#
- NavMesh
- Animator
- UGUI / TextMeshPro
- PlayerPrefs
- URP

## 主要功能

- 第一人称移动与鼠标视角控制，支持角色移动、跳跃、重力检测和基础 FPS 操作体验。
- 武器系统，支持手枪 / M16 切换、开火、换弹、弹药消耗、单发 / 连发 / 自动射击。
- 射击反馈，支持开镜 ADS、射击扩散、后坐力动画、枪口特效、命中特效和血液特效。
- 中心射线交互系统，支持武器、弹药、手雷和烟雾弹的描边提示与按键拾取。
- 投掷物系统，支持手雷和烟雾弹拾取、蓄力投掷、延迟触发和范围效果。
- 僵尸 AI，基于 NavMesh 与 Animator 状态机实现巡逻、发现玩家、追击、攻击、受击和死亡流程。
- 波次系统，支持僵尸分批生成、清场冷却、波次递增、倒计时 UI 和当前波次展示。
- 游戏流程，支持受击红屏、死亡界面、返回主菜单和最高波次本地存档。

## 核心脚本

- `Assets/Scripts/Weapon.cs`：武器开火、换弹、射击模式、ADS、扩散和子弹生成。
- `Assets/WeaponManager.cs`：武器槽切换、武器拾取、弹药管理和投掷物管理。
- `Assets/InteractionManager.cs`：中心射线检测、物品描边提示和按键拾取。
- `Assets/ZombieSpawnController.cs`：僵尸波次生成、清场检测、冷却倒计时和难度递增。
- `Assets/ZombiePatrolingState.cs`、`Assets/ZombieChaseState.cs`、`Assets/ZombieAttackState.cs`：僵尸状态机逻辑。
- `Assets/HUDManager.cs`：弹药、武器、投掷物和准星 UI 展示。
- `Assets/SaveLoadManager.cs`：使用 PlayerPrefs 保存和读取最高波次。


