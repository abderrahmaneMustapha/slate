---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the StockAndBuy API! You can use our API to access StockAndBuy API endpoints, which can get information on various products and products variants in our database.

We have language bindings in Shell, Ruby, Python, JavaScript and C# ! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: StockAndBuyKey"
```

> Make sure to replace `StockAndBuyKey` with your API key.

StockAndBuy uses API keys to allow access to the API. You can register a new StockAndBuy API key at our [developer portal](http://example.com/developers).

StockAndBuy expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: StockAndBuyKey`

<aside class="notice">
You must replace <code>StockAndBuyKey</code> with your personal API key.
</aside>

# Products

## Get All Products

```shell
curl "http://stockAndBuy.com/api/products" \
  -H "Authorization: StockAndBuyKey"
```

> The above command returns JSON structured like this:

```json
{
  "page": 0,
  "size": 50,
  "count": 265,
  "pages": 6,
  "result": [
    {
      "Id": 2,
      "Name": "shirt",
      "Barcode": "azeazeaz",
      "SKU": "nice",
      "Unit": null,
      "PriceStrategy": "nice",
      "Handle": "handle",
      "Options": null,
      "ProductType": "shirt",
      "Description": "a nice shirt",
      "LastUpdatedTime": "2021-02-15T11:03:39.187",
      "ProductTags": [],
      "Variants": [
        {
          "ProductVariantsId": 6,
          "ComparePrice": 0.0,
          "Barcode": null,
          "Quantity": 33,
          "Sku": "EIEIEIEIEIE",
          "ImageId": null,
          "Image": null,
          "OptionValues": null,
          "Position": 0,
          "PurchasePrice": 456.0,
          "WholesalePrice": 0.0,
          "RetailPrice": 683.0,
          "EntryDate": "2021-02-15T11:03:40.28",
          "LastUpdatedTime": "2021-02-15T11:03:40.28",
          "Cost": 0.0,
          "Weight": 2.0
        },
        {
          "ProductVariantsId": 7,
          "ComparePrice": 0.0,
          "Barcode": null,
          "Quantity": 33,
          "Sku": "ryt345",
          "ImageId": null,
          "Image": null,
          "OptionValues": null,
          "Position": 0,
          "PurchasePrice": 456.0,
          "WholesalePrice": 0.0,
          "RetailPrice": 683.0,
          "EntryDate": "2021-02-15T11:03:40.287",
          "LastUpdatedTime": "2021-02-15T11:03:40.287",
          "Cost": 0.0,
          "Weight": 2.0
        }
      ]
    },
    {
      "Id": 3,
      "Name": "Zara shirt",
      "Barcode": null,
      "SKU": null,
      "Unit": null,
      "PriceStrategy": null,
      "Handle": "handle",
      "Options": null,
      "ProductType": "shirt",
      "Description": null,
      "LastUpdatedTime": "2021-02-15T11:03:39.19",
      "ProductTags": [],
      "Variants": [
        {
          "ProductVariantsId": 11,
          "ComparePrice": 0.0,
          "Barcode": null,
          "Quantity": 33,
          "Sku": "ryt345",
          "ImageId": null,
          "Image": null,
          "OptionValues": null,
          "Position": 0,
          "PurchasePrice": 456.0,
          "WholesalePrice": 0.0,
          "RetailPrice": 683.0,
          "EntryDate": "2021-02-15T11:03:40.32",
          "LastUpdatedTime": "2021-02-15T11:03:40.32",
          "Cost": 0.0,
          "Weight": 2.0
        },
        {
          "ProductVariantsId": 12,
          "ComparePrice": 0.0,
          "Barcode": null,
          "Quantity": 33,
          "Sku": "ryt345",
          "ImageId": null,
          "Image": null,
          "OptionValues": null,
          "Position": 0,
          "PurchasePrice": 456.0,
          "WholesalePrice": 0.0,
          "RetailPrice": 683.0,
          "EntryDate": "2021-02-15T11:03:40.33",
          "LastUpdatedTime": "2021-02-15T11:03:40.33",
          "Cost": 0.0,
          "Weight": 2.0
        }
      ]
    }
  ]
}
```

This endpoint retrieves all products.

### HTTP Request

`GET http://stockAndBuy.com/api/products`

### Query Parameters

