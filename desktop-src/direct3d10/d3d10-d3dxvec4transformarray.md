---
description: Trasforma una matrice (x, y, z, w) in base a una determinata matrice.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: Funzione D3DXVec4TransformArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 2c6fdcdd2a404e4122a0c8c66995fdabaf1284dfa67ebade888d2964c0c1fb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852801"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a>Funzione D3DXVec4TransformArray (D3DX10Math.h)

Trasforma una matrice (x, y, z, w) in base a una determinata matrice.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore alla [**matrice D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*OutStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride tra vettori nel flusso di dati di output.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Puntatore alla matrice D3DXVECTOR4 di origine.

</dd> <dt>

*VStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Stride tra vettori nel flusso di dati di input.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a [**una struttura D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta la matrice trasformata.

## <a name="remarks"></a>Commenti

Questa funzione trasforma la matrice pV (x, y, z, w) dalla matrice pM.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXVec4TransformArray** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
