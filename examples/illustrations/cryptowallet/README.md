<!--
GENERATED FILE

README.md is generated from a template file, src/README.md.in, and JSON snippets under src/.  If you need to revise narrative text, edit src/README.md.in.  If you need to revise data, please find and revise the containing snippet.  Editing patterns follow the patterns described in the CASE website's CONTRIBUTE.md:
https://github.com/casework/casework.github.io/blob/master/CONTRIBUTE.md#maintenance-of-generated-files
-->


# Cryptowallet and Cryptoaddress Examples

This illustration includes example investigative questions involving cryptowallets and cryptoaddresses.


## Disclaimer

Participation by NIST in the creation of the documentation of mentioned software is not intended to imply a recommendation or endorsement by the National Institute of Standards and Technology, nor is it intended to imply that any specific software is necessarily the best available for the purpose.


## Example representations

The proposed representation of cryptoaddress is illustrated using the seizure of assets from BitCoin address 1HQ3Go3ggs8pFnXuHVHRytPCq5fGG8Hbhx related to the Silk Road marketplace
Reference: https://www.justice.gov/usao-ndca/press-release/file/1334771/download

```json
       {
            "@id": "kb:1de3-f681-4bc6-a66e-b70a7ecdb3a5",
            "@type": "uco-observable:ObservableObject",
            "uco-core:hasFacet": [
                {
                    "@type": "drafting:CryptoAddressFacet",
                    "drafting:addressValue": "1HQ3Go3ggs8pFnXuHVHRytPCq5fGG8Hbhx",
                    "drafting:cryptoCurrencyType": "BitCoin",
                    "drafting:cryptoAddressFormat": "P2PKH",
                    "drafting:cryptoAddressCreatedTime": {
                        "@type": "xsd:dateTime",
                        "@value": "2013-04-09T17:03:36Z"
                    },
                    "drafting:cryptoCurrencyCompletedTransactionCount": "260",
                    "drafting:cryptoCurrencyBalance": {
                        "@id": "kb:cryptocurrency-sent-9301548a-a60e-41a8-8cb6-27a748639850"
                    }
                }
            ]
        }
```

An example of cryptowallet and cryptoaddress related to the investigation of the Silk Road marketplace and the BitCoin address 127B3qwztPyA67uq63LG8G5izwhFcJ7j4A associated with Shaun Bridges.
Reference: https://btc.com/btc/search/127B3qwztPyA67uq63LG8G5izwhFcJ7j4A:

```json
[
    {
        "@id": "kb:wallet-426a-0be4-db43-a66e-c43b6edc6b3a",
        "@type": "uco-observable:ObservableObject",
        "uco-core:hasFacet": [
            {
                "drafting:cryptoWalletIdentifier": "73108d1b19",
                "@type": "drafting:CryptoWalletFacet",
                "drafting:cryptoWalletAddress": {
                    "@id": "kb:cryptoaddress-9de3-a681-db43-a66e-b70a7ecc4a2e"
                },
                "drafting:cryptoWalletName": "Jane Doe",
                "drafting:cryptoWalletCreatedTime": {
                    "@type": "xsd:dateTime",
                    "@value": "2022-01-25T18:37:52Z"
                }
            }
        ]
    }
]
```


The relationship between cryptoAddresses and the verified owner can be represented as follows:

```json
       {
            "@id": "kb:cryptoaddress-ownedby-relationship-uuid",
            "@type": "uco-core:Relationship",
            "uco-core:source": {
                "@id": "kb:cryptoAddress1-uuid"
            },
            "uco-core:target": {
                "@id": "kb:ShaunBridgesIdentity-uuid"
            },
            "uco-core:kindOfRelationship": "Owned_By",
            "uco-core:isDirectional": true
        },
```
