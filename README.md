# Deribit Quick Order (GEXmonitor 极速下单面板)

🚀 **一个纯前端、100% 开源的 Deribit 期权极速下单工具。**

本工具专为期权高频交易员和做市商设计，完全剥离了传统架构中的后端服务器，通过浏览器 WebSocket 直连 Deribit 撮合引擎，将下单延迟降至物理极限。

## 💡 核心亮点

- **极致速度**：0 中间件，0 后端服务器。通过 `wss://` 直连官方接口，免除 TCP/TLS 握手开销。
- **纯前端架构**：只需一个 `index.html` 即可运行。可托管在 GitHub Pages，或下载到本地双击打开。
- **降低托管风险**：API Key 仅保存在浏览器本地的 `localStorage` 中。**您的私钥绝不会发送给 GEXmonitor 或任何第三方服务器，仅用于向 Deribit 官方请求鉴权**。
- **近端 Delta 过滤**：专为末日期权设计，自动过滤无流动性合约。
- **移动端适配**：完美的底部抽屉交互，在手机浏览器中也能实现“一键盲狙”。

## ⚠️ 安全与免责声明

**资金安全是第一要务。在使用本工具前，请务必阅读并理解以下安全模型：**

1. **权限控制**：请在 Deribit 后台创建一个专属的 API Key。**强烈建议仅勾选 `Read` 和 `Trade` 权限。绝不要在此工具或任何第三方工具中输入带有 `Withdraw` (提现) 权限的 API Key！**
2. **环境风险**：虽然本代码绝无收集私钥的后门，但前端环境天生受制于客户端安全。请确保您的电脑没有中木马，浏览器没有安装恶意的流氓插件，不要在网吧等公共共享电脑上输入您的 API Key。
3. **免责条款**：本开源项目不构成任何形式的投资建议。所有的交易策略及损益均由使用者自行承担。开发者不对任何因为 API 滥用、软件 Bug 或极端行情导致的资金损失负责。
4. **非官方产品**：本工具由 [GEXmonitor](https://gexmonitor.com) 团队开发并开源，并非 Deribit 官方发行的客户端软件。

## 🚀 如何使用

### 方案 A：直接使用在线版（最快）

代码已托管在 GitHub Pages 上，您无需任何配置即可直接访问：
👉 [https://gexmonitor-pixel.github.io/deribit-quick-order/](https://gexmonitor-pixel.github.io/deribit-quick-order/)

### 方案 B：本地运行（最硬核）

如果您有极高的安全洁癖，不信任任何在线托管服务，您可以将代码下载到您的本地电脑上运行。
1. `git clone https://github.com/gexmonitor-pixel/deribit-quick-order.git`
2. 用任意浏览器双击打开文件夹里的 `index.html` 文件，即可直接交易。

## 🎁 福利与社区

- **9折手续费**：使用我们的 [专属邀请链接](https://www.deribit.com/action?reg=15541.6830) 注册 Deribit，可享受 9 折手续费。
- **加入社区**：欢迎加入我们的 [Telegram 交流群](https://t.me/Ljbp1008) 探讨期权策略，或订阅 [YouTube 频道](https://www.youtube.com/@gexmonitor) 获取实战复盘。
- **访问主站**：想要大资金量级的期权异动和 Gamma 墙数据？欢迎访问 [GEXmonitor 主站](https://gexmonitor.com)。

## 📄 许可证
本项目采用 MIT License 开源。
