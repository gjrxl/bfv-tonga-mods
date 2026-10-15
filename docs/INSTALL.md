# 安装与回退

## 准备

- 已有可正常启动的 BFV、Frosty 和 Tonga 私人房间环境。本仓库不提供这些程序。
- 作者环境为 Frosty Mod Manager 1.0.6.3、BFV head 3564730。不要把这一信息理解为对其他版本的兼容承诺。
- 从 Release 下载所需 `.fbmod`，对照 `SHA256SUMS.txt` 校验。Release 附件名位于各包的说明页面。

## 安装顺序

1. 正常退出游戏。在 Frosty 中新建一个独立 Pack，例如 `TONGA_COMMUNITY_TEST`，保留原组合。
2. 点击 `Add Mod(s)`，导入需要的 `.fbmod`。导入不等于启用：将其加入右侧 Applied Mods 并勾选。
3. 首次只开一个包，关闭其他包。先测试步兵补给，再测试配备互通，最后才两包一起测试。
4. 保持原有可用的启动方式，通过 Frosty `Launch` 加载 MOD，再使用 Tonga `Host A Game` 开自己的私人测试房间。
5. 补给包先拿 PIAT 测试；互通包在 3／4 号配备槽检查选项，然后部署实际使用。具体检查见 TESTING.md。

## 两个 MOD 在管理器中的名称

| Release 文件 | Frosty 显示名称 |
| --- | --- |
| `infantry-resupply-v0.2.1.fbmod` | `Tonga test - ammo resupply` |
| `all-class-gadgets-v0.1.1.fbmod` | `Tonga test - all four classes gadgets` |

这两个包不要求同时启用。配备互通不负责解除装备自身的拥有或等级限制。

## 冲突排查

- 不要同时打开旧 PIAT 补弹包、旧突击兵互通包或未经验证的 Super Tonga 整合包。
- 缺少装备、无法部署或补给无效时，先记录完整启用清单；退出游戏后仅保留出问题的单包再对照。
- 不因故障删除游戏文件、保护组件或管理器缓存；先反馈具体报错和复现步骤。
- 若 Frosty 无法读取文件，先核对校验值、工具版本和下载是否完整。

## 回退

正常退出游戏，在 Frosty 取消相应 MOD，或选回原 Pack，再重新启动。保留下载文件即可，无须修改原游戏源资源。若自己曾改过其他配置，请按自己的备份恢复；本仓库没有更改你的账号进度。

## 图标版升级

下载 v0.1.0-test.2 的新文件，退出游戏后在 Frosty 导入。在 Pack 中停用旧版，启用对应新版；不要将同一 MOD 的新旧版本同时勾选。补给包为橙黄色无限补给箱，配备包为蓝绿色四格。若仍看到默认图标，先核对文件版本和 Applied Mods 中选择的是否为新版。
