---
title: DXCoreAdapterMemoryBudget
description: Descrive il budget della memoria per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474070"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>Struttura DXCoreAdapterMemoryBudget

Specifica lo stato dell'adattatore <em>AdapterMemoryBudget</em> , che recupera o richiede il budget di memoria dell'adapter per l'adapter. Impostando (richiedente) un budget rappresenta la memoria fisica minima richiesta da riservare, in byte, sulla scheda. Si consiglia di impostare una prenotazione per l'adapter per indicare la quantità di memoria fisica che l'applicazione non può usare. Questo valore consente al sistema operativo di ridurre rapidamente l'effetto di grandi situazioni di pressione della memoria.

Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), lo stato dell'adattatore <em>AdapterMemoryBudget</em> è <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e il tipo **DXCoreAdapterMemoryBudget** per *outputBuffer*.

Quando si [chiama lo stato,](./nf-dxcore_interface-idxcoreadapter-setstate.md)lo stato dell'adattatore <em>AdapterMemoryBudget</em> è di tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e il tipo **uint64_t** per *inputData*.

## <a name="syntax"></a>Sintassi

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>Members

### <a name="budget"></a>budget

Tipo: **uint64_t**

Specifica il budget di memoria dell'adapter fornito dal sistema operativo, in byte, di destinazione dell'applicazione. Se il valore di *currentUsage* è maggiore del *budget*, l'applicazione potrebbe comportare un calo o un calo delle prestazioni a causa dell'attività in background da parte del sistema operativo, progettato per fornire ad altre applicazioni un utilizzo corretto della memoria dell'adapter.

### <a name="currentusage"></a>currentUsage

Tipo: **uint64_t**

Specifica l'utilizzo corrente della memoria dell'adapter Applicaton, in byte.

### <a name="availableforreservation"></a>availableForReservation

Tipo: **uint64_t**

Specifica la quantità di memoria dell'adapter, in byte, disponibile per la prenotazione da parte dell'applicazione. Per riservare la memoria dell'adapter, l'applicazione deve chiamare [IDXCoreAdapter:: sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md) con *stato* impostato su [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).

### <a name="currentreservation"></a>currentReservation

Tipo: **uint64_t**

Specifica la quantità di memoria dell'adapter, in byte, riservata dall'applicazione. Il sistema operativo usa la prenotazione come un suggerimento per determinare la working set minima dell'applicazione. L'applicazione deve tentare di verificare che l'utilizzo della memoria dell'adapter possa essere tagliato per soddisfare questo requisito.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)