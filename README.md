# Accessibility Assistant Plugin

A Shopware 6.7 plugin that integrates the Accesstive Assistant Widget into your storefront to enhance website accessibility for all users.

## Overview

The Accessibility Assistant plugin seamlessly integrates the Accesstive Assistant Widget into your Shopware storefront. This widget provides accessibility features that help users with disabilities navigate and interact with your website more effectively.

## Features

- **Easy Integration**: Simple one-click activation through the Shopware administration panel
- **Configurable**: Enable or disable the widget through the plugin configuration
- **Non-Intrusive**: Lightweight implementation that doesn't affect your storefront's performance
- **Token-Based**: Secure integration using Accesstive's token-based authentication system

## Requirements

- Shopware 6.7.0 or higher
- PHP 8.1 or higher

## Installation

### Via Composer (Recommended)

1. Add the plugin to your `composer.json`:
```bash
composer require accesstive/shopware-accesstive
```

2. Refresh the plugin list:
```bash
bin/console plugin:refresh
```

3. Install and activate the plugin:
```bash
bin/console plugin:install --activate ShopwareAccesstive
```

## Configuration

1. Navigate to **Settings** → **System** → **Plugins** in your Shopware administration
2. Find **Accessibility Assistant** in the plugin list
3. Click on the plugin to open its configuration
4. Enable the **"Enable Accesstive"** option
5. You can also use the Accesstive through token if you have.
5. Save the configuration

The Accesstive Assistant widget will now be loaded on your storefront pages.

## Troubleshooting

### Widget Not Appearing

1. **Check Configuration**: Ensure the "Enable Accesstive" option is enabled in the plugin settings
2. **Clear Cache**: Clear the Shopware cache:
   ```bash
   bin/console cache:clear
   ```
3. **Check Browser Console**: Open your browser's developer console to check for any JavaScript errors
4. **Verify Token**: Ensure the Accesstive token in the template is valid

### Cache Issues

If changes aren't appearing, try:
```bash
bin/console cache:clear
bin/console plugin:refresh
```

## Uninstallation

To uninstall the plugin:

```bash
bin/console plugin:deactivate ShopwareAccesstive
bin/console plugin:uninstall ShopwareAccesstive
```

Or using DDEV:
```bash
ddev exec bin/console plugin:deactivate ShopwareAccesstive
ddev exec bin/console plugin:uninstall ShopwareAccesstive
```

## Support

For support and documentation, visit: https://accesstive.com

## License

GPL-2.0-or-later
