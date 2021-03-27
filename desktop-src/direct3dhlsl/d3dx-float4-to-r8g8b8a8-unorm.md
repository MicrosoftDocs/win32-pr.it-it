---
title: Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM shader in un XMFLOAT4. | Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762323"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a>D3DX \_ float4 \_ to \_ R8G8B8A8 \_ UNORM Function

Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM shader in un XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
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

 

 





