---
description: 'Funzione D3DXVec3Project (D3dx9math.h): proietta un vettore 3D dallo spazio oggetto allo spazio dello schermo.'
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: Funzione D3DXVec3Project (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bb0d7b962dd4595ec9246c036d4ff9e459e062f366b6e62f46cce1a5a3ebab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803813"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a>Funzione D3DXVec3Project (D3dx9math.h)

Proietta un vettore 3D dallo spazio oggetto allo spazio dello schermo.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> <dt>

*pViewport* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntatore a [**una struttura D3DVIEWPORT9,**](d3dviewport9.md) che rappresenta il viewport.

</dd> <dt>

*pProjection* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice di proiezione.

</dd> <dt>

*pView* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.

</dd> <dt>

*pWorld* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice globale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore proiettato dallo spazio oggetto allo spazio dello schermo.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec3Project** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 




