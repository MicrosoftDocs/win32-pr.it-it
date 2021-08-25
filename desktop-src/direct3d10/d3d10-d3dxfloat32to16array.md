---
description: 'Funzione D3DXFloat32To16Array (D3DX10Math.h): converte una matrice di valori float a 32 bit in float a 16 bit.'
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Funzione D3DXFloat32To16Array (D3DX10Math.h)
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
ms.openlocfilehash: f0de2e2cda9724a5bfa12d13171276694bcd8fbcbbd5dffbb81ae185ebbda381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853411"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>Funzione D3DXFloat32To16Array (D3DX10Math.h)

Converte una matrice di valori float a 32 bit in valori float a 16 bit.

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

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Puntatore alla matrice di valori float a 16 bit.

</dd> <dt>

*pIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di valori float a 32 bit.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Puntatore a una matrice di valori float a 16 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
