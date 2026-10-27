<div align="center">

# CigalPay

**Crypto payments for your app, SaaS or website.**
Price in USD or EUR, let your customers pay in BTC, ETH, USDT, SOL and more, and get notified the moment it's paid.

[Website](https://cigalpay.com) · [Developer docs](https://cigalpay.com/developers) · [Create an account](https://merchant.cigalpay.com/signup)

</div>

## Official SDKs and plugins

| For | Install | Package | Source |
| --- | --- | --- | --- |
| Node.js 18+ | `npm install cigalpay-js-sdk` | [npm](https://www.npmjs.com/package/cigalpay-js-sdk) | [cigalpay-js-sdk](https://github.com/cigalpay/cigalpay-js-sdk) |
| PHP 7.4+ | `composer require cigalpay/cigalpay-php-sdk` | [Packagist](https://packagist.org/packages/cigalpay/cigalpay-php-sdk) | [cigalpay-php-sdk](https://github.com/cigalpay/cigalpay-php-sdk) |
| WooCommerce 8+ | Upload the zip in **Plugins → Add New Plugin** | [Download](https://github.com/cigalpay/cigalpay-woocommerce/releases/latest/download/cigalpay-for-woocommerce.zip) | [cigalpay-woocommerce](https://github.com/cigalpay/cigalpay-woocommerce) |

## Accept a payment in a few lines

```js
import CigalPay from 'cigalpay-js-sdk';

const cigalpay = new CigalPay({ accountId: process.env.CIGALPAY_ACCOUNT_ID });

const { chargeLink } = await cigalpay.createCheckout({
  amount: 49.9,
  currency: 'USD',
  orderId: '1042',
  description: 'Pro plan - 1 month',
  returnUrl: 'https://example.com/thanks',
  notifyUrl: 'https://example.com/cigalpay/webhook',
});
// send the customer to chargeLink
```

Payment updates reach your `notifyUrl` signed with HMAC-SHA512. Check them with `CigalPay.verifyWebhook()`. See [Verify notifications](https://cigalpay.com/developers#verify-notifications).

## Why CigalPay

- **Hosted checkout:** your customer picks the coin, and the amount stays locked in USD or EUR.
- **Many coins:** BTC, ETH, USDT, SOL, LTC, DOGE, BCH, MATIC and more.
- **Signed notifications:** know when an order is paid, with no polling.
- **REST APIs with OpenAPI 3.1 specs:** [Core API](https://core-api.cigalpay.com/docs) and [Coins API](https://coins-api.cigalpay.com/docs).

## Follow us

[YouTube](https://www.youtube.com/@cigalpay) · [Telegram](https://t.me/cigalpay) · [Instagram](https://www.instagram.com/cigalpay) · [TikTok](https://www.tiktok.com/@cigalpay) · [Facebook](https://www.facebook.com/cigalpay)

Questions? Email support@cigalpay.com.
