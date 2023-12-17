# Typecho Plugin Template

This is a template for developing Typecho plugins.

[中文说明](README.zh-CN.md)

## How to Use

Click the "Use this template" button to create a new repository from this template.

## Suggested Directory Structure

```
LICENSE
README.md
/plugin
    ├── Plugin.php
    ├── ...
```

All source code should be placed in the `/plugin` directory.

## Plugin.php

The `Plugin.php` file is the main file of the plugin. It should contain a class named `Plugin` which implements the `Typecho\Plugin\PluginInterface` interface.

```php

namespace TypechoPlugin\Example;

use Typecho\Plugin\PluginInterface;

/**
 * Example plugin.
 *
 * @package Example
 * @author Typecho
 * @version %version%
 * @link https://typecho.org
 */
class Plugin implements PluginInterface
{
    // Methods to implement the PluginInterface.
}
```

Important notes:

- The namespace of the plugin should be `TypechoPlugin\{PluginName}`. For example, if the plugin name is `Example`, the namespace should be `TypechoPlugin\Example`. This is required for the plugin to be loaded by Typecho.
- The version of the plugin should be replaced with `%version%`. The version number will be replaced by the build script automatically. **Do not** replace the version number manually.

## Release Steps

Create a release on GitHub and name a tag with the version number. For example, if the version number is `1.0.0`, the tag name should be `1.0.0`.

The build script will automatically create a zip file for the release and upload it to the release page.