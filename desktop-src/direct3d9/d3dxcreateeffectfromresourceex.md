---
description: Creare un effetto dalla descrizione di un effetto ASCII o binario. Si tratta di una versione estesa di D3DXCreateEffectFromResource che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Funzione D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323255"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a>D3DXCreateEffectFromResourceEx (funzione)

Creare un effetto dalla descrizione di un effetto ASCII o binario. Si tratta di una versione estesa di [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo.

</dd> <dt>

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

*pSkipConstants* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Una stringa di parametri effetti che verrà ignorata dal sistema di effetti. La stringa deve essere con terminazione **null** e deve contenere il nome di ogni costante gestita dall'applicazione separata da un punto e virgola.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se *pSrcResource* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *pSrcResource* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX. Il compilatore Direct3D 10 HLSL è ora il valore predefinito. Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .

</dd> <dt>

*pPool* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi. Se questo valore è **null**, non verrà condiviso alcun parametro.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Restituisce un buffer contenente l'effetto compilato.

</dd> <dt>

*ppCompilationErrors* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente un elenco di errori di compilazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione è una versione estesa di [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) che consente a un'applicazione di specificare quali costanti di effetto verranno gestite dall'applicazione. Una costante gestita dall'applicazione viene ignorata dal sistema di effetti. In altre condizioni, l'applicazione è responsabile dell'inizializzazione della costante, nonché del salvataggio e del ripristino dello stato quando appropriato.

Questa funzione controlla ogni costante in pSkipConstants per vedere quanto segue:

-   È associato a un registro costante.
-   Viene usato solo nel codice shader HLSL.

Se una costante viene denominata nella stringa non presente nell'effetto, viene ignorata.

Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceA perché vengono utilizzate le stringhe ANSI.

D3DXCreateEffectFromResource carica i dati da una risorsa di tipo RT \_ RCDATA. Per ulteriori informazioni sulle risorse di Windows, vedere MSDN.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni effetto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
