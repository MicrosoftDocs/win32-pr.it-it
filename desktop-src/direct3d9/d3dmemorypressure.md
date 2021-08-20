---
description: Contiene i dati per la creazione di report sull'utilizzo della memoria.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Struttura D3DMEMORYPRESSURE (D3d9types.h)
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
ms.openlocfilehash: ca5a6dd95a35cae231b80fbeee9ee05bbdfe9f0ecacc70b13493ad8d16739637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911095"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Struttura D3DMEMORYPRESSURE (D3d9types.h)

Contiene i dati per la creazione di report sull'utilizzo della memoria.

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

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di byte che sono stati sgomberati dal processo durante la durata della query.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero totale di byte inseriti in segmenti di memoria non nonoptimal, a causa di spazio non adeguato all'interno dei segmenti di memoria preferiti.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Efficienza complessiva delle allocazioni di memoria inserite in memoria non ottimale. Il valore è espresso come percentuale. Ad esempio, il valore 95 indica che le allocazioni inserite in segmenti di memoria non di riferimento sono efficienti al 95%. Questo numero non deve essere considerato una misura esatta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
