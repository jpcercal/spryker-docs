---
title: Product Barcode feature overview
description: The Barcode Generator can be used for any kind of entity, and by default, we provide a solution for products.
last_updated: Jul 23, 2021
template: concept-topic-template
originalLink: https://documentation.spryker.com/2021080/docs/product-barcode-feature-overview
originalArticleId: 6d6d1bee-375f-4767-a866-a7d6f28eeaa1
redirect_from:
  - /2021080/docs/product-barcode-feature-overview
  - /2021080/docs/en/product-barcode-feature-overview
  - /docs/product-barcode-feature-overview
  - /docs/en/product-barcode-feature-overview
  - /docs/scos/user/features/202200.0/product-barcode-feature-overview.html
---

The *Product Barcode* feature lets you create barcodes for any kind of entity. By default, barcodes are only generated for [products](/docs/scos/user/features/{{page.version}}/product-feature-overview/product-feature-overview.html).

## What is a barcode?

A barcode is a square or rectangular image consisting of a series of parallel black lines (bars) and white spaces of varying widths that can be read by a scanner and printed. Barcodes are applied to entities as a means of quick identification.
![Barcode example](https://spryker.s3.eu-central-1.amazonaws.com/docs/Features/Product+Management/Barcode+Generator/Barcode+Generator+Feature+Overview/barcode.png)

By default, barcodes are generated based on product SKUs using the [Code128](https://en.wikipedia.org/wiki/Code_128) format.

{% info_block infoBox %}

You can read more about the product types we differentiate in [Product Abstraction](/docs/scos/user/features/{{page.version}}/product-feature-overview/product-feature-overview.html).

{% endinfo_block %}

{% info_block errorBox %}

In your project, you can also implement the QR code functionality by creating similar plugins.

{% endinfo_block %}

Barcodes are dynamically generated for concrete products, which ensures that barcodes are immediately valid.

The feature also has plugin support to change the way the barcodes are generated. It includes support for different barcode formats.

The barcodes help a store administrator update product stock numbers according to the actual information provided by the warehouse.

Creating barcodes requires two main prerequisites:

1. *Unique product codes for each product you offer*. These can be UPC codes that identify manufactured goods, unique SKU numbers that you use to track inventory your way, or other identifying numbers.
2. *A system that lets you input codes to create barcodes*. Your codes need to be entered into a device or software system that can translate the numeric or alphanumeric code into a scannable barcode.

Nowadays, B2B businesses face extraordinary challenges as more and more consumers are making comparisons of various ecommerce applications. To stay on top of the industry trends, improve customer experience and increase sales, every business must innovate with a deep understanding of their customer’s physical, emotional, and financial needs and triggers.

Barcodes are often overlooked as a way to cut costs and save time. A valuable and viable choice for businesses looking to improve efficiency and reduce overhead, barcodes are both cost-effective and reliable. Both inexpensive and user-friendly, barcodes provide an indispensable tool for tracking a variety of data, from pricing to inventory. The ultimate result of a comprehensive barcoding system is a reduction in overhead.

The Barcode Generator can be used for any kind of entity, and by default, Spryker provides a solution for products.

**What is a barcode?**
<br>A *barcode* is a square or rectangular image consisting of a series of parallel black lines (bars) and white spaces of varying widths that can be read by a scanner and printed. Barcodes are applied to entities as a means of quick identification.

In the default configuration, barcodes are generated based on the SKU of a concrete product using the Code128 format. Though, Spryker provides highly customizable solutions through plugins with the help of which the setup can be changed.

Barcodes are dynamically generated for concrete products. This ensures that barcodes are immediately valid.

You can see the barcodes in the Back Office, in the **Catalog&nbsp;<span aria-label="and then">></span> Product Barcodes** section. The section is designed as a review; thus, no actual actions are performed here. The barcode is generated automatically once a new concrete product is added.

You can see the Product ID, product name, SKU, and the barcode itself.

## Related Business User articles

|BACK OFFICE USER GUIDES|
|---|
| [Viewing product barcodes](/docs/scos/user/back-office-user-guides/{{page.version}}/catalog/product-barcodes/viewing-product-barcodes.html)  |

{% info_block warningBox "Developer guides" %}

Are you a developer? See [Product Barcodes feature walkthrough](/docs/scos/dev/feature-walkthroughs/{{page.version}}/product-barcode-feature-walkthrough.html) for developers.

{% endinfo_block %}
