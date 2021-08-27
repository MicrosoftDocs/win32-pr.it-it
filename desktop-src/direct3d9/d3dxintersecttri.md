---
description: "Funzione D3DXIntersectTri (D3DX9Mesh.h): calcola l'intersezione di un raggio e di un triangolo."
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Funzione D3DXIntersectTri (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb542c5c7bb4edb4dafffa1254b76504aaf0f256a9d694db9d55724f2c94c2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069281"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a>Funzione D3DXIntersectTri (D3DX9Mesh.h)

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive la posizione del primo vertice triangolare.

</dd> <dt>

*p1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive la posizione del secondo vertice triangolare.

</dd> <dt>

*p2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive la posizione del terzo vertice triangolare.

</dd> <dt>

*pRayPos* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione del raggio.

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

Restituisce **TRUE** se il raggio interseca l'area del triangolo. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

La [**funzione D3DXIntersect**](d3dxintersect.md) consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + U(V2 - V1) + V(V3 - V1).

Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (U,V). Il parametro U controlla quanto V2 viene ponderato nel risultato e il parametro V controlla quanto V3 viene ponderato nel risultato. Infine, il valore 1 - (U + V) controlla quanto \[ \] V1 viene ponderato nel risultato.

Le coordinate barycentriche sono una forma di coordinate generali. In questo contesto, l'uso di coordinate barycentrice rappresenta una modifica nei sistemi di coordinate. Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
