---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Descrive un gruppo di segmenti di memoria per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b39557226034e9462e8d51c79aa9b8276659cfe296138df2a3a57f279106f5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118655"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>Struttura DXCoreAdapterMemoryBudgetNodeSegmentGroup

Descrive un gruppo di segmenti di memoria per un adapter.

## <a name="syntax"></a>Sintassi

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Members

### <a name="nodeindex"></a>nodeIndex

Tipo: **uint32_t**

Specifica l'adattatore fisico del dispositivo per il quale vengono richieste le informazioni sulla memoria della scheda. Per l'operazione a scheda singola, impostare questa proprietà su zero. Se sono presenti più nodi di scheda, impostare questo valore sull'indice del nodo (la scheda fisica del dispositivo) per il quale si desidera eseguire una query per ottenere informazioni sulla memoria della scheda (vedere Sistemi con più [schede).](../../direct3d12/multi-engine.md)

### <a name="segmentgroup"></a>segmentGroup

Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Specifica il raggruppamento dei segmenti di memoria dell'adattatore su cui si desidera eseguire una query.

## <a name="see-also"></a>Vedi anche

[Informazioni di riferimento su DXCore](../dxcore-reference.md)

[Uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)

[Sistemi con più schede](../../direct3d12/multi-engine.md)