| Parameter   | Default | Description                                                                  |
| ----------- | ------- | ---------------------------------------------------------------------------- |
| pageSize    | 50      | Return up to this many results per page                                      |
| page        | 1       | Return the products by page number                                           |
| since_id    | null    | Return only products after the specified ID.                                 |
| ids         | null    | Return only products specified by a comma-separated list of product IDs.     |
| name        | null    | Return only products specified by a comma-separated list of product names.   |
| handle      | null    | Return only products specified by a comma-separated list of product handles. |
| productType | null    | Return products by product type.                                             |

<aside class="success">
Remember — to authenticate !
</aside>

## Get a Specific Product

```shell
curl "http://stockAndBuy.com/api/products/2" \
  -H "Authorization: stockAndBuyApiKey"
```

> The above command returns JSON structured like this:

```json
 {
    "Id": 2,
    "Name": "shirt",
    "Barcode": "azeazeaz",
    "SKU": "nice",
    "Unit": null,
    "PriceStrategy": "nice",
    "Handle": "handle",
    "Options": null,
    "ProductType": "shirt",
    "Description": "a nice shirt",
    "LastUpdatedTime": "2021-02-15T11:03:39.187",
    "ProductTags": [],
    "Variants": [
        {
            "ProductVariantsId": 6,
            "ComparePrice": 0.0,
            "Barcode": null,
            "Quantity": 33,
            "Sku": "EIEIEIEIEIE",
            "ImageId": null,
            "Image": null,
            "OptionValues": null,
            "Position": 0,
            "PurchasePrice": 456.0,
            "WholesalePrice": 0.0,
            "RetailPrice": 683.0,
            "EntryDate": "2021-02-15T11:03:40.28",
            "LastUpdatedTime": "2021-02-15T11:03:40.28",
            "Cost": 0.0,
            "Weight": 2.0
        },
        {
            "ProductVariantsId": 7,
            "ComparePrice": 0.0,
            "Barcode": null,
            "Quantity": 33,
            "Sku": "ryt345",
            "ImageId": null,
            "Image": null,
            "OptionValues": null,
            "Position": 0,
            "PurchasePrice": 456.0,
            "WholesalePrice": 0.0,
            "RetailPrice": 683.0,
            "EntryDate": "2021-02-15T11:03:40.287",
            "LastUpdatedTime": "2021-02-15T11:03:40.287",
            "Cost": 0.0,
            "Weight": 2.0
        },
    ]
},
```

This endpoint retrieves a specific product.

### HTTP Request

`GET http://stockAndBuy.com/api/products/<ID>`

## Update a Specific Product

```shell
curl "http://stockAndBuy.com/api/products/2" \
  -X PATCH \
  -H "Authorization: stockAndBuyApiKey" \
  -H "Content-Type: application/json" \
    -d '{"name" : "Name",
        "barCode":"AZCV345ERFFG2334",
        "description": "description",
        "sku": "sku",
        "unit" : "DA",
        "priceStrategy" : "strategy"
      }'
```

> The above command returns JSON structured like this:

```json
{
    "Id": 2,
    "Name": "Name",
    "Barcode": "AZCV345ERFFG2334",
    "SKU": "sku",
    "Unit": "DA",
    "PriceStrategy": "nice",
    "Handle": "handle",
    "Options": null,
    "ProductType": "shirt",
    "Description": "description",
    "LastUpdatedTime": "2021-02-15T11:03:39.187",
    "ProductTags": [],
    "Variants": [
        {
            "ProductVariantsId": 6,
            "ComparePrice": 0.0,
            "Barcode": null,
            "Quantity": 33,
            "Sku": "EIEIEIEIEIE",
            "ImageId": null,
            "Image": null,
            "OptionValues": null,
            "Position": 0,
            "PurchasePrice": 456.0,
            "WholesalePrice": 0.0,
            "RetailPrice": 683.0,
            "EntryDate": "2021-02-15T11:03:40.28",
            "LastUpdatedTime": "2021-02-15T11:03:40.28",
            "Cost": 0.0,
            "Weight": 2.0
        },
        {
            "ProductVariantsId": 7,
            "ComparePrice": 0.0,
            "Barcode": null,
            "Quantity": 33,
            "Sku": "ryt345",
            "ImageId": null,
            "Image": null,
            "OptionValues": null,
            "Position": 0,
            "PurchasePrice": 456.0,
            "WholesalePrice": 0.0,
            "RetailPrice": 683.0,
            "EntryDate": "2021-02-15T11:03:40.287",
            "LastUpdatedTime": "2021-02-15T11:03:40.287",
            "Cost": 0.0,
            "Weight": 2.0
        },
    ]
},
```

