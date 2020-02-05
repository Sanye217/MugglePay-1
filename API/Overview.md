# API Overview

MugglePay expands your payment options by accepting instant payments of cryptocurrencies, including USDT, EOS, BTC, BCH, LTC and etc, without price fluctuations and chargeback risks.
We provide a reliable payments solution that helps both you and your customers: safe, convenient and customer oriented.

The MugglePay framework is demonstrated as follows:

![]()
<img src="http://dcdn.mugglepay.com/dt/pay/api.002.jpeg" width="500px"/>

## Get started

You can accept payments today on MugglePay in an easy way. MugglePay is a pre-built payment page and complete checkout experience that can be branded for your business. Integrate once, gain new features as MugglePay evolves.

Use the following steps to create a Checkout page that lets a customer make a one-time payment or subscribe to recurring payment plans:
 * Register and Get API Key
 * Integrate with MugglePay Checkout on your website.
 * Integration test for MugglePay.

### Step 1. Register and Get API Key
Register your MugglePay merchant accounts with your invitation code and get your API key at [Merchants Portal](https://merchants.mugglepay.com/). 

<img src="http://dcdn.mugglepay.com/dt/pay/docs/mp-login.png" width="300px"/>


You will find your API Auth Token (API key) for authentication. [MORE](https://mugglepay.docs.stoplight.io/api-overview/authentication)

<img src="http://dcdn.mugglepay.com/dt/pay/docs/mp-apikey.png" width="300px"/>




### Step 2. Integrate MugglePay Checkout with your website

#### 2.1 Add the Button
To integrate Checkout on your website, you need to add a payment button first. Some images options can be found 
<br/>
<img src="http://dcdn.mugglepay.com/dt/pay/button/mpay-en.png" width="100px"/>
<img src="http://dcdn.mugglepay.com/dt/pay/button/mpay-zh.png" width="100px"/>
<img src="http://dcdn.mugglepay.com/dt/pay/button/mpay-icon.png" width="33px"/>
<img src="http://dcdn.mugglepay.com/dt/pay/button/mpay-en-black.png" width="100px"/>

<br/>

<img src="http://dcdn.mugglepay.com/dt/pay/docs/mp-checkout2.png" width="400px"/>

#### 2.2 Send Request to Create Order

The button should trigger [Create Order](https://mugglepay.docs.stoplight.io/payment-api/create-order) a request with purchase order information. It tells us the price amount, description, and merchant ID generated by your service.

<img src="http://dcdn.mugglepay.com/dt/pay/docs/mp-create.png" width="500px"/>

#### 2.3 Redirect user to Payment Page

After the Create Order succeeds, you should redirect the customer to MugglePay payment_url URL and redirects the customer to Crypto Payment page, which contains the purchase order information provided by [Create Order](https://mugglepay.docs.stoplight.io/payment-api/create-order).

<img src="http://dcdn.mugglepay.com/dt/pay/docs/mp-payment.png" width="300px"/>


#### 2.4 Payment Callback (Webhook)

When your customer successfully completes their payment, they are redirected to the success URL that you specified. Typically, this is a page on your website that informs the customer that their payment was successful. The cancel URL is the page where Checkout redirects customers when they cancel the payment process.



Once payment is successful, you should fulfill the customer’s purchase. You can use [Payment Callback](https://mugglepay.docs.stoplight.io/api-overview/payment-callback) webhooks to fulfill the purchase when callback event triggers.


### Step 3. Integration test

Once the integration has been completed, there will then be testing from our team to ensure it's functionality. If all checks pass, it will be ready to go.

All the transactions of orders and withdraws can be viewed in the [Merchants Portal](https://merchants.mugglepay.com/). 

<img src="http://dcdn.mugglepay.com/dt/pay/docs/mp-admin.png" width="500px"/>