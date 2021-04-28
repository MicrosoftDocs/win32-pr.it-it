---
description: "Funzione D3DXCreateEffectFromResource: crea un effetto da una descrizione dell'effetto ASCII o binario."
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Funzione D3DXCreateEffectFromResource (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107689"
---
# <a name="d3dxcreateeffectfromresource-function"></a>Funzione D3DXCreateEffectFromResource

Creare un effetto da una descrizione dell'effetto ASCII o binario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo.

</dd> <dt>

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle per un modulo contenente la descrizione dell'effetto. Se questo parametro è **NULL,** verrà usato il modulo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore alla risorsa. Questo parametro supporta sia stringhe Unicode che ANSI. Vedere la sezione Osservazioni.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matrice facoltativa **con terminazione NULL** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore. Questo valore può essere **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include. Se questo valore è **NULL,** include verrà rispettato durante la compilazione da un file o causerà un errore durante la compilazione \# da una risorsa o da una memoria.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se *hSrcModule contiene* un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e [D3DXFX;](d3dxfx.md) In caso contrario, *hSrcModule contiene* un effetto binario e gli unici flag rispettati sono i flag D3DXFX. Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita. Per [informazioni dettagliate, vedere Strumento di compilazione effetti.](../direct3dtools/fxc.md)

</dd> <dt>

*pPool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntatore a [**un oggetto ID3DXEffectPool**](id3dxeffectpool.md) da usare per i parametri condivisi. Se questo valore è **NULL,** non verrà condiviso alcun parametro.

</dd> <dt>

*ppEffect* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Restituisce un buffer contenente l'effetto compilato.

</dd> <dt>

*ppCompilationErrors* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente un elenco di errori di compilazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceA perché vengono usate stringhe ANSI.

D3DXCreateEffectFromResource carica i dati da una risorsa di tipo RT \_ RCDATA. Per altre informazioni sulle risorse di Windows, vedere MSDN.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni degli effetti](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
