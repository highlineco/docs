# Employments

## Get user's employments

```shell
curl -X GET https://api.highline.co/users/ae16efec-d1.../employments \
  -H "Authorization Bearer: AccessToken" \
  -H "Content-Type: application/json"
```

> <div class="code-block-title">Response</div>

```json
[{
  "id": "d6b10b60-55...",
  "user_id": "ae16efec-d1...",
  "employer_id": "d5b6c756-f9...",
  "employer": {
    "id": "d5b6c756-f9...",
    "name": "Kroger"
  },
  "job_title": "1635 - Helpline Agent",
  "start_date": 1393924766,
  "end_date": 1636225502,
  "base_pay": 25599,
  "base_annual_income": 25599,
  "pay_cycle": "weekly",
  "pay_currency": "USD",
  "type": "full-time",
  "status": "active",
  "created_at": 1633633503,
  "updated_at": 1633633503
}]
```

The user employment API provides key details on your users' employment information. This data is provided from our payroll provider and employer partners, and gives a full view into the individual’s employment status, tenure, and other key details.

### HTTP Request

`GET https://api.highline.co/users/{id}/employments`

### Parameters

Name | Type | In | Description
--------- | ------- | ------- | ------
`id` *required* | string | path | User id

### Response

Parameter | Type | Description
--------- | ------- | -----------
`id` | string | Employment ID
`user_id` | string | User ID
`employer_id` | string | Employer ID
`employer` | json | Employer object
`job_title` | string | Current job title
`start_date` | timestamp | Date that this employment started
`end_date` | timestamp | Date employment ended (if ended)
`base_pay` | int | Value used as base of payment (in cents)
`base_annual_income` | int | Value paid annually (in cents)
`pay_cycle` | string | Frequency interval that user receives payments
`pay_currency` | string | Currency
`type` | string | Type of job ("full-time" "part-time" "contractor" "seasonal" "temporary" "other")
`status` | string | Status of employment ("active" "inactive" "terminated")


## Get employment

```shell
curl -X GET https://api.highline.co/employments/d6b10b60-55... \
  -H "Authorization Bearer: AccessToken" \
  -H "Content-Type: application/json"
```

> <div class="code-block-title">Response</div>

```json
{
  "id": "d6b10b60-55...",
  "user_id": "ae16efec-d1...",
  "employer_id": "d5b6c756-f9...",
  "employer": {
    "id": "d5b6c756-f9...",
    "name": "Kroger",
  },
  "job_title": "1635 - Helpline Agent",
  "start_date": 1393924766,
  "end_date": 1636225502,
  "base_pay": 25599,
  "base_annual_income": 25599,
  "pay_cycle": "weekly",
  "pay_currency": "USD",
  "type": "full-time",
  "status": "active",
  "created_at": 1633633503,
  "updated_at": 1633633503
}
```

This API endpoint returns the employment details based on the provided employment id.

### HTTP Request

`GET https://api.highline.co/employments/{id}`

### Parameters

Name | Type | In | Description
--------- | ------- | ------- | ------
`id` *required* | string | path | Employment id

### Response

Parameter | Type | Description
--------- | ------- | -----------
`id` | string | Employment ID
`user_id` | string | User ID
`employer_id` | string | Employer ID
`employer` | json | Employer object
`job_title` | string | Current job title
`start_date` | timestamp | Date that this employment started
`end_date` | timestamp | Date employment ended (if ended)
`base_pay` | int | Value used as base of payment (in cents)
`base_annual_income` | int | Value paid annually (in cents)
`pay_cycle` | string | Frequency interval that user receives payments
`pay_currency` | string | Currency
`type` | string | Type of job ("full-time" "part-time" "contractor" "seasonal" "temporary" "other")
`status` | string | Status of employment ("active" "inactive" "terminated")
