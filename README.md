# Hexo TTS Learning Plugin

<img width="817" height="451" alt="image" src="https://github.com/user-attachments/assets/a2c4fedc-c3b1-4d64-8948-f39fbae310b1" />

[Demo](https://rduanchen.github.io/language_learning/)

## Purpose

**Hexo TTS Learning** is a plugin for [Hexo](https://hexo.io/) that adds interactive language learning cards to your blog posts. Each card allows users to:

- Listen to sentences or individual words with Text-to-Speech (TTS).
- Record and play back their own pronunciation.
- View translations and notes.
- Enjoy dark and light theme support.

This plugin is ideal for language blogs, pronunciation practice, or any educational content where audio feedback and interactivity are valuable.

## Installation (Manual)

**Note:** This plugin uses a manual installation approach.  
You must copy the provided files into the correct directories in your Hexo project.

### 1. Download or clone the repository

Download the files from this repository or clone it:

```bash
git clone https://github.com/<yourusername>/hexo-tts-learning.git
```

### 2. Copy files to your Hexo project

Place the files into your Hexo blog project with the following structure:

```
your-hexo-blog/
├── source/
│   ├── js/
│   │   └── tts-learning.js
│   ├── css/
│   │   ├── tts-learning-bright.css
│   │   └── tts-learning-dark.css
├── scripts/
│   └── tts-learning-plugin.js
```

- Copy `js/tts-learning.js` to `source/js/`
- Copy `css/tts-learning-bright.css` and `css/tts-learning-dark.css` to `source/css/`
- Copy `tts-learning-plugin.js` to `scripts/`

**Note:** Ensure that if the `source/js/` or `source/css/` is existing in your Hexo project, please copy the files into those directories instead of covering them.

## Usage

### 1. Inject assets

The plugin automatically injects the necessary JS and CSS files into your HTML output.  
No need to manually edit your theme files.

### 2. Add TTS Learning Cards in your posts

You can use either of these two tag formats in your Markdown posts:

#### **A. Key-Value Tag Format**

```markdown
{% tts_learning sentence="Hello, how are you?" translation="你好，你今天過得如何？" note="Common greeting in English." language="en-US" %}
```

- `sentence`: The main sentence to be practiced.
- `translation`: The translation to display.
- `note`: Additional notes (optional).
- `language`: TTS language code (optional, default is `en-US`).

#### **B. Positional Tag Format**

```markdown
{% tts_learning "Bonjour tout le monde" "Hello everyone" "French greeting" "fr-FR" %}
```

Order:

1. Sentence
2. Translation
3. Note (optional)
4. Language (optional)

**Tips:**

- Always use quotes around parameters if they contain spaces.
- You may omit `note` and `language` if not needed.

## Features

- **Text-to-Speech:** Speak entire sentences or individual words by clicking.
- **Recording:** Record your own pronunciation and play it back for comparison.
- **Theme Support:** Automatically uses bright or dark CSS depending on your blog's style or preference.
- **Debug Mode:** Enable detailed logging for troubleshooting.

## Configuration

You can enable debug mode or force dark mode by editing your Hexo `_config.yml`:

```yaml
tts_learning:
  darkmode: true # Force dark theme (optional)
  debug: true # Enable debug logs (optional)
```

## Contributing

If you want to contribute to this project, feel free to fork the repository and submit a pull request.

## License

This plugin is released under the GNU General Public License.  
See `LICENSE` for details.

## Author

Created by [Rduanchen](https://github.com/Rduanchen).  
Email: [chenyouduan@gmail.com](mailto:chenyouduan@gmail.com)

# Hexo TTS Learning 插件

<img width="817" height="451" alt="image" src="https://github.com/user-attachments/assets/a2c4fedc-c3b1-4d64-8948-f39fbae310b1" />

[範例](https://rduanchen.github.io/language_learning/)

### 📚 目的

Hexo TTS Learning 是一個為 Hexo 部落格平台設計的外掛，能夠在文章中加入互動式語言學習卡片。每張卡片提供以下功能：

- 使用文字轉語音（TTS）播放句子或單字

- 錄製並回放自己的發音

- 顯示翻譯與備註

- 支援亮／暗主題切換

此外掛特別適合語言學習部落格、發音練習，或任何需要音訊回饋與互動的教育內容。

### ⚙️ 安裝方式（手動）

**注意**： 此外掛採用「手動安裝」方式。
你必須將提供的檔案複製到 Hexo 專案中對應的資料夾。

步驟一：下載或 clone 此儲存庫  
你可以使用以下指令

```bash
git clone https://github.com/<yourusername>/hexo-tts-learning.git
```

或者直接下載檔案。

步驟二：將檔案複製至 Hexo 專案中
請依照以下結構放置檔案：

```bash
your-hexo-blog/
├── source/
│ ├── js/
│ │ └── tts-learning.js
│ ├── css/
│ │ ├── tts-learning-bright.css
│ │ └── tts-learning-dark.css
├── scripts/
│ └── tts-learning-plugin.js
```

將 `js/tts-learning.js` 複製到 `source/js/`

將 `css/tts-learning-bright.css` 和 `css/tts-learning-dark.css` 複製到 `source/css/`

將 `tts-learning-plugin.js` 複製到 `scripts/`

**注意**： 如果你的 Hexo 專案已經有 `source/js/` 或 `source/css/` 資料夾，請不要覆蓋，而是將檔案新增進去。

### 🧪 使用方式

1. 自動引入資源
   此外掛會自動將所需的 JS 和 CSS 檔案插入到輸出的 HTML 中，無需手動修改佈景主題的檔案。

2. 在文章中加入語言學習卡片
   你可以在 Markdown 文章中使用以下任一種語法：

A. 鍵值格式語法

```markdown
{% tts_learning sentence="Hello, how are you?" translation="你好，你今天過得如何？" note="英文常見問候語。" language="en-US" %}
`sentence`: 要練習的主句
`translation`: 要顯示的翻譯
`note`: 額外備註（可選）
`language`: TTS 語言代碼（可選，預設為 en-US）
```

B. 位置參數格式

```markdown
{% tts_learning "Bonjour tout le monde" "Hello everyone" "法文問候語" "fr-FR" %}
```

順序為：

1. 句子
2. 翻譯
3. 備註（可選）
4. 語言代碼（可選）

小提醒：

> 若參數中包含空格，請務必加上引號
> 如果不需要備註與語言代碼，可以省略最後兩項

### ✨ 功能特色

- 文字轉語音（TTS）： 可點擊播放整句或單字
- 錄音功能： 可錄下自己的發音並播放比對
- 主題支援： 自動依部落格風格切換亮／暗主題
- 除錯模式： 可啟用詳細日誌，便於問題排查

### 🔧 設定方式

可在 Hexo 的 \_config.yml 中啟用除錯模式或強制使用暗色主題：

```yaml
tts_learning:
  darkmode: true # 強制使用暗色主題（可選）
  debug: true # 啟用除錯日誌（可選）
```

### 🤝 貢獻開發

如果你有興趣參與本專案，歡迎 fork 此儲存庫並提交 pull request！

### 📄 授權條款

本外掛使用 GNU 通用公共授權（GPL）發佈。
詳情請見 LICENSE 檔案。

### 👤 作者

由 Rduanchen 開發
電子信箱：chenyouduan@gmail.com
