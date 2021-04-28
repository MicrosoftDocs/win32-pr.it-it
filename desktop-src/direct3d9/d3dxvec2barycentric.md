---
description: 'Funzione D3DXVec2BaryCentric (D3dx9math.h): restituisce un punto in coordinate barycentriche, usando i vettori 2D specificati.'
ms.assetid: afbffe6d-d786-4d65-b737-ae201613d1ac
title: Funzione D3DXVec2BaryCentric (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3210624087a3d1d5a612ba1eb628e7d85ba4fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117789"
---
# <a name="d3dxvec2barycentric-function-d3dx9mathh"></a>Funzione D3DXVec2BaryCentric (D3dx9math.h)

Restituisce un punto in coordinate barycentriche, usando i vettori 2D specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _Out_       D3DXVECTOR2 *pOut,
  _In_  const D3DXVECTOR2 *pV1,
  _In_  const D3DXVECTOR2 *pV2,
  _In_  const D3DXVECTOR2 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine.

</dd> <dt>

*pV3* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine.

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> <dt>

*g* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) in coordinate barycentriche.

## <a name="remarks"></a>Commenti

La **funzione D3DXVec2BaryCentric** consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + f(V2-V1) + g(V3-V1).

Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (f,g). Il parametro *f* controlla quanto V2 viene ponderato nel risultato e il parametro *g* controlla quanto V3 viene ponderato nel risultato. Infine, 1-f-g controlla quanto V1 viene ponderato nel risultato.

Si notino le relazioni seguenti.

-   Se (f>=0 &, & g>=0 &, & 1-f-g>=0), il punto si trova all'interno del triangolo V1V2V3.
-   Se (f==0 &, & g>=0 &, & 1-f-g>=0), il punto si trova sulla riga V1V3.
-   Se (f>=0 &, & g==0 &, & 1-f-g>=0), il punto si trova sulla riga V1V2.
-   Se (f>=0 &, & g>=0 &, & 1-f-g==0), il punto si trova sulla riga V2V3.

Le coordinate barycentriche sono una forma di coordinate generali. In questo contesto, l'uso di coordinate barycentric rappresenta una modifica nei sistemi di coordinate. Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec2BaryCentric** può essere usata come parametro per un'altra funzione.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html) Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
