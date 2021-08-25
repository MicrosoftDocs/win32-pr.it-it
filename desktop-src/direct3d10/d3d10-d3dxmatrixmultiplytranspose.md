---
description: 'Funzione D3DXMatrixMultiplyTranspose (D3DX10Math.h): calcola il prodotto trasposto di due matrici.'
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Funzione D3DXMatrixMultiplyTranspose (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55bf8dc8eaed13c6bfdc4a8cedacd02b9c5cc5aa11ca0d3e494ed194c8cc9245
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858781"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a>Funzione D3DXMatrixMultiplyTranspose (D3DX10Math.h)

Calcola il prodotto trasposto di due matrici.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pM1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore a una struttura D3DXMATRIX di origine (lato sinistro).

</dd> <dt>

*pM2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore a una struttura D3DXMATRIX di origine (lato destro).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che è il prodotto di due matrici.

## <a name="remarks"></a>Commenti

Il risultato è il prodotto trasposto di due matrici di trasformazione, Out = T(M1 \* M2).

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixMultiplyTranspose può essere usata come parametro per un'altra funzione.

Questa funzione è utile per impostare matrici come costanti per vertex shader e pixel shader.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
