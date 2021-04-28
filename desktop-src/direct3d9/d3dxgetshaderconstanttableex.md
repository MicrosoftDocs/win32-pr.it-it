---
description: 'Funzione D3DXGetShaderConstantTableEx: ottiene la tabella costante shader incorporata in uno shader.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Funzione D3DXGetShaderConstantTableEx (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114430"
---
# <a name="d3dxgetshaderconstanttableex-function"></a>Funzione D3DXGetShaderConstantTableEx

Ottiene la tabella costante shader incorporata all'interno di uno shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
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

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Usare il flag D3DXCONSTTABLE LARGEADDRESSAWARE per accedere a un massimo di 4 GB di spazio degli indirizzi virtuali (anziché il valore predefinito \_ di 2 GB). Se non è necessario lo spazio indirizzi virtuali aggiuntivo, usare [**D3DXGetShaderConstantTable.**](d3dxgetshaderconstanttable.md)

</dd> <dt>

 *ppConstantTable* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Restituisce l'interfaccia di tabella costante (vedere [**ID3DXConstantTable)**](id3dxconstanttable.md)che gestisce la tabella costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Una tabella costante viene generata da [**D3DXCompileShader**](d3dxcompileshader.md) e incorporata nel corpo dello shader.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
