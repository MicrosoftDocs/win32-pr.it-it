---
description: Mappe gli indici nell'intervallo da 0 a 255 per gli stati di trasformazione corrispondenti.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: D3DTS_WORLDMATRIX macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 03a93753790378a7066f4a3ffa6bc6b7fb8139b77f9096886161013653312bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850061"
---
# <a name="d3dts_worldmatrix-macro"></a>Macro D3DTS \_ WORLDMATRIX

Mappe gli indici nell'intervallo da 0 a 255 per gli stati di trasformazione corrispondenti.

## <a name="syntax"></a>Sintassi


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* 
</dt> <dd>

Valore di indice compreso tra 0 e 255.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

[**D3DTRANSFORMSTATETYPE mappato**](./d3dtransformstatetype.md) all'indice *specificato.*

## <a name="remarks"></a>Commenti

Gli stati di trasformazione nell'intervallo da 256 a 511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate usando indici a 8 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
