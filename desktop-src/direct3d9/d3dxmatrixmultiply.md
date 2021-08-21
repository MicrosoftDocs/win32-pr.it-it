---
description: 'Funzione D3DXMatrixMultiply (D3dx9math.h): determina il prodotto di due matrici.'
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Funzione D3DXMatrixMultiply (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 64831287ab16f9b866ec5cd21b376fa190e8b42716453265875b2d8b5e7137d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122901"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a>Funzione D3DXMatrixMultiply (D3dx9math.h)

Determina il prodotto di due matrici.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.

</dd> <dt>

*pM1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una [**struttura D3DXMATRIX di**](d3dxmatrix.md) origine.

</dd> <dt>

*pM2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una [**struttura D3DXMATRIX di**](d3dxmatrix.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è il prodotto di due matrici.

## <a name="remarks"></a>Commenti

Il risultato rappresenta la trasformazione M1 seguita dalla trasformazione M2 (Out = M1 \* M2).

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixMultiply** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




