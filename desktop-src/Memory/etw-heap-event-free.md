---
description: Evento di traccia di gestione della memoria per un'operazione senza heap.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: ETW_HEAP_EVENT_FREE evento (Ntwmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 4cdc7623f666e20b40bda5393b3ff31369181a7f93f3f2f2dc9881cf0c91f7ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992878"
---
# <a name="etw_heap_event_free-event"></a>Evento \_ ETW HEAP \_ EVENT \_ FREE

**L'evento ETW \_ HEAP EVENT \_ \_ FREE** è un evento di traccia di gestione della memoria per un'operazione senza heap.


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle dell'heap in cui è stata allocata la memoria. Si tratta dell'heap handle di un'app passata alla [**funzione AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.

</dd> <dt>

*Indirizzo* 
</dt> <dd>

Indirizzo della memoria liberata.

</dd> <dt>

*Origine* 
</dt> <dd>

Origine della memoria usata dall'allocatore per l'allocazione dell'heap.

Nella tabella seguente sono elencati i valori possibili per il *parametro Source,* come definito nel file di intestazione *ntetw.h:*



| Valore                                                                                                                                                                                                                                                                               | Significato                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**MEMORIA \_ DA \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Memoria dall'elenco lookaside.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**MEMORIA \_ DA \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memoria dall'heap a bassa frammentazione.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**MEMORIA \_ FROM \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memoria dal percorso del codice principale.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **MEMORIA \_ DA \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria da c lenta.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**MEMORIA \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Memoria non valida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**MEMORIA \_ \_ \_ DALL'HEAP DEI SEGMENTI**</dt> <dt>6</dt> </dl>                             | Questo valore è riservato per un uso futuro e non verrà mai restituito.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'evento EVENT \_ \_ \_ FREE dell'heap ETW** viene registrato in tutte le operazioni senza heap.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di traccia di Gestione memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
