# Siteation - Hyva Icon Pack - Flags

[![Packagist Version](https://img.shields.io/packagist/v/siteation/magento2-hyva-icons-flags?style=for-the-badge)](https://packagist.org/packages/siteation/magento2-hyva-icons-flags)
![Supported Magento Versions](https://img.shields.io/badge/magento-%202.4-brightgreen.svg?logo=magento&longCache=true&style=for-the-badge)
[![Hyva Themes Module](https://img.shields.io/badge/Hyva_Themes-Module-3df0af.svg?longCache=true&style=for-the-badge)](https://hyva.io/)
![License](https://img.shields.io/github/license/siteation/magento2-hyva-icons-flags?color=%23234&style=for-the-badge)

This Magento 2 module adds the option to use [Flagpack](https://flagpack.xyz/) in your Hyvä frontend.

This requires that you have a working Hyvä frontend,
this icon pack was made specifically for Hyvä Themes and will not work out of the box with any other frontend.

## Installation

Install the package via;

```bash
composer require siteation/magento2-hyva-icons-flags
bin/magento setup:upgrade
```

> **Warning** This Module requires Magento 2.4 or higher and requires Hyvä!
> For more requirements see the `composer.json`.

## How to use

By default this module loads nothing.

To use this icon pack instead of the default Hyvä icons, add the following to your phtml file;

```php
<?php
use Hyva\Theme\Model\ViewModelRegistry;
use Siteation\HyvaIconsFlags\ViewModel\FlagsIcons;

/** @var ViewModelRegistry $viewModels */

/** @var FlagsIcons $flagsIcons */
$flagsIcons = $viewModels->require(FlagsIcons::class);
```

and use the FlagsIcons just as the HeroIcons in Hyvä;

```php
<?= $flagsIcons->nlHtml('p-1', 24, 24, ["aria-label" => "Netherlands"]) ?>
```

### Using SVG icons in CMS content

You can now also use the SVG icons in your CMS content.

Bringing svg icon support to you CMS pages, Blocks and Widgets.

```txt
{{icon "flags/nl"}}
```

[For more information on how and what see the Hyvä Docs](https://docs.hyva.io/hyva-themes/writing-code/working-with-view-models/svgicons.html#using-svg-icons-in-cms-content)

> This feature is supported since Hyvä v1.1.12

## Other icon packs for Hyvä

- Hero Icons (Default for Hyvä)
- [Lucide Icons](https://github.com/Siteation/magento2-hyva-icons-lucide)
- [Feather Icons](https://github.com/Siteation/magento2-hyva-icons-feather)
- [Bootstrap Icons](https://github.com/Siteation/magento2-hyva-icons-bootstrap)
- [Siteation Payment Icons](https://github.com/Siteation/magento2-hyva-icons-payment)
- [Hyvä Payment Icons](https://gitlab.hyva.io/hyva-themes/magento2-payment-icons) (Requires Hyvä Gitlab or License to access)
- [Font Awesome 5 Icons](https://github.com/JaJuMa-GmbH/awesome-hyva)

_If you are looking for a Luma based option [checkout this icon pack instead](https://github.com/GrimLink/magento2-icon-packs)._

## Icon License

[Flagpack](https://flagpack.xyz/) used in this module were created by [Yummygum](https://yummygum.com/) under a [MIT License, found here](https://github.com/Yummygum/flagpack-core/blob/main/LICENSE)

