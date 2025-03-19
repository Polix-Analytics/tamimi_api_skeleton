# API Documentation

## Endpoint: `getVendorsByCreationTime`

### Overview
This endpoint retrieves all vendors that have been created within a specified date range.

---

### Endpoint Details

- **Method**: `GET`
- **URL**: `/getVendorsByCreationTime`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Parameters

#### Query Parameters
| Parameter | Type     | Required | Description                                                                 |
|-----------|----------|----------|-----------------------------------------------------------------------------|
| `from`    | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the start date-time filter.     |
| `to`      | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the end date-time filter.       |

**Example**:
```
GET /getVendorsByCreationTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "vendor_id": "V1234",
      "name": "Vendor Name",
      "created_at": "2024-06-01T12:34:56Z",
      "updated_at": "2024-06-02T12:34:56Z"
      // ... Additional Fields
    },
    // ... more vendors
  ]
}
```

#### Error Responses

##### Invalid or Missing `from` or `to`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing from or to. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with `from` and `to`:
```
GET /getVendorsByCreationTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
Authorization: Bearer <your-token>
```

---

## Endpoint: `getVendorsByUpdateTime`

### Overview
This endpoint retrieves all vendors that have been updated within a specified date range.

---

### Endpoint Details

- **Method**: `GET`
- **URL**: `/getVendorsByUpdateTime`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Parameters

#### Query Parameters
| Parameter | Type     | Required | Description                                                                 |
|-----------|----------|----------|-----------------------------------------------------------------------------|
| `from`    | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the start date-time filter.     |
| `to`      | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the end date-time filter.       |

**Example**:
```
GET /getVendorsByUpdateTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "vendor_id": "V1234",
      "name": "Vendor Name",
      "created_at": "2024-05-01T12:34:56Z",
      "updated_at": "2024-06-02T12:34:56Z"
      // ... Additional Fields
    },
    // ... more vendors
  ]
}
```

#### Error Responses

##### Invalid or Missing `from` or `to`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing from or to. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with `from` and `to`:
```
GET /getVendorsByUpdateTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
Authorization: Bearer <your-token>
```

---


## Endpoint: `getProjectsByCreationTime`

### Overview
This endpoint retrieves all projects that have been created within a specified date range.

---

### Endpoint Details

- **Method**: `GET`
- **URL**: `/getProjectsByCreationTime`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Parameters

#### Query Parameters
| Parameter | Type     | Required | Description                                                                 |
|-----------|----------|----------|-----------------------------------------------------------------------------|
| `from`    | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the start date-time filter.     |
| `to`      | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the end date-time filter.       |

**Example**:
```
GET /getProjectsByCreationTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "project_id": "P1234",
      "name": "Project Name",
      "description": "Project Description",
      "created_at": "2024-06-01T12:34:56Z",
      "updated_at": "2024-06-02T12:34:56Z",
      "bom": [
        {
          "item_id": "1234",
          "allotted_quantity": 48
        }
      ]
      // ... Additional Fields
    },
    // ... more projects
  ]
}
```

#### Error Responses

##### Invalid or Missing `from` or `to`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing from or to. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with `from` and `to`:
```
GET /getProjectsByCreationTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
Authorization: Bearer <your-token>
```

---

## Endpoint: `getProjectsByUpdateTime`

### Overview
This endpoint retrieves all projects that have been updated within a specified date range.

---

### Endpoint Details

- **Method**: `GET`
- **URL**: `/getProjectsByUpdateTime`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Parameters

#### Query Parameters
| Parameter | Type     | Required | Description                                                                 |
|-----------|----------|----------|-----------------------------------------------------------------------------|
| `from`    | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the start date-time filter.     |
| `to`      | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the end date-time filter.       |

**Example**:
```
GET /getProjectsByUpdateTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "project_id": "P1234",
      "name": "Project Name",
      "description": "Project Description",
      "created_at": "2024-05-01T12:34:56Z",
      "updated_at": "2024-06-02T12:34:56Z",
      "bom": [
        {
          "item_id": "1234",
          "allotted_quantity": 48
        }
      ]
      // ... Additional Fields
    },
    // ... more projects
  ]
}
```

#### Error Responses

##### Invalid or Missing `from` or `to`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing from or to. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with `from` and `to`:
```
GET /getProjectsByUpdateTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
Authorization: Bearer <your-token>
```

---


## Endpoint: `createGrn`

### Overview
This endpoint is used to close a Goods Receipt Note (GRN) by providing details of the received items.

---

### Endpoint Details

- **Method**: `POST`
- **URL**: `/createGrn`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Body

