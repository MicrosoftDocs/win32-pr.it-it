---
description: Ottiene la tabella delle costanti shader incorporata all'interno di uno shader.
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: Funzione D3DXGetShaderConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTable
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 876802023601c14b4cceed0ef0e2db431d7339e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322661"
---
# <a name="d3dxgetshaderconstanttable-function"></a>D3DXGetShaderConstantTable (funzione)

Ottiene la tabella delle costanti shader incorporata all'interno di uno shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFunction* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione.

</dd> <dt>

 *ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Restituisce l'interfaccia della tabella costante (vedere [**ID3DXConstantTable**](id3dxconstanttable.md)) che gestisce la tabella delle costanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Una tabella di costanti viene generata da [**D3DXCompileShader**](d3dxcompileshader.md) e incorporata nel corpo dello shader. Se è necessario uno spazio degli indirizzi virtuali aggiuntivo, vedere [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
