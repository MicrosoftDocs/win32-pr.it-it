---
title: D3D11Reflect (funzione)
description: Ottiene un puntatore a un'interfaccia di Reflection.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- Funzione D3D11Reflect HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132398"
---
# <a name="d3d11reflect-function"></a>D3D11Reflect (funzione)

Ottiene un puntatore a un'interfaccia di Reflection.

## <a name="syntax"></a>Sintassi

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntatore ai dati di origine come codice HLSL compilato.

</dd> <dt>

*SrcDataSize* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza di *pSrcData*.

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

Indirizzo di un puntatore all'interfaccia [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Restituisce uno dei codici restituiti descritti nell'argomento [codici restituiti Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).

## <a name="remarks"></a>Commenti

La funzione inline del compilatore **D3D11Reflect** è un wrapper per la funzione del compilatore [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) . **D3D11Reflect** può recuperare solo un'interfaccia [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) da uno shader. **D3DReflect** può recuperare un'interfaccia **ID3D11ShaderReflection** o un'interfaccia di Reflection direct3d 10 o Direct3D 10,1, ad esempio [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

Il codice dello shader contiene metadati che possono essere controllati tramite le API di Reflection.

Nel codice seguente viene illustrato come recuperare un'interfaccia [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) da uno shader.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DCompiler. inl</dt> </dl>     |
| Libreria<br/> | <dl> <dt>D3dcompiler \_ 47. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>\_47.dllD3dcompiler</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

