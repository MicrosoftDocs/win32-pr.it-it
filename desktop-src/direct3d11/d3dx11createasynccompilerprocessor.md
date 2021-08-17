---
title: Funzione D3DX11CreateAsyncCompilerProcessor (D3DX11async.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un processore di dati asincrono per uno shader.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Funzione D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5d3767bafda4f1914d37b7baacf599335877c30de216282f172ebe55739920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124906"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a>Funzione D3DX11CreateAsyncCompilerProcessor

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.

 

Creare un processore di dati asincrono per uno shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Stringa che contiene il nome file dello shader.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const D3D11 \_ SHADER \_ MACRO \***

Matrice con terminazione NULL di macro shader. impostare questa proprietà **su NULL** per non specificare macro.

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntatore a un'interfaccia di inclusione. Questo parametro può essere **NULL**.

</dd> <dt>

*pFunctionName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX11CreateAsyncCompilerProcessor** ignora *pFunctionName*; È consigliabile impostare *pFunctionName* su **NULL** perché è consigliabile impostare un parametro del puntatore su **NULL** se la funzione chiamata non lo userà.

</dd> <dt>

*pProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Stringa che specifica il profilo shader o il modello di shader. può essere qualsiasi profilo nel modello shader 2, nel modello shader 3, nel modello shader 4 o nel modello shader 5. Il profilo può essere anche per il tipo di effetto (ad esempio, fx \_ 4 \_ 1).

</dd> <dt>

*Flag1* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag di compilazione shader.

</dd> <dt>

*Flag2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag di compilazione dell'effetto. Quando si compila uno shader e non un file di effetto, **D3DX11CreateAsyncCompilerProcessor** ignora *Flags2*; È consigliabile impostare *Flags2* su zero perché è consigliabile impostare un parametro nonpointer su zero se la funzione chiamata non lo userà.

</dd> <dt>

*ppCompiledShader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore all'effetto compilato.

</dd> <dt>

*ppErrorBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore agli errori di compilazione.

</dd> <dt>

*ppDataProcessor* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**l'interfaccia ID3DX11DataProcessor).**](id3dx11dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Non esiste alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.

Per Windows Store, gli esempi di DirectX (ad esempio, l'esempio di esercitazione [Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Per le app desktop Win32, è possibile usare il runtime di concorrenza per implementare un elemento simile al modello di programmazione asincrona Windows Runtime. [](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

