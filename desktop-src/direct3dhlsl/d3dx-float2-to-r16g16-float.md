---
title: D3DX_FLOAT2_to_R16G16_FLOAT funzione
description: Racchiude l'oggetto XMFLOAT2 specificato in un float DXGI \_ FORMAT \_ R16G16. \_
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- D3DX_FLOAT2_to_R16G16_FLOAT funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f96d9c2652966ef4b35f4c07ec13d1ea5b6f92af641c2e86a1bf4e0b12ca4487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516607"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a>Funzione FLOAT da D3DX \_ FLOAT2 \_ a \_ R16G16 \_ FLOAT

Racchiude l'oggetto XMFLOAT2 specificato in un float DXGI \_ FORMAT \_ R16G16. \_

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Dati dello shader decompressi.

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

[Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place delle immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





