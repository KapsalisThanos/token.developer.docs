# API reference

## 📁 Collection: Notarization

### End-point: Stamping a hash

#### Description: Creates a timestamp for a given SHA-256 hash hexadecimal digest. Please note that POST requests must include the Content-Type: application/json header.

The response is JSON-encoded object containing the ID and the time of the stamp. The receipt object gives an estimated time in seconds for the different receipt types \(ethereum and bitcoin\) to be ready for retrieval. Method: POST

> ```text
> http://api.ledgerproject.eu/stamp
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

#### 🔑 Authentication bearer

| Param | value | Type |
| :--- | :--- | :--- |
| token | eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1NTAwMzM1NzksInVzZXJuYW1lIjoiam9yZ2U3NzMiLCJvcmdOYW1lIjoiT3JnMSIsImlhdCI6MTU0OTk5NzU3OX0.JZOoLBO5Jq5ed-2PUYctboVdxcLVm3kdGdpdAhTcADU | string |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: SignUp

#### Description: Creates a timestamp for a given SHA-256 hash hexadecimal digest. Please note that POST requests must include the Content-Type: application/json header.

The response is JSON-encoded object containing the ID and the time of the stamp. The receipt object gives an estimated time in seconds for the different receipt types \(ethereum and bitcoin\) to be ready for retrieval. Method: POST

> ```text
> {{protocol}}://{{host}}:{{port}}/{{services.notarization}}/users
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

#### 🔑 Authentication noauth

| Param | value | Type |
| :--- | :--- | :--- |


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: Retrieving all stamps

#### Description: Retrieves all stamps made by the requesting client, ordered by date, from newest to oldest, paginated in chunks of 50.

You can add ?page=N at the end of the URL in order to show the Nth page. If N is not specified, it is assumed to be 0 and therefore the last 50 stamps are returned.

The response is a JSON-encoded object containing an array of stamps. If a certain receipt found inside a stamp is a number instead of an object, that number is the estimated number of seconds before the final receipt will be ready. Method: GET

> ```text
> {{protocol}}://{{host}}:{{port}}/{{services.notarization}}/stamps
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: blockinfos transactionID

#### Description: Retrieves all stamps made by the requesting client, ordered by date, from newest to oldest, paginated in chunks of 50.

You can add ?page=N at the end of the URL in order to show the Nth page. If N is not specified, it is assumed to be 0 and therefore the last 50 stamps are returned.

The response is a JSON-encoded object containing an array of stamps. If a certain receipt found inside a stamp is a number instead of an object, that number is the estimated number of seconds before the final receipt will be ready. Method: GET

> ```text
> {{protocol}}://{{host}}:{{port}}/{{services.notarization}}/blockinfos/transactions/582dfec2972af002022b1a84e0fe2605464846233f4c05edc4e91825f143b9c0
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: blockinfos blockHash

#### Description: Retrieves all stamps made by the requesting client, ordered by date, from newest to oldest, paginated in chunks of 50.

You can add ?page=N at the end of the URL in order to show the Nth page. If N is not specified, it is assumed to be 0 and therefore the last 50 stamps are returned.

The response is a JSON-encoded object containing an array of stamps. If a certain receipt found inside a stamp is a number instead of an object, that number is the estimated number of seconds before the final receipt will be ready. Method: GET

> ```text
> http://api.ledgerproject.eu/blockinfos/blocks/hash/48815dc12e627f5ccaea4106a9255a277a95b7c87d5a64d6fb04cc634ba8d4d3
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: blockinfos blockID

#### Description: Retrieves all stamps made by the requesting client, ordered by date, from newest to oldest, paginated in chunks of 50.

You can add ?page=N at the end of the URL in order to show the Nth page. If N is not specified, it is assumed to be 0 and therefore the last 50 stamps are returned.

The response is a JSON-encoded object containing an array of stamps. If a certain receipt found inside a stamp is a number instead of an object, that number is the estimated number of seconds before the final receipt will be ready. Method: GET

> ```text
> {{protocol}}://{{host}}:{{port}}/{{services.notarization}}/blockinfos/blocks/3
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: blockinfos

#### Description: Retrieves all stamps made by the requesting client, ordered by date, from newest to oldest, paginated in chunks of 50.

You can add ?page=N at the end of the URL in order to show the Nth page. If N is not specified, it is assumed to be 0 and therefore the last 50 stamps are returned.

The response is a JSON-encoded object containing an array of stamps. If a certain receipt found inside a stamp is a number instead of an object, that number is the estimated number of seconds before the final receipt will be ready. Method: GET

> ```text
> {{protocol}}://{{host}}:{{port}}/{{services.notarization}}/blockinfos/stamp/keys/blablabla
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

### End-point: Retrieving receipts for a stamp

#### Description: Retrieves all receipts \(also known as proofs in former Stampery API versions\) for a certain stamp.

The response is a JSON-encoded object containing an array of stamps. If a certain receipt found inside a stamp is a number instead of an object, that number is the estimated number of seconds before the final receipt will be ready. Method: GET

> ```text
> {{protocol}}://{{host}}:{{port}}/{{services.notarization}}/stamp/2f3f3a85340bde09b505b0d37235d1d32a674e43a66229f9a205e7d8d5328ed1
> ```
>
> #### Headers

| Content-Type | Value |
| :--- | :--- |
| Content-Type | application/x-www-form-urlencoded |

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃
