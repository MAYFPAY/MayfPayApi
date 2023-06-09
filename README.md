# MayfPayApi

## MayfPayApi is a Python library for interacting with the MayfPay payment system API. It provides methods for retrieving kassa balances, creating and checking invoices.

## Installation

You can install MayfPayApi using pip:

```python
pip install mayfpayapi
```


## Usage

To use MayfPayApi, you need to create an instance of the MayfPayApi class, passing in your API token, kassa ID, and kassa secret key:


```python
from mayfpayapi import MayfPayApi

api = MayfPayApi(api_token='YOUR_API_TOKEN', kassa_id=1234, kassa_s_key='YOUR_SECRET_KEY')
```


## Get Kassa Balance

To get the balance of your kassa, call the get_kassa_balance method:
```python
balance = api.get_kassa_balance()
print(balance)
```


## Create Invoice

To create an invoice, call the create_invoice method, passing in the amount, order ID, expiry time, payment method, comment and any additional data you wish to attach to the invoice:
```python
invoice = api.create_invoice(
    amount=10.0,
    order_id='ORDER123',
    expire_invoice=3600,
    payment_method='card',
    comment='Test Invoice',
    data={'customer': 'John Doe'}
)
print(invoice)
```


## Check Invoice

To check the status of an invoice, call the check_invoice method, passing in the order ID:
```python
status = api.check_invoice('ORDER123')
print(status)
```



## Contributing

Contributions are welcome! Please feel free to submit a pull request.

## License
### MayfPayApi is released under the MIT License. See LICENSE for more information.
