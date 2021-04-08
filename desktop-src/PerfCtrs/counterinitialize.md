---
description: Registra il provider e inizializza gli insiemi di contatori.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967521"
---
# <a name="counterinitialize-function"></a>CounterInitialize (funzione)

Registra il provider e inizializza gli insiemi di contatori.

## <a name="syntax"></a>Sintassi


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ l'errore in caso di esito positivo; in caso contrario, un codice di errore Win32 standard.

## <a name="remarks"></a>Commenti

Il provider chiama questa funzione. La funzione include le chiamate alla funzione [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) e alla funzione [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .

Lo strumento [**CTRPP**](ctrpp.md) genera questa funzione inline quando si specifica l'argomento **-o** . Il nome della funzione include una stringa di *prefisso* se si specifica l'argomento **-Prefix** .

Se si specificano gli argomenti **-MemoryRoutines** o **-NotificationCallback** (o si specifica l'attributo di **callback** per l'elemento [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) ), la firma **CounterInitialize** apportata come segue:

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

dove

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback
</dt> <dd>

Nome della funzione di callback [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) implementata per ricevere la notifica delle richieste del consumer (ad esempio, le richieste di aggiungere o rimuovere i contatori dalla query). Impostare su **null** se non si implementa la funzione di callback *ControlCallback* .

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

Nome della funzione di callback [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) chiamata da Perflib per allocare memoria. Impostare su **null** se non è stato specificato l'argomento **-MemoryRoutines** .

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

Nome della funzione di callback [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) chiamata da Perflib per liberare la memoria allocata tramite la funzione [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) . Impostare su **null** se *MemoryAllocationFunction* è **null**.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext
</dt> <dd>

Informazioni di contesto da passare all'allocazione di memoria e alle routine gratuite. Può essere **null**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

