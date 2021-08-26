---
description: Restituisce le dimensioni di un vertice dalla dichiarazione del vertice.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Funzione D3DXGetDeclVertexSize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c120e0089c350133372526f1b030eb1a94ede5a511ba44fb21b5ae320aa7090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986861"
---
# <a name="d3dxgetdeclvertexsize-function"></a>Funzione D3DXGetDeclVertexSize

Restituisce le dimensioni di un vertice dalla dichiarazione del vertice.

## <a name="syntax"></a>Sintassi


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDecl* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntatore alla dichiarazione del vertice. Vedere [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> <dt>

*Flusso* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice del flusso in base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensioni della dichiarazione del vertice, in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
