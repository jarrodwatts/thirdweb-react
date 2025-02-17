<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@thirdweb-dev/react](./react.md) &gt; [useUnclaimedNFTs](./react.useunclaimednfts.md)

## useUnclaimedNFTs() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Use this to get a list of \*unclaimed\* NFT tokens of your ERC721 Drop contract.

<b>Signature:</b>

```typescript
export declare function useUnclaimedNFTs(contract: RequiredParam<NFTDrop>, queryParams?: QueryAllParams): import("@tanstack/react-query").UseQueryResult<{
    [x: string]: import("@thirdweb-dev/sdk/dist/browser").Json;
    name?: string | number | undefined;
    description?: string | null | undefined;
    image?: string | null | undefined;
    external_url?: string | null | undefined;
    animation_url?: string | null | undefined;
    uri: string;
    id: import("ethers").BigNumber;
}[], unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  contract | [RequiredParam](./react.requiredparam.md)<!-- -->&lt;NFTDrop&gt; | an instance of a contract that extends the Erc721 spec (nft drop, custom contract that follows the Erc721 &amp; drop spec) |
|  queryParams | QueryAllParams | <i>(Optional)</i> query params to pass to the query for the sake of pagination |

<b>Returns:</b>

import("@tanstack/react-query").UseQueryResult&lt;{ \[x: string\]: import("@thirdweb-dev/sdk/dist/browser").Json; name?: string \| number \| undefined; description?: string \| null \| undefined; image?: string \| null \| undefined; external\_url?: string \| null \| undefined; animation\_url?: string \| null \| undefined; uri: string; id: import("ethers").BigNumber; }\[\], unknown&gt;

a response object that includes an array of NFTs that are unclaimed

## Example


```javascript
const { data: unclaimedNfts, isLoading, error } = useUnclaimedNFTs(<YourERC721DropContractInstance>, { start: 0, count: 100 });
```

