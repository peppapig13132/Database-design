# Gift Card for e-Commerce Project
:label: MySQL

## About Gift Card System
A customer can buy a gift card and send it by specific time with desired amount and text.

A customer who received this gift card can use the card balance only this platform to purchase the products.

The gift card has an expiration date(1 year by default), and can't use out of available date.

A gift card consumer should input the email and the gift card code.

1. _Buy a gift card -> A new gift card created in database -> Send email at receiver_
2. _Buy products with a gift card -> Update the balance of the gift card -> Create a giftcard_log -> Send email at gift card holder with order number, gift card balance, expiration date_

_Supporse `user` table is already defined._

### Model: Giftcard
```
{
  id: number,
  receiver_firstname: string,
  receiver_lastname: string,
  receiver_email: string,
  sender_name: string,
  sender_email: string,
  gift_message: string,
  code: string,
  amount: number,
  balance: number,
  shipping_at: string,
  created_at: string,
  updated_at: string,
  expired_at: string,
}
```

### Model: GiftcardLog
```
{
  id: number,
  giftcard_id: number,
  product_order_id: number,
  status: enum(draft, pending, success, failed, canceled),
  created_at: number,
  updated_at: number,
}
```
