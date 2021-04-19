---
description: Converte una matrice di float a 32 bit in float a 16 bit.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Funzione D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323344"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>Funzione D3DXFloat32To16Array (D3DX10Math. h)

Converte una matrice di float a 32 bit in float a 16 bit.

## <a name="syntax"></a>Sintassi


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Puntatore alla matrice di float a 16 bit.

</dd> <dt>

*Aggiungi* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di float a 32 bit.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Puntatore a una matrice di float a 16 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
