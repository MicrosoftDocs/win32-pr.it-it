---
description: Trasforma una matrice (x, y, z,1) in base a una matrice specificata e proietta il risultato di nuovo in w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: Funzione D3DXVec3TransformCoordArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b0b7ca3c2898e07dc8b5e9ced0117e642bfdfb41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969386"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a>Funzione D3DXVec3TransformCoordArray (D3DX10Math. h)

Trasforma una matrice (x, y, z,1) in base a una matrice specificata e proietta il risultato di nuovo in w = 1.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride tra i vettori nel flusso di dati di output.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore alla matrice D3DXVECTOR3 di origine.

</dd> <dt>

*VStride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride tra i vettori nel flusso di dati di input.

</dd> <dt>

*PM* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a una struttura D3DXVECTOR3 che rappresenta la matrice trasformata.

## <a name="remarks"></a>Commenti

Questa funzione trasforma la matrice pV (x, y, z,1) dalle pM della matrice, proiettando il risultato in w = 1.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
