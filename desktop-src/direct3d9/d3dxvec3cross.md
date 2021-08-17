---
description: Determina il prodotto incrociato di due vettori 3D.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: Funzione D3DXVec3Cross (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3fdf2a5d3c3771056f169900df519d90a183798d6f5c60df0904444dbce5fd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122575"
---
# <a name="d3dxvec3cross-function"></a>Funzione D3DXVec3Cross

Determina il prodotto incrociato di due vettori 3D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il prodotto incrociato di due vettori 3D.

## <a name="remarks"></a>Commenti

Questa funzione determina il prodotto incrociato con il codice seguente.


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec3Cross** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Dot**](d3dxvec3dot.md)
</dt> </dl>

 

 




