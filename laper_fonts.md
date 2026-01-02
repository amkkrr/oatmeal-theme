# Laper.ai 字体使用分析报告

根据对 Laper.ai 网站源码及 CSS 文件的分析，该网站使用了以下字体组合：

## 1. 界面与正文 (UI & Body Text)

这是网站最主要的字体配置，用于大多数标题、段落和界面元素。

*   **英文字体:** **Montserrat**
*   **中文字体:** **Noto Sans SC (思源黑体)** / **PingFang SC (苹方)**
*   **CSS 定义:**
    ```css
    --font-sans: "Montserrat", -apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Arial, "Noto Sans SC", "PingFang SC", sans-serif;
    ```
    > **说明:** 浏览器会优先加载 `Montserrat`。对于中文内容，优先使用 Google Fonts 提供的 `Noto Sans SC`；如果未加载成功，在 macOS 上会回退到系统自带的 `PingFang SC`。

## 2. 特殊展示标题 (Display Headings)

部分设计感较强的大标题或特殊区域使用了此字体。

*   **字体:** **Bebas Neue**
*   **来源:** Google Fonts (`family=Bebas+Neue`)

## 3. 剧本编辑器 (Script Editor)

为了符合行业标准并模拟传统剧本的打字机风格，编辑器区域使用了等宽字体。

*   **首选字体:** **Courier New**
*   **后备字体:** Courier, Songti SC (宋体-简), Songti TC (宋体-繁)
*   **CSS 定义:**
    ```css
    .ProseMirror {
        font-family: Courier New, Courier, Songti SC, Songti TC, SimSun, NSimSun, serif, monospace;
    }
    ```

## 4. 代码与技术字体 (Monospace / Code)

用于显示代码片段或技术相关的等宽字符。

*   **字体组合:**
    ```css
    --font-mono: "SF Mono", "Menlo", Monaco, "Cascadia Code", Consolas, "Courier New", monospace;