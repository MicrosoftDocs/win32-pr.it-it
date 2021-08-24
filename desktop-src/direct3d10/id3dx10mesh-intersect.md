---
description: Determina se un raggio si interseca con questa mesh.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Metodo ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1693db027baad13d69c43e394407ed8eb037d2dbb95eb217ccca473d1f91d08a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634551"
---
# <a name="id3dx10meshintersect-method"></a>Metodo ID3DX10Mesh::Intersect

Determina se un raggio si interseca con questa mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Intersect(
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

*pRayPos* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che specifica la direzione del raggio.

</dd> <dt>

*pHitCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Numero di volte in cui il raggio si interseca con la mesh.

</dd> <dt>

*pFaceIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore a un valore di indice del viso più vicino all'origine del raggio, se pHit è **TRUE.**

</dd> <dt>

*pU* \[ Pollici\]
</dt> <dd>

Tipo: **\* float**

Puntatore a una coordinata di hit barycentric, U.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **\* float**

Puntatore a una coordinata di hit barycentric, V.

</dd> <dt>

*pDist* \[ Pollici\]
</dt> <dd>

Tipo: **\* float**

Puntatore a una distanza del parametro di intersezione dei raggi.

</dd> <dt>

*ppAllHits* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a [**un'interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)contenente una matrice [**di strutture D3DX10 \_ INTERSECT \_ INFO.**](d3dx10-intersect-info.md) Questo è un elenco di tutti i riscontri che si sono verificati nel test di intersezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questa API consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + U(V2 - V1) + V(V3 - V1).

Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (U,V). Il parametro U controlla quanto V2 viene ponderato nel risultato e il parametro V controlla quanto V3 viene ponderato nel risultato. Infine, il valore 1 - (U + V) controlla quanto \[ \] V1 viene ponderato nel risultato.

Le coordinate barycentriche sono una forma di coordinate generali. In questo contesto, l'uso di coordinate barycentrice rappresenta una modifica nei sistemi di coordinate. Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
