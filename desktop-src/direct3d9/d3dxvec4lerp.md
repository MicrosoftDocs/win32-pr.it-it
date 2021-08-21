---
description: Esegue un'interpolazione lineare tra due vettori 4D.
ms.assetid: a068a626-17cd-4df9-8f41-9b417bfda1d1
title: Funzione D3DXVec4Lerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 726bd212947a37d69dd21e6003d550845799e4ac7aba237794d465ad3da5b509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856971"
---
# <a name="d3dxvec4lerp-function"></a>Funzione D3DXVec4Lerp

Esegue un'interpolazione lineare tra due vettori 4D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4Lerp(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_          FLOAT       s
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

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parametro che interpola in modo lineare tra i vettori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'interpolazione lineare.

## <a name="remarks"></a>Commenti

Questa funzione esegue l'interpolazione lineare in base alla formula seguente: V1 + s(V2-V1).

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec4Lerp** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
