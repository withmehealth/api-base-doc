# Pharmacy Claim

## Post RxClaim

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
    "domain": "RxClaim",
    "action": "Post RxClaim",
    "environment": "dev",
    "sender": "ScriptCare",
    "format": "flat",
    "request": {
        "ProductName": "Dorzolamide HCl-Timolol Mal",
        "DrugCategoryCode": "inwork",
        "TransactionStatusType": "P",
        "PrescriberDEA": null,
        "FillNumber": 2,
        "BIN": "004410",
        "PatientPayDeductible": 0,
        "TransactionSequenceNumber": "1",
        "WholesaleAcquiredCost": 4.849,
        "PrescriberAddress": null,
        "ProductDescription": "Dorzolamide HCl-Timolol Mal Ophthalmic Solution 22.3-6.8 MG/ML",
        "PatientDateOfBirth/SubmittedDateOfBirth": "1970-01-01",
        "DispenserNABP": "3425560",
        "ProductMultiSourceCode": "Y",
        "PatientAddress": "123 16th Ave",
        "ApprovedAuthorizationIDReversed": "",
        "PatientLastName": "LASTNAME",
        "MACName": "inwork",
        "RxOriginCode": 3,
        "PatientPayBenefitMax": 0,
        "Plan": "GIVENS ESTATES, INC",
        "TherapeuticClassCode": "inwork",
        "PrescriberSpecialty": "",
        "PrescriberLastName": "CRANDALL",
        "DispenserPhone": 8286968021,
        "PrescriberCity": "ASHEVILLE",
        "FormularyTier": "inwork",
        "TransactionKey": "1340755",
        "PatientRetailCardId": "990463534",
        "DispenserChainID": "229",
        "TransactionNumber": "1UCP40PPN40I",
        "PrescriberFirstName": "JAMES",
        "RxOTCIndicator": "S",
        "PatientPayCoinsurance": 0,
        "FlatSalesTaxAmountPaid": 0,
        "PatientGender": "M",
        "PersonCode": "02",
        "DispenserName": "TEST PHARMACY NAME",
        "NDC": "700690051011",
        "TotalAmountPaid": 20.57,
        "TransactionTimestamp": "2020-04-10T12:24:13",
        "AdjudicatedIngredientCost": 48.32,
        "DAWPenality": "inwork",
        "PrescriberLicense": null,
        "UnitOfMeasure": "MG/ML",
        "Manufacturer": "SOMERSET THERAPEUTICS",
        "PatientPayCoPay": 30,
        "DEAClassCode": null,
        "IncentiveAmountPaid": 0,
        "DMRClaim": "inwork",
        "DaysSupply": 50,
        "StateFeeSchedule": "inwork",
        "RedbookAWP": 0.001,
        "GenericIndicator": "G",
        "LevelOfService": null,
        "ApprovedAuthorizationID": "2010100000653879PBMT",
        "GCN": "inwork",
        "ProductStrength": "22.3-6.8",
        "PharmacistLicense": null,
        "PrescriberZip": "288032493",
        "IngredientCostPaid": 48.32,
        "BasisOfCostDetermination": null,
        "DispenserLicense": "BW5431084",
        "DispenserZip": "28792",
        "TotalCompoundUOM": "ML",
        "MaximumRefills": 2,
        "DrugType": "inwork",
        "DispensingFeePaid": 2.25,
        "DosageFormCode": "SOLN",
        "PCN": "SCL",
        "DiagnosisCode": "inwork",
        "MedispanAWP": 12.26,
        "PrescriberPhone": "8282581586",
        "PrescriberNPI": "1891889135",
        "DateWritten": "2019-08-29",
        "UsualAndCustomaryCharge": 95.55,
        "MaximumAllowableCost": 0.001,
        "MaintenanceInd": "2",
        "DateSubmitted": "2020-04-10T12:24:13",
        "OtherPayorAmountRecognized": 0,
        "PatientCity": "Washington",
        "CarrierCode": "comcast",
        "PriorAuthNumber": null,
        "PrescriberState": "NC",
        "FormularyInd": "inwork",
        "TotalCompoundQuantityDispensed": 10,
        "MACPrice": 0.001,
        "ApprovedFormulary": "inwork",
        "GroupID": "XYZ103",
        "GenericIndicatorOverride": "inwork",
        "DispenserNPI": "1295752442",
        "DispenseAsWrittenCode": "0",
        "RxNumber": "1234567890",
        "FillDate": "2020-04-10",
        "GPI": "86259902202020",
        "MONYCode": "Y",
        "QuantityDispensed": 10,
        "IngredientCostSubmitted": 122.6,
        "MemberPriorAuthNumber": null,
        "PrimaryPrescriberNPI": "1891889135",
        "DispenserState": "NC",
        "DispenserAddress": "250 HIGHLANDS SQUARE DRIVE",
        "Claim Status Indicator": "Paid",
        "PatientZip": "20020",
        "Location": "",
        "OtherAmountPaid": 0,
        "CompoundCode": 1,
        "PatientFirstName": "FIRSTNAME",
        "PharmacistLastname": null,
        "DispenserCity": "HENDERSONVILLE",
        "PercentageSalesTaxAmountPaid": 0,
        "TotalMemberPaid": 30,
        "PatientState": "DC"
    }
}
```

This endpoint creates Pharmacy Claim object.

### HTTP Request

`GET https://api.test.withmehealth.com/api/v1/api/send_message`

