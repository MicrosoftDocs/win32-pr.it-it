---
description: Trasforma una matrice (x, y, z,1) in base a una matrice specificata.
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: Funzione D3DXVec3TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9ae223d4e1b8c424230ba12719f25258dae18548
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058654"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a>Funzione D3DXVec3TransformArray (D3DX10Math. h)

Trasforma una matrice (x, y, z,1) in base a una matrice specificata.

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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore alla matrice [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride tra i vettori nel flusso di dati di output.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore alla matrice [**D3DXVECTOR3**](d3d10-d3dxvector3.md) di origine.

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

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Puntatore a una matrice trasformata [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .

## <a name="remarks"></a>Commenti

Questa funzione trasforma la matrice pV (x, y, z, 1) dalle pM della matrice.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXVec3TransformArray può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
