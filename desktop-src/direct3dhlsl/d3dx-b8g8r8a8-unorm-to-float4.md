---
title: Funzione D3DX_B8G8R8A8_UNORM_to_FLOAT4
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8A8 UNORM shader in un XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- Funzione D3DX_B8G8R8A8_UNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bca17f350d40b1f74884232da9d1250bdb0abd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982115"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ to \_ float4 Function

Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8A8 UNORM shader in un XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*packedInput* 
</dt> <dd>

Dati dello shader compressi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati dello shader decompressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





