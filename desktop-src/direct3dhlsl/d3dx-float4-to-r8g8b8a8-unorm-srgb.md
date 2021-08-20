---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB funzione
description: Racchiude L'oggetto XMFLOAT4 specificato in un formato DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e930935e34ff1aa76c99949949e12b5c57254eeea59262cf2ec7828482965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516279"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a>Funzione SRGB DA D3DX FLOAT4 a \_ \_ \_ R8G8B8A8 \_ UNORM \_

Racchiude L'oggetto XMFLOAT4 specificato in un formato DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Dati shader da imballare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati dello shader di cui è stato effettuato il pacchetto.

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

 

 





