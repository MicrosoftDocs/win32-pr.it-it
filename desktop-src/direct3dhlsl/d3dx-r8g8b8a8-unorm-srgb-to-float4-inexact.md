---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact funzione
description: Decomprime i dati dello shader DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB in XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact funzione
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede0d10bd8c90514771fa6520eb41e0bd555a3d969b230bb2932665ec0c81796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727346"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>Funzione inesatta da D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB a \_ \_ FLOAT4 \_

Decomprime i dati dello shader DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB in XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*packedInput* 
</dt> <dd>

Dati dello shader di cui è stato effettuato il pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati shader decompressi.

## <a name="remarks"></a>Commenti

Questa funzione usa istruzioni shader che non hanno una precisione sufficiente per fornire la risposta esatta. La funzione alternativa [**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB in \_ \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esatta da SRGB a float.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e impacchettamento del formato DXGI \_ per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





