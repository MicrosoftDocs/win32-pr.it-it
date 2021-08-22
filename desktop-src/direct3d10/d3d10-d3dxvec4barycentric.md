---
description: 'Funzione D3DXVec4BaryCentric (D3DX10Math.h): restituisce un punto in coordinate barycentriche, usando i vettori 4D specificati.'
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: Funzione D3DXVec4BaryCentric (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5ecd9a1882e268ae3f398dd42f16d97e00085f2797a98fb42ad4c1f8851ce89d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753971"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a>Funzione D3DXVec4BaryCentric (D3DX10Math.h)

Restituisce un punto in coordinate barycentriche, usando i vettori 4D specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _In_       D3DXVECTOR4 *pOut,
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2,
  _In_ const D3DXVECTOR4 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore a una struttura D3DXVECTOR4 di origine.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore a una struttura D3DXVECTOR4 di origine.

</dd> <dt>

*pV3* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore a una struttura D3DXVECTOR4 di origine.

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

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a una struttura D3DXVECTOR4 in coordinate barycentriche.

## <a name="remarks"></a>Commenti

La funzione D3DXVec4BaryCentric consente di comprendere i punti all'interno e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante usando l'equazione seguente: V1 + f(V2-V1) + g(V3-V1).

Qualsiasi punto nel piano V1V2V3 può essere rappresentato dalla coordinata barycentrica (f,g). Il parametro f controlla quanto V2 viene ponderato nel risultato e il parametro g controlla la quantità di V3 ponderata nel risultato. Infine, 1-f-g controlla la quantità di V1 ponderata nel risultato.

Si notino le relazioni seguenti.

-   Se (f>=0 &, & g>=0 &, & 1-f-g>=0), il punto si trova all'interno del triangolo V1V2V3.
-   Se (f===0 &, & g>=0 &, & 1-f-g>=0), il punto si trova sulla riga V1V3.
-   Se (f>=0 &, & g==0 &, & 1-f-g>=0), il punto si trova sulla riga V1V2.
-   Se (f>=0 &, & g>=0 &, & 1-f-g==0), il punto si trova sulla riga V2V3.

Le coordinate barycentriche sono una forma di coordinate generali. In questo contesto, l'uso delle coordinate barycentriche rappresenta una modifica nei sistemi di coordinate. Ciò che vale per le coordinate cartesiane è vero per le coordinate barycentriche.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXVec4BaryCentric può essere usata come parametro per un'altra funzione.

Le coordinate barycentriche definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate barycentriche, vedere Descrizione delle coordinate [barycentriche di Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
