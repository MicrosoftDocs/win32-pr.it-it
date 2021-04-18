---
description: Restituisce le dimensioni in byte del codice byte dello shader.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Funzione D3DXGetShaderSize (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322655"
---
# <a name="d3dxgetshadersize-function"></a>D3DXGetShaderSize (funzione)

Restituisce le dimensioni in byte del codice byte dello shader.

## <a name="syntax"></a>Sintassi


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFunction* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Restituisce le dimensioni in byte del codice byte dello shader.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
