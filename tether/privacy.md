# 牵线隐私政策 / Tether SSH Privacy Policy


[中文](#中文) · [English](#english) · [支持 / Support](support.md)

## 中文

开发者：**Rongqin Liang**

联系邮箱：[aitim97@icloud.com](mailto:aitim97@icloud.com)

生效日期：**2026年10月17日**

牵线（Tether SSH）是一款免费的 SSH 工作区客户端，用于连接你有权使用的服务器、远程 HTTP 网页和终端。App 不要求注册牵线账号，不提供服务器账号。当前公开版本不提供系统 VPN，也不转发其他 App 的流量。

### 1. 本机配置与登录凭据

为保存和复用连接，SSH 路线、服务器地址、用户名及网页和终端关联保存在本机工作区；密码、私钥及私钥口令保存在系统钥匙串。App 没有内置的配置云同步功能。

配置和凭据会在本机保留，供后续连接使用，直至通过相应删除操作移除。删除步骤及可能的清理限制见下文。App 不替你删除远程服务器上的账户、文件或记录。

### 2. SSH、网页与终端的数据流

连接时，App 向你指定的 SSH 主机发送认证和会话流量。使用跳板路线时，会依次连接配置的各层主机。终端输入和输出经 SSH 传输；远端是否记录命令、保留会话或备份文件，由服务器运营方决定。

内置网页使用系统 WebKit，并为每个页面保留独立的网站数据，例如 Cookie、缓存和登录状态。App 还保存用于恢复的网页地址、位置及受支持的普通表单草稿或状态。这些本地数据用于后续打开或恢复该页面，不保证所有网站、登录流程或编辑器都能恢复。

远程网站可能向自身和第三方服务发出请求。服务器、网站和所选文件服务分别依其自身规则处理数据；本政策不代替它们的政策。

### 3. 配置备份与导入

只有你主动导出时，App 才将配置写入你选择的备份文件。备份包括 SSH 认证信息等凭据，默认使用备份密码加密，也允许你明确选择未加密文件。**任何持有未加密文件的人都可以读取其中保存的凭据。** 备份密码不保存在 App 中，忘记后无法从 App 找回。

文件保存在系统文件窗口中选择的位置，可能是本机，也可能是第三方云文件服务。文件的保存、同步和删除还受所选服务的规则影响。App 不承诺导出的文件始终只留在设备上。

导入会先显示预览，经你确认后追加配置，不自动连接。配置备份不包含网页登录状态、页面草稿、运行中的远端会话或诊断日志。旧备份中的 VPN 参数及令牌可以保留并再次导出；当前公开版本不会启用它们。

### 4. 本地诊断记录

为帮助排查问题，App 默认记录有上限的本地诊断日志，你可以关闭记录、清除日志或主动导出。日志不会自动上传，不包含在配置备份中，也被排除在系统备份之外。

记录内容包括事件时间、App 版本和构建号、系统版本和平台、固定事件和错误码、固定源码记录位置，以及每次运行随机生成的会话标记。系统提供诊断报告时，日志可保留有限的崩溃、卡顿、内存等数字摘要，以及最多 32 帧二进制 UUID、代码偏移、层级和线程归属，用于匹配版本的离线定位。它不保存原始系统报告、任意异常描述或网页内容。系统报告可能延迟或不交付，不能保证包含每次异常的完整原因。

日志接口不记录服务器地址、用户名、用户文件路径、配置标识、密码、私钥、口令、VPN 令牌、网页内容或终端输入输出。本机最多保留最近 512 条事件，文件上限为 256 KiB；达到任一上限时移除最旧记录。

关闭记录会停止后续记录，已有记录仍可单独清除。清除仅影响 App 内日志，不影响配置、网站数据或已导出的文件。

### 5. 管理和删除数据

- **网页：** 在工作区编辑网页并选择“删除网页”，会删除入口和恢复记录，并异步清理该页面的持久网站数据。清理失败时会显示提示；请留意提示，不要将删除入口视为网站数据已无条件清除。
- **终端：** 删除终端入口会关闭相应本地连接；不会删除 SSH 路线凭据，也不等于删除远端 tmux 会话、文件或服务器记录。
- **SSH 路线：** 先删除引用该路线的网页和终端，再编辑路线、选择“删除 SSH 路线”并确认。App 会尝试逐项删除对应钥匙串凭据。配置保存和钥匙串删除可能分别失败，请留意错误提示。
- **历史 VPN 数据：** 从旧备份导入的待启用 VPN 草稿可能阻止 SSH 路线删除；当前公开版没有该草稿的管理入口，遇到此情况请联系支持。此版本不提供清除全部历史 VPN 数据的一键操作。
- **Mac 标签页：** 仅关闭标签页不会删除配置、凭据或网站数据。
- **导出文件和远端数据：** 已导出的备份和日志需在实际保存位置另行删除；服务器或网站中的数据需通过相应服务管理。

卸载 App 不能作为清除系统钥匙串、已导出文件或服务器端数据的保证。删除前如需保留配置，请自行妥善保存备份。

### 6. 支持邮件与其他运营数据

你主动发送邮件时，收件人和所用邮件服务会收到发件地址、正文及你附上的文件。请只提供复现步骤和必要的诊断信息，不发送密码、私钥、网站登录信息或包含凭据的配置备份。

支持邮件由开发者 Rongqin Liang 本人处理，使用 Apple 的 iCloud Mail 接收和存储。开发者仅将你主动提供的邮件和附件用于回复、排查和处理反馈，不用于营销。邮件和附件在处理反馈期间保留，问题解决后90天内删除。你可以向同一支持邮箱申请提前删除或撤回对继续处理支持资料的同意；请说明相关反馈，避免再次发送敏感内容。删除所需的资料可能使我们无法继续处理该反馈。

除本页说明的本地客户端处理、你指定的远程服务和主动发送的支持邮件外，开发者没有另外运营接收此 App 用户数据的服务。

### 7. 本文档网站与其他平台

本页以公开仓库中的 Markdown 文档形式在 github.com 展示。访问本页时，GitHub 按其隐私声明处理网站访问和服务使用信息；App 的本地日志说明不适用于 GitHub 网站本身。本页没有引入 mastermind.ink 原博客主题或其中的访客统计脚本；如果你另行访问该博客，其页面的数据处理与本页分别适用。

GitHub 的网站服务、Apple 的商店及系统服务，以及你选择的第三方服务，各自有相应的数据处理规则。参阅 [GitHub 隐私声明](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)。

### 8. 政策更新与联系

数据处理方式发生变化时，本页和生效日期将相应更新。关于本政策或支持数据删除的问题，请使用上方联系邮箱。此政策说明不替代 App Store 中需要单独填写的隐私信息。

## English

Developer: **Rongqin Liang**

Contact email: [aitim97@icloud.com](mailto:aitim97@icloud.com)

Effective date: **October 17, 2026**

Tether SSH is a free SSH workspace client for servers, remote HTTP pages, and terminals you are authorized to access. It does not require a Tether account or supply server accounts. The current public version does not provide system VPN functionality or forward traffic from other apps.

### 1. Local configuration and credentials

To save and reuse connections, SSH routes, server addresses, usernames, and page and terminal associations are stored in the local workspace. Passwords, private keys, and key passphrases are stored in the system Keychain. The app has no built-in cloud synchronization for configuration.

Configuration and credentials remain locally available for later connections until removed through the applicable deletion actions. Deletion steps and limitations are described below. The app does not delete accounts, files, or records on your remote servers.

### 2. SSH, web pages, and terminals

When you connect, the app sends authentication and session traffic to the SSH hosts you specify. A jump-host route connects through its configured hosts in order. Terminal input and output travel over SSH. Command logging, remote session retention, and server backups are controlled by the server operator.

Embedded pages use system WebKit with a separate persistent website data store for each page, including data such as cookies, caches, and sign-in state. The app also stores the page address, position, and supported ordinary form drafts or state for restoration. These local records help reopen or restore a page; restoration is not guaranteed for every website, sign-in flow, or editor.

Remote websites may contact their own services and third parties. Servers, websites, and selected file services process data under their own rules. This policy does not replace their policies.

### 3. Configuration backups and imports

The app writes configuration to a backup file when you choose to export it. Backups include credentials such as SSH authentication information. Password protection is enabled by default, and you may explicitly choose an unencrypted file. **Anyone holding an unencrypted file can read the credentials it contains.** The backup password is not stored in the app and cannot be recovered from it if forgotten.

You choose the destination in the system file interface. It may be local storage or a third-party cloud file service. The chosen service also controls file storage, synchronization, and deletion. The app does not promise that exported files always remain only on your device.

Import shows a preview and adds configuration after your confirmation; it does not automatically connect. Backups do not include website sign-in state, page drafts, running remote sessions, or diagnostic logs. VPN parameters and tokens from older backups can be preserved and exported again, but this public version does not activate them.

### 4. Local diagnostics

To help investigate problems, the app records bounded local diagnostics by default. You can disable recording, clear logs, or export them yourself. Logs are not automatically uploaded, are not included in configuration backups, and are excluded from system backups.

Records include event time, app version and build, system version and platform, fixed events and error codes, fixed source locations, and a random identifier generated for each app run. If the system supplies a diagnostic report, logs may retain limited numerical crash, hang, and memory summaries, plus up to 32 frames containing binary UUIDs, code offsets, hierarchy, and thread attribution for offline analysis with the matching build. Raw system reports, arbitrary exception descriptions, and web content are not retained. System reports may arrive late or not at all; a complete explanation of every incident is not guaranteed.

The logging interface does not record server addresses, usernames, user file paths, configuration identifiers, passwords, private keys, passphrases, VPN tokens, web content, or terminal input and output. Local storage is limited to the latest 512 events and 256 KiB; the oldest events are removed when either limit is reached.

Disabling recording stops new records. Existing records can be cleared separately. Clearing affects only the app's logs, not configuration, website data, or files already exported.

### 5. Managing and deleting data

- **Pages:** Edit a page in the workspace and choose “Delete page.” This removes the entry and restoration record and asynchronously clears that page's persistent website data. A message appears if clearing fails; removing the entry is not an unconditional guarantee that website data was cleared.
- **Terminals:** Deleting a terminal entry closes its local connection. It does not delete SSH route credentials, remote tmux sessions, files, or server records.
- **SSH routes:** First delete pages and terminals that reference the route. Then edit the route, choose “Delete SSH route,” and confirm. The app attempts to delete the associated Keychain credentials individually. Saving the configuration change and deleting Keychain items can fail separately; check any error message.
- **Legacy VPN data:** Pending VPN drafts imported from older backups may prevent an SSH route from being deleted. This public version has no interface for managing those drafts; contact support if affected. It has no one-step action that clears all legacy VPN data.
- **Mac tabs:** Closing a tab does not delete configuration, credentials, or website data.
- **Exported and remote data:** Delete exported backups and logs from their actual storage location. Manage server and website data through the respective service.

Uninstalling the app is not a guarantee that system Keychain items, exported files, or server-side data are erased. If you want to keep your configuration before deleting it, save a backup securely yourself.

### 6. Support email and other operational data

If you send email, the recipient and the email services used receive your sender address, message, and any attachments you choose to include. Send reproduction steps and necessary diagnostics only. Do not send passwords, private keys, website sign-in details, or configuration backups containing credentials.

Support email is handled personally by Rongqin Liang and received and stored using Apple's iCloud Mail service. The developer uses messages and attachments you choose to send only to respond to, investigate, and handle your feedback, not for marketing. Messages and attachments are retained while the feedback is being handled and deleted within 90 days after the issue is resolved. You may email the same support address to request earlier deletion or withdraw your consent to further handling of support materials. Identify the relevant feedback without sending sensitive content again. Deleting information needed for the investigation may prevent us from continuing to handle it.

Beyond the local client processing, remote services you select, and support email you choose to send as described here, the developer does not operate other services that receive this app's user data.

### 7. This documentation website and other platforms

This page is a Markdown document in a public repository rendered on github.com. GitHub processes website visits and service-usage information under its privacy statement. The app's local-log description does not apply to GitHub's website. This page does not include the mastermind.ink blog theme or its visitor-counter scripts. If you separately visit that blog, its pages have their own data practices.

GitHub's website services, Apple's store and system services, and third-party services you select have their own data practices. See the [GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

### 8. Updates and contact

This page and its effective date will be updated when data practices change. Use the contact email above for policy questions or support-data deletion requests. This policy does not replace the separate privacy information required in App Store Connect.
