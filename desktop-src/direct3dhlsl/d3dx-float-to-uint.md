---
title: D3DX_FLOAT_to_UINT funzione
description: Converte un valore FLOAT in UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37665d3630979dee3fad7c109152a852883455f5de40c064faa8f1ea4f0645cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855621"
---
# <a name="d3dx_float_to_uint-function"></a>Funzione da D3DX \_ FLOAT \_ a \_ UINT

Converte un valore FLOAT in UINT.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*\_Presso* 
</dt> <dd>

Vettore v.

</dd> <dt>

*\_Scalabilità* 
</dt> <dd>

Valore di scala.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore FLOAT convertito

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

 

 





