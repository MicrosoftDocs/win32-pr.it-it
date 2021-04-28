---
description: 'Funzione D3DXVec4Normalize (D3dx9math.h): restituisce la versione normalizzata di un vettore 4D.'
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Funzione D3DXVec4Normalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78984c393d7caf259b4c310a31e01ed8fcbd4d47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097659"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a>Funzione D3DXVec4Normalize (D3dx9math.h)

Restituisce la versione normalizzata di un vettore 4D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore alla struttura [**D3DXVECTOR4 di**](d3dxvector4.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta la versione normalizzata del vettore.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec4Normalize** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




