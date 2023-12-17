# Typecho Plugin Template

这是一个用于开发 Typecho 插件的模板。

[English](README.md)

## 如何使用

点击 "Use this template" 按钮，从这个模板创建一个新的仓库。

## 建议的目录结构

```
LICENSE
README.md
/plugin
    ├── Plugin.php
    ├── ...
```

所有源代码应该放在 `/plugin` 目录下。

## Plugin.php

`Plugin.php` 文件是插件的主文件。它应该包含一个名为 `Plugin` 的类，该类实现了 `Typecho\Plugin\PluginInterface` 接口。

```php

namespace TypechoPlugin\Example;

use Typecho\Plugin\PluginInterface;

/**
 * 示例插件。
 *
 * @package Example
 * @author Typecho
 * @version %version%
 * @link https://typecho.org
 */
class Plugin implements PluginInterface
{
    // 实现 PluginInterface 的方法。
}
```

重要提示：

- 插件的命名空间应该是 `TypechoPlugin\{PluginName}`。例如，如果插件名为 `Example`，命名空间应该是 `TypechoPlugin\Example`。这是 Typecho 加载插件所必需的。
- 插件的版本号应该用 `%version%` 替换。版本号将由构建脚本自动替换。**不要**手动替换版本号。

## 发布步骤

在 GitHub 上创建一个发布，将标签命名为版本号。例如，如果版本号为 `1.0.0`，标签名应该是 `1.0.0`。

构建脚本将自动为发布创建一个 zip 文件，并将其上传到发布页面。