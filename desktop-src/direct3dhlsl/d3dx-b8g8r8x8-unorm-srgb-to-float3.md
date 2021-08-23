---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 funzione
description: Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB in XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 funzione
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5f638d827a7b6ebf3543b3cde212fd56b0ace41ffb69bf4b7f79b56c28dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793857"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>Da D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ alla funzione \_ FLOAT3

Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB in XMFLOAT3.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e impacchettamento del formato DXGI \_ per In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





