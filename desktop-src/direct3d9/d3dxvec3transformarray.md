---
description: 'Funzione D3DXVec3TransformArray (D3dx9math.h): trasforma una matrice (x, y, z, 1) in base a una determinata matrice.'
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: Funzione D3DXVec3TransformArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cd17da7f3eb8e9c21ab2890ab112194c7f393b89c6761f2b14741e557318efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122538"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a>Funzione D3DXVec3TransformArray (D3dx9math.h)

Trasforma una matrice (x, y, z, 1) in base a una determinata matrice.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
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

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore alla [**matrice D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.

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

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore a [**una matrice trasformata D3DXVECTOR4.**](d3dxvector4.md)

## <a name="remarks"></a>Commenti

Questa funzione trasforma la matrice *pV* (x, y, z, 1) dalla matrice *pM*.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec3TransformArray** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
