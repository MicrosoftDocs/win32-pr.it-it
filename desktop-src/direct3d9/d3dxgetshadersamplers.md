---
description: Ottenere i nomi dei campionatori a cui si fa riferimento in uno shader.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Funzione D3DXGetShaderSamplers (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da4c7381b0fe058e18dd2edfd86ef49f434cd1b57bff18303fce0ba939c5d299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044999"
---
# <a name="d3dxgetshadersamplers-function"></a>Funzione D3DXGetShaderSamplers

Ottenere i nomi dei campionatori a cui si fa riferimento in uno shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFunction* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione shader.

</dd> <dt>

*pSamplers* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di LPCSTRs. La funzione riempirà questa matrice con puntatori ai nomi del campionatore contenuti in *pFunction*. La dimensione massima della matrice è il numero massimo di registri campionatori (16 per vs \_ 3 \_ 0 e ps \_ 3 \_ 0).

Per trovare il numero di campionatori usati, controllare *pCount* dopo aver chiamato **D3DXGetShaderSamplers** con pSamplers = **NULL.**

</dd> <dt>

*pCount* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Restituisce il numero di campionatori a cui fa riferimento lo shader.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
