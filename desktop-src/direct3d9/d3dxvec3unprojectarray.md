---
description: 'Funzione D3DXVec3UnprojectArray (D3dx9math.h): proietta una matrice (x, y, z, 0) dallo spazio dello schermo allo spazio oggetto.'
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Funzione D3DXVec3UnprojectArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67e42b30a8f8d44bb9b21668a515a202436b7631
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097719"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a>Funzione D3DXVec3UnprojectArray (D3dx9math.h)

Proietta una matrice (x, y, z, 0) dallo spazio dello schermo allo spazio oggetto.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*OutStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride tra vettori nel flusso di dati di output.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> <dt>

*VStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride tra vettori nel flusso di dati di input.

</dd> <dt>

*pViewport* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntatore a [**una struttura D3DVIEWPORT9,**](d3dviewport9.md) che rappresenta il viewport.

</dd> <dt>

*pProjection* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di proiezione.

</dd> <dt>

*pView* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.

</dd> <dt>

*pWorld* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice globale.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice proiettata dallo spazio dello schermo allo spazio dell'oggetto.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la [**funzione D3DXVec3Unproject**](d3dxvec3unproject.md) può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Project**](d3dxvec3project.md)
</dt> </dl>

 

 
