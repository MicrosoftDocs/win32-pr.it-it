---
description: Compila uno shader da un effetto che contiene una o più funzioni.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'Metodo ID3DXEffectCompiler:: CompileShader (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323081"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>Metodo ID3DXEffectCompiler:: CompileShader

Compila uno shader da un effetto che contiene una o più funzioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFunction* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco della funzione da compilare. Questo valore non può essere **null**. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*PTarget* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a un profilo dello shader che determina il set di istruzioni dello shader. Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di compilazione identificate da diversi flag. Il compilatore Direct3D 10 HLSL è ora il valore predefinito. Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .

</dd> <dt>

*ppShader* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente lo shader compilato. Lo shader del compilatore è una matrice di DWORD. Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente almeno il primo messaggio di errore di compilazione che si è verificato. Sono inclusi gli errori del compilatore degli effetti e gli errori di compilazione del linguaggio di alto livello. Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Restituisce un'interfaccia [**ID3DXConstantTable**](id3dxconstanttable.md) che può essere utilizzata per accedere alle costanti dello shader. Questo valore può essere **null**. Se l'applicazione viene compilata con un indirizzo di grandi dimensioni (ovvero si usa l'opzione del linker/LARGEADDRESSAWARE per gestire gli indirizzi maggiori di 2 GB), non è possibile usare questo parametro e deve essere impostato su **null**. È invece necessario utilizzare la funzione [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella delle costanti shader incorporata all'interno dello shader. In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK.

Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.

Se il metodo ha esito negativo, il valore restituito sarà E avrà \_ esito negativo.

## <a name="remarks"></a>Commenti

È possibile specificare le destinazioni per i vertex shader, i pixel shader e le funzioni di riempimento della trama.



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| Destinazioni vertex shader | vs \_ 1 \_ , vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0                               |
| Destinazioni pixel shader  | PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0 |
| Destinazioni riempimento trama  | TX \_ 0, TX \_ 1                                                          |



 

Questo metodo compila uno shader da una funzione scritta in un linguaggio simile a C. Per ulteriori informazioni, vedere [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
