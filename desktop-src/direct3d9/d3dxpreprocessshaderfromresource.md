---
description: Pre-elabora una risorsa shader senza eseguire la compilazione. In questo modo vengono \# risolte tutte le operazioni defines e includes, fornendo uno shader autonomo \# per la compilazione successiva.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: Funzione D3DXPreprocessShaderFromResource (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 235b1146cd589d09d4718f938f15e7250fdb57993295d48eaa94290abe1cd52f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298519"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a>Funzione D3DXPreprocessShaderFromResource

Pre-elabora una risorsa shader senza eseguire la compilazione. In questo modo vengono \# risolte tutte le operazioni defines e includes, fornendo uno shader autonomo \# per la compilazione successiva.

> [!Note]  
> Invece di usare questa funzione legacy, è consigliabile usare [**l'API D3DPreprocess.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess)

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle per il modulo che contiene la risorsa shader. Se questo valore è **NULL,** verrà usato il modulo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che rappresenta il nome della risorsa nel modulo.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matrice facoltativa con terminazione **NULL** di [**strutture D3DXMACRO.**](d3dxmacro.md) Questo valore può essere **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione delle \# direttive include. Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.

</dd> <dt>

*ppShaderText* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente una singola stringa di grandi dimensioni che rappresenta il flusso di token formattato risultante.

</dd> <dt>

*ppErrorMsgs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente un elenco di errori e avvisi rilevati durante la compilazione. Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug. Questo valore può essere **NULL.**

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
</dt> <dt>

[**D3DXPreprocessShaderFromFile**](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[**D3DXPreprocessShader**](d3dxpreprocessshader.md)
</dt> </dl>

 

 
