# wp-woo-pre-orders

Pre-orders for WooCommerce with a release date, message and quantity limit.

A companion to [wp-woo-idempotent-importer](https://github.com/JamesonRGrieve/wp-woo-idempotent-importer):
the importer mirrors stores from Shopify, BigCommerce, Squarespace, Wix, Magento, Lightspeed, Ecwid, Etsy and
Square into WooCommerce, and must enforce everything the source store enforced. Where WooCommerce can't hold
a concern natively, a companion plugin like this one holds it, one plugin per concern.

## Scope

- Pre-order availability with a release date and message, and a quantity limit.
- Payment taken upfront or on release.
- Orders stay marked as pre-orders until release.

## Contract

- A stable data model and a PHP API the importer writes into idempotently: an unchanged source causes zero
  writes.
- Usable on its own as a WooCommerce plugin, with an admin UI to view and edit its records.
- Requires WooCommerce; it does nothing until they are active.

## Status

Scaffold: the plugin boots, checks its required plugins and runs the full quality gate. The features above
are tracked on its Deck card (http://192.168.1.12/index.php/apps/deck/board/3/card/397).

## Development

```
composer install   # also wires the pre-commit hook
composer check     # lint, format, PHPStan max, unit tests, audit, validate
```

## License

AGPL-3.0-or-later.
