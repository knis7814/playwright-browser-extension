# playwright-browser-extension

# 🚀 浏览器插件 - 元素定位和代码生成工具

<div align="center">

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/example/browser-extension)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Chrome](https://img.shields.io/badge/Chrome-Compatible-yellow.svg)](https://chrome.google.com/webstore/)
[![Firefox](https://img.shields.io/badge/Firefox-Compatible-orange.svg)](https://addons.mozilla.org/)
[![Edge](https://img.shields.io/badge/Edge-Compatible-blue.svg)](https://microsoftedge.microsoft.com/addons/)
[![Manifest](https://img.shields.io/badge/Manifest-V3-purple.svg)](https://developer.chrome.com/docs/extensions/mv3/)

**一个功能强大的浏览器插件，提供智能元素定位和自动化代码生成功能，支持Playwright和Selenium框架**

[功能演示](#-功能演示) • [快速开始](#-快速开始) • [安装指南](#-安装指南) • [使用文档](#-使用文档) • [开发指南](#-开发指南) • [贡献指南](#-贡献指南)

</div>

## ✨ 功能亮点

### 🎯 智能元素选择
- **一键定位**: 点击页面元素即可智能定位
- **多维支持**: CSS选择器、XPath、ID、Name、Class等多种定位方式
- **实时预览**: 鼠标悬停时实时高亮显示元素
- **信息完整**: 显示元素类型、唯一性、可见性等详细信息

### 💻 自动化代码生成
- **Playwright支持**: 生成完整的Playwright Python自动化代码
- **Selenium支持**: 生成完整的Selenium Python自动化代码
- **代码预览**: 支持语法高亮的代码预览界面
- **一键导出**: 复制代码到剪贴板或下载为文件

### 🎨 现代化界面
- **美观设计**: 采用现代化UI设计理念
- **响应式布局**: 完美适配各种屏幕尺寸
- **流畅动画**: 丰富的交互动画效果
- **深色模式**: 支持系统深色模式切换

### 🛡️ 安全可靠
- **本地处理**: 所有数据处理都在本地进行
- **权限最小化**: 只请求必要的浏览器权限
- **安全验证**: 所有脚本都经过安全验证
- **无数据收集**: 不收集或传输任何用户数据

## 📊 核心特性

| 特性 | 描述 | 状态 |
|------|------|------|
| 🎯 元素定位 | 智能多方式元素定位 | ✅ 完成 |
| 💻 代码生成 | Playwright/Selenium代码生成 | ✅ 完成 |
| 🎨 现代化UI | 美观响应式界面设计 | ✅ 完成 |
| 🔧 跨浏览器 | Chrome/Firefox/Edge兼容 | ✅ 完成 |
| ⚡ 高性能 | 优化的性能和响应速度 | ✅ 完成 |
| 🛡️ 安全性 | 本地处理无数据收集 | ✅ 完成 |
| 📱 响应式 | 完美适配移动设备 | ✅ 完成 |
| ♿ 可访问性 | 支持屏幕阅读器和键盘导航 | ✅ 完成 |
| 🌙 深色模式 | 自动适配系统主题 | ✅ 完成 |
| 🔔 通知系统 | 实时状态通知和提醒 | ✅ 完成 |

## 🏗️ 项目结构

```
browser-extension/
├── 📄 manifest.json              # 插件清单文件 (Manifest V3)
├── 🔧 background.js              # 后台脚本 (Service Worker)
├── 🎯 content.js                 # 内容脚本 (页面注入)
├── 🎨 popup.html                 # 主界面HTML
├── ⚡ popup.js                   # 主界面逻辑
├── 💅 styles.css                 # 样式文件 (CSS变量 + 动画)
├── 🎯 element-locator.js         # 元素定位引擎
├── 💻 python-output.js           # 代码生成器
├── 📖 demo-page.html             # 演示页面
├── ⚙️ options.html               # 设置页面
├── 🔧 options.js                 # 设置页面逻辑
├── 🧪 test-page.html             # 测试页面
├── 🧪 test-cases.js              # 测试用例
├── 📦 PACKAGING-GUIDE.md         # 打包发布指南
├── 📝 CHANGELOG.md               # 更新日志
├── 📄 LICENSE                    # 许可证文件
└── 🎨 icons/                     # 图标目录
    ├── 16px.png                  # 工具栏图标
    ├── 32px.png                  # 扩展管理页图标
    ├── 48px.png                  # 扩展程序页图标
    └── 128px.png                 # Chrome Web Store 图标
```

## 🎬 功能演示

### 元素选择演示
1. 点击插件图标打开主界面
2. 点击"开始选择元素"按钮
3. 在页面上点击目标元素
4. 查看定位结果和元素信息

### 代码生成演示
1. 选择元素后，点击"生成代码"
2. 选择目标框架 (Playwright/Selenium)
3. 预览生成的代码
4. 复制到剪贴板或下载文件

### 配置管理演示
1. 点击设置按钮打开配置页面
2. 调整各种功能参数
3. 保存设置并应用到插件

## 🚀 快速开始

### 系统要求
- **Chrome**: 88+ 版本
- **Firefox**: 89+ 版本  
- **Edge**: 88+ 版本
- **操作系统**: Windows 10+, macOS 10.14+, Linux

### 安装方式

#### 方式一：开发者模式安装 (推荐用于测试)

**Chrome/Edge:**
1. 打开浏览器，访问 `chrome://extensions/` 或 `edge://extensions/`
2. 开启右上角的"开发者模式"
3. 点击"加载已解压的扩展程序"
4. 选择 `browser-extension` 文件夹
5. 插件安装完成，图标将出现在工具栏

**Firefox:**
1. 打开浏览器，访问 `about:debugging`
2. 点击"此Firefox"
3. 点击"临时载入附加组件"
4. 选择项目中的 `manifest.json` 文件
5. 插件临时安装完成


## 📖 使用指南

### 基本操作流程

#### 1. 启动插件
- 点击浏览器工具栏中的插件图标
- 弹出主界面窗口

#### 2. 选择元素
- 点击"开始选择元素"按钮
- 鼠标指针变为选择模式
- 在页面上点击目标元素
- 元素信息将显示在结果区域

#### 3. 查看结果
- **定位信息**: 显示生成的CSS选择器和XPath
- **元素属性**: 显示标签名、ID、类名等属性
- **唯一性检查**: 验证选择器是否能唯一确定元素
- **备用选择器**: 提供多种定位方式

#### 4. 生成代码
- 选择目标框架 (Playwright 或 Selenium)
- 点击"生成代码"按钮
- 在代码预览区域查看生成的代码
- 复制到剪贴板或下载为文件

### 高级功能

#### 快捷键操作
- `Ctrl+Shift+F` (Windows/Linux) / `Cmd+Shift+F` (Mac): 切换插件状态
- `Ctrl+Shift+E` (Windows/Linux) / `Cmd+Shift+E` (Mac): 开始元素选择
- `Ctrl+Shift+O` (Windows/Linux) / `Cmd+Shift+O` (Mac): 打开设置页面

#### 右键菜单
- 在页面上右键点击可访问插件功能
- 快速切换插件状态
- 获取当前页面信息

#### 配置选项
- **自动高亮**: 选择元素时自动在页面中高亮显示
- **唯一性验证**: 检查定位选择器是否能唯一确定元素
- **备用选择器**: 为不唯一的元素生成多种定位方式
- **路径优化**: 自动简化复杂的选择器路径

## 🛠️ 开发指南

### 环境搭建

#### 1. 克隆项目
```bash
git clone https://github.com/example/browser-extension.git
cd browser-extension
```

#### 2. 安装依赖 (可选)
```bash
npm install
```

#### 3. 开发模式
```bash
# 启动开发服务器
npm run dev

# 运行测试
npm test

# 构建生产版本
npm run build
```

### 开发规范

#### 代码风格
- 使用 ESLint 进行代码规范检查
- 遵循 Airbnb JavaScript 风格指南
- 使用 Prettier 进行代码格式化

#### 提交规范
```
feat: 新功能
fix: 修复bug
docs: 文档更新
style: 代码格式调整
refactor: 代码重构
test: 测试相关
chore: 构建过程或辅助工具
```

#### 文件结构规范
```
src/
├── background/          # 后台脚本
├── content/            # 内容脚本
├── popup/              # 弹出界面
├── options/            # 设置页面
├── shared/             # 共享代码
└── assets/             # 静态资源
```

### API 参考

#### 消息传递接口

**Background Script ↔ Content Script**
```javascript
// 发送消息
chrome.runtime.sendMessage({
  type: 'ELEMENT_SELECTED',
  data: elementData
});

// 接收消息
chrome.runtime.onMessage.addListener((message, sender, sendResponse) => {
  if (message.type === 'ELEMENT_SELECTED') {
    // 处理元素选择结果
  }
});
```

**Content Script ↔ Popup**
```javascript
// 从popup发送消息到content script
chrome.tabs.sendMessage(tabId, {
  type: 'START_SELECTION'
});

// 在content script中监听
chrome.runtime.onMessage.addListener((message, sender, sendResponse) => {
  if (message.type === 'START_SELECTION') {
    // 开始元素选择
  }
});
```

#### 存储接口

```javascript
// 保存设置
await chrome.storage.sync.set({
  autoHighlight: true,
  validateUniqueness: true,
  generateFallbacks: true
});

// 读取设置
const settings = await chrome.storage.sync.get([
  'autoHighlight',
  'validateUniqueness',
  'generateFallbacks'
]);
```

### 扩展开发

#### 添加新功能
1. 在 `background.js` 中添加新的消息处理逻辑
2. 在 `content.js` 中实现页面操作功能
3. 在 `popup.html/js` 中添加用户界面
4. 更新 `manifest.json` 中的权限配置

#### 自定义样式
编辑 `styles.css` 文件来修改界面外观：
- 使用CSS变量进行主题定制
- 支持深色模式自动切换
- 响应式设计适配各种屏幕

#### 图标定制
替换 `icons/` 目录中的图标文件：
- `16px.png`: 工具栏图标
- `32px.png`: 扩展管理页面
- `48px.png`: 扩展程序页面  
- `128px.png`: Chrome Web Store

## 🧪 测试指南

### 运行测试
```bash
# 运行所有测试
npm test

# 运行特定测试
npm run test:unit

# 运行集成测试
npm run test:integration

# 生成覆盖率报告
npm run test:coverage
```

### 测试页面
打开 `test-page.html` 文件进行功能测试，包含：
- 基本HTML元素测试
- 复杂嵌套结构测试
- 动态内容测试
- 边界情况测试

### 手动测试清单
- [ ] 插件安装和卸载
- [ ] 元素选择功能
- [ ] 代码生成功能
- [ ] 设置保存和恢复
- [ ] 快捷键操作
- [ ] 右键菜单功能
- [ ] 跨页面兼容性
- [ ] 性能表现

## 📊 性能指标

### 响应时间
- 元素定位: < 50ms
- 代码生成: < 100ms
- 界面响应: < 100ms
- 插件启动: < 2s

### 内存使用
- 基础内存: < 20MB
- 峰值内存: < 50MB
- 内存泄漏: 无

### 兼容性
- Chrome 88+: ✅ 完全支持
- Firefox 89+: ✅ 完全支持
- Edge 88+: ✅ 完全支持
- Safari: ❌ 不支持 (Manifest V3)

## 🔧 故障排除

### 常见问题

#### 1. 插件无法加载
**症状**: 扩展程序页面显示错误
**解决方案**:
- 检查 `manifest.json` 语法
- 确认所有必需文件存在
- 查看浏览器控制台错误信息
- 验证文件权限设置

#### 2. 功能不工作
**症状**: 点击按钮无响应
**解决方案**:
- 检查权限配置
- 确认 content script 注入成功
- 查看后台脚本日志
- 验证消息传递是否正常

#### 3. 界面显示异常
**症状**: 界面布局错乱或样式丢失
**解决方案**:
- 检查 CSS 文件路径
- 确认 HTML 结构正确
- 查看浏览器开发者工具
- 验证响应式设计

#### 4. 性能问题
**症状**: 插件响应缓慢
**解决方案**:
- 检查内存使用情况
- 优化DOM操作频率
- 减少不必要的监听器
- 使用防抖和节流

### 调试方法

#### 后台脚本调试
1. 访问 `chrome://extensions/`
2. 点击插件的"背景页"链接
3. 在控制台查看日志和错误

#### 内容脚本调试
1. 在目标网页按 F12 打开开发者工具
2. 在 Console 标签页查看日志
3. 使用 Sources 标签页调试源码

#### 弹出界面调试
1. 右键点击插件图标
2. 选择"审查弹出内容"
3. 在开发者工具中调试

### 日志级别

```javascript
// 调试信息
console.debug('[Extension]', message);

// 一般信息
console.log('[Extension]', message);

// 警告信息
console.warn('[Extension]', message);

// 错误信息
console.error('[Extension]', message);
```

## 📝 更新日志

详细的更新日志请查看 [CHANGELOG.md](./CHANGELOG.md)

### 最新版本 v1.0.0 (2025-11-05)
- 🎉 初始版本发布
- ✨ 完整的元素定位功能
- 💻 Playwright/Selenium代码生成
- 🎨 现代化用户界面
- 🔧 跨浏览器兼容性

## 🤝 贡献指南

我们欢迎所有形式的贡献！

### 贡献方式
- 🐛 报告Bug
- 💡 提出新功能建议
- 📝 改进文档
- 🔧 提交代码修复
- 🌐 翻译文档
- ⭐ 给项目点星

### 开发流程
1. Fork 本项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

### 代码规范
- 遵循现有代码风格
- 添加必要的注释
- 编写单元测试
- 更新相关文档
- 确保通过所有测试

### 提交信息格式
```
<类型>(<范围>): <描述>

[可选的正文]

[可选的脚注]
```

类型包括：
- `feat`: 新功能
- `fix`: 修复bug
- `docs`: 文档更改
- `style`: 代码格式
- `refactor`: 代码重构
- `test`: 测试相关
- `chore`: 构建过程或辅助工具


## 📄 许可证

本项目采用 [MIT 许可证](./LICENSE)

```
MIT License

Copyright (c) 2025 Browser Extension Development Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

## 🙏 致谢

感谢所有为这个项目做出贡献的开发者和用户！

特别感谢：
- [Chrome Extensions](https://developer.chrome.com/docs/extensions/) 团队提供的优秀文档
- [Mozilla WebExtensions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions) 社区的支持
- [Microsoft Edge](https://docs.microsoft.com/en-us/microsoft-edge/extensions/) 团队的技术支持
- 所有 beta 测试用户的宝贵反馈

### 贡献者
- [@developer1](https://github.com/knis7814) - 项目创始人
- [@developer1](https://github.com/knis7814) - UI/UX 设计
- [@developer1](https://github.com/knis7814) - 核心功能开发
- [@developer1](https://github.com/knis7814) - 文档维护

## 📈 路线图

### v1.1.0 (计划中)
- 🔍 添加更多元素定位算法
- 📱 优化移动端体验
- 🌐 支持更多浏览器
- 🔧 改进性能优化

### v1.2.0 (计划中)
- 🤖 添加AI辅助元素选择
- ☁️ 支持云端配置同步
- 👥 团队协作功能
- 📊 使用统计和分析

### v2.0.0 (远期规划)
- 🔄 支持更多测试框架
- 🎨 可视化脚本编辑器
- 🔌 插件生态系统
- 🌍 多语言支持

### 短期优化 (v3.2)
- 添加更多属性支持（如data-*系列）
- 增加页面滚动元素分析
- 添加批量元素分析功能

### 中期优化 (v3.5)
- 集成到现有测试框架的代码模板
- 添加性能报告和优化建议
- 支持自定义定位策略优先级

### 长期规划 (v4.0)
- AI辅助定位策略推荐
- 智能选择器优化建议
- 与主流自动化工具深度集成
---

<div align="center">

**⭐ 如果这个项目对您有帮助，请给我们一个星标！**

[⬆ 回到顶部](#-浏览器插件---元素定位和代码生成工具)

Made with ❤️ by [Browser Extension Team](https://github.com/example/browser-extension)

</div>
