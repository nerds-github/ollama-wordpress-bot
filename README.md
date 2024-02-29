# Alpaca Bot

<div align="center">
  
### 🌟 A privately hosted WordPress AI agent.💡
  
  <img src="https://alpaca.bot/wp-content/uploads/2024/02/alpaca-bot-icon-1006.png" alt="Alpaca Bot" width="256px">

  [![Discord](https://img.shields.io/discord/485971823821979648?logo=discord&label=Discord&color=72edad)](https://discord.gg/vWQTHphkVt)
  ![GitHub release (latest by date)](https://img.shields.io/github/v/release/carmelosantana/alpaca-bot?label=Latest%20Release&color=668bf2)
  <a href="https://demo.alpaca.bot/">
    <img src="https://img.shields.io/badge/Live-Demo-ed72b1" alt="Alpaca Demo">
  </a>
  <a href="https://www.patreon.com/carmelosantana">
    <img src="https://img.shields.io/badge/Subscribe-Become%20a%20Patreon-826EB4?logo=patreon" alt="Patreon">
  </a>
</div>

WordPress plugin for quick content creation and code completion! Use `[agent]` to retrieve remote content, summarize webpages and more!

---

- [Requirements](#requirements)
- [Installation](#installation)
- [Setup](#setup)
- [Features](#features)
- [Usage](#usage)
  - [Text Completion](#text-completion)
  - [Agents](#agents)
    - [Example](#example)
- [Shortcodes](#shortcodes)
  - [💬 `[alpaca]` - Chat with Alpaca Bot](#-alpaca---chat-with-alpaca-bot)
    - [Attributes](#attributes)
  - [👥 `[agent]` - Execute tasks on your behalf](#-agent---execute-tasks-on-your-behalf)
    - [Attributes](#attributes-1)
  - [Caching](#caching)
    - [Transient](#transient)
    - [Post Meta](#post-meta)
    - [Option](#option)
    - [Disable](#disable)
- [Core Agents](#core-agents)
  - [`get`](#get)
    - [Attributes](#attributes-2)
  - [`summarize`](#summarize)
    - [Attributes](#attributes-3)
- [Support](#support)
- [Funding](#funding)
- [Made Possible By](#made-possible-by)
- [License](#license)

---

## Requirements

- Access to [Ollama](https://github.com/ollama/ollama) v0.1.24 or later.
- PHP `^8.1`
- WordPress `^6.4`
  - Permalinks enabled

## Installation

1. Download the latest release from the [releases page](https://github.com/carmelosantana/alpaca-bot/releases).
2. Upload the plugin to your WordPress site.
3. Activate the plugin.

## Setup

1. Setup your [Ollama](https://github.com/ollama/ollama) instance in one of the following ways:
   - Install [Ollama](https://github.com/ollama/ollama) on your localhost or server.
   - ⭐️ **[Become a Patreon](https://www.patreon.com/carmelosantana)** and subscribe to [Alpaca Bot](https://alpaca.bot/) for premium API features and share our community hosted Ollama instances.
2. Add your [Ollama](https://github.com/ollama/ollama) API URL to the settings page by navigating to `Alpaca Bot > Settings` in your WordPress admin dashboard.
3. Enter your [Ollama](https://github.com/ollama/ollama) API URL.
   - Add your [Alpaca Bot](https://app.alpaca.bot/) Username and API Application Password if you are using our hosted service.
4. Click `Save Changes`.

> [Patreon subscriptions](#support) include support via Discord as well! 🎉

## Features

- Store conversation history **privately** in your `wp_` database.
- Use `[agent]` to execute tasks on your behalf.
- Chat with dozens of pre-trained LLMs or train your own.
- Switch conversational model on the fly.

## Usage

### Text Completion

You have two options to communicate with your AI models;

1. Click **Alpaca Bot** found in the admin menu, below Dashboard and above Posts.
2. **Use the shortcode** `[alpaca]` to generate a response within any post or page.

### Agents

Use the `[agent]` shortcode to execute tasks on your behalf. Agents are a powerful way to empower your AI models to perform tasks on your behalf.

For example, you can use the `[agent]` shortcode to retrieve content from a remote source. `[agent]`s can interact directly with your models and help summarize a webpage or rewrite content.

#### Example

Basic webpage summarization:

```html
[agent name=summarize model=tinyllama url=https://example.com/]
```

## Shortcodes

### 💬 `[alpaca]` - Chat with Alpaca Bot

*Chat with Alpaca Bot from any post or page.*

#### Attributes

- `model` - The model to use for the text generation. *(optional)*
- `system` - Specifies the [system message](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#system) that will be set in the template. *(optional)*

### 👥 `[agent]` - Execute tasks on your behalf

*Execute tasks via Agents.*

#### Attributes

Agents can support a wide rang of attributes. The following are core attributes that are supported by all agents.

- `name` - The agent to execute.
- `model` - The model to use for the text generation. *(optional)*

### Caching

Requests can be cached by setting the `cache` attribute. `cache` supports short and long term options.

By default responses are cached to the current post or page.

#### Transient

Numeric values are treated as seconds and will cache the response for the specified duration.

- `cache=60` - Cache the response for 60 seconds.
- `cache=3600` - Cache the response for 1 hour.

#### Post Meta

This is useful for caching responses permanently and associating them with a specific post or page.

- `cache=postmeta` - Cache to current post or page.

#### Option

Use WordPress option storage to cache permanently but not associated with a specific post or page.

This can be useful for sharing responses across multiple pages.

- `cache=option` - Cache to WordPress options.

#### Disable

The following values can all disable caching. Pick one or use them interchangeably. 🙂

- `cache=0` - Disable caching.
- `cache=false` - Disable caching.
- `cache=none` - Disable caching.
- `cache=off` - Disable caching.

## Core Agents

The following are core agents that are provided by the **Alpaca Bot** plugin.

### `get`

Retrieve content from a remote source.

#### Attributes

- `url` - The URL to retrieve content from.

### `summarize`

Summarize remote content.

#### Attributes

- `url` - The URL to summarize.
- `length` - Describe the length of the summary.
- `content` - The type of content we want to summarize.

## Support

If you need help or have questions, please join our [Discord](https://discord.gg/vWQTHphkVt) community.

Premium support and video calls are available to our [Patreon](https://www.patreon.com/carmelosantana) subscribers. We can help  setup your [Ollama](https://github.com/ollama/ollama) instance, troubleshoot issues, demonstrate shortcode functionality and more.

Patreon's also receive;

- Access to our hosted [Ollama](https:/github.com/ollama/ollama) instances.
- Priority feature requests.
- Early access to new features and releases.

Please consider [becoming a Patreon](https://www.patreon.com/carmelosantana) today!

## Funding

If you find this project useful or use it in a commercial environment please consider donating today with one of the following options.

- Bitcoin `bc1qhxu9yf9g5jkazy6h4ux6c2apakfr90g2rkwu45`
- Ethereum `0x9f5D6dd018758891668BF2AC547D38515140460f`
- Patreon [`patreon.com/carmelosantana`](https://www.patreon.com/carmelosantana)

## Made Possible By

- [Ollama](https://github.com/ollama/ollama) and the research behind these great open source [Large Language Models](https://ollama.ai/library) (LLMs).
- [Emma Delaney](https://emma-delaney.medium.com/how-to-create-your-own-chatgpt-in-html-css-and-javascript-78e32b70b4be) *How to Create Your Own ChatGPT in HTML CSS and JavaScript*
- [Hint.css](https://github.com/chinchang/hint.css) A CSS only tooltip library for your lovely websites.

## License

- The code is licensed [GNU General Public License version 2](http://www.gnu.org/licenses/gpl-2.0.html) or later.
- The documentation is licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
