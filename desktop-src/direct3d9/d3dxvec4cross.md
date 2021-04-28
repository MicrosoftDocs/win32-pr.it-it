---
description: 'Funzione D3DXVec4Cross (D3dx9math.h): determina il prodotto incrociato in quattro dimensioni.'
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: Funzione D3DXVec4Cross (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3630a486f6c8fcd456373445bd931d878fdc38e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097689"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a>Funzione D3DXVec4Cross (D3dx9math.h)

Determina il prodotto incrociato in quattro dimensioni.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.

</dd> <dt>

*pV3* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a una [**struttura D3DXVECTOR4 di**](d3dxvector4.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il prodotto incrociato.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec4Cross** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Dot**](d3dxvec4dot.md)
</dt> </dl>

 

 




