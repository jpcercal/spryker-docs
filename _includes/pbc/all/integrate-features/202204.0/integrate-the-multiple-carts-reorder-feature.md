

## Install feature core

### Prerequisites

To start feature integration, overview and install the necessary features:

| NAME | VERSION |
| --- | --- |
| Multiple Carts | {{site.version}} |
| Reorder | {{site.version}} |
| Spryker Core | {{site.version}} |

### 1) Set up behavior

Register the following plugins:

| PLUGIN | SPECIFICATION | PREREQUISITES | NAMESPACE |
| --- | --- | --- | --- |
| ReorderPersistentCartChangeExpanderPlugin | Adds a default reorder name and adds it to add item request. | 1 | Spryker\Client\MultiCart\Plugin |

**src/Pyz/Client/PersistentCart/PersistentCartDependencyProvider.php**

```php
<?php

namespace Pyz\Client\PersistentCart;

use Spryker\Client\MultiCart\Plugin\ReorderPersistentCartChangeExpanderPlugin;
use Spryker\Client\PersistentCart\PersistentCartDependencyProvider as SprykerPersistentCartDependencyProvider;

class PersistentCartDependencyProvider extends SprykerPersistentCartDependencyProvider
{
 /**
 * @return \Spryker\Client\PersistentCartExtension\Dependency\Plugin\PersistentCartChangeExpanderPluginInterface[]
 */
 protected function getChangeRequestExtendPlugins(): array
 {
 return [
 new ReorderPersistentCartChangeExpanderPlugin(),
 ];
 }
}
```

{% info_block warningBox "Verification" %}

When using the reorder feature, a new customer quote must be created with the name "Cart from order {Order reference}".

{% endinfo_block %}
