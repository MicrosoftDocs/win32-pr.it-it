---
description: Crea una matrice di identità.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Funzione D3DXMatrixIdentity (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce7d891eb446372b749c7085a37e80241c52f1cf862a61b3fc9edeb544776b2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044898"
---
# <a name="d3dxmatrixidentity-function"></a>Funzione D3DXMatrixIdentity

Crea una matrice di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di identità.

## <a name="remarks"></a>Commenti

La matrice identity è una matrice in cui tutti i coefficienti sono 0, ad eccezione dei \[ coefficienti 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, che sono impostati \] su 1. La matrice di identità è speciale in quanto, quando viene applicata ai vertici, rimane invariata. La matrice identity viene usata come punto di partenza per le matrici che modificheranno i valori dei vertici per creare rotazioni, traslazioni ed eventuali altre trasformazioni che possono essere rappresentate da una matrice 4 x4.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixIdentity** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




