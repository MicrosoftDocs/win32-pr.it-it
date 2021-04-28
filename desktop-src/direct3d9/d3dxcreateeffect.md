---
description: "Funzione D3DXCreateEffect: creare un effetto da una descrizione dell'effetto ASCII o binario."
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Funzione D3DXCreateEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6821375dfc672d4937c335cf85dab12ba31b726c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115779"
---
# <a name="d3dxcreateeffect-function"></a>Funzione D3DXCreateEffect

Creare un effetto da una descrizione dell'effetto ASCII o binario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
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

Lunghezza in byte dei dati dell'effetto.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matrice facoltativa **con terminazione NULL** di [**strutture D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore. Questo valore può essere **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione delle \# direttive include. Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.

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

 

 
