---
description: Restituisce il componente z prendendo il prodotto incrociato di due vettori 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Funzione D3DXVec2CCW (D3dx9math. h)
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
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322565"
---
# <a name="d3dxvec2ccw-function"></a>D3DXVec2CCW (funzione)

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

*pV1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Componente z.

## <a name="remarks"></a>Commenti

Questa funzione determina il componente z determinando il prodotto incrociato in base alla formula seguente: ((x1, Y1, 0) Cross (X2, Y2, 0)). O come illustrato nell'esempio seguente.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Se il valore del componente z è positivo, il vettore V2 è in senso antiorario rispetto al vettore v1. Queste informazioni sono utili per l'abbattimento del back-face.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
