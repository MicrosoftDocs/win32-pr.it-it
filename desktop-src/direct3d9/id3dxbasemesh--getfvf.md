---
description: Ottiene il valore del vertice della funzione fissa.
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'Metodo ID3DXBaseMesh:: GetFVF (D3DX9Mesh. h)'
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
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969394"
---
# <a name="id3dxbasemeshgetfvf-method"></a>Metodo ID3DXBaseMesh:: GetFVF

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

Questo metodo può restituire 0 se non è possibile eseguire il mapping diretto del formato vertex a un codice FVF. Ciò si verifica per una mesh creata da una dichiarazione di vertice che non ha lo stesso ordine e gli stessi elementi supportati dai codici FVF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
