---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM funzione
description: Racchiude L'oggetto XMFLOAT3 specificato in un UINT UNORM DXGI \_ FORMAT \_ B8G8R8X8. \_
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee8da37854e78abb09e8d6781453d47cf3abed43847a96fe09b7d637e52ca429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516379"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a>Funzione UNORM da D3DX FLOAT3 a \_ \_ \_ B8G8R8X8 \_

Racchiude L'oggetto XMFLOAT3 specificato in un UINT UNORM DXGI \_ FORMAT \_ B8G8R8X8. \_

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
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

[Decompressione e impacchettamento del formato DXGI \_ per In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