| Parameter                  | Type              | Required | Description                                                 |
|----------------------------|-------------------|----------|-------------------------------------------------------------|
| `po_id`                    | `string`          | Yes      | The purchase order ID.                                      |
| `images_at_receiving`      | `list of strings` | Yes      | List of image URLs taken at the time of receiving.          |
| `items`                    | `list of objects` | Yes      | List of items received. Each item includes the fields below. |
| `items.good_quantity`      | `number`          | Yes      | Quantity of good items received.                            |
| `items.damaged_quantity`   | `number`          | Yes      | Quantity of damaged items received.                         |
| `items.missing_quantity`   | `number`          | Yes      | Quantity of missing items.                                  |
| `items.comments`           | `string`          | No       | Comments about the received items.                          |
| `items.received_by`        | `string`          | Yes      | Name of the person who received the items.                  |
| `items.received_at`        | `string`          | Yes      | Timestamp (ISO 8601 format) when the items were received.   |
| `items.site_warehouse_location` | `string`     | Yes      | Exact Location of the item.                 |
| `is_partial`               | `boolean`         | Yes      | Indicates if the GRN is partial.                            |
| `shipment_number`          | `number`          | No       | The shipment number, required if `is_partial` is true.      |
| `close_for_receipt`        | `boolean`         | No       | Used to to manage damaged items.                            |

**Example**:
```json
{
  "po_id": "PO12345",
  "images_at_receiving": [
    "http://example.com/image1.jpg",
    "http://example.com/image2.jpg"
  ],
  "items": [
    {
      "good_quantity": 10,
      "damaged_quantity": 2,
      "missing_quantity": 1,
      "comments": "Some items were damaged",
      "received_by": "John Doe",
      "received_at": "2024-06-01T12:34:56Z",
      "site_warehouse_location": "691 Buraq, A1"
    }
  ],
  "is_partial": true,
  "shipment_number": 1,
  "close_for_receipt": false
}
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "message": "GRN created successfully."
}
```

#### Error Responses

##### Invalid or Missing Fields
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing fields in the request body."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with all required fields:
```
POST /createGrn
Authorization: Bearer <your-token>
Content-Type: application/json

{
  "po_id": "PO12345",
  "images_at_receiving": [
    "http://example.com/image1.jpg",
    "http://example.com/image2.jpg"
  ],
  "items": [
    {
      "good_quantity": 10,
      "damaged_quantity": 2,
      "missing_quantity": 1,
      "comments": "Some items were damaged",
      "received_by": "John Doe",
      "received_at": "2024-06-01T12:34:56Z",
      "site_warehouse_location": "691 Buraq, A1"
    }
  ],
  "is_partial": true,
  "shipment_number": 1,
  "close_for_receipt": false
}
```

---

## Endpoint: `getItemsByCreationTime`

### Overview
This endpoint retrieves all items that have been created within a specified date range.

---

### Endpoint Details

- **Method**: `GET`
- **URL**: `/getItemsByCreationTime`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Parameters

#### Query Parameters
| Parameter | Type     | Required | Description                                                                 |
|-----------|----------|----------|-----------------------------------------------------------------------------|
| `from`    | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the start date-time filter.     |
| `to`      | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the end date-time filter.       |

**Example**:
```
GET /getItemsByCreationTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "item_number": "I1234",
      "product_name": "Product Name",
      "search_name": "Search Name",
      "bom_unit": "Unit",
      "item_type": "Type",
      "line_matching_policy": "Policy",
      "project_category": "Category",
      "created_at": "2024-06-01T12:34:56Z",
      "created_by": "Creator",
      "modified_by": "Modifier",
      "modified_at": "2024-06-02T12:34:56Z",
      "price": 100.0,
      "purchase_unit": "Unit",
      "inventory_unit": "Unit",
      "sales_unit": "Unit",
      "item_group": "Group",
      "item_model_group": "Model Group"
    },
    // ... more items
  ]
}
```

#### Error Responses

##### Invalid or Missing `from` or `to`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing from or to. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with `from` and `to`:
```
GET /getItemsByCreationTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
Authorization: Bearer <your-token>
```

---

## Endpoint: `getItemsByUpdateTime`

### Overview
This endpoint retrieves all items that have been updated within a specified date range.

---

### Endpoint Details

- **Method**: `GET`
- **URL**: `/getItemsByUpdateTime`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Parameters

#### Query Parameters
| Parameter | Type     | Required | Description                                                                 |
|-----------|----------|----------|-----------------------------------------------------------------------------|
| `from`    | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the start date-time filter.     |
| `to`      | `string` | Yes      | A UTC timestamp (ISO 8601 format) specifying the end date-time filter.       |

