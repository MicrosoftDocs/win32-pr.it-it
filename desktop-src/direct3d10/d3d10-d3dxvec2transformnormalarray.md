---
description: Trasforma una matrice (x, y, 0, 0) in base a una matrice specificata.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: Funzione D3DXVec2TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4850961560ae810b9a21f58fbefa9b6b07227c77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323221"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a>Funzione D3DXVec2TransformNormalArray (D3DX10Math. h)

Trasforma una matrice (x, y, 0, 0) in base a una matrice specificata.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride tra i vettori nel flusso di dati di output.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore alla matrice D3DXVECTOR2 di origine.

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

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore a una struttura D3DXVECTOR2 che rappresenta la matrice trasformata.

## <a name="remarks"></a>Commenti

Questa funzione trasforma il vettore (pV->x, pV->y, 0, 0) dalla matrice a cui fa riferimento il pM.

Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXVec2TransformNormalArray** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
