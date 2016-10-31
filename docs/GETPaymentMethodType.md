
# GETPaymentMethodType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cardHolderInfo** | [**GETPaymentMethodTypeCardHolderInfo**](GETPaymentMethodTypeCardHolderInfo.md) |  |  [optional]
**cardNumber** | **String** | Credit or debit card number, 16 characters or less, masked for security purposes.  |  [optional]
**cardType** | **String** | The type of credit card or debit card being billed.  Possible values are: &#x60;Visa&#x60;, &#x60;MasterCard&#x60;, &#x60;AmericanExpress&#x60;, &#x60;Discover&#x60;.  |  [optional]
**defaultPaymentMethod** | **Boolean** | Contains true if this is the default payment method for this customer, otherwise false.  |  [optional]
**expirationMonth** | **String** | Two-digit expiration month (01 - 12).  |  [optional]
**expirationYear** | **String** | Four-digit expiration year.  |  [optional]
**id** | **String** | Unique ID generated by Zuora when this payment method was created.  |  [optional]


