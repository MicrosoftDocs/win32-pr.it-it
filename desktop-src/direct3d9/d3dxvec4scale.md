---
description: Ridimensiona un vettore 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: Funzione D3DXVec4Scale (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12f030330d01e004d80de92920c84f8cc8ffc47fe009582d64d34497bb684418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118961"
---
# <a name="d3dxvec4scale-function"></a>Funzione D3DXVec4Scale

Ridimensiona un vettore 4D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
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

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore alla struttura [**D3DXVECTOR4 di**](d3dxvector4.md) origine.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore di ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore ridimensionato.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec4Scale** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Add**](d3dxvec4add.md)
</dt> <dt>

[**D3DXVec4Subtract**](d3dxvec4subtract.md)
</dt> </dl>

 

 
