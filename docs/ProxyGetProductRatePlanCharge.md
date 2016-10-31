
# ProxyGetProductRatePlanCharge

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accountingCode** | **String** | The accounting code for the charge. Accounting codes group transactions that contain similar accounting attributes. **Character limit**: 100 **Values**: an active accounting code in your Zuora Chart of Accounts  |  [optional]
**applyDiscountTo** | **String** | Specifies the type of charges that you want a specific discount to apply to. All field values are case sensitive: note that these values are in all-caps. **Character limit**: 21 **Values**: one of the following:  - &#x60;ONETIME (1)&#x60; - &#x60;RECURRING (2)&#x60; - &#x60;USAGE (4)&#x60; - &#x60;ONETIMERECURRING (3)&#x60; - &#x60;ONETIMEUSAGE (5)&#x60; - &#x60;RECURRINGUSAGE (6)&#x60; - &#x60;ONETIMERECURRINGUSAGE (7)&#x60;  |  [optional]
**billCycleDay** | **Integer** |  Sets the bill cycle day (BCD) for the charge. The BCD determines which day of the month customer is billed. The BCD value in the account can override the BCD in this object. **Character limit**: 2 **Values**: a valid BCD integer, 1 - 31  |  [optional]
**billCycleType** | **String** |  Specifies how to determine the billing day for the charge. **Character limit**: 20 **Values**: one of the following:  - &#x60;DefaultFromCustomer&#x60; - &#x60;SpecificDayofMonth:&#x60; - &#x60;SubscriptionStartDay&#x60; - &#x60;ChargeTriggerDay&#x60; - &#x60;SpecificDayofWeek&#x60; **Note**:  - If you set this field to &#x60;SpecificDayofMonth&#x60;, you must specify which day of the month as the billing day for the charge in the BillCycleDay field. - If you set this field to &#x60;SpecificDayofWeek&#x60;, you must specify which day of the week as the billing day for the charge in the WeeklyBillCycleDay field.  |  [optional]
**billingPeriod** | **String** |  The billing period for the charge. The start day of the billing period is also called the bill cycle day (BCD). **Character limit**: 15 **Values**: one of the following  - &#x60;Month&#x60; - &#x60;Quarter&#x60; - &#x60;Annual&#x60; - &#x60;Semi-Annual&#x60; - &#x60;Specific Months&#x60; - &#x60;Subscription Term&#x60; (This value is in **Limited Availability**.) - &#x60;Week&#x60; - &#x60;Specific Weeks&#x60; **Note**: Specify the number of months or weeks in the SpecificBillingPeriod field if you set this field to &#x60;Specific Months&#x60; or &#x60;Specific Weeks&#x60;.  |  [optional]
**billingPeriodAlignment** | **String** |  Aligns charges within the same subscription if multiple charges begin on different dates. **Character limit**: 24 **Values**: one of the following:  - &#x60;AlignToCharge&#x60; - &#x60;AlignToSubscriptionStart&#x60; - &#x60;AlignToTermStart&#x60;  |  [optional]
**billingTiming** | **String** |  The billing timing for the charge. You can choose to bill in advance or in arrears for recurring charge types. This field is not used in one-time or usage based charge types. **Character limit**: **Values**: one of the following:  - &#x60;In Advance&#x60; - &#x60;In Arrears&#x60;  This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com/).   |  [optional]
**chargeModel** | **String** |  Determines how to calculate charges. Charge models must be individually activated in Z-Billing administration. **Character limit**: 27 **Values**: one of the following:  - &#x60;Discount-Fixed Amount&#x60; - &#x60;Discount-Percentage&#x60; - &#x60;Flat Fee Pricing&#x60; - &#x60;Per Unit Pricing&#x60; - &#x60;Overage Pricing&#x60; - &#x60;Tiered Pricing&#x60; - &#x60;Tiered with Overage Pricing&#x60; - &#x60;Volume Pricing&#x60;  |  [optional]
**chargeType** | **String** |  Specifies the type of charge. **Character limit**: 9 **Values**: one of the following:  - &#x60;OneTime&#x60; - &#x60;Recurring&#x60; - &#x60;Usage&#x60;  |  [optional]
**createdById** | **String** | The ID of the Zuora user who created the &#x60;ProductRatePlanCharge&#x60; object. **Character limit**: 32 **Values**: automatically generated  |  [optional]
**createdDate** | [**DateTime**](DateTime.md) |  The date when the  &#x60;ProductRatePlanCharge&#x60; object was created. **Character limit**: 29 **Values**: automatically generated  |  [optional]
**defaultQuantity** | **Double** |  The default quantity of units, such as the number of authors in a hosted wiki service. This field is required if you use a per-unit pricing model. **Character limit**: 16 **Values**: a valid quantity value  |  [optional]
**deferredRevenueAccount** | **String** |  The name of the deferred revenue account for this charge. **Character limit**: 100 **Values**: an active accounting code in your Zuora Chart of Accounts This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com/).   |  [optional]
**description** | **String** | A description of the charge. **Character limit**: 500 **Values**: a string of 500 characters or fewer  |  [optional]
**discountLevel** | **String** |  Specifies if the discount applies to just the product rate plan, the entire subscription, or to any activity in the account. **Character limit**: 12 **Values**: one of the following:  - &#x60;rateplan&#x60; - &#x60;subscription&#x60;, &#x60;account&#x60;  |  [optional]
**endDateCondition** | **String** |  Defines when the charge ends after the charge trigger date. **Values**: one of the following:  - &#x60;SubscriptionEnd&#x60;: The charge ends on the subscription end date after a specified period based on the trigger date of the charge. This is the default value. - &#x60;FixedPeriod&#x60;: The charge ends after a specified period based on the trigger date of the charge. If you set this field to &#x60;FixedPeriod&#x60;, you must specify the length of the period and a period type by defining the &#x60;UpToPeriods&#x60; and &#x60;UpToPeriodsType&#x60; fields. **Note**: If the subscription ends before the charge end date, the charge ends when the subscription ends. But if the subscription end date is subsequently changed through a Renewal, or Terms and Conditions amendment, the charge will end on the charge end date.  |  [optional]
**id** | **String** | Object identifier. |  [optional]
**includedUnits** | **Double** | Specifies the number of units in the base set of units. **Character limit**: 16 **Values**: a positive decimal value  |  [optional]
**legacyRevenueReporting** | **Boolean** |  |  [optional]
**listPriceBase** | **String** | The list price base for the product rate plan charge. **Values**: one of the following:  - &#x60;Per Month&#x60; - &#x60;Per Billing Period&#x60; - &#x60;Per Week&#x60;  |  [optional]
**maxQuantity** | **Double** |  Specifies the maximum number of units for this charge. Use this field and the &#x60;MinQuantity&#x60; field to create a range of units allowed in a product rate plan charge. **Character limit**: 16 **Values**: a positive decimal value  |  [optional]
**minQuantity** | **Double** | Specifies the minimum number of units for this charge. Use this field and the &#x60;MaxQuantity&#x60; field to create a range of units allowed in a product rate plan charge. **Character limit**: 16 **Values**: a positive decimal value  |  [optional]
**name** | **String** | The name of the product rate plan charge. **Character limit**: 100 **Values**: a string of 100 characters or fewer  |  [optional]
**numberOfPeriod** | **Long** | Specifies the number of periods to use when calculating charges in an overage smoothing charge model. **Character limit**: **Values**: a positive whole number  |  [optional]
**overageCalculationOption** | **String** | Determines when to calculate overage charges. If the value of the SmoothingMode field is not specified, the value of this field is ignored. **Character limit**: 20 **Values**: one of the following:  - &#x60;EndOfSmoothingPeriod&#x60;: This option is used by default. The overage is charged at the end of the smoothing period. - &#x60;PerBillingPeriod&#x60;: The overage is charged on-demand rather than waiting until the end of the smoothing period.  |  [optional]
**overageUnusedUnitsCreditOption** | **String** |  Determines whether to credit the customer with unused units of usage. **Character limit**: 20 **Values**: one of the following:  - &#x60;NoCredit&#x60; - &#x60;CreditBySpecificRate&#x60;  |  [optional]
**priceChangeOption** | **String** |  Applies an automatic price change when a termed subscription is renewed. **Character limit**: **Values**: one of the following:  - &#x60;NoChange&#x60; (default) - &#x60;SpecificPercentageValue&#x60; - &#x60;UseLatestProductCatalogPricing&#x60;  |  [optional]
**priceIncreasePercentage** | **Double** |  Specifies the percentage to increase or decrease the price of a termed subscription&#39;s renewal. Use this field if you set the [&#x60;PriceChangeOption&#x60;](https://knowledgecenter.zuora.com/DC_Developers/SOAP_API/E1_SOAP_API_Object_Reference/ProductRatePlanCharge#PriceIncreaseOption) value to &#x60;SpecificPercentageValue&#x60;. **Character limit**: 16 **Values**: a decimal value between -100 and 100  |  [optional]
**productRatePlanId** | **String** |  The ID of the product rate plan associated with this product rate plan charge. **Character limit**: 32 **Values**: a valid product rate plan ID  |  [optional]
**recognizedRevenueAccount** | **String** |  The name of the recognized revenue account for this charge.  - Required when the Allow Blank Accounting Code setting is No. - Optional when the Allow Blank Accounting Code setting is Yes. Navigate to **Z-Finance Settings &gt; Configure Accounting Rules** to check this setting. **Character limit**: 100 **Values**: an active accounting code in your Zuora Chart of Accounts This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com/).   |  [optional]
**revRecCode** | **String** | Associates this product rate plan charge with a specific revenue recognition code. **Character limit**: 70 **Values**: a valid revenue recognition code  |  [optional]
**revRecTriggerCondition** | **String** |  Specifies when revenue recognition begins. **Character limit**: 22 **Values**: one of the following:  - &#x60;ContractEffectiveDate&#x60; - &#x60;ServiceActivationDate&#x60; - &#x60;CustomerAcceptanceDate&#x60;  |  [optional]
**revenueRecognitionRuleName** | **String** | Determines when to recognize the revenue for this charge. **Character limit**: 25 **Values**: one of the following:  - &#x60;Recognize upon invoicing&#x60; - &#x60;Recognize daily over time&#x60;  |  [optional]
**smoothingModel** | **String** |  Specifies the smoothing model for an overage smoothing charge model. **Character limit**: 22 **Values**: one of the following:  - &#x60;RollingWindow&#x60; - &#x60;Rollover&#x60;  |  [optional]
**specificBillingPeriod** | **Long** |  Customizes the number of months or weeks for the charges billing period. This field is required if you set the value of the BillingPeriod field to &#x60;Specific Months&#x60; or &#x60;Specific Weeks&#x60;. **Values**: a positive integer  |  [optional]
**taxCode** | **String** |  Specifies the tax code for taxation rules. Required when the Taxable field is set to &#x60;True&#x60;. **Character limit**: 64 **Values**: a valid tax code  |  [optional]
**taxMode** | **String** |  Determines how to define taxation for the charge. Required when the Taxable field is set to &#x60;True&#x60;. **Character limit**: 12 **Values**: one of the following:  - &#x60;TaxExclusive&#x60; - &#x60;TaxInclusive&#x60;  |  [optional]
**taxable** | **Boolean** |  Determines whether the charge is taxable. When set to &#x60;True&#x60;, the TaxMode and TaxCode fields are required when creating or updating th ProductRatePlanCharge object. **Character limit**: 5 **Values**: &#x60;True&#x60;, &#x60;False&#x60;  |  [optional]
**triggerEvent** | **String** |  Specifies when to start billing the customer for the charge. **Character limit**: 18 **Values**: one of the following:  - &#x60;ContractEffective&#x60; is the date when the subscription&#39;s contract goes into effect and the charge is ready to be billed. - &#x60;ServiceActivation&#x60; is the date when the services or products for a subscription have been activated and the customers have access. - &#x60;CustomerAcceptance&#x60; is when the customer accepts the services or products for a subscription.  |  [optional]
**UOM** | **String** |  Specifies the units to measure usage. Units of measure are configured in the web-based UI: **Z-Billing &gt; Settings**. **Character limit**: 25 **Values**: a configured unit of measure **Note**: You must specify this field when creating the following charge models:  - Per Unit Pricing - Volume Pricing - Overage Pricing - Tiered Pricing - Tiered with Overage Pricing  |  [optional]
**upToPeriods** | **Long** |  Specifies the length of the period during which the charge is active. If this period ends before the subscription ends, the charge ends when this period ends. **Character limit**: 5 **Values**: a whole number between 0 and 65535, exclusive **Note**:  - You must use this field together with the &#x60;UpToPeriodsType&#x60; field to specify the time period. This field is applicable only when the &#x60;EndDateCondition&#x60; field is set to &#x60;FixedPeriod&#x60;. - If the subscription end date is subsequently changed through a Renewal, or Terms and Conditions amendment, the charge end date will change accordingly up to the original period end.  |  [optional]
**upToPeriodsType** | **String** |  The period type used to define when the charge ends. **Character limit**: -- **Values**: one of the following:  - &#x60;Billing Periods&#x60; (default) - &#x60;Days&#x60; - &#x60;Weeks&#x60; - &#x60;Months&#x60; - Years **Note**:  - You must use this field together with the &#x60;UpToPeriods&#x60; field to specify the time period. - This field is applicable only when the &#x60;EndDateCondition&#x60; field is set to &#x60;FixedPeriod&#x60;.  |  [optional]
**updatedById** | **String** | The ID of the last user to update the object. **Character limit**: 32 **Values**: automatically generated  |  [optional]
**updatedDate** | [**DateTime**](DateTime.md) | The date when the object was last updated. **Character limit**: 29 **Values**: automatically generated  |  [optional]
**useDiscountSpecificAccountingCode** | **Boolean** | Determines whether to define a new accounting code for the new discount charge. **Character limit**: 5 **Values**: &#x60;True&#x60;, &#x60;False&#x60;  |  [optional]
**useTenantDefaultForPriceChange** | **Boolean** |  Applies the tenant-level percentage uplift value for an automatic price change to a termed subscription&#39;s renewal. You set the tenant uplift value in the web-based UI: **Z-Billing &gt; Define Default Subscription Settings** **Character limit**: 5 **Values**: &#x60;true&#x60;, &#x60;false&#x60;  |  [optional]
**weeklyBillCycleDay** | **String** |  Specifies which day of the week as the bill cycle day (BCD) for the charge. This feature is in **Limited Availability**. If you wish to have access to the feature, submit a request at [Zuora Global Support](http://support.zuora.com/).  **Values**: one of the following:  - &#x60;Sunday&#x60; - &#x60;Monday&#x60; - &#x60;Tuesday&#x60; - &#x60;Wednesday&#x60; - &#x60;Thursday&#x60; - &#x60;Friday&#x60; - &#x60;Saturday&#x60;  |  [optional]


