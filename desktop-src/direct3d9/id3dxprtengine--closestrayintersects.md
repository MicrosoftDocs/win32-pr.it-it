---
description: Usa un ray tracing efficiente nelle simulazioni PRT (Precomputed Radiance Transfer) per determinare se un raggio interseca una mesh.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: Metodo ID3DXPRTEngine::ClosestRayIntersects (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2620140337807891efa739da4540e3895394f63bcc494396c13e7c15d0c1b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729787"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>Metodo ID3DXPRTEngine::ClosestRayIntersects

Usa un ray tracing efficiente nelle simulazioni PRT (Precomputed Radiance Transfer) per determinare se un raggio interseca una mesh. Se viene trovata un'intersezione, il metodo restituisce l'indice del viso mesh più vicino raggiunto dal raggio e le coordinate barycentriche del punto di intersezione.

## <a name="syntax"></a>Sintassi


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRayPos* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione normalizzata del raggio.

</dd> <dt>

*pFaceIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore all'indice del viso della mesh corrente che viene raggiunto per la prima volta dal raggio specificato, in base all'impilamento di tutti i visi di mesh bloccanti davanti alla mesh corrente.

</dd> <dt>

*pU* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a una coordinata di hit barycentrica, U, per il vertice 0 del triangolo.

</dd> <dt>

*pV* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a una coordinata di hit barycentrica, V, per il vertice 1 del triangolo.

</dd> <dt>

*pDist* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore alla distanza del punto di intersezione lungo il raggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se il raggio interseca la mesh corrente. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Usare [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) per impostare le distanze minime e massime dell'intersezione con il raggio.

La coordinata barycentrica del terzo vertice (vertice 2) del triangolo è 1 - ( U + V ).

Questo metodo viene eseguito più lentamente rispetto a [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md). Usare **ID3DXPRTEngine::ShadowRayIntersects se** la posizione del punto di intersezione non è necessaria.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate barycentriche, vedere Descrizione delle coordinate [barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
