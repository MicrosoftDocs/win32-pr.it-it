---
title: Funzione D3DX_SRGB_to_FLOAT_inexact
description: Converte un valore SRGB in FLOAT. | Funzione D3DX_SRGB_to_FLOAT_inexact
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- Funzione D3DX_SRGB_to_FLOAT_inexact HLSL
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
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982208"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ sRGB \_ per \_ float- \_ funzione inesatta

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

Questa funzione non ha una precisione sufficientemente elevata per fornire la risposta esatta. La funzione alternativa [**D3DX \_ sRGB \_ per \_ float**](d3dx-srgb-to-float.md) usa una tabella di ricerca per ottenere una conversione esattamente da sRGB a virgola mobile.

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

 

 





