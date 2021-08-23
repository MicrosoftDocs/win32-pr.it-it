---
title: D3DX_UINT2_to_R16G16_UINT funzione
description: Racchiude L'oggetto XMUINT2 specificato in un UINT DXGI \_ FORMAT \_ R16G16. \_
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- D3DX_UINT2_to_R16G16_UINT funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31d938f74874748715a0e90e4eace54f222699b61fbb4655238b2ebca8ace7ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986795"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a>Funzione UINT da D3DX \_ a \_ \_ R16G16 \_

Racchiude L'oggetto XMUINT2 specificato in un UINT DXGI \_ FORMAT \_ R16G16. \_

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
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

 

 





