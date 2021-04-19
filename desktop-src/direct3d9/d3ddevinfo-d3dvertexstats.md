---
description: Indica il numero di triangoli elaborati e ritagliati dall'elaborazione dei vertici software del runtime.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: Struttura D3DDEVINFO_D3DVERTEXSTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3baa6738e5d90d2353beb6c7d7bf0ab85770af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322402"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>\_Struttura D3DDEVINFO D3DVERTEXSTATS

Indica il numero di triangoli elaborati e ritagliati dall'elaborazione dei vertici software del runtime.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero totale di triangoli non ritagliati in questo frame.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di nuovi triangoli generati dal ritaglio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare il runtime di debug e l'elaborazione dei vertici software per ottenere il numero di primitive non ritagliate e ritagliate per una particolare scena. Le primitive vengono in genere ritagliate in base a una banda di protezione (se presente). Il gruppo di protezione di ritaglio viene impostato con parametri come GuardBandLeft in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
