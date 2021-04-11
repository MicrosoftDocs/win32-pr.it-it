---
description: Compilare un file shader.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Funzione D3DXCompileShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354729"
---
# <a name="d3dxcompileshader-function"></a>D3DXCompileShader (funzione)

Compilare un file shader.

> [!Note]  
> Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che contiene lo shader.

</dd> <dt>

*srcDataLen* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Lunghezza dei dati in byte.

</dd> <dt>

*pDefines* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) . Questo valore può essere **null**.

</dd> <dt>

*pInclude* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include. Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.

</dd> <dt>

*pFunctionName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che contiene il nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione.

</dd> <dt>

*pProfile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a un profilo dello shader che determina il set di istruzioni dello shader. Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di compilazione identificate da diversi flag. Il compilatore Direct3D 10 HLSL è ora il valore predefinito. Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente lo shader creato. Questo buffer contiene il codice dello shader compilato, nonché tutte le informazioni di debug e di tabella dei simboli incorporate.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione. Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug. Questo valore può essere **null**.

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Restituisce un'interfaccia [**ID3DXConstantTable**](id3dxconstanttable.md) che può essere utilizzata per accedere alle costanti dello shader. Questo valore può essere **null**. Se l'applicazione viene compilata con un indirizzo di grandi dimensioni (ovvero si usa l'opzione del linker/LARGEADDRESSAWARE per gestire gli indirizzi maggiori di 2 GB), non è possibile usare questo parametro e deve essere impostato su **null**. È invece necessario utilizzare la funzione [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella delle costanti shader incorporata all'interno dello shader. In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.

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
</dt> <dt>

[**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
