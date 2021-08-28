---
description: "Funzione D3DXIntersectTri (D3DX10math.h): calcola l'intersezione di un raggio e di un triangolo."
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Funzione D3DXIntersectTri (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 29f0ae90c8a6fee1f675a6128fce1b2b8276490f61e93e707e5471f734449b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853391"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a>Funzione D3DXIntersectTri (D3DX10math.h)

Calcola l'intersezione di un raggio e di un triangolo.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*p0* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive la prima posizione del vertice del triangolo.

</dd> <dt>

*p1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive la seconda posizione del vertice del triangolo.

</dd> <dt>

*p2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive la posizione del terzo vertice del triangolo.

</dd> <dt>

*pRayPos* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica la direzione del raggio.

</dd> <dt>

*pU* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Coordinate di hit barycentriche, U.

</dd> <dt>

*pV* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Coordinate di hit barycentriche, V.

</dd> <dt>

*pDist* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Distanza dei parametri di intersezione dei raggi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se il raggio interseca l'area del triangolo. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentrica (U,V). Il parametro U controlla quanto V2 viene ponderato nel risultato e il parametro V controlla la quantità di V3 ponderata nel risultato. Infine, il valore 1 - (U + V) controlla quanto \[ \] V1 viene ponderato nel risultato.

Le coordinate barycentriche sono una forma di coordinate generali. In questo contesto, l'uso di coordinate barycentriche rappresenta una modifica nei sistemi di coordinate. Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate barycentriche, vedere Descrizione delle coordinate [barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
