---
description: Determina il prodotto di due matrici.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Funzione D3DXMatrixMultiply (D3dx9math. h)
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
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322131"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a>Funzione D3DXMatrixMultiply (D3dx9math. h)

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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pM1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.

</dd> <dt>

*pM2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che è il prodotto di due matrici.

## <a name="remarks"></a>Commenti

Il risultato rappresenta la trasformazione M1 seguita dalla trasformazione m2 (out = M1 \* m2).

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXMatrixMultiply** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




