---
description: Aggiunge due vettori 2D.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: Funzione D3DXVec2Add (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9ab63d23a4370c2c64143d2289bd1324a3ebf684d30caf06db3eab2cd4e2915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730894"
---
# <a name="d3dxvec2add-function"></a>Funzione D3DXVec2Add

Aggiunge due vettori 2D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta la somma dei due vettori.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec2Add** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Subtract**](d3dxvec2subtract.md)
</dt> <dt>

[**D3DXVec2Scale**](d3dxvec2scale.md)
</dt> </dl>

 

 




