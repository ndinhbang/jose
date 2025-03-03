# Class: CompactEncrypt

## [💗 Help the project](https://github.com/sponsors/panva)

Support from the community to continue maintaining and improving this module is welcome. If you find the module useful, please consider supporting the project by [becoming a sponsor](https://github.com/sponsors/panva).

---

The CompactEncrypt class is used to build and encrypt Compact JWE strings.

**`Example`**

```js
const jwe = await new jose.CompactEncrypt(
  new TextEncoder().encode('It’s a dangerous business, Frodo, going out your door.'),
)
  .setProtectedHeader({ alg: 'RSA-OAEP-256', enc: 'A256GCM' })
  .encrypt(publicKey)

console.log(jwe)
```

## Table of contents

### Constructors

- [constructor](jwe_compact_encrypt.CompactEncrypt.md#constructor)

### Methods

- [encrypt](jwe_compact_encrypt.CompactEncrypt.md#encrypt)
- [setContentEncryptionKey](jwe_compact_encrypt.CompactEncrypt.md#setcontentencryptionkey)
- [setInitializationVector](jwe_compact_encrypt.CompactEncrypt.md#setinitializationvector)
- [setKeyManagementParameters](jwe_compact_encrypt.CompactEncrypt.md#setkeymanagementparameters)
- [setProtectedHeader](jwe_compact_encrypt.CompactEncrypt.md#setprotectedheader)

## Constructors

### constructor

• **new CompactEncrypt**(`plaintext`)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `plaintext` | [`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) | Binary representation of the plaintext to encrypt. |

## Methods

### encrypt

▸ **encrypt**(`key`, `options?`): [`Promise`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise )\<`string`\>

Encrypts and resolves the value of the Compact JWE string.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | [`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) \| [`KeyLike`](../types/types.KeyLike.md) | Public Key or Secret to encrypt the JWE with. See [Algorithm Key Requirements](https://github.com/panva/jose/issues/210#jwe-alg). |
| `options?` | [`EncryptOptions`](../interfaces/types.EncryptOptions.md) | JWE Encryption options. |

#### Returns

[`Promise`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise )\<`string`\>

___

### setContentEncryptionKey

▸ **setContentEncryptionKey**(`cek`): [`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

Sets a content encryption key to use, by default a random suitable one is generated for the JWE
enc" (Encryption Algorithm) Header Parameter.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cek` | [`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) | JWE Content Encryption Key. |

#### Returns

[`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

**`Deprecated`**

You should not use this method. It is only really intended for test and vector
  validation purposes.

___

### setInitializationVector

▸ **setInitializationVector**(`iv`): [`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

Sets the JWE Initialization Vector to use for content encryption, by default a random suitable
one is generated for the JWE enc" (Encryption Algorithm) Header Parameter.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `iv` | [`Uint8Array`]( https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array ) | JWE Initialization Vector. |

#### Returns

[`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

**`Deprecated`**

You should not use this method. It is only really intended for test and vector
  validation purposes.

___

### setKeyManagementParameters

▸ **setKeyManagementParameters**(`parameters`): [`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

Sets the JWE Key Management parameters to be used when encrypting the Content Encryption Key.
You do not need to invoke this method, it is only really intended for test and vector
validation purposes.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `parameters` | [`JWEKeyManagementHeaderParameters`](../interfaces/types.JWEKeyManagementHeaderParameters.md) | JWE Key Management parameters. |

#### Returns

[`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

___

### setProtectedHeader

▸ **setProtectedHeader**(`protectedHeader`): [`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)

Sets the JWE Protected Header on the CompactEncrypt object.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `protectedHeader` | [`CompactJWEHeaderParameters`](../interfaces/types.CompactJWEHeaderParameters.md) | JWE Protected Header object. |

#### Returns

[`CompactEncrypt`](jwe_compact_encrypt.CompactEncrypt.md)
