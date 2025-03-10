# Class: AsyncGzip

Asynchronous streaming GZIP compression

## Table of contents

### Constructors

- [constructor](AsyncGzip.md#constructor)

### Properties

- [ondata](AsyncGzip.md#ondata)
- [terminate](AsyncGzip.md#terminate)

### Methods

- [push](AsyncGzip.md#push)

## Constructors

### constructor

• **new AsyncGzip**(`opts`, `cb?`)

Creates an asynchronous GZIP stream

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | [`GzipOptions`](../interfaces/GzipOptions.md) | The compression options |
| `cb?` | [`AsyncFlateStreamHandler`](../README.md#asyncflatestreamhandler) | The callback to call whenever data is deflated |

• **new AsyncGzip**(`cb?`)

Creates an asynchronous GZIP stream

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `cb?` | [`AsyncFlateStreamHandler`](../README.md#asyncflatestreamhandler) | The callback to call whenever data is deflated |

## Properties

### ondata

• **ondata**: [`AsyncFlateStreamHandler`](../README.md#asyncflatestreamhandler)

The handler to call whenever data is available

___

### terminate

• **terminate**: [`AsyncTerminable`](../interfaces/AsyncTerminable.md)

A method to terminate the stream's internal worker. Subsequent calls to
push() will silently fail.

## Methods

### push

▸ **push**(`chunk`, `final?`): `void`

Pushes a chunk to be GZIPped

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `chunk` | `Uint8Array` | The chunk to push |
| `final?` | `boolean` | Whether this is the last chunk |

#### Returns

`void`
