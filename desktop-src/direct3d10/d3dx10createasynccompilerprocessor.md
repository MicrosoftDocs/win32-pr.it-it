---
description: Creare un processore di dati asincrono per uno shader.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Funzione D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234979"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a>D3DX10CreateAsyncCompilerProcessor (funzione)

Creare un processore di dati asincrono per uno shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che contiene il nome file dello shader.

</dd> <dt>

*pDefines* \[ in\]
</dt> <dd>

Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.

</dd> <dt>

*pInclude* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Questo parametro può essere **NULL**.

</dd> <dt>

*pFunctionName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX10CreateAsyncCompilerProcessor** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.

</dd> <dt>

*pProfile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md) o il modello dello shader.

</dd> <dt>

*Flags1* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Flag di compilazione shader](d3d10-shader.md).

</dd> <dt>

*Flags2* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

[Flag di compilazione effetto](d3d10-graphics-reference-effect-constants.md). Quando si compila uno shader e non un file di effetto, **D3DX10CreateAsyncCompilerProcessor** ignora *Flags2*; si consiglia di impostare *Flags2* su zero perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.

</dd> <dt>

*ppCompiledShader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore all'effetto compilato (vedere l' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore per la compilazione degli errori (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

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

 

 
