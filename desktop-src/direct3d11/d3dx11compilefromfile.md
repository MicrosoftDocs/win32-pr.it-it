---
title: Funzione D3DX11CompileFromFile (D3DX11async.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando Fxc.exe o usare una delle API di compilazione HLSL, ad esempio l'API D3DCompileFromFile. Compilare uno shader o un effetto da un file.
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
ms.openlocfilehash: 53a62a5a3d60dc62317fdd6f08e99faea025a172f77af7f10fd48e6752fb1b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989871"
---
# <a name="d3dx11compilefromfile-function"></a>Funzione D3DX11CompileFromFile

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché usare questa funzione, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando Fxc.exe o usare una delle API di compilazione HLSL, ad esempio [**l'API D3DCompileFromFile.**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)

 

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

*pSrcFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del file che contiene il codice shader. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

facoltativo. Puntatore a una matrice di definizioni di macro (vedere [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). L'ultima struttura nella matrice funge da terminatore e deve avere tutti i membri impostati su 0. Se non viene usato, *impostare pDefines* su **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

facoltativo. Puntatore a un'interfaccia per la gestione dei file di inclusione. L'impostazione di questa proprietà su **NULL** causerà un errore di compilazione se uno shader contiene \# un'inclusione.

</dd> <dt>

*pFunctionName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della funzione del punto di ingresso shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX11CompileFromFile** ignora *pFunctionName*; È consigliabile impostare *pFunctionName* su **NULL** perché è consigliabile impostare un parametro puntatore su **NULL** se la funzione chiamata non lo userà.

</dd> <dt>

*pProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Stringa che specifica il modello shader. può essere qualsiasi profilo nel modello shader 2, nel modello shader 3, nel modello shader 4 o nel modello shader 5. Il profilo può essere anche per il tipo di effetto (ad esempio, fx \_ 4 \_ 1).

</dd> <dt>

*Flag1* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag [**di compilazione shader**](/windows/desktop/direct3dhlsl/d3dcompile-constants).

</dd> <dt>

*Flag2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag [**di compilazione dell'effetto**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants). Quando si compila uno shader e non un file degli effetti, **D3DX11CompileFromFile** ignora *Flags2*; È consigliabile impostare *Flags2* su zero perché è buona norma di programmazione impostare un parametro nonpointer su zero se la funzione chiamata non lo userà.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia thread pump (vedere [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Usare **NULL** per specificare che questa funzione non deve restituire finché non viene completata.

</dd> <dt>

*ppShader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria che contiene lo shader compilato, nonché qualsiasi informazione incorporata sul debug e sulla tabella dei simboli.

</dd> <dt>

*ppErrorMsgs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria che contiene un elenco di errori e avvisi che si sono verificati durante la compilazione. Questi errori e avvisi sono identici all'output di debug di un debugger.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere un percorso di memoria valido fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

**D3DX11CompileFromFile** restituisce E INVALIDARG se si specifica un valore non NULL al parametro pHResult quando si specifica NULL al \_ parametro *pPump.*    Per altre informazioni su questa situazione, vedere Note.

## <a name="remarks"></a>Commenti

Per altre informazioni su **D3DX11CompileFromFile,** vedere [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).

È necessario fornire **NULL** al *parametro pHResult* se si specifica **anche NULL** al *parametro pPump.* In caso contrario, non è possibile creare uno shader usando il codice shader compilato restituito da **D3DX11CompileFromFile** nella memoria a cui punta il *parametro ppShader.* Per creare uno shader dal codice dello shader conforme, chiamare uno dei metodi di interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) seguenti:

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Inoltre, se si specifica un valore non **NULL** a *pHResult* quando si specifica **NULL** a *pPump,* **D3DX11CompileFromFile** restituisce il codice di errore E \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

