---
description: 'Funzione D3DXFloat16To32Array (D3dx9math.h): converte una matrice di valori float a 16 bit in float a 32 bit.'
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Funzione D3DXFloat16To32Array (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107599"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>Funzione D3DXFloat16To32Array (D3dx9math.h)

Converte una matrice di valori float a 16 bit in float a 32 bit.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore alla matrice di valori float a 32 bit.

</dd> <dt>

*pIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Puntatore a una matrice di float a 16 bit.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di valori float a 32 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
