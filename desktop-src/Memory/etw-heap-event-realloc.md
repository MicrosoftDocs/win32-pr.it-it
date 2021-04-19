---
description: Evento di traccia della gestione della memoria per un'operazione di riallocazione dell'heap.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Evento ETW_HEAP_EVENT_REALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311740"
---
# <a name="etw_heap_event_realloc-event"></a>Evento \_ \_ REALLOC evento \_ heap ETW

L'evento **ETW \_ heap \_ Event \_ REALLOC** è un evento di traccia di gestione della memoria per un'operazione di riallocazione dell'heap.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle dell'heap in cui è stata allocata la memoria. Si tratta dell'heap che consente di gestire un'app passata alla funzione [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.

</dd> <dt>

*NewAddress* 
</dt> <dd>

Nuovo indirizzo della memoria allocata.

</dd> <dt>

*OldAddress* 
</dt> <dd>

Indirizzo precedente della memoria allocata in precedenza.

</dd> <dt>

*NewSize* 
</dt> <dd>

Nuova dimensione in byte allocata dall'heap.

</dd> <dt>

*OldSize* 
</dt> <dd>

Dimensione precedente in byte allocata in precedenza dall'heap.

</dd> <dt>

*Origine* 
</dt> <dd>

Origine della memoria utilizzata dall'allocatore per l'allocazione dell'heap.

Nella tabella seguente sono elencati i valori possibili per il parametro di *origine* , come definito nel file di intestazione *ntetw. h* :



| Valore                                                                                                                                                                                                                                                                               | Significato                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**Memoria \_ di DA \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Memoria dall'elenco lookaside.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**Memoria \_ di DA \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memoria dall'heap di frammentazione bassa.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**Memoria \_ di DA \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memoria dal percorso del codice principale.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **Memoria \_ da \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria da c lento.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**Memoria \_ di DA \_ 5 non valido**</dt> <dt></dt> </dl>                                             | Memoria non valida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**Memoria \_ di Dall' \_ \_ heap del segmento**</dt> <dt>6</dt> </dl>                             | Questo valore è riservato per un utilizzo futuro e non verrà mai restituito.<br/> |



 

</dd> </dl>

Questo evento non contiene parametri.

## <a name="remarks"></a>Commenti

L'evento **ETW \_ heap \_ Event \_ REALLOC** viene registrato in tutte le riallocazioni dell'heap.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Ntwmi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di traccia di gestione della memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
