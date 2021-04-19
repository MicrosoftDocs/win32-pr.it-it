---
description: Restituisce la dimensione di un vertice per un formato di vertice flessibile (FVF).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Funzione D3DXGetFVFVertexSize (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322666"
---
# <a name="d3dxgetfvfvertexsize-function"></a>D3DXGetFVFVertexSize (funzione)

Restituisce la dimensione di un vertice per un formato di vertice flessibile (FVF).

## <a name="syntax"></a>Sintassi


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FVF* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

FVF su cui eseguire una query. Combinazione di [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensioni del vertice FVF in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
