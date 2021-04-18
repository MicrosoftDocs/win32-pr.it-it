---
description: Ottiene i nomi dei sampler a cui si fa riferimento in uno shader.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Funzione D3DXGetShaderSamplers (D3DX9Shader. h)
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
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322657"
---
# <a name="d3dxgetshadersamplers-function"></a>D3DXGetShaderSamplers (funzione)

Ottiene i nomi dei sampler a cui si fa riferimento in uno shader.

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

*pFunction* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione shader.

</dd> <dt>

*pSamplers* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di LPCSTRs. La funzione riempirà questa matrice con i puntatori ai nomi del campionatore contenuti in *pFunction*. La dimensione massima della matrice è il numero massimo di registri del campionatore (16 per vs \_ 3 \_ 0 e PS \_ 3 \_ 0).

Per trovare il numero di campioni utilizzati, controllare *pcount* dopo aver chiamato **D3DXGetShaderSamplers** con pSamplers = **null**.

</dd> <dt>

*pcount* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Restituisce il numero di campioni a cui fa riferimento lo shader.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
