---
title: PaymentRequest
slug: Web/API/PaymentRequest
page-type: web-api-interface
tags:
  - API
  - Commerce
  - Interface
  - Merchants
  - Money
  - Payment Request
  - Payment Request API
  - PaymentRequest
  - Payments
  - Reference
  - Secure context
browser-compat: api.PaymentRequest
---

{{APIRef("Payment Request API")}}{{SecureContext_Header}}

The [Payment Request API's](/en-US/docs/Web/API/Payment_Request_API) **`PaymentRequest`** interface is the primary access point into the API, and lets web content and apps accept payments from the end user on behalf of the operator of the site or the publisher of the app.

{{InheritanceDiagram}}

## Constructor

- {{domxref('PaymentRequest.PaymentRequest()','PaymentRequest()')}} {{SecureContext_Inline}}
  - : Creates a new `PaymentRequest` object.

## Properties

- {{domxref('PaymentRequest.id')}} {{ReadOnlyInline}} {{SecureContext_Inline}}
  - : An unique identifier for a particular `PaymentRequest`, which can be set via `details.id`. When none is set, it defaults to a UUID.
- {{domxref('PaymentRequest.shippingAddress')}} {{ReadOnlyInline}} {{SecureContext_Inline}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : If requested via payment options, returns the shipping address chosen by the user for the purposes of calculating shipping. This property is only populated if the constructor is called with the `requestShipping` flag set to true. Additionally, in some browsers, the parts of the address will be redacted for privacy until the user indicates they are ready to complete the transaction (i.e., they hit "Pay").
- {{domxref('PaymentRequest.shippingOption')}} {{ReadOnlyInline}} {{SecureContext_Inline}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Returns the identifier of the selected shipping option. This property is only populated if the constructor is called with the `requestShipping` flag set to true.
- {{domxref('PaymentRequest.shippingType')}} {{ReadOnlyInline}} {{SecureContext_Inline}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Returns the type of shipping used to fulfill the transaction. This will be one of `shipping`, `delivery`, `pickup`, or `null` if a value was not provided in the constructor.

## Methods

- {{domxref('PaymentRequest.canMakePayment()')}} {{SecureContext_Inline}}
  - : Indicates whether the `PaymentRequest` object can make a payment before calling `show()`.
- {{domxref('PaymentRequest.show()')}} {{SecureContext_Inline}}
  - : Causes the user agent to begin the user interaction for the payment request.
- {{domxref('PaymentRequest.abort()')}} {{SecureContext_Inline}}
  - : Causes the user agent to end the payment request and to remove any user interface that might be shown.

## Events

- {{domxref("PaymentRequest.merchantvalidation_event", "merchantvalidation")}} {{SecureContext_Inline}} {{Deprecated_Inline}}
  - : With some payment handlers (e.g., Apple Pay), this event handler is called to handle the {{domxref("PaymentRequest.merchantvalidation_event", "merchantvalidation")}} event, which is dispatched when the user agent requires that the merchant validate that the merchant or vendor requesting payment is legitimate.
- {{domxref("PaymentRequest.paymentmethodchange_event", "paymentmethodchange")}} {{SecureContext_Inline}}
  - : With some payment handlers (e.g., Apple Pay), dispatched whenever the user changes payment instrument, like switching from a credit card to a debit card.
- {{domxref("PaymentRequest.shippingaddresschange_event", "shippingaddresschange")}} {{SecureContext_Inline}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Dispatched whenever the user changes their shipping address.
- {{domxref("PaymentRequest.shippingoptionchange_event", "shippingoptionchange")}} {{SecureContext_Inline}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Dispatched whenever the user changes a shipping option.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