### Parameters (in the request property)

Name | Type | Mandatory? | Description
-----| ---- | ---------- | -----------
`ProductName` | `string` | False |
`DrugCategoryCode` | `string` | False |
`TransactionStatusType` | `string` | True |
`PrescriberDEA` | `string` | False |
`FillNumber` | `int` | False |
`BIN` | `string` | False |
`PatientPayDeductible` | `float` | False |
`TransactionSequenceNumber` | `string` | False |
`WholesaleAcquiredCost` | `float` | False |
`PrescriberAddress` | `string` | False |
`ProductDescription` | `string` | False |
`PatientDateOfBirth/SubmittedDateOfBirth` | `string` | False |
`DispenserNABP` | `string` | False |
`ProductMultiSourceCode` | `string` | False |
`PatientAddress` | `string` | False |
`ApprovedAuthorizationIDReversed` | `string` | False |
`PatientLastName` | `string` | False |
`MACName` | `string` | False |
`RxOriginCode` | `int` | False |
`PatientPayBenefitMax` | `float` | False |
`Plan` | `string` | False |
`TherapeuticClassCode` | `string` | False |
`PrescriberSpecialty` | `string` | False |
`PrescriberLastName` | `string` | False |
`DispenserPhone` | `string` | False |
`PrescriberCity` | `string` | False |
`FormularyTier` | `string` | False |
`TransactionKey` | `string` | True |
`PatientRetailCardId` | `string` | True |
`DispenserChainID` | `string` | False |
`TransactionNumber` | `string` | False |
`PrescriberFirstName` | `string` | False |
`RxOTCIndicator` | `string` | False |
`PatientPayCoinsurance` | `float` | False |
`FlatSalesTaxAmountPaid` | `float` | False |
`PatientGender` | `string` | False |
`PersonCode` | `string` | True |
`DispenserName` | `string` | False |
`NDC` | `string` | False |
`TotalAmountPaid` | `float` | False |
`TransactionTimestamp` | `string` | False |
`AdjudicatedIngredientCost` | `float` | False |
`DAWPenality` | `string` | False |
`PrescriberLicense` | `string` | False |
`UnitOfMeasure` | `string` | False |
`Manufacturer` | `string` | False |
`PatientPayCoPay` | `float` | False |
`DEAClassCode` | `string` | False |
`IncentiveAmountPaid` | `float` | False |
`DMRClaim` | `string` | False |
`DaysSupply` | `int` | False |
`StateFeeSchedule` | `string` | False |
`RedbookAWP` | `float` | False |
`GenericIndicator` | `string` | False |
`LevelOfService` | `string` | False |
`ApprovedAuthorizationID` | `string` | False |
`GCN` | `string` | False |
`ProductStrength` | `string` | False |
`PharmacistLicense` | `string` | False |
`PrescriberZip` | `string` | False |
`IngredientCostPaid` | `float` | False |
`BasisOfCostDetermination` | `string` | False |
`DispenserLicense` | `string` | False |
`DispenserZip` | `string` | False |
`TotalCompoundUOM` | `string` | False |
`MaximumRefills` | `int` | False |
`DrugType` | `string` | False |
`DispensingFeePaid` | `float` | False |
`DosageFormCode` | `string` | False |
`PCN` | `string` | False |
`DiagnosisCode` | `string` | False |
`MedispanAWP` | `float` | False |
`PrescriberPhone` | `string` | False |
`PrescriberNPI` | `string` | False |
`DateWritten` | `string` | False |
`UsualAndCustomaryCharge` | `float` | False |
`MaximumAllowableCost` | `float` | False |
`MaintenanceInd` | `string` | False |
`DateSubmitted` | `string` | False |
`OtherPayorAmountRecognized` | `float` | False |
`PatientCity` | `string` | False |
`CarrierCode` | `string` | True |
`PriorAuthNumber` | `string` | False |
`PrescriberState` | `string` | False |
`FormularyInd` | `string` | False |
`TotalCompoundQuantityDispensed` | `int` | False |
`MACPrice` | `float` | False |
`ApprovedFormulary` | `string` | False |
`GroupID` | `string` | True |
`GenericIndicatorOverride` | `string` | False |
`DispenserNPI` | `string` | False |
`DispenseAsWrittenCode` | `string` | False |
`RxNumber` | `string` | False |
`FillDate` | `string` | False |
`GPI` | `string` | False |
`MONYCode` | `string` | False |
`QuantityDispensed` | `int` | False |
`IngredientCostSubmitted` | `float` | False |
`MemberPriorAuthNumber` | `string` | False |
`PrimaryPrescriberNPI` | `string` | False |
`DispenserState` | `string` | False |
`DispenserAddress` | `string` | False |
`Claim Status Indicator` | `string` | False |
`PatientZip` | `string` | False |
`Location` | `string` | False |
`OtherAmountPaid` | `float` | False |
`CompoundCode` | `string` | False |
`PatientFirstName` | `string` | False |
`PharmacistLastname` | `string` | False |
`DispenserCity` | `string` | False |
`PercentageSalesTaxAmountPaid` | `float` | False |
`TotalMemberPaid` | `float` | False |
`PatientState` | `string` | False |

<!-- <aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside> -->

