---
description: 'Funzione D3DXVec3BaryCentric (D3dx9math.h): restituisce un punto in coordinate barycentriche, usando i vettori 3D specificati.'
ms.assetid: ecbabc76-9936-4f31-adec-1ec807984787
title: Funzione D3DXVec3BaryCentric (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c966eeabe78deabefb2877405f649f3d162f9d73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097895"
---
# <a name="d3dxvec3barycentric-function-d3dx9mathh"></a>Funzione D3DXVec3BaryCentric (D3dx9math.h)

Restituisce un punto nelle coordinate barycentriche, usando i vettori 3D specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _Out_       D3DXVECTOR3 *pOut,
  _In_  const D3DXVECTOR3 *pV1,
  _In_  const D3DXVECTOR3 *pV2,
  _In_  const D3DXVECTOR3 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> <dt>

*pV3* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.

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

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) in coordinate barycentriche.

## <a name="remarks"></a>Commenti

La **funzione D3DXVec3BaryCentric** consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + f(V2-V1) + g(V3-V1).

Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentric (f,g). Il parametro *f* controlla quanto V2 viene ponderato nel risultato e il parametro *g* controlla quanto V3 viene ponderato nel risultato. Infine, 1-f-g controlla quanto V1 viene ponderato nel risultato.

Si notino le relazioni seguenti.

-   Se (f>=0 &, & g>=0 &, & 1-f-g>=0), il punto si trova all'interno del triangolo V1V2V3.
-   Se (f==0 &, & g>=0 &, & 1-f-g>=0), il punto si trova sulla riga V1V3.
-   Se (f>=0 &, & g==0 &, & 1-f-g>=0), il punto si trova sulla riga V1V2.
-   Se (f>=0 &, & g>=0 &, & 1-f-g==0), il punto si trova sulla riga V2V3.

Le coordinate barycentriche sono una forma di coordinate generali. In questo contesto, l'uso di coordinate barycentric rappresenta una modifica nei sistemi di coordinate. Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec3BaryCentric** può essere usata come parametro per un'altra funzione.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più dettagliata delle coordinate barycentric, vedere Descrizione delle [coordinate barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
