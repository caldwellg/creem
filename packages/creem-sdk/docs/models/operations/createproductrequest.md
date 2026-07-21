# CreateProductRequest

## Example Usage

```typescript
import { CreateProductRequest } from "creem/models/operations";

let value: CreateProductRequest = {
  idempotencyKey: "<value>",
  createProductRequestEntity: {
    name: "<value>",
    description:
      "ingratiate premier innovate carefully never shyly afterwards hmph phew pfft",
    imageUrl: "https://picsum.photos/200/300",
    price: 400,
    currency: "USD",
    billingType: "onetime",
    payWhatYouWant: false,
    suggestedPrice: 1500,
    defaultSuccessUrl: "https://example.com/?status=successful",
    customFields: [
      {
        type: "text",
        key: "companyName",
        label: "Company Name",
        text: {
          maxLength: 200,
          minLength: 1,
        },
        checkbox: {
          label:
            "I agree to the [terms and conditions](https://example.com/terms)",
        },
      },
    ],
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                               | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `createProductRequestEntity`                                                                   | [components.CreateProductRequestEntity](../../models/components/createproductrequestentity.md) | :heavy_check_mark:                                                                             | Product creation payload                                                                       |