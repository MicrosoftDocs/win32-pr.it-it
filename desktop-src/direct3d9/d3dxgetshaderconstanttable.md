---
description: 'Funzione D3DXGetShaderConstantTable: ottiene la tabella delle costanti shader incorporata in uno shader.'
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: Funzione D3DXGetShaderConstantTable (D3DX9Shader.h)
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
ms.openlocfilehash: a1375dfcf1bc75d6f2dee6f9923360b1b90fef01df5489f9f710175e7e1c2652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045009"
---
# <a name="d3dxgetshaderconstanttable-function"></a>Funzione D3DXGetShaderConstantTable

Ottiene la tabella costante shader incorporata all'interno di uno shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFunction* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione.

</dd> <dt>

 *ppConstantTable* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Restituisce l'interfaccia della tabella costante (vedere [**ID3DXConstantTable**](id3dxconstanttable.md)) che gestisce la tabella costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Una tabella costante viene generata [**da D3DXCompileShader**](d3dxcompileshader.md) e incorporata nel corpo dello shader. Se è necessario spazio di indirizzi virtuali aggiuntivo, vedere [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
