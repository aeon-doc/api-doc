# Brief Description

This API can parse the QR code and return the corresponding payment account information.

# API Description

Request Method:`POST`

Request Path:`open/ai/scanCode`

# Parameters

| Parameter Name | Signature Required | Required | Type   | Length | Description    |
| -------------- | ------------------ | -------- | ------ | ------ | -------------- |
| appId          | Yes                | Yes      | string | 64     | appId          |
| sign           | Yes                | Yes      | string | 512    | Signature      |
| qrCode         | Yes                | Yes      | string | 512    | QR Code String |

# Request Example

```json
{
    "appId": "TEST000001",
    "sign": "TEST000001",
    "qrCode": "00020101021138560010A0000007270126000697041501121170028740400208QRIBFTTA53037045802VN63048A1C"
}
```

# Response Parameters

| Parameter Name | Type    | Description      |
| -------------- | ------- | ---------------- |
| success        | boolean | Success flag     |
| error          | boolean | Error flag       |
| code           | long    | Response code    |
| msg            | string  | Response message |
| traceId        | string  | traceId          |
| model          | object  | Response content |

## model Response Parameters

| Parameter Name    | Type   | Description          | Required |
| ----------------- | ------ | -------------------- | -------- |
| bankAccountName   | string | Bank account name    | Yes      |
| bankAccountNumber | string | Bank account number  | Yes      |
| bankCode          | string | Bank code            | Yes      |
| bankName          | string | Bank name            | Yes      |
| currency          | string | Currency             | Yes      |
| amount            | string | Amount (in currency) | No       |

# Response Example

```json
{
  "code": "0",
  "msg": "success",
  "model": {
    "bankAccountName": "NGUYEN MINH HANH",
    "bankAccountNumber": "888812345678",
    "bankCode": "Techcombank",
    "bankName": "bankName",
    "currency": "VND",
    "amount": "100000"
  },
  "traceId": "6668024eeb989c77a375967aded5d646",
  "success": true,
  "error": false
}
```