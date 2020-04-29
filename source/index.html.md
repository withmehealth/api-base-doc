---
title: API Reference

<!-- language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python -->

toc_footers:
  - <a href='#'>Sign Up for a API Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - rx_claims
  - eligibility
  - errors

search: true
---

# Introduction

> **Base URL:**

```shell
https://api.test.withmehealth.com/api/v1/api
```

This servers as an onboarding and reference document to exchange data with WithMe in a real time manner using WithMe API (Application Programming Interface). This document specifies the URLs’ and the data structures (JSON formats) for various domains along with response codes and contact information.

WithMe will accept two kinds of data formats, flat (WithMe standard) and FHIR. Our implementation team can work with you in exploring options that enables ease-of-use, interoperability, portability meeting client/vendor needs coupled with industry evolution.

# Authentication and header

<blockquote>
    <div class="box">
        <span class="method get">GET</span>
        https://api.test.withmehealth.com/api/v1/api/health
    </div>
</blockquote>

> Authenticated request:

```shell
curl "https://api.test.withmehealth.com/api/v1/api/health"
  -H "API-KEY: ${API-KEY}"
```

Key part of message exchange is the ability to trust and shield. WithMe authentication process is a MFA (multi-factor authentication) based and involves registration, validation and apikey generation.

Every user is expected to go through registration process and after successful registration there will be a unique key generated for that user (apikey) which should be used in all the subsequent calls as part of the header. User authentication and key authentication are a must before continuing to use the API.

<aside class="notice">
To authenticate, please include <code>API-KEY</code> header with your API key in every request.
</aside>

# Domains and actions

Following table summarizes various domains and actions that can be performed by leveraging WithMe APIs.

Domain      | Action
----------- | -------
Eligibility | Create member
RxClaim     | Post RxClaim

# API data structure (JSON)

Request structure is a JSON structure with key/value pairs and is provided below. It contains the following attributes/keys:

 - **Environment:** The environment to which this request should be applied. Possible values include: [&quot;test&quot;, &quot;prod&quot;]
 - **Format:** sender specifies if they would like to use the flat format or the FHIR standard to exchange data
 - **Domain:** specify the domain this request relates to. Possible value set includes: [&quot;eligibility&quot;, &quot;rxclaims&quot;, &quot;medclaims&quot;, &quot;labclaims&quot;, &quot;trialclaims&quot;, &quot;prior auth&quot;, &quot;call center&quot;, &quot;formulary&quot;, &quot;pharmacy&quot;, &quot;benefits&quot;]
 - **Action:** specify what action to take with the request data belonging to the domain
 - **Request:** Request body contains the data relating to the request as key/value pairs and the attributes required for the domain/action are specified in detail in each of the domains.
