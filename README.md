# Hexo TTS Learning Plugin

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
