# Eligibility

## Create Member

<blockquote>
    <div class="box">
        <span class="method post">POST</span>
        https://api.test.withmehealth.com/api/v1/api/send_message
    </div>
</blockquote>

```shell
curl "https://api.test.withmehealth.com/api/v1/api/send_message"
  -X POST
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "API-KEY: ${API-KEY}"
  --data "${JSON_PAYLOAD}"
```

> Example JSON Payload:

```json
{
    "action": "Create Member",
    "domain": "Eligibility",
    "sender": "ScriptCare",
    "environment": "dev",
    "format": "flat",
    "request": {
        "client": "scriptcare",
        "group": "XYZ103",
        "subscribernum": "WTME123456",
        "personcode": "02",
        "lastname": "John",
        "firstname": "Doe",
        "mi": null,
        "dob": "1990-12-26",
        "gender": "F",
        "addr1": "123 Main St",
        "addr2": "Apt 99",
        "city": "San Francisco",
        "state": "CA",
        "zip": "94020",
        "cellphone": "1234567890",
        "startdt": "2019-01-01",
        "enddt": "2019-12-31",
        "status": "active"
    }
}
```

This endpoint creates Patient, Person and Coverage objects.

### HTTP Request

`GET https://api.test.withmehealth.com/api/v1/api/send_message`

### Parameters (in the request property)

Name | Type | Mandatory? | Description
-----| ---- | ---------- | -----------
`client` | `string` | True | Client name
`group` | `string` | True | Group ID
`subscribernum` | `string` | True | Subscriber ID
`personcode` | `string` | True | Person code
`lastname` | `string` | True | Member's lastname
`firstname` | `string` | True |  Member's firstname
`mi` | `string` | False |  Member's middle initial
`dob` | `string` | True | Member's date of birth
`gender` | `string` | True | Member's gender
`addr1` | `string` | True | Member's address line 1
`addr2` | `string` | False | Member's address line 2
`city` | `string` | True | Member's city
`state` | `string` | True | Member's state
`zip` | `string` | True | Member's zipcode
`cellphone` | `string` | True | Member's cell phone
`homephone` | `string` | False | Member's home phone
`workphone` | `string` | False | Member's work phone
`startdt` | `string` | True | Member's coverage start date
`enddt` | `string` | False | Member's coverage end date
`status` | `string` | True | Member's coverage status

<!-- <aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside> -->
