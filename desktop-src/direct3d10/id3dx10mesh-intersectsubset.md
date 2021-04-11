---
description: Determina se un raggio si interseca con un subset di questa mesh.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: Metodo ID3DX10Mesh::IntersectSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235117"
---
# <a name="id3dx10meshintersectsubset-method"></a>Metodo ID3DX10Mesh:: IntersectSubset

Determina se un raggio si interseca con un subset di questa mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AttribId* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID attributo che identifica il subset della mesh.

</dd> <dt>

*pRayPos* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che specifica la direzione del raggio.

</dd> <dt>

*pHitCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di volte in cui il raggio è stato intersecato con la mesh.

</dd> <dt>

*pFaceIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore a un valore di indice della faccia più vicina all'origine del raggio, se pHit è **true**.

</dd> <dt>

unità di *elaborazione* \[ in\]
</dt> <dd>

Tipo: **float \***

Puntatore a una coordinata baricentrica hit, U.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **float \***

Puntatore a una coordinata baricentrica hit, V.

</dd> <dt>

*pDist* \[ in\]
</dt> <dd>

Tipo: **float \***

Puntatore alla distanza del parametro di intersezione del raggio.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)contenente una matrice di strutture [**di \_ \_ informazioni di intersezione d3dx10**](d3dx10-intersect-info.md) . Si tratta di un elenco di tutti i riscontri che si sono verificati nel test di intersezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Questa API fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + U (v2-v1) + V (V3-V1).

Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V). Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato. Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.

Le coordinate baricentrica sono costituite da coordinate generali. In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate. Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
