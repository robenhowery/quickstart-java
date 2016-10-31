
# ProxyGetInvoiceItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accountingCode** | **String** |  The accounting code for the item&#39;s charge. Accounting codes group transactions that contain similar accounting attributes. **Character limit**: 100 **Values**: inherited from &#x60;RatePlanCharge.AccountingCode&#x60;  |  [optional]
**appliedToInvoiceItemId** | **String** |  Associates a discount invoice item to a specific invoice item. **Character limit**: 32 **Values**: inherited from the ID of the charge that a discount applies to  |  [optional]
**chargeAmount** | **Double** |  The amount being charged for the invoice item. This amount doesn&#39;t include taxes regardless if the charge&#39;s tax mode is inclusive or exclusive. **Character limit**: **Values**: automatically calculated from multiple fields in multiple objects  |  [optional]
**chargeDate** | [**DateTime**](DateTime.md) |  The date when the Invoice Item is created . **Character limit**: 29 **Values**: automatically generated  |  [optional]
**chargeName** | **String** |  The name of the invoice item&#39;s charge. **Character limi**t: 50 **Values: **inherited from &#x60;RatePlanCharge.Name&#x60;  |  [optional]
**createdById** | **String** |  The user ID of the person who created the invoice item. **Character limit**: 32 **Values**: automatically generated  |  [optional]
**createdDate** | [**DateTime**](DateTime.md) |  The date the invoice item was created. **Character limit:** 29 **Values**: automatically generated  |  [optional]
**id** | **String** | Object identifier. |  [optional]
**invoiceId** | **String** |  The ID of the invoice that&#39;s associated with this invoice item. **Character limit**: 32 **Values**: inherited from &#x60;Invoice.Id&#x60;  |  [optional]
**processingType** | **Double** |  Identifies the kind of charge where 0 is a charge, 1 is a discount, 2 is a prepayment, and 3 is a tax. The returned value is text not decimal on data sources. **Character limit**: **Values: **  - 0: charge - 1: discount - 2: prepayment - 3: tax  |  [optional]
**productDescription** | **String** |  A description of the product associated with this invoice item. **Character limit**: 500 **Values**: inherited from &#x60;Product.Description&#x60;  |  [optional]
**quantity** | **Double** |  The number of units for this invoice item. **Values**: inherited from &#x60;RatePlanCharge.Quantity&#x60;  |  [optional]
**ratePlanChargeId** | **String** |  The ID of the rate plan charge that&#39;s associated with this invoice item. **Character limit**: 32 **Values**: inherited from &#x60;RatePlanCharge.Id&#x60;  |  [optional]
**revRecStartDate** | [**LocalDate**](LocalDate.md) |  The date when revenue recognition is triggered. **Character limit**: 29 **Values**: generated from &#x60;InvoiceItem.RevRecTriggerCondition&#x60;  |  [optional]
**SKU** | **String** |  The unique SKU for the product associated with this invoice item. **Character limit**: 255 **Values**: inherited from &#x60;Product.SKU&#x60;  |  [optional]
**serviceEndDate** | [**LocalDate**](LocalDate.md) |  The end date of the service period associated with this invoice item. Service ends one second before the date in this value. **Character limit**: 29 **Values**: automatically generated  |  [optional]
**serviceStartDate** | [**LocalDate**](LocalDate.md) |  The start date of the service period associated with this invoice item. If the associated charge is a one-time fee, then this date is the date of that charge. **Character limit:** 29 **Values**: automatically generated  |  [optional]
**subscriptionId** | **String** |  The ID of the subscription associated with the invoice item. **Character limit**: 32 **Values**: inherited from &#x60;Subscription.Id&#x60;  |  [optional]
**taxAmount** | **Double** |  The amount of tax applied to the invoice item&#39;s charge. **Character limit**: **Values**: calculated from multiple fields in the ProductRatePlanCharge object  |  [optional]
**taxCode** | **String** |  Specifies the tax code for taxation rules. **Character limit**: 6 **Values**: inherited from &#x60;ProductRatePlanCharge.TaxCode&#x60;  |  [optional]
**taxExemptAmount** | **Double** |  The amount of the invoice item&#39;s charge that&#39;s tax exempt. **Character limit**: **Values**: calculated from multiple fields in the ProductRatePlanCharge object  |  [optional]
**taxMode** | **String** |  The tax mode of the invoice item. **Character limit**: 12 **Values**: &#x60;TaxExclusive&#x60;, &#x60;TaxInclusive&#x60;  |  [optional]
**UOM** | **String** |  Specifies the units to measure usage. Units of measure are configured in the web-based UI: **Z-Billing &gt; Settings** **Character limit**: **Values**: inherited from &#x60;ProductRatePlanCharge.UOM&#x60;  |  [optional]
**unitPrice** | **Double** |  The per-unit price of the invoice item. **Character limit**: **Values**: calculated from multiple fields in ProductRatePlanCharge and ProductRatePlanChargeTier objets  |  [optional]
**updatedById** | **String** |  The ID of the user who last updated the invoice item. **Character limit**: 32 **Values**: automatically generated  |  [optional]
**updatedDate** | [**DateTime**](DateTime.md) |  The date when the invoice item was last updated. **Character limit**: 29 **Values**: automatically generated  |  [optional]


