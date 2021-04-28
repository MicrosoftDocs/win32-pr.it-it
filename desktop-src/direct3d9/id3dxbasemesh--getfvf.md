---
description: 'Metodo ID3DXBaseMesh::GetFVF: ottiene il valore del vertice della funzione fissa.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: Metodo ID3DXBaseMesh::GetFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115439"
---
# <a name="id3dxbasemeshgetfvf-method"></a>Metodo ID3DXBaseMesh::GetFVF

Ottiene il valore del vertice della funzione fissa.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Restituisce i codici FVF (Flexible Vertex Format).

## <a name="remarks"></a>Commenti

Questo metodo può restituire 0 se il formato del vertice non può essere mappato direttamente a un codice FVF. Ciò si verifica per una mesh creata da una dichiarazione di vertice che non ha lo stesso ordine e gli elementi supportati dai codici FVF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
