---
description: Questa struttura contiene i dati per la segnalazione di utilizzo intensivo della memoria.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Struttura D3DMEMORYPRESSURE (D3d9types. h) per Microsoft Media Foundation
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
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334396"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Struttura D3DMEMORYPRESSURE (D3d9types. h) per Microsoft Media Foundation

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

Numero di byte rimossi dal processo durante la durata della query.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Numero totale di byte posizionati in segmenti di memoria non ottimali a causa di uno spazio inadeguato nei segmenti di memoria preferiti.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Efficienza complessiva delle allocazioni di memoria posizionate nella memoria non ottimale. Il valore è espresso come percentuale. Ad esempio, il valore 95 indica che le allocazioni posizionate nei segmenti di memoria non preferiti sono efficienti al 95%. Questo numero non deve essere considerato una misura esatta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato | \[Solo app desktop di Windows 7\]                                                              |
| Server minimo supportato | Solo app desktop Windows Server 2008 R2 \[\]                                                 |
| Intestazione                  | D3d9types. h (include d3d9. h) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Segnalazione di utilizzo intensivo della memoria](memory-pressure-reporting.md)
</dt> </dl>

 

 