This endpoint update a specific product.

`PATCH http://stockAndBuy.com/api/products/<ID>`

### URL Parameters

| Parameter | Description                     |
| --------- | ------------------------------- |
| ID        | The ID of the product to delete |

## Post a Specific Product

```shell
curl "http://stockAndBuy.com/api/products" \
  -X POST \
  -H "Authorization: stockAndBuyApiKey" \
  -H "Content-Type: application/json" \
    -d '{"name" : "Shirt",
        "barCode":"AZCV345ERFFG2334",
        "description": "a good product",
        "sku": "sku",
        "unit" : "DA",
        "priceStrategy" : "strategy"
      }'
```

> The above command returns JSON structured like this:

```json
{
  "Id": 500,
  "Name": "Shirt",
  "Barcode": "AZCV345ERFFG2334",
  "SKU": "sku",
  "Unit": "DA",
  "PriceStrategy": "strategy",
  "Handle": null,
  "Options": null,
  "ProductType": null,
  "Description": "a good product",
  "LastUpdatedTime": "2021-02-15T11:03:39.187",
  "ProductTags": [],
  "Variants": []
}
```

This endpoint create a specific product.

### HTTP Request

`POST http://stockAndBuy.com/api/products`

## Delete a Specific Product

```shell
curl "http://stockAndBuy.com/api/products/6" \
  -X DELETE \
  -H "Authorization: stockAndBuyApiKey"
```

> The above command returns JSON structured like this:

```json
{
  "Id": 6,
  "Name": "CD",
  "Barcode": "AZCV345E44RFFG2334",
  "SKU": "sku",
  "Unit": "DA",
  "PriceStrategy": "strategy",
  "Handle": null,
  "Options": null,
  "ProductType": null,
  "Description": "a good product",
  "LastUpdatedTime": "2021-02-15T11:03:39.187",
  "ProductTags": [],
  "Variants": []
}
```

This endpoint deletes a specific product.

### HTTP Request

`DELETE http://StockAndBuy.com/api/products/<ID>`

### URL Parameters

| Parameter | Description                     |
| --------- | ------------------------------- |
| ID        | The ID of the product to delete |

# Variants

## Get All Variants

```shell
curl "http://stockAndBuy.com/api/products/2/variants" \
  -H "Authorization: stockAndBuyApiKey"
```

> The above command returns JSON structured like this:

```json
[
  {
    "ProductVariantsId": 6,
    "ComparePrice": 0.0,
    "Barcode": null,
    "Quantity": 33,
    "Sku": "EIEIEIEIEIE",
    "ImageId": null,
    "Image": null,
    "OptionValues": null,
    "Position": 0,
    "PurchasePrice": 456.0,
    "WholesalePrice": 0.0,
    "RetailPrice": 683.0,
    "EntryDate": "2021-02-15T11:03:40.28",
    "LastUpdatedTime": "2021-02-15T11:03:40.28",
    "Cost": 0.0,
    "Weight": 2.0
  },
  {
    "ProductVariantsId": 7,
    "ComparePrice": 0.0,
    "Barcode": null,
    "Quantity": 33,
    "Sku": "ryt345",
    "ImageId": null,
    "Image": null,
    "OptionValues": null,
    "Position": 0,
    "PurchasePrice": 456.0,
    "WholesalePrice": 0.0,
    "RetailPrice": 683.0,
    "EntryDate": "2021-02-15T11:03:40.287",
    "LastUpdatedTime": "2021-02-15T11:03:40.287",
    "Cost": 0.0,
    "Weight": 2.0
  }
]
```

This endpoint retrieves all products.

### HTTP Request

`GET http://stuckAndBuyApi.com/api/products/<IDPRODUCT>/variants`

### URL Parameters

| Parameter | Description                     |
| --------- | ------------------------------- |
| IDPRODUCT | The id of the variant to delete |

### Query Parameters

| Parameter   | Default | Description                                                                  |
| ----------- | ------- | ---------------------------------------------------------------------------- |
| pageSize    | 50      | Return up to this many results per page                                      |
| page        | 1       | Return the products by page number                                           |
| since_id    | null    | Return only products after the specified ID.                                 |
| ids         | null    | Return only products specified by a comma-separated list of product IDs.     |
| name        | null    | Return only products specified by a comma-separated list of product names.   |
| handle      | null    | Return only products specified by a comma-separated list of product handles. |
| productType | null    | Return products by product type.                                             |

