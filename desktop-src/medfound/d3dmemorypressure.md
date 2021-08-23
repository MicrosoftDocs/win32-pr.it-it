---
description: Questa struttura contiene i dati per la creazione di report sull'utilizzo della memoria.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Struttura D3DMEMORYPRESSURE (D3d9types.h) per Microsoft Media Foundation
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
ms.openlocfilehash: ec6fdf0d27edb5e1cafa575664b07dfe0807c8d124e1b066161734e75247709f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449421"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Struttura D3DMEMORYPRESSURE (D3d9types.h) per Microsoft Media Foundation

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

Numero di byte che sono stati sgomberati dal processo durante la durata della query.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Numero totale di byte inseriti in segmenti di memoria non nonoptimal, a causa di spazio non adeguato all'interno dei segmenti di memoria preferiti.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Efficienza complessiva delle allocazioni di memoria inserite in memoria non ottimale. Il valore è espresso come percentuale. Ad esempio, il valore 95 indica che le allocazioni inserite in segmenti di memoria non di riferimento sono efficienti al 95%. Questo numero non deve essere considerato una misura esatta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 7 \[ app desktop\]                                                              |
| Server minimo supportato | Windows Solo app desktop server 2008 R2 \[\]                                                 |
| Intestazione                  | D3d9types.h (includere D3d9.h) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Creazione di report sull'utilizzo della memoria](memory-pressure-reporting.md)
</dt> </dl>

 

 




