---
description: 'Funzione D3DXVec3TransformNormalArray (D3dx9math.h): trasforma una matrice (x, y, z, 0) in base a una determinata matrice.'
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Funzione D3DXVec3TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f90521b51c9c939d459fb10bcf2badd7e551b80e5e9f134d5dfd38b5ec8e18aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730820"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a>Funzione D3DXVec3TransformNormalArray (D3dx9math.h)

Trasforma una matrice (x, y, z, 0) in base a una determinata matrice.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla [**matrice D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*OutStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride tra vettori nel flusso di dati di output.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla matrice [**D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> <dt>

*VStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride tra i vettori nel flusso di dati di input.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una matrice D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice trasformata.

## <a name="remarks"></a>Commenti

Questa funzione trasforma il vettore (*pV*->x, *pV*->y, *pV*->z, 0) dalla matrice a cui punta *pM*.

Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec3TransformNormalArray** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
