---
description: Genera una dichiarazione di vertice di output dalla dichiarazione di input. La dichiarazione di output è destinata all'uso da parte delle funzioni a trama mesh.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Funzione D3DXGenerateOutputDecl (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1f74440ce7bbd72f62aa35de242ea48f615a4ed02d82c5782f7f0eaff1d5bc25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096046"
---
# <a name="d3dxgenerateoutputdecl-function"></a>Funzione D3DXGenerateOutputDecl

Genera una dichiarazione di vertice di output dalla dichiarazione di input. La dichiarazione di output è destinata all'uso da parte delle funzioni a trama mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOutput* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

Puntatore alla dichiarazione del vertice di output. Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pInput* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntatore alla dichiarazione del vertice di input. Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




