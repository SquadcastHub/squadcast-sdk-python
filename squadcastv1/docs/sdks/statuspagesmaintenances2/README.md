# StatuspagesMaintenances2
(*statuspages.maintenances*)

## Overview

### Available Operations

* [get_by_id](#get_by_id) - Get Maintenance By ID

## get_by_id

Get Maintenance By ID

### Example Usage

<!-- UsageSnippet language="python" operationID="Maintenances_getMaintenanceById" method="get" path="/v4/statuspages/{statuspageID}/maintenance/{maintenance_id}" -->
```python
from squadcast_sdk import SquadcastSDK


with SquadcastSDK(
    bearer_auth="<YOUR_BEARER_TOKEN_HERE>",
) as ss_client:

    res = ss_client.statuspages.maintenances.get_by_id(statuspage_id="<id>", maintenance_id="<id>")

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `statuspage_id`                                                     | *str*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `maintenance_id`                                                    | *str*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.MaintenancesGetMaintenanceByIDResponse](../../models/maintenancesgetmaintenancebyidresponse.md)**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.BadRequestError          | 400                             | application/json                |
| errors.UnauthorizedError        | 401                             | application/json                |
| errors.PaymentRequiredError     | 402                             | application/json                |
| errors.ForbiddenError           | 403                             | application/json                |
| errors.NotFoundError            | 404                             | application/json                |
| errors.ConflictError            | 409                             | application/json                |
| errors.UnprocessableEntityError | 422                             | application/json                |
| errors.InternalServerError      | 500                             | application/json                |
| errors.BadGatewayError          | 502                             | application/json                |
| errors.ServiceUnavailableError  | 503                             | application/json                |
| errors.GatewayTimeoutError      | 504                             | application/json                |
| errors.SDKDefaultError          | 4XX, 5XX                        | \*/\*                           |