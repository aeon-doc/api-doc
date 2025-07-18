# Brief Description

This API processes payments using the uploaded QR code string.

# API Description

Request Method:`POST`

Request Path:`open/ai/scan/payment`

## Parameters

| Parameter Name | Signature Required | Required | Type   | Length | Description         |
| -------------- | ------------------ | -------- | ------ | ------ | ------------------- |
| appId          | Yes                | Yes      | string | 64     | appId               |
| sign           | No                 | Yes      | string | 512    | Signature           |
| qrCode         | Yes                | Yes      | string | 512    | QR Code String      |
| amount         | Yes                | Yes      | string | 20     | Amount              |
| address        | Yes                | NO       | string | 64     | User wallet address |

## Request Example

```json
{
    "appId": "TEST000001",
    "sign": "TEST000001",
    "amount": "100000",
    "qrCode": "00020101021138580010A000000727012800069704070114190360421800120208QRIBFTTA53037045802VN830084006304EDC5",
	"address": "0x1BC48a3a17dD27C7Ee294Ab679638F6C6583B7Bf",
}
```

## Response Parameters

| Parameter Name | Type    | Description      |
| -------------- | ------- | ---------------- |
| success        | boolean | Success flag     |
| error          | boolean | Error flag       |
| code           | long    | Response code    |
| msg            | string  | Response message |
| traceId        | string  | traceId          |
| model          | object  | Response content |

## Response Example

```json
{
  "code": "0",
  "msg": "success",
  "model": {},
  "traceId": "6668024eeb989c77a375967aded5d646",
  "success": true,
  "error": false
}
```