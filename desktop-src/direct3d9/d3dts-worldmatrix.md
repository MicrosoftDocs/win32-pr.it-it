---
description: Esegue il mapping degli indici nell'intervallo compreso tra 0 e 255 e gli Stati di trasformazione corrispondenti.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: D3DTS_WORLDMATRIX macro (D3d9types. h)
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
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530876"
---
# <a name="d3dts_worldmatrix-macro"></a>D3DTS \_ WORLDMATRIX-macro

Esegue il mapping degli indici nell'intervallo compreso tra 0 e 255 e gli Stati di trasformazione corrispondenti.

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

[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) che esegue il mapping all' *Indice* specificato.

## <a name="remarks"></a>Commenti

Gli Stati di trasformazione nell'intervallo compreso tra 256 e 511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate tramite indici a 8 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
