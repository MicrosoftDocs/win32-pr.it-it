---
description: Nota Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando Fxc.exe o l'API D3DCompile. Compilare uno shader o un effetto caricato in memoria.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Funzione D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: f5cd6772079f872fe575a3a2f49fee536b89dab00f29a62dba151842dbc99b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281711"
---
# <a name="d3dx10compilefrommemory-function"></a>Funzione D3DX10CompileFromMemory

> [!Note]  
> Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe della riga di comando o l'API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)

 

Compilare uno shader o un effetto caricato in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
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

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore allo shader in memoria.

</dd> <dt>

*SrcDataLen* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Dimensioni dello shader in memoria.

</dd> <dt>

*pFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del file che contiene il codice dello shader.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

facoltativo. Puntatore a una matrice di definizioni di macro (vedere [**D3D \_ SHADER \_ MACRO).**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) L'ultima struttura nella matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0. Se non viene usato, *impostare pDefines* su **NULL.**

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

facoltativo. Puntatore a [**un'interfaccia ID3D10Include per**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) la gestione dei file di inclusione. L'impostazione di **questa proprietà su NULL** causerà un errore di compilazione se uno shader contiene \# un'inclusione.

</dd> <dt>

*pFunctionName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader. Quando si compila un effetto, **D3DX10CompileFromMemory** ignora *pFunctionName*; È consigliabile impostare *pFunctionName* su **NULL** perché è consigliabile impostare un parametro del puntatore su **NULL** se la funzione chiamata non lo userà.

</dd> <dt>

*pProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che specifica il modello di shader. può essere qualsiasi profilo nel [modello shader 2,](../direct3dhlsl/dx-graphics-hlsl-sm2.md) [nel modello shader 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o nel [modello shader 4.](../direct3dhlsl/dx-graphics-hlsl-sm4.md)

</dd> <dt>

*Flag1* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Flag di compilazione shader](d3d10-shader.md).

</dd> <dt>

*Flag2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

[Flag di compilazione dell'effetto](d3d10-graphics-reference-effect-constants.md). Quando si compila uno shader e non un file di effetto, **D3DX10CompileFromMemory** ignora *Flags2*; È consigliabile impostare *Flags2* su zero perché è consigliabile impostare un parametro nonpointer su zero se la funzione chiamata non lo userà.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntatore a un'interfaccia pump di thread (vedere [**l'interfaccia ID3DX10ThreadPump).**](id3dx10threadpump.md) Usare **NULL** per specificare che questa funzione non deve restituire alcun valore finché non viene completata.

</dd> <dt>

*ppShader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a [**un'interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene lo shader compilato, nonché eventuali informazioni incorporate sul debug e sulla tabella dei simboli.

</dd> <dt>

*ppErrorMsgs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntatore a [**un'interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene un elenco di errori e avvisi che si sono verificati durante la compilazione. Questi errori e avvisi sono identici all'output di debug di un debugger.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
