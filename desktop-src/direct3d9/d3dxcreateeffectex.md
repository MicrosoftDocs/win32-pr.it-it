---
description: Crea un effetto da una descrizione di effetto ASCII o binario. Questa funzione è una versione estesa di D3DXCreateEffect che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: Funzione D3DXCreateEffectEx (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19321dde9f44a2262ee3875d40bd5822e65eff9b84d1fc01656993ea584a8dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988651"
---
# <a name="d3dxcreateeffectex-function"></a>Funzione D3DXCreateEffectEx

Crea un effetto da una descrizione di effetto ASCII o binario. Questa funzione è una versione estesa di [**D3DXCreateEffect**](d3dxcreateeffect.md) che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
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

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo che creerà l'effetto. Vedere [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)

</dd> <dt>

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer contenente una descrizione dell'effetto.

</dd> <dt>

*SrcDataLen* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Lunghezza dei dati dell'effetto, in byte.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matrice facoltativa **con terminazione NULL** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore. Questo valore può essere **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione delle \# direttive include. Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.

</dd> <dt>

*pSkipConstants* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa di parametri dell'effetto che verrà ignorata dal sistema di effetti. La stringa deve **terminare** con NULL e deve contenere il nome di ogni costante gestita dall'applicazione separati da un punto e virgola.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se *pSrcData contiene* un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e [flag D3DXFX;](d3dxfx.md) In caso contrario, *pSrcData* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX. Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita. Per [informazioni dettagliate, vedere Effect-Compiler Tool](../direct3dtools/fxc.md) .

</dd> <dt>

*pPool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Puntatore a [**un oggetto ID3DXEffectPool**](id3dxeffectpool.md) da usare per i parametri condivisi. Se questo valore è **NULL,** non verrà condiviso alcun parametro.

</dd> <dt>

*ppEffect* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Restituisce un puntatore a [**un'interfaccia ID3DXEffect.**](id3dxeffect.md)

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

Questa funzione è una versione estesa di [**D3DXCreateEffect**](d3dxcreateeffect.md) che consente a un'applicazione di specificare quali costanti di effetto verranno gestite dall'applicazione. Una costante gestita dall'applicazione viene ignorata dal sistema di effetti. In altri casi, l'applicazione è responsabile dell'inizializzazione della costante, nonché del salvataggio e del ripristino dello stato quando appropriato.

Questa funzione controlla ogni costante in pSkipConstants per verificare che:

-   È associato a un registro costante.
-   Viene usato solo nel codice dello shader HLSL.

Se una costante viene denominata nella stringa che non è presente nell'effetto, viene ignorata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di effetto](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