**Example**:
```
GET /getItemsByUpdateTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
```
---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "item_number": "I1234",
      "product_name": "Product Name",
      "search_name": "Search Name",
      "bom_unit": "Unit",
      "item_type": "Type",
      "line_matching_policy": "Policy",
      "project_category": "Category",
      "created_at": "2024-05-01T12:34:56Z",
      "created_by": "Creator",
      "modified_by": "Modifier",
      "modified_at": "2024-06-02T12:34:56Z",
      "price": 100.0,
      "purchase_unit": "Unit",
      "inventory_unit": "Unit",
      "sales_unit": "Unit",
      "item_group": "Group",
      "item_model_group": "Model Group"
    },
    // ... more items
  ]
}
```

#### Error Responses

##### Invalid or Missing `from` or `to`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing from or to. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

### Example Requests

#### Request with `from` and `to`:
```
GET /getItemsByUpdateTime?from=2024-06-01T00:00:00Z&to=2024-06-30T23:59:59Z
Authorization: Bearer <your-token>
```

---

### Endpoint Details

- **Method**: `POST`
- **URL**: `/CreateTransferjournal`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Body

| Parameter                                                        | Type | Required | Description |
|------------------------------------------------------------------|------|----------|-------------|
| `Transferjournal`                                                | `object` | Yes | The transfer journal object |
| `Transferjournal.journalDesc`                                    | `string` | Yes | Description of the transfer journal |
| `Transferjournal.transferJournalId`                              | `string` | Yes | A unique ID for this transfer journal (will be required during posting) |
| `Transferjournal.inventjournalTransLines`                        | `array` | Yes | Array of items to transfer |
| `Transferjournal.inventjournalTransLines[].ItemId`               | `string` | Yes | ID of the item being transferred |
| `Transferjournal.inventjournalTransLines[].FromwMSLocationId`    | `string` | Yes | WMS location ID of the source |
| `Transferjournal.inventjournalTransLines[].Frominventlocationid` | `string` | Yes | Inventory location ID of the source |
| `Transferjournal.inventjournalTransLines[].FrominventSideId`     | `string` | Yes | Inventory site ID of the source |
| `Transferjournal.inventjournalTransLines[].TowMSLocationId`      | `string` | Yes | WMS location ID of the destination |
| `Transferjournal.inventjournalTransLines[].Toinventlocationid`   | `string` | Yes | Inventory location ID of the destination |
| `Transferjournal.inventjournalTransLines[].ToinventSiteId`       | `string` | Yes | Inventory site ID of the destination |
| `Transferjournal.inventjournalTransLines[].Qty`                  | `number` | Yes | Quantity to be transferred |

**Example**:
```json
{
    "Transferjournal":
        {
            "transferJournalId": "TJ12345",
            "journalDesc": "transfer Journal from API",
            "inventjournalTransLines": [
                {
                    "ItemId": "183670",
                    "FromwMSLocationId": "QIDDIYA",
                    "Frominventlocationid": "691",
                    "FrominventSideId": "PEB-JUBAIL",
                    "TowMSLocationId": "Default",
                    "Toinventlocationid": "691",
                    "ToinventSiteId": "PEB-JUBAIL",
                    "Qty": 23
                }
            ]
        }
}
```

---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "message": "Transfer journal created successfully",
  "transferJournalId": "TJ12345"
}
```

#### Error Responses

##### Invalid or Missing Fields
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing fields in the request body."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

## Endpoint: `PostTransferJournal`

### Overview
This endpoint posts a previously created transfer journal using the same transferJournalID that was provided during creation.

---

### Endpoint Details

- **Method**: `POST`
- **URL**: `/PostTransferJournal`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

### Request Body

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `transferJournalId` | `string` | Yes | The unique ID of the transfer journal to post (must match the ID provided in CreateTransferjournal) |

**Example**:
```json
{
  "transferJournalId": "TJ12345"
}
```

---

### Response

#### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "message": "Transfer journal posted successfully",
  "details": {
    "transferJournalId": "TJ12345",
    "postedAt": "2024-07-01T14:32:18Z"
  }
}
```

#### Error Responses

##### Invalid or Missing ID
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid or missing transfer journal ID."
}
```

##### Journal Not Found
**Status Code**: `404 Not Found`

**Response Body**:
```json
{
  "status": "error",
  "message": "Transfer journal with ID TJ12345 not found."
}
```

##### ID Mismatch
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "The provided transferJournalId does not match any previously created journal."
}
```

##### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

##### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```