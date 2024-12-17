# API Documentation

## Endpoint: `getConfirmedPOs`

## Overview
This endpoint retrieves all confirmed Purchase Orders (POs) that have been updated after a specified `startingTime`. If no `startingTime` is provided, the endpoint will return all confirmed POs.

---

## Endpoint Details

- **Method**: `GET`
- **URL**: `/getConfirmedPOs`
- **Authentication**: Required (Bearer Token)
- **Content-Type**: `application/json`

---

## Request Parameters

### Query Parameters
| Parameter      | Type     | Required | Description                                                                 |
|----------------|----------|----------|-----------------------------------------------------------------------------|
| `startingTime` | `string` | No       | A UTC timestamp (ISO 8601 format) specifying the starting date-time filter. |

**Example**:
```
GET /getConfirmedPOs?startingTime=2024-06-01T00:00:00Z
```

If no `startingTime` is provided, the endpoint will return all confirmed POs.

---

## Response

### Success Response
**Status Code**: `200 OK`

**Response Body**:
```json
{
  "status": "success",
  "data": [
    {
      "id": "PO12345",
      "projID": "P1234",
      "updatedAt": "2024-06-02T12:34:56Z",
      "vendorID": "V1234"
      // ... Remaining Fields
    },
    // ... more POs
  ]
}
```

### Error Responses

#### Invalid `startingTime`
**Status Code**: `400 Bad Request`

**Response Body**:
```json
{
  "status": "error",
  "message": "Invalid startingTime format. Use ISO 8601 format (e.g., 2024-06-01T00:00:00Z)."
}
```

#### Unauthorized Access
**Status Code**: `401 Unauthorized`

**Response Body**:
```json
{
  "status": "error",
  "message": "Unauthorized. Please provide a valid Bearer Token."
}
```

#### Internal Server Error
**Status Code**: `500 Internal Server Error`

**Response Body**:
```json
{
  "status": "error",
  "message": "An unexpected error occurred. Please try again later."
}
```

---

## Example Requests

### Request with `startingTime`:
```
GET /getConfirmedPOs?startingTime=2024-06-01T00:00:00Z
Authorization: Bearer <your-token>
```

### Request without `startingTime`:
```
GET /getConfirmedPOs
Authorization: Bearer <your-token>
```

---

## Example Response

**Example Success Response**:
```json
{
  "status": "success",
  "data": [
    {
      "id": "PO12345",
      "projID": "P1234",
      "updatedAt": "2024-06-02T12:34:56Z",
      "vendorID": "V1234"
      // ... Remaining Fields
    },
    // ... more POs
  ]
}
