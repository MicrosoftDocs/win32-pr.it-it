---
title: Funzione D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8A8 UNORM \_ sRGB shader in un XMFLOAT4. | Funzione D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- Funzione D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995789"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ float4 \_ unexact Function

Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8A8 UNORM \_ sRGB shader in un XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

Questa funzione Usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta. La funzione alternativa [**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ a \_ float4**](d3dx-r10g10b10a2-unorm-to-float4.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esattamente da sRGB a virgola mobile.

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

 

 





