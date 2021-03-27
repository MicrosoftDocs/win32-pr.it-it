---
title: Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT3. | Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- Funzione D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982112"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 \_ unexact Function

Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT3.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
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

## <a name="remarks"></a>Commenti

Questa funzione Usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta. La funzione alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esattamente da sRGB a virgola mobile.

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

 

 





