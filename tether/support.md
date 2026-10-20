# 牵线支持 / Tether SSH Support


[中文](#中文) · [English](#english) · [隐私政策 / Privacy policy](privacy.md)

## 中文

牵线是一款免费的 SSH 工作区 App，可访问你有权使用的远程 HTTP 网页和 SSH 终端。你需要准备可连接的 SSH 服务器及认证信息；App 不提供服务器账号，也不要求注册牵线账号。当前公开版本不提供系统 VPN，不转发其他 App 的流量。

### 联系支持

开发者：**Rongqin Liang**

支持邮箱：[aitim97@icloud.com](mailto:aitim97@icloud.com)

反馈时请尽量提供：

- App 版本及构建号、系统版本、设备型号。
- 大致发生时间、操作步骤、期望结果和实际结果。
- 是连接失败、单个网页白屏／重载、终端异常，还是整个 App 退出。
- 必要的脱敏截图：遮住服务器地址、账户和页面私人内容。

请勿发送密码、私钥、私钥口令、网站登录信息或包含凭据的配置备份。复现步骤与主动导出的诊断日志通常足以开始排查。支持邮件仅用于处理反馈，不用于营销；问题解决后90天内删除邮件和附件，也可向同一邮箱申请提前删除。完整的数据处理说明见[隐私政策](privacy.md)。

### SSH 连接不上怎么办？

检查当前网络是否能访问 SSH 服务器，以及主机、端口、用户名和认证方式是否正确。多层跳板的每一层都需要有效的连接信息。首次连接时，请向服务器管理员核对准确的主机指纹；不要为了继续操作而忽略指纹变化警告。

服务器、网络限制和凭据均可能导致连接失败；单凭“连接失败”提示无法确定是哪一方的问题。反馈时说明出现问题的步骤即可，不要发送真实凭据。

### SSH 已连接，网页仍打不开怎么办？

网页目标必须能从最后一台 SSH 主机访问。配置中的 `127.0.0.1` 表示最后一台 SSH 主机自身，不是手机或 Mac。当前网页映射针对 HTTP 服务，不保证任意网站、登录流程或编辑器均能使用或恢复。请先确认服务器上的 HTTP 服务、端口和路径。

### 如何迁移或备份配置？

在工作区选择“导出配置”，用系统文件窗口保存备份；在另一台设备选择“导入配置”。加密文件需输入备份密码，未加密文件直接进入预览。确认后追加配置，已有配置继续保留，导入本身不会自动连接。首次连接仍需核对 SSH 指纹。

导出默认开启密码保护，也可明确选择未加密备份。备份可能包含完整登录凭据，未加密文件可被持有人直接读取。请妥善保管文件和密码；密码不保存在 App 中，忘记后无法从 App 找回。

同一份备份重复导入不会增加副本，也不会补回首次导入后主动删除的条目。重新导出的新备份按另一份备份处理。网页登录状态、页面草稿、运行中的远端会话和诊断日志不包含在配置备份里。

### 网页异常或 App 退出后，如何提供诊断？

重新打开 App，从工作区“配置备份”区域进入“诊断日志”；Mac 的入口位于侧栏底部。选择“导出诊断日志”，用系统文件窗口保存 `tether-diagnostics.json`，并记下大致发生时间。区分整个 App 退出与单个网页白屏或重新加载，可以帮助定位。

日志在本地记录，不会自动上传。你可以关闭记录、清除 App 内日志，或自行选择是否发送导出的文件。系统报告可能延迟或不交付，日志不保证包含每次异常的完整原因。清除 App 内日志不会删除已导出的文件。

### 切换 App 或关闭终端后，远端任务还在吗？

后台连接受系统限制，普通 SSH 终端关闭连接后不保证远端任务继续。服务器安装 tmux 且相关会话仍存在时，可以重接该会话；App 不保证服务器永久保留它。Mac 关闭标签页只关闭该标签的显示，不等于删除终端配置或远端任务。

### 怎样删除本地配置和网站数据？

在工作区编辑网页或终端，使用对应删除操作。删除网页会尝试清理其恢复记录及持久网站数据；删除终端不会删除 SSH 凭据。先删引用某条 SSH 路线的页面和终端，再编辑并删除路线，App 会尝试删除其钥匙串凭据。请留意清理失败提示。

Mac 关闭标签页不是删除配置；卸载也不保证清除钥匙串、导出文件或服务器端数据。历史 VPN 草稿可能阻止路线删除，公开版暂无草稿管理入口。详见[数据管理与删除](privacy.md#5-管理和删除数据)。

### 为什么没有系统 VPN 入口？

系统 VPN 尚未包含在当前公开版本中。SSH 终端与 App 内网页映射仍可使用。旧备份中的 VPN 参数和令牌可保留并再次导出，但这个版本不会启用它们；不承诺后续提供时间。

## English

Tether SSH is a free SSH workspace app for remote HTTP pages and SSH terminals you are authorized to access. You need a reachable SSH server and its authentication details. The app does not supply server accounts or require a Tether account. The current public version has no system VPN and does not forward traffic from other apps.

### Contact support

Developer: **Rongqin Liang**

Support email: [aitim97@icloud.com](mailto:aitim97@icloud.com)

When reporting a problem, please include:

- App version and build, system version, and device model.
- Approximate time, steps to reproduce, expected result, and actual result.
- Whether a connection failed, one page went blank or reloaded, a terminal failed, or the entire app exited.
- Necessary screenshots with server addresses, accounts, and private page content removed.

Do not send passwords, private keys, key passphrases, website sign-in details, or configuration backups containing credentials. Reproduction steps and diagnostic logs you choose to export are usually enough to begin an investigation. Support email is used only to handle feedback, not for marketing. Messages and attachments are deleted within 90 days after the issue is resolved; you may request earlier deletion at the same address. See the [privacy policy](privacy.md) for the full data-handling details.

### What if SSH will not connect?

Check that your current network can reach the SSH server and that the host, port, username, and authentication method are correct. Every host in a jump route needs valid connection details. Verify a new host fingerprint with the server administrator. Do not ignore a changed-fingerprint warning just to continue.

Server availability, network restrictions, and credentials can all cause connection failures. A generic failure message alone does not identify the cause. Report the step at which it happens without sending real credentials.

### Why does a page fail when SSH is connected?

The page's destination must be reachable from the final SSH host. `127.0.0.1` in the page configuration means that final host, not your phone or Mac. Web forwarding currently targets HTTP services; access or restoration is not guaranteed for every website, sign-in flow, or editor. First check the HTTP service, port, and path on the server.

### How do I move or back up my configuration?

Choose “Export configuration” in the workspace and save the file using the system file interface. On the other device, choose “Import configuration.” Encrypted files require the backup password; unencrypted files go directly to preview. Confirmation adds configuration alongside what you already have and does not automatically connect. Verify SSH fingerprints when first connecting after import.

Password protection is on by default, but you can explicitly choose an unencrypted backup. Backups may contain full login credentials; anyone holding an unencrypted file can read them. Keep the file and password safe. The password is not stored in the app and cannot be recovered from it.

Importing the same backup again does not add duplicates or restore entries you deleted after its first import. A newly exported backup is treated as a different backup. Website sign-in state, page drafts, running remote sessions, and diagnostic logs are not included in configuration backups.

### How can I provide diagnostics after a page failure or app exit?

Reopen the app and find “Diagnostic logs” in the workspace's “Configuration backup” area; on Mac it is at the bottom of the sidebar. Choose “Export diagnostic logs” and use the system file interface to save `tether-diagnostics.json`. Note the approximate time and whether the entire app exited or only one page went blank or reloaded.

Logs are local and are not automatically uploaded. You can disable recording, clear the app's logs, or decide whether to send an exported file. System reports may arrive late or not at all, so a complete explanation of every incident is not guaranteed. Clearing the app's logs does not delete exported copies.

### Do remote tasks survive switching apps or closing a terminal?

Background connections are subject to system limits. A remote task in a plain SSH terminal is not guaranteed to continue after the connection closes. If tmux is installed on the server and its session still exists, you can reconnect to that session. The app does not guarantee that a server keeps sessions forever. On Mac, closing a tab only closes its presentation; it is not a deletion of terminal configuration or remote tasks.

### How do I delete local configuration and website data?

Edit a page or terminal in the workspace and use its delete action. Deleting a page attempts to clear its restoration record and persistent website data. Deleting a terminal does not delete SSH credentials. First delete pages and terminals referencing an SSH route, then edit and delete the route; the app attempts to remove its Keychain credentials. Check any clearing-failure messages.

Closing a Mac tab does not delete configuration. Uninstalling is not a guarantee that Keychain items, exported files, or server data are erased. Legacy VPN drafts may prevent a route from being deleted, and this public version has no draft-management interface. See [Managing and deleting data](privacy.md#5-managing-and-deleting-data).

### Why is there no system VPN entry?

System VPN is not included in this public version. SSH terminals and in-app web forwarding remain available. VPN parameters and tokens from older backups can be preserved and exported again, but this version does not activate them. No future availability date is promised.

## Third-party acknowledgements / 第三方致谢

This product includes software developed by Niels Provos.

This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit. (http://www.openssl.org/)

This product includes cryptographic software written by Eric Young (eay@cryptsoft.com).

This product includes software written by Tim Hudson (tjh@cryptsoft.com).
