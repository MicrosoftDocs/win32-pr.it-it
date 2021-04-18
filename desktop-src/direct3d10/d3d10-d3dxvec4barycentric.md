---
description: Restituisce un punto nelle coordinate baricentrica, usando i vettori 4D specificati.
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: Funzione D3DXVec4BaryCentric (D3DX10Math. h)
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
ms.openlocfilehash: 026012a3e7410cf962b4cc40bd82cd7606529770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323187"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a>Funzione D3DXVec4BaryCentric (D3DX10Math. h)

Restituisce un punto nelle coordinate baricentrica, usando i vettori 4D specificati.

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

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore a una struttura D3DXVECTOR4 di origine.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore a una struttura D3DXVECTOR4 di origine.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore a una struttura D3DXVECTOR4 di origine.

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> <dt>

*g* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a una struttura D3DXVECTOR4 nelle coordinate di baricentrica.

## <a name="remarks"></a>Commenti

La funzione D3DXVec4BaryCentric fornisce un modo per comprendere i punti in e intorno a un triangolo, indipendentemente dalla posizione in cui si trova effettivamente il triangolo. Questa funzione restituisce il punto risultante utilizzando l'equazione seguente: V1 + f (v2-v1) + g (V3-V1).

Qualsiasi punto nel V1V2V3 del piano può essere rappresentato dalla coordinata baricentrica (f, g). Il parametro f controlla la quantità di V2 che viene ponderata nel risultato e il parametro g controlla la quantità di V3 che viene ponderata nel risultato. Infine, 1-f-g controlla la quantità di V1 che viene ponderata nel risultato.

Si notino le relazioni seguenti.

-   Se (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), il punto si trova all'interno del triangolo V1V2V3.
-   Se (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), il punto si trova nella riga V1V3.
-   Se (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), il punto si trova nella riga V1V2.
-   Se (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), il punto si trova nella riga V2V3.

Le coordinate baricentrica sono costituite da coordinate generali. In questo contesto, l'utilizzo delle coordinate baricentrica rappresenta una modifica nei sistemi di coordinate. Ciò che è valido per le coordinate cartesiane è valido per le coordinate baricentrica.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXVec4BaryCentric può essere utilizzata come parametro per un'altra funzione.

Le coordinate baricentrica definiscono un punto all'interno di un triangolo in termini di vertici del triangolo. Per una descrizione più approfondita delle coordinate baricentrica, vedere [la descrizione delle coordinate baricentrica di articolo MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
