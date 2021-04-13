---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Descrive un gruppo di segmenti di memoria per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399168"
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

Specifica la scheda fisica del dispositivo per la quale vengono eseguite query sulle informazioni sulla memoria dell'adapter. Per l'operazione a singolo adapter, impostare su zero. Se sono presenti più nodi dell'adapter, impostarlo sull'indice del nodo (scheda fisica del dispositivo) per cui si desidera eseguire una query per le informazioni sulla memoria dell'adapter (vedere [sistemi a più schede](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>segmentGroup

Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Specifica il raggruppamento del segmento di memoria dell'adapter su cui si desidera eseguire una query.

## <a name="see-also"></a>Vedi anche

[Riferimento a DXCore](../dxcore-reference.md)

[Uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)

[Sistemi con più adapter](../../direct3d12/multi-engine.md)