---
description: "Funzione D3DXMatrixInverse (D3dx9math.h): calcola l'inverso di una matrice."
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Funzione D3DXMatrixInverse (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cacb0c8ccff72506c82f0145955cb2a95d4c1084f3e9e6c508682d2761189e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044889"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a>Funzione D3DXMatrixInverse (D3dx9math.h)

Calcola l'inverso di una matrice.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.

</dd> <dt>

*pDeterminant* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a un valore FLOAT contenente il determinante della matrice. Se il determinante non è necessario, impostare questo parametro su **NULL.**

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta l'inverso della matrice. Se l'inversione della matrice ha esito negativo, **viene restituito NULL.**

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixInverse** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
