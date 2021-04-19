---
description: Contiene i dati per la segnalazione di richieste di memoria.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Struttura D3DMEMORYPRESSURE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322925"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Struttura D3DMEMORYPRESSURE (D3d9types. h)

Contiene i dati per la segnalazione di richieste di memoria.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Members

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

Tipo: **[ **UInt64**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di byte rimossi dal processo durante la durata della query.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Tipo: **[ **UInt64**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero totale di byte posizionati in segmenti di memoria non ottimali a causa di uno spazio inadeguato nei segmenti di memoria preferiti.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Efficienza complessiva delle allocazioni di memoria posizionate nella memoria non ottimale. Il valore è espresso come percentuale. Ad esempio, il valore 95 indica che le allocazioni posizionate nei segmenti di memoria non preferiti sono efficienti al 95%. Questo numero non deve essere considerato una misura esatta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
