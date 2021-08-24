---
description: Nota Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando Fxc.exe compilatore da riga di comando o l'API D3DCompile. Compilare uno shader o un effetto da una risorsa.
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
ms.openlocfilehash: 2c938ca302e21be16dfd1d2700a80e0ee350d7acb52ce7ab72fe2c52cbae4bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634931"
---
# <a name="d3dx10compilefromresource-function"></a>Funzione D3DX10CompileFromResource

> [!Note]  
> Anziché usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando Fxc.exe compilatore da riga di comando o usare l'API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

 

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

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle al modulo della risorsa contenente lo shader. È possibile ottenere HMODULE con [la funzione GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome della risorsa contenente lo shader. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*pSrcFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

facoltativo. Nome file dell'effetto, usato solo per i messaggi di errore. Può essere **NULL.**

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

facoltativo. Puntatore a una matrice di definizioni di macro (vedere [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)). L'ultima struttura nella matrice funge da terminatore e deve avere tutti i membri impostati su 0. Se non viene usato, *impostare pDefines* su **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

facoltativo. Puntatore a [**un'interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) per la gestione dei file di inclusione. L'impostazione di questa proprietà su **NULL** causerà un errore di compilazione se uno shader contiene \# un'inclusione.

</dd> <dt>

*pFunctionName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome della funzione del punto di ingresso shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX10CompileFromResource** ignora *pFunctionName*; È consigliabile impostare *pFunctionName* su **NULL** perché è consigliabile impostare un parametro puntatore su **NULL** se la funzione chiamata non lo userà.

</dd> <dt>

*pProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che specifica il modello shader. può essere qualsiasi profilo nel modello [shader 2,](../direct3dhlsl/dx-graphics-hlsl-sm2.md)nel modello [shader 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o nel [modello shader 4.](../direct3dhlsl/dx-graphics-hlsl-sm4.md)

</dd> <dt>

*Flag1* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Flag di compilazione shader](d3d10-shader.md).

</dd> <dt>

*Flag2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Flag di compilazione dell'effetto](d3d10-graphics-reference-effect-constants.md). Quando si compila uno shader e non un file di effetti, **D3DX10CompileFromResource** ignora *Flags2*; È consigliabile impostare *Flags2* su zero perché è buona norma di programmazione impostare un parametro nonpointer su zero se la funzione chiamata non lo userà.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntatore a un'interfaccia thread pump (vedere [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Usare **NULL** per specificare che questa funzione non deve restituire finché non viene completata.

</dd> <dt>

*ppShader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a [**un'interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene lo shader compilato, nonché qualsiasi informazione incorporata sul debug e sulla tabella dei simboli.

</dd> <dt>

*ppErrorMsgs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a [**un'interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene un elenco di errori e avvisi che si sono verificati durante la compilazione. Questi errori e avvisi sono identici all'output di debug di un debugger.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere un percorso di memoria valido fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
