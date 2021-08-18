---
title: D3DX_SRGB_to_FLOAT_inexact funzione
description: Converte un valore SRGB in FLOAT. | D3DX_SRGB_to_FLOAT_inexact funzione
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515692"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>Funzione inesatta da D3DX \_ SRGB \_ \_ a FLOAT \_

Converte un valore SRGB in FLOAT.

## <a name="syntax"></a>Sintassi

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Val* 
</dt> <dd>

Valore SRGB da convertire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore SRGB convertito.

## <a name="remarks"></a>Commenti

Questa funzione non ha una precisione sufficientemente elevata da fornire la risposta esatta. La funzione alternativa [**da D3DX \_ SRGB \_ \_**](d3dx-srgb-to-float.md) a FLOAT usa una tabella di ricerca per fornire una conversione esatta da SRGB a float.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





