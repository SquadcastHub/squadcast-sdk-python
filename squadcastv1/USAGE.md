<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
from openapi import SquadcastSDK


with SquadcastSDK(
    bearer_auth="<YOUR_BEARER_TOKEN_HERE>",
) as squadcast_sdk:

    res = squadcast_sdk.analytics.get_org_analytics(from_="<value>", to="<value>")

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from openapi import SquadcastSDK

async def main():

    async with SquadcastSDK(
        bearer_auth="<YOUR_BEARER_TOKEN_HERE>",
    ) as squadcast_sdk:

        res = await squadcast_sdk.analytics.get_org_analytics_async(from_="<value>", to="<value>")

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->