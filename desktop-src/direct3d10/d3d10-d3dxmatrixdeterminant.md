---
description: 'Funzione D3DXMatrixDeterminant (D3DX10Math.h): restituisce il determinante di una matrice.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: Funzione D3DXMatrixDeterminant (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce78181cb2fe0c9f2ebeedc18ca57df7429a15d7e18329b511a1a5c0b95c12df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070051"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a>Funzione D3DXMatrixDeterminant (D3DX10Math.h)

Restituisce il determinante di una matrice.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura D3DXMATRIX di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Restituisce il determinante della matrice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
