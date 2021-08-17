---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact funzione
description: Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB in XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact funzione
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact funzione HLSL
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
ms.openlocfilehash: f696381402d8ad42c92310029631e66b457e3b211d22d8f9de3dd98c1f1312ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986871"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>Funzione inesatta da D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ \_ a FLOAT3 \_

Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB in XMFLOAT3.

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

Dati dello shader di cui è stato effettuato il pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati shader decompressi.

## <a name="remarks"></a>Commenti

Questa funzione usa istruzioni shader che non hanno una precisione sufficiente per fornire la risposta esatta. La funzione alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB in \_ \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esatta da SRGB a float.

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

 

 





