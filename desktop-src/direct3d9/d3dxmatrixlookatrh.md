---
description: Funzione D3DXMatrixLookAtRH (D3dx9math.h) - Compila una matrice di tipo right-handed e look-at.
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: Funzione D3DXMatrixLookAtRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2242cff74f38727edf69f0092b6fc22f46d73147952831a0c772619ee89bf26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095843"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a>Funzione D3DXMatrixLookAtRH (D3dx9math.h)

Compila una matrice di tipo right-handed e look-at.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che è il risultato dell'operazione.

</dd> <dt>

*pEye* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce il punto dell'occhio. Questo valore viene usato nella conversione.

</dd> <dt>

*pAt* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce la destinazione di ricerca della fotocamera.

</dd> <dt>

*pUp* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce il mondo corrente verso l'alto, in genere \[ 0, 1, \] 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è una matrice di tipo right-handed.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixLookAtRH** può essere usata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x            yaxis.x            zaxis.x           0
 xaxis.y            yaxis.y            zaxis.y           0
 xaxis.z            yaxis.z            zaxis.z           0
 -dot(xaxis, eye)   -dot(yaxis, eye)   -dot(zaxis, eye)  1
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




