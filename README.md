Cyber Zen — 电子木鱼 / 泡泡纸模拟器

这是一个极简 Web 单页应用（SPA），用于教学和课堂练习。核心功能：
- 点击屏幕中心的“木鱼”发声（使用 WebAudio，包含“禅咚”和“清脆”两种音色）
- 点击计数器
- 波纹与果冻回弹动画
- 飘字 “+1 功德”

文件：
- index.html       单一 HTML/CSS/JS 文件（可直接打开）
- manifest.json    PWA manifest
- README.md        使用与打包说明
- capacitor.config.json   Capacitor 入门配置信息

如何在浏览器中运行
1. 将 index.html 打开即可体验（双击或用本地静态服务器）。

如何打包成 Android APK（两种推荐方式）
A) 使用 Capacitor（推荐 — 可本地构建）
1. 在你的机器上安装 Node.js、npm、Android Studio、以及 Capacitor： 
   npm i -g @capacitor/cli
2. 在项目目录运行：
   npm init -y
   npm install @capacitor/core @capacitor/cli
   npx cap init cyberzen com.example.cyberzen --web-dir=.
3. 构建 web 资源（这里直接用文件，不需要额外构建），然后：
   npx cap add android
   npx cap copy android
   npx cap open android
4. Android Studio 会打开项目，在那里可以点击 Run -> Build Bundle(s) / APK(s) -> Build APK(s)。

B) 使用 PWABuilder（在线）
1. 将本项目托管到 GitHub 或提供一个 HTTPS 可访问的 URL。
2. 打开 https://www.pwabuilder.com/，输入你的 URL，选择 Android -> Build，使用他们的服务生成 APK / AAB。
注意：使用在线服务可能需要公开托管和遵守其条款。

我无法在本环境直接构建 APK（缺少 Android SDK & build toolchain），但已把完整的 Web 项目打包，你可按上面步骤在本地或用在线服务生成 APK。

如果需要，我可以：
- 生成一个 Capacitor 项目骨架（package.json 等）并打包为 zip，方便你直接打开并执行 npx cap add android（需要我生成的话我会把文件打包供下载）。
- 或者把 index.html 改为“可选的像素字体”版本，或加入自定义音色文件（需要你提供音频或我用 WebAudio 合成）。

告诉我你要哪种：直接给我 APK（我不能直接构建），或让我把 Capacitor 项目骨架打好并打包为 zip（我已包含 basic capacitor.config.json）。
