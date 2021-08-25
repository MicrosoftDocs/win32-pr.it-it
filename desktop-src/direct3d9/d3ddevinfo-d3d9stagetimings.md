---
description: Percentuale di tempo di elaborazione dei dati shader.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: D3DDEVINFO_D3D9STAGETIMINGS struttura (D3D9Types.h)
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
ms.openlocfilehash: eb4302b86d31c074f58fd003601557864aee152da9e532771336097f4228ea61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676731"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>Struttura D3DDEVINFO \_ D3D9STAGETIMINGS

Percentuale di tempo di elaborazione dei dati shader.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato nello shader per gli accessi alla memoria.

</dd> <dt>

**ComputationProcessingPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo di elaborazione (spostamento dei dati nei registri o esecuzione di operazioni matematiche).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per prestazioni ottimali, è consigliabile un carico bilanciato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
