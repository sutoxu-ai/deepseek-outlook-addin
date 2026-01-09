
# DeepSeek Outlook Add-in（最简版）

> 这是一个最小可用的 Outlook 加载项：在撰写邮件时打开任务窗格，调用 DeepSeek API 生成中文回复，并插入到草稿。

## 使用步骤
1. **托管网页（必须 HTTPS）**：
   - 将 `web/index.html` 上传到可访问的 HTTPS 地址，例如 `https://YOUR_HOST/web/index.html`。
   - 编辑 `manifest.xml`，把 `https://YOUR_HOST/web/index.html` 改为你的实际网址。
2. **设置 API Key（开发测试）**：
   - 打开 `web/index.html`，用你的 `DeepSeek API Key` 替换 `REPLACE_WITH_YOUR_DEEPSEEK_API_KEY`。
   - 生产环境请改为**后端代理**以保护密钥。
3. **Outlook 安装自定义加载项**：
   - 进入 Outlook Web → 设置 → 加载项 → 我的加载项 → 上传自定义加载项，选择 `manifest.xml`。
   - 在撰写新邮件界面找到“DeepSeek 智能回复助手”，打开使用。

## 注意事项
- 本示例为教学与内测用途：前端直连 API 有密钥泄露风险，请在正式环境使用后端代理。
- Office.js 文档与自定义加载项概念参见：
  - Office Add-ins 概览：https://learn.microsoft.com/office/dev/add-ins/overview/ 
  - Outlook 加载项：https://learn.microsoft.com/office/dev/add-ins/outlook/outlook-add-ins-overview 
- 若中国大陆访问 DeepSeek API 受网络影响，请确保你的服务器出口网络可达。