<aside class="success">
Remember — to authenticate !
</aside>

## Get a Specific Variant

```shell
curl "http://stockAndBuy.com/api/products/2/variants/6" \
  -H "Authorization: stockAndBuyApiKey"
```

> The above command returns JSON structured like this:

```json
{
    "ProductVariantsId": 6,
    "ComparePrice": 0.0,
    "Barcode": null,
    "Quantity": 33,
    "Sku": "EIEIEIEIEIE",
    "ImageId": null,
    "Image": null,
    "OptionValues": null,
    "Position": 0,
    "PurchasePrice": 456.0,
    "WholesalePrice": 0.0,
    "RetailPrice": 683.0,
    "EntryDate": "2021-02-15T11:03:40.28",
    "LastUpdatedTime": "2021-02-15T11:03:40.28",
    "Cost": 0.0,
    "Weight": 2.0
  },
```

This endpoint retrieves a specific product.

### HTTP Request

`GET http://stockAndBuy.com/api/products/<IDPRODUCT>/variants/<IDVARIANTS>`

### URL Parameters

| Parameter  | Description               |
| ---------- | ------------------------- |
| IDPRODUCT  | The id of a product       |
| IDVARIANTS | The id of updated variant |

## Update a Specific Variant

```shell
curl "http://stockAndBuy.com/api/products/2/variants/6" \
  -X PATCH \
  -H "Authorization: stockAndBuyApiKey" \
  -H "Content-Type: application/json" \
    -d '{
    
        "quantity" : 34,
        "sku" :  "sku",
     
      }'
```

> The above command returns JSON structured like this:

```json
{
  "Id" : 6,
  "Quantity": 34,
  "Sku": "sku",
  "ImageId": null,
  "Image": null,
  "OptionValues": null,
  "Position": 1,
  "PurchasePrice": 233.33,
  "WholesalePrice": 400.12,
  "RetailPrice": 450.12
}
```

This endpoint update a specific variant.

### HTTP Request

`PATCH http://stockAndBuy.com/api/products/<IDPRODUCT>/variants/<IDVARIANTS>`

### URL Parameters

| Parameter  | Description               |
| ---------- | ------------------------- |
| IDPRODUCT  | The id of a product       |
| IDVARIANTS | The id of updated variant |

## Post a Specific Variant

```shell
curl "http://stockAndBuy.com/api/products/2/variants" \
   -X POST \
  -H "Authorization: stockAndBuyApiKey" \
  -H "Content-Type: application/json" \
    -d '{
       "comparePrice" :  12344.456,
       "barcode" : "123FFKRKG45",
        "quantity" : 34,
        "sku" :  "sku",
        "positions" : 1,
        "purchasePrice" : 233.33,
        "wholesalePrice" : 400.12,
        "retailPrice": 450.12,
      }'
```

> The above command returns JSON structured like this:

```json
{
  "Id" : 6,
  "Quantity": 34,
  "Sku": "sku",
  "ImageId": null,
  "Image": null,
  "OptionValues": null,
  "Position": 1,
  "PurchasePrice": 233.33,
  "WholesalePrice": 400.12,
  "RetailPrice": 450.12
}
```

This endpoint create a specific variant.

### HTTP Request

`POST http://stockAndBuy.com/api/products/<IDPRODUCT>/variants`

### URL Parameters

| Parameter | Description         |
| --------- | ------------------- |
| IDPRODUCT | The id of a product |

## Delete a Specific Variant

```shell
curl "http://stockAndBuy.com/api/products/2/variants/6" \
  -X DELETE \
  -H "Authorization: stockAndBuyApiKey"
```

> The above command returns JSON structured like this:

```json
{
  "Id" : 6,
  "Quantity": 34,
  "Sku": "sku",
  "ImageId": null,
  "Image": null,
  "OptionValues": null,
  "Position": 1,
  "PurchasePrice": 233.33,
  "WholesalePrice": 400.12,
  "RetailPrice": 450.12
}
```

This endpoint deletes a specific product.

### HTTP Request

`DELETE http://StockAndBuy/api/products/<IDPRODUCT>/variants/<IDVARIANT>`

### URL Parameters

| Parameter | Description         |
| --------- | ------------------- |
| IDPRODUCT | The id of a product |
| IDVARIANT | The id of a variant |
