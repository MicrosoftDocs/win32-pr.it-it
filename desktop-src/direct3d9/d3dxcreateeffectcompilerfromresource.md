---
description: Crea un ID3DXEffectCompiler da una descrizione dell'effetto ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Funzione D3DXCreateEffectCompilerFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235067"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a>D3DXCreateEffectCompilerFromResource (funzione)

Crea un [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) da una descrizione dell'effetto ASCII.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSrcModule* \[ in\]
</dt> <dd>

Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**

Handle per un modulo che contiene la descrizione dell'effetto. Se questo parametro è **null**, verrà usato il modulo corrente.

</dd> <dt>

*pSrcResource* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore alla risorsa. Questo parametro supporta sia stringhe Unicode che ANSI. Vedere la sezione Osservazioni.

</dd> <dt>

*pDefines* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore. Questo valore può essere **null**.

</dd> <dt>

*pInclude* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include. Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di compilazione identificate da vari flag (vedere [flag D3DXSHADER](d3dxshader-flags.md)). Il compilatore Direct3D 10 HLSL è ora il valore predefinito. Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .

</dd> <dt>

*ppEffectCompiler* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenente il compilatore di effetti.

</dd> <dt>

*ppParseErrors* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) contenente tutti i messaggi di errore verificatisi durante la compilazione. Questo parametro può essere impostato su **null** per ignorare i messaggi di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromResourceW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromResourceA perché vengono utilizzate le stringhe ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni effetto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
