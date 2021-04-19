---
description: Genera una dichiarazione del vertice di output dalla dichiarazione di input. La dichiarazione di output è destinata all'uso da parte delle funzioni a mosaico mesh.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Funzione D3DXGenerateOutputDecl (D3DX9Mesh. h)
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
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322674"
---
# <a name="d3dxgenerateoutputdecl-function"></a>D3DXGenerateOutputDecl (funzione)

Genera una dichiarazione del vertice di output dalla dichiarazione di input. La dichiarazione di output è destinata all'uso da parte delle funzioni a mosaico mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOutput* \[ out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

Puntatore alla dichiarazione del vertice di output. Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*Pinput* \[ in\]
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
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




