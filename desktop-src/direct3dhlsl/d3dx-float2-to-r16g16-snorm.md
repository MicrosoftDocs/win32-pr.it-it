---
title: D3DX_FLOAT2_to_R16G16_SNORM funzione
description: Racchiude L'oggetto XMFLOAT2 specificato in uno SNORM DXGI \_ FORMAT \_ R16G16. \_
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9ad7d4ff95113d4d684cba7cc348c2d60a536e12171afa6ad421724a668e63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025001"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>Funzione SNORM da D3DX FLOAT2 a \_ \_ \_ R16G16 \_

Racchiude L'oggetto XMFLOAT2 specificato in uno SNORM DXGI \_ FORMAT \_ R16G16. \_

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Dati shader decompressi.

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

 

 





