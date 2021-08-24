---
description: Restituisce il componente z prendendo il prodotto incrociato di due vettori 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Funzione D3DXVec2CCW (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b38adaf28b6e2394608cfb6f73f4a39d803d4fd5106f826d810a5c8dfd02618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630701"
---
# <a name="d3dxvec2ccw-function"></a>Funzione D3DXVec2CCW

Restituisce il componente z prendendo il prodotto incrociato di due vettori 2D.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Componente z.

## <a name="remarks"></a>Commenti

Questa funzione determina il componente z determinando il prodotto incrociato in base alla formula seguente: ((x1,y1,0) cross (x2,y2,0)). Oppure, come illustrato nell'esempio seguente.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Se il valore del componente z è positivo, il vettore V2 è in senso antiorario rispetto al vettore V1. Queste informazioni sono utili per il back-face culling.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
