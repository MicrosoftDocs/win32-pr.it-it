---
description: Nota invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o l'API D3DCompile. Compilare uno shader o un effetto da una risorsa.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: Funzione D3DX10CompileFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322428"
---
# <a name="d3dx10compilefromresource-function"></a>D3DX10CompileFromResource (funzione)

> [!Note]  
> Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .

 

Compilare uno shader o un effetto da una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSrcModule* \[ in\]
</dt> <dd>

Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**

Handle per il modulo della risorsa contenente lo shader. HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome della risorsa contenente lo shader. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*pSrcFileName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

facoltativo. Nome del file di effetto, che viene usato solo per i messaggi di errore. Può essere **null**.

</dd> <dt>

*pDefines* \[ in\]
</dt> <dd>

Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

facoltativo. Puntatore a una matrice di definizioni di macro (vedere la [**\_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0. Se non viene usato, impostare *pDefines* su **null**.

</dd> <dt>

*pInclude* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

facoltativo. Puntatore a un'interfaccia di [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) per la gestione dei file di inclusione. Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.

</dd> <dt>

*pFunctionName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX10CompileFromResource** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.

</dd> <dt>

*pProfile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che specifica il modello di shader; può essere qualsiasi profilo in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).

</dd> <dt>

*Flags1* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Flag di compilazione shader](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Flag di compilazione effetto](d3d10-graphics-reference-effect-constants.md). Quando si compila uno shader e non un file di effetto, **D3DX10CompileFromResource** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)). Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) contenente un elenco di errori e avvisi che si sono verificati durante la compilazione. Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **null**. Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
