# Function: importX509

## [💗 Help the project](https://github.com/sponsors/panva)

Support from the community to continue maintaining and improving this module is welcome. If you find the module useful, please consider supporting the project by [becoming a sponsor](https://github.com/sponsors/panva).

---

▸ **importX509**\<`KeyLikeType`\>(`x509`, `alg`, `options?`): [`Promise`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise )\<`KeyLikeType`\>

Imports the SPKI from an X.509 string certificate as a runtime-specific public key representation
(KeyObject or CryptoKey).

#### Type parameters

| Name | Type |
| :------ | :------ |
| `KeyLikeType` | extends [`KeyLike`](../types/types.KeyLike.md) = [`KeyLike`](../types/types.KeyLike.md) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x509` | `string` | - |
| `alg` | `string` | (Only effective in Web Crypto API runtimes) JSON Web Algorithm identifier to be used with the imported key, its presence is only enforced in Web Crypto API runtimes. See [Algorithm Key Requirements](https://github.com/panva/jose/issues/210). |
| `options?` | [`PEMImportOptions`](../interfaces/key_import.PEMImportOptions.md) | - |

#### Returns

[`Promise`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise )\<`KeyLikeType`\>

**`Example`**

```js
const algorithm = 'ES256'
const x509 = `-----BEGIN CERTIFICATE-----
MIIBXjCCAQSgAwIBAgIGAXvykuMKMAoGCCqGSM49BAMCMDYxNDAyBgNVBAMMK3Np
QXBNOXpBdk1VaXhXVWVGaGtjZXg1NjJRRzFyQUhXaV96UlFQTVpQaG8wHhcNMjEw
OTE3MDcwNTE3WhcNMjIwNzE0MDcwNTE3WjA2MTQwMgYDVQQDDCtzaUFwTTl6QXZN
VWl4V1VlRmhrY2V4NTYyUUcxckFIV2lfelJRUE1aUGhvMFkwEwYHKoZIzj0CAQYI
KoZIzj0DAQcDQgAE8PbPvCv5D5xBFHEZlBp/q5OEUymq7RIgWIi7tkl9aGSpYE35
UH+kBKDnphJO3odpPZ5gvgKs2nwRWcrDnUjYLDAKBggqhkjOPQQDAgNIADBFAiEA
1yyMTRe66MhEXID9+uVub7woMkNYd0LhSHwKSPMUUTkCIFQGsfm1ecXOpeGOufAh
v+A1QWZMuTWqYt+uh/YSRNDn
-----END CERTIFICATE-----`
const ecPublicKey = await jose.importX509(x509, algorithm)
```
