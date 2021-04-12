---
description: Interseca il raggio specificato con il subset di mesh specificato. Questo fornisce funzionalità simili a D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Funzione D3DXIntersectSubset (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235013"
---
# <a name="d3dxintersectsubset-function"></a>D3DXIntersectSubset (funzione)

Interseca il raggio specificato con il subset di mesh specificato. Questo fornisce funzionalità simili a [**D3DXIntersect**](d3dxintersect.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta la mesh da testare. La mesh deve essere ordinata come attributo.

</dd> <dt>

*AttribId* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Identificatore dell'attributo del subset da intersecare con.

</dd> <dt>

*pRayPos* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione del raggio.

</dd> <dt>

*pHit* \[ out\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)\***

Puntatore a un BOOL. Se il raggio interseca un quadrante triangolare sulla mesh, questo valore verrà impostato su **true**. In caso contrario, questo valore è impostato su **false**.

</dd> <dt>

*pFaceIndex* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un valore di indice della faccia più vicina all'origine del raggio, se pHit è **true**.

</dd> <dt>

unità di *elaborazione* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a una coordinata baricentrica hit, U.

</dd> <dt>

*PV* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a una coordinata baricentrica hit, V.

</dd> <dt>

*pDist* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore alla distanza del parametro di intersezione del raggio.

</dd> <dt>

*ppAllHits* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Matrice di strutture [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) , che rappresenta tutti i riscontri, non solo i riscontri più vicini.

</dd> <dt>

*pCountOfHits* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Numero di elementi nella matrice restituiti da ppAllHits.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

La funzione **D3DXIntersectSubset** fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + U (v2-v1) + V (V3-V1).

Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (U, V). Il parametro U controlla la quantità di V2 che viene ponderata nel risultato e il parametro V controlla la quantità di V3 che viene ponderata nel risultato. Infine, il valore \[ 1-(U + V) controlla la \] quantità di V1 che viene ponderata nel risultato.

Le coordinate baricentrica sono costituite da coordinate generali. In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate. Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
