---
description: Percentuale del tempo di elaborazione dei dati dello shader.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: Struttura D3DDEVINFO_D3D9STAGETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322403"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>\_Struttura D3DDEVINFO D3D9STAGETIMINGS

Percentuale del tempo di elaborazione dei dati dello shader.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**MemoryProcessingPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo nello shader dedicato agli accessi alla memoria.

</dd> <dt>

**ComputationProcessingPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di elaborazione del tempo (spostando i dati in registri o eseguendo operazioni matematiche).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ottenere prestazioni ottimali, è consigliabile un carico bilanciato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
