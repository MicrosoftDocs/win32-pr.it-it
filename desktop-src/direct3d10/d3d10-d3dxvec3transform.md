---
description: 'Funzione D3DXVec3Transform (D3DX10Math.h): trasforma il vettore (x, y, z, 1) in base a una determinata matrice.'
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: Funzione D3DXVec3Transform (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9b5cd69ce603f56e4837818cac6ee18fe3ab1e53
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108139"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a>Funzione D3DXVec3Transform (D3DX10Math.h)

Trasforma il vettore (x, y, z, 1) in base a una determinata matrice.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore alla [**struttura D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore all'oggetto [**D3DXVECTOR3 di origine.**](d3d10-d3dxvector3.md)

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a una struttura D3DXVECTOR4 che rappresenta il vettore trasformato.

## <a name="remarks"></a>Commenti

Questa funzione trasforma il vettore, pV (x, y, z, 1), in base alla matrice pM.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXVec3Transform può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
