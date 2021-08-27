---
description: Restituisce le dimensioni di un vertice per un formato di vertice flessibile (FVF).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Funzione D3DXGetFVFVertexSize (D3dx9mesh.h)
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
ms.openlocfilehash: f00faa489481faf436a30fe6e6313429d446cd8000173131d823442e960b5a08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119211"
---
# <a name="d3dxgetfvfvertexsize-function"></a>Funzione D3DXGetFVFVertexSize

Restituisce le dimensioni di un vertice per un formato di vertice flessibile (FVF).

## <a name="syntax"></a>Sintassi


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FVF* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

FVF su cui eseguire query. Combinazione di [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensioni del vertice FVF, in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
