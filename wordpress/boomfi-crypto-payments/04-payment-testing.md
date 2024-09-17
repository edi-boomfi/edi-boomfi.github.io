# Payment Testing

In this section we will be simulating an action done by a customer and later on checking the order in WooCommerce and BoomFi merchant portal to track transaction

## Checkout flow as Customer

1. Open the WordPress shop section
   1. click "Add to Cart" on the "Dummy Product" listing
   2. Click "View Cart"
   3. Click "Proceed to Checkout"

   ![Dummy Listing](images/wordpress-05.png)

   ![View Cart](images/wordpress-06.png)

2. Fill in Payment Details then click "Place Order", make sure "BoomFi Crypto Payments" is selected as the payment option

   ![Fill Checkout](images/wordpress-07.png)

3. In the BoomFi checkout page, fill in customer name and email address then click "Continue"

   ![Checkout 1](images/checkout-01.png)

4. Then following steps

   1. Select "wallet Transfer"
   2. Chose "Polygon"
   3. Chose "USDT"
   4. Tick "Enable Test Mode" to simulate payment.
   5. Click Reveal payment details

   ![Checkout 2](images/checkout-02.png)

   After Selecting "Wallet Transfer"

   ![Checkout 2](images/checkout-03.png)

5. Wait until payment completed

   ![Payment Completed](images/checkout-04.png)

6. Finally user will be redirected back to the original WordPress eCommerce site

   ![Payment Completed](images/checkout-05.png)

## Verifying payment as Merchant

1. Login to [BoomFi Test](https://test.boomfi.xyz) using the email used previously when signing up as a new merchant. You will see all the transactions there

   ![BoomFi Transactions List](images/checkout-06.png)

2. Login to WordPress as admin, then click "Orders" on WooCommerce section

   ![WordPress Transactions List](images/checkout-07.png)
