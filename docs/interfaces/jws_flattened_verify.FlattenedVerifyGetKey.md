# Interface: FlattenedVerifyGetKey

## [💗 Help the project](https://github.com/sponsors/panva)

Support from the community to continue maintaining and improving this module is welcome. If you find the module useful, please consider supporting the project by [becoming a sponsor](https://github.com/sponsors/panva).

---

Interface for Flattened JWS Verification dynamic key resolution. No token components have been
verified at the time of this function call.

**`See`**

[createRemoteJWKSet](../functions/jwks_remote.createRemoteJWKSet.md#function-createremotejwkset) to verify using a remote JSON Web Key Set.

## Callable

### FlattenedVerifyGetKey

▸ **FlattenedVerifyGetKey**(`protectedHeader`, `token`): [`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) \| [`KeyLike`](../types/types.KeyLike.md) \| [`Promise`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise )\<[`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) \| [`KeyLike`](../types/types.KeyLike.md)\>

Dynamic key resolution function. No token components have been verified at the time of this
function call.

If you cannot match a key suitable for the token, throw an error instead.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `protectedHeader` | `undefined` \| [`JWSHeaderParameters`](types.JWSHeaderParameters.md) | JWE or JWS Protected Header. |
| `token` | [`FlattenedJWSInput`](types.FlattenedJWSInput.md) | The consumed JWE or JWS token. |

#### Returns

[`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) \| [`KeyLike`](../types/types.KeyLike.md) \| [`Promise`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise )\<[`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) \| [`KeyLike`](../types/types.KeyLike.md)\>
