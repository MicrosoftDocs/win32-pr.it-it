---
description: Calcola l'intersezione tra un raggio e un triangolo.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Funzione D3DXIntersectTri (D3DX10math. h)
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
ms.openlocfilehash: af96d25b4f13995d60e7926ec5da2d15ff86f282
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322781"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a>Funzione D3DXIntersectTri (D3DX10math. h)

Calcola l'intersezione tra un raggio e un triangolo.

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

*P0* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive la prima posizione del vertice del triangolo.

</dd> <dt>

*P1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive la seconda posizione del vertice del triangolo.

</dd> <dt>

*P2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive la posizione del vertice del terzo triangolo.

</dd> <dt>

*pRayPos* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica la direzione del raggio.

</dd> <dt>

unità di *elaborazione* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Coordinate baricentrica hit, U.

</dd> <dt>

*PV* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Coordinate baricentrica hit, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Distanza del parametro di intersezione tra Ray.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce **true** se il raggio interseca l'area del triangolo. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V). Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato. Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.

Le coordinate baricentrica sono costituite da coordinate generali. In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate. Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
