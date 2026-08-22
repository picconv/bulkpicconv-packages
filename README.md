# BulkPicConv — Download Packages

Pre-built packages for all BulkPicConv tools and integrations. Download and use directly — no source code compilation needed.

**[Website](https://www.bulkpicconv.com)** · **[API Docs](https://www.bulkpicconv.com/api-docs)** · **[API Pricing](https://www.bulkpicconv.com/api-pricing)**

## Downloads

| Tool                | Download                                          | Description                                                          |
| ------------------- | ------------------------------------------------- | -------------------------------------------------------------------- |
| 🧩 Chrome Extension | [chrome-extension.zip](dist/chrome-extension.zip) | Right-click to optimize any image. AI alt text & background removal. |
| ⌨️ CLI              | [cli.zip](dist/cli.zip)                           | Command-line batch conversion with glob patterns.                    |
| 🟢 Node.js SDK      | [sdk-node.zip](dist/sdk-node.zip)                 | TypeScript-first Node.js SDK. Zero dependencies.                     |
| 🐍 Python SDK       | [sdk-python.zip](dist/sdk-python.zip)             | Python 3.9+ SDK. No external dependencies.                           |
| 🐘 PHP SDK          | [sdk-php.zip](dist/sdk-php.zip)                   | PHP 8.1+ SDK via Composer.                                           |
| ⚡ Zapier / Make    | [zapier.zip](dist/zapier.zip)                     | No-code automation for 5000+ apps.                                   |
| 📝 WordPress Plugin | [wordpress-plugin.zip](dist/wordpress-plugin.zip) | Auto-convert images on upload. AI alt text.                          |
| 🖼️ Embed Widget     | [embed-widget.zip](dist/embed-widget.zip)         | Embeddable conversion widget for any website.                        |

## Quick Start

### Chrome Extension

1. Download `chrome-extension.zip` and extract
2. Open Chrome → `chrome://extensions` → Enable "Developer mode"
3. Click "Load unpacked" → Select the extracted folder
4. Right-click any image to optimize

### CLI

```bash
# Extract and install
unzip cli.zip && cd cli
npm install -g .

# Convert images
bulkpicconv convert photo.jpg --format webp --quality 80
```

### Node.js SDK

```bash
unzip sdk-node.zip && cd sdk-node
npm install
```

```js
import { BulkPicConv } from './index.js'
const client = new BulkPicConv({ apiKey: 'sk_...' })
await client.convertFile('photo.jpg', 'photo.webp', { quality: 80 })
```

### Python SDK

```bash
unzip sdk-python.zip && cd sdk-python
pip install .
```

```python
from bulkpicconv import BulkPicConv
client = BulkPicConv("sk_...")
client.convert_file("photo.jpg", "photo.webp", {"quality": 80})
```

### PHP SDK

```bash
unzip sdk-php.zip
composer require bulkpicconv/php-sdk
```

```php
$client = new BulkPicConv\Client('sk_...');
$client->convertFile('photo.jpg', 'photo.webp', ['quality' => 80]);
```

### WordPress Plugin

1. Download `wordpress-plugin.zip`
2. WordPress Admin → Plugins → Add New → Upload Plugin
3. Activate and configure in Settings → BulkPicConv

### Embed Widget

```html
<script src="https://www.bulkpicconv.com/sdk/bic-embed.js"></script>
<div id="bic-embed"></div>
<script>
  BulkImageConverter.embed('#bic-embed', { apiKey: 'sk_...' })
</script>
```

### Zapier / Make

1. Download `zapier.zip`
2. Follow [Zapier CLI app setup guide](https://platform.zapier.com/cli_tutorials/getting-started)
3. Or use the provided `index.js` as a reference integration

## API Key

All tools share the same API key. Get yours at [API Pricing](https://www.bulkpicconv.com/api-pricing).

- **Free tier**: 50 conversions/month, no credit card required
- **Pro**: Starts at $9.99/mo with higher limits and AI tools

## License

MIT
