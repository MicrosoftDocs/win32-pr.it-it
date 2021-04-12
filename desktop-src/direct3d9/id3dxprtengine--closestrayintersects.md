---
description: Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'Metodo ID3DXPRTEngine:: ClosestRayIntersects (D3DX9Mesh. h)'
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
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235177"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>Metodo ID3DXPRTEngine:: ClosestRayIntersects

Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh. Se viene rilevata un'intersezione, il metodo restituisce l'indice della faccia mesh più vicina raggiunta dal raggio e dalle coordinate baricentrica del punto di intersezione.

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

*pRayPos* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione normalizzata del raggio.

</dd> <dt>

*pFaceIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore all'indice della faccia mesh corrente che viene raggiunto prima dal raggio specificato, in base allo stack di tutti i visi della mesh di blocco davanti alla mesh corrente.

</dd> <dt>

unità di *elaborazione* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a una coordinata di hit baricentrica, U, per il vertice 0 del triangolo.

</dd> <dt>

*PV* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a una coordinata baricentrica hit, V, per il vertice 1 del triangolo.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore alla distanza del punto di intersezione lungo il raggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce **true** se il raggio interseca la mesh corrente; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Usare [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) per impostare le distanze minime e massime dell'intersezione con il raggio.

La coordinata baricentrica del terzo vertice (vertice 2) del triangolo è 1-(U + V).

Questo metodo viene eseguito più lentamente di [**ID3DXPRTEngine:: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md). Usare **ID3DXPRTEngine:: ShadowRayIntersects** se il percorso del punto di intersezione non è necessario.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
