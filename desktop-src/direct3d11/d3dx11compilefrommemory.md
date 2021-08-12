---
title: Funzione D3DX11CompileFromMemory (D3DX11async.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando di Fxc.exe o usare una delle API di compilazione HLSL, ad esempio l'API D3DCompile. Compilare uno shader o un effetto caricato in memoria.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- Funzione D3DX11CompileFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 055fa070eb698298716abef11090a8c178cb4ef85f46bc6733df037a5778e4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536820"
---
# <a name="d3dx11compilefrommemory-function"></a>Funzione D3DX11CompileFromMemory

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando di Fxc.exe o una delle API di compilazione HLSL, come l'API [**D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile)

 

Compilare uno shader o un effetto caricato in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
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

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore allo shader in memoria.

</dd> <dt>

*SrcDataLen* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni dello shader in memoria.

</dd> <dt>

*pFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del file che contiene il codice dello shader.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D10 \_ SHADER \_ MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

facoltativo. Puntatore a una matrice di definizioni di macro (vedere [**D3D10 \_ SHADER \_ MACRO).**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) L'ultima struttura nella matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0. Se non viene usato, *impostare pDefines* su **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

facoltativo. Puntatore a un'interfaccia per la gestione dei file di inclusione. L'impostazione di **questa proprietà su NULL** causerà un errore di compilazione se uno shader contiene \# un'inclusione.

</dd> <dt>

*pFunctionName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX11CompileFromMemory** ignora *pFunctionName*; È consigliabile impostare *pFunctionName* su **NULL** perché è consigliabile impostare un parametro del puntatore su **NULL** se la funzione chiamata non lo userà.

</dd> <dt>

*pProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Stringa che specifica il modello di shader. può essere qualsiasi profilo nel modello shader 2, nel modello shader 3, nel modello shader 4 o nel modello shader 5. Il profilo può essere anche per il tipo di effetto (ad esempio, fx \_ 4 \_ 1).

</dd> <dt>

*Flag1* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag [**di compilazione shader**](/windows/desktop/direct3dhlsl/d3dcompile-constants).

</dd> <dt>

*Flag2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag [**di compilazione dell'effetto**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants). Quando si compila uno shader e non un file di effetto, **D3DX11CompileFromMemory** ignora *Flags2*; È consigliabile impostare *Flags2* su zero perché è consigliabile impostare un parametro nonpointer su zero se la funzione chiamata non lo userà.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntatore a un'interfaccia pump di thread (vedere [**l'interfaccia ID3DX11ThreadPump).**](id3dx11threadpump.md) Usare **NULL** per specificare che questa funzione non deve restituire alcun valore finché non viene completata.

</dd> <dt>

*ppShader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria che contiene lo shader compilato, nonché eventuali informazioni incorporate sul debug e sulla tabella dei simboli.

</dd> <dt>

*ppErrorMsgs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore alla memoria che contiene un elenco di errori e avvisi che si sono verificati durante la compilazione. Questi errori e avvisi sono identici all'output di debug di un debugger.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

**D3DX11CompileFromMemory** restituisce E INVALIDARG se si specifica un valore diverso da NULL per il parametro pHResult quando si specifica NULL al \_ parametro *pPump.*    Per altre informazioni su questa situazione, vedere La sezione Osservazioni.

## <a name="remarks"></a>Commenti

Per altre informazioni su **D3DX11CompileFromMemory,** vedere [**D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile)

È necessario fornire **NULL** al *parametro pHResult* se si specifica **anche NULL** al *parametro pPump.* In caso contrario, non è possibile creare successivamente uno shader usando il codice dello shader compilato restituito da **D3DX11CompileFromMemory** nella memoria a cui punta *il parametro ppShader.* Per creare uno shader dal codice dello shader conforme, chiamare uno dei metodi di interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) seguenti:

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Inoltre, se si specifica un valore non **NULL** a *pHResult* quando si specifica **NULL** a *pPump,* **D3DX11CompileFromMemory** restituisce il codice di errore E \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

