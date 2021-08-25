---
title: D3DX_INT_to_FLOAT funzione
description: Converte un valore INT in FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d49320c2b7bfd53b2fa4e0303a7d2e9bf6c22427557ee3827aed31f5915d1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855491"
---
# <a name="d3dx_int_to_float-function"></a>Funzione da D3DX \_ INT \_ a \_ FLOAT

Converte un valore INT in FLOAT.

## <a name="syntax"></a>Sintassi

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*\_Presso* 
</dt> <dd>

Valore v.

</dd> <dt>

*\_Scalabilità* 
</dt> <dd>

Valore di scala.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore int convertito.

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

 

 





