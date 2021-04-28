---
description: 'Funzione D3DXVec2TransformCoord (D3DX10Math.h): trasforma un vettore 2D in base a una determinata matrice, proiettando di nuovo il risultato in w = 1.'
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Funzione D3DXVec2TransformCoord (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 95321d377ad5af29075764e2c2d9386abf5b1441
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108339"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a>Funzione D3DXVec2TransformCoord (D3DX10Math.h)

Trasforma un vettore 2D in base a una determinata matrice, proiettando il risultato in w = 1.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore [**all'oggetto D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore alla struttura D3DXVECTOR2 di origine.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore a una struttura D3DXVECTOR2 che rappresenta il vettore trasformato.

## <a name="remarks"></a>Commenti

Questa funzione trasforma il vettore, pV (x, y, 0, 1), dalla matrice, pM, proiettando di nuovo il risultato in w=1.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXVec2TransformCoord può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
