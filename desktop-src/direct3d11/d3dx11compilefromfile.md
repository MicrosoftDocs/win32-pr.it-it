---
title: Funzione D3DX11CompileFromFile (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o una delle API di compilazione HLSL, ad esempio l'API D3DCompileFromFile. Compilare uno shader o un effetto da un file.
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Funzione D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132374"
---
# <a name="d3dx11compilefromfile-function"></a>D3DX11CompileFromFile (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .

 

Compilare uno shader o un effetto da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del file che contiene il codice dello shader. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*pDefines* \[ in\]
</dt> <dd>

Tipo: **const [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

facoltativo. Puntatore a una matrice di definizioni di macro (vedere [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0. Se non viene usato, impostare *pDefines* su **null**.

</dd> <dt>

*pInclude* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

facoltativo. Puntatore a un'interfaccia per la gestione dei file di inclusione. Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.

</dd> <dt>

*pFunctionName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX11CompileFromFile** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.

</dd> <dt>

*pProfile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Stringa che specifica il modello di shader; può essere qualsiasi profilo in Shader Model 2, Shader Model 3, Shader Model 4 o Shader Model 5. Il profilo può essere anche per il tipo di effetto (ad esempio, FX \_ 4 \_ 1).

</dd> <dt>

*Flags1* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Flag di [**compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-constants)shader.

</dd> <dt>

*Flags2* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

[**Flag di compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)effetto. Quando si compila uno shader e non un file di effetto, **D3DX11CompileFromFile** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)). Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.

</dd> <dt>

*ppShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria contenente un elenco di errori e avvisi che si sono verificati durante la compilazione. Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **null**. Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

**D3DX11CompileFromFile** restituisce E \_ INVALIDARG se si fornisce un valore non **null** al parametro *pHResult* quando si fornisce **null** al parametro *pPump* . Per ulteriori informazioni su questa situazione, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su **D3DX11CompileFromFile**, vedere [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

È necessario fornire **null** al parametro *pHResult* se si fornisce anche **null** al parametro *pPump* . In caso contrario, non è possibile creare uno shader usando il codice dello shader compilato restituito da **D3DX11CompileFromFile** nella memoria a cui punta il parametro *ppShader* . Per creare uno shader dal codice dello shader rispettato, chiamare uno dei seguenti metodi di interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Inoltre, se si fornisce un valore non **null** a *pHResult* quando si fornisce **null** a *pPump*, **D3DX11CompileFromFile** restituisce il codice di \_ errore E INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

