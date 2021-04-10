---
description: Evento di traccia di gestione della memoria per un'operazione di allocazione heap.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: Evento ETW_HEAP_EVENT_ALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343621"
---
# <a name="etw_heap_event_alloc-event"></a>\_Evento di \_ allocazione evento heap ETW \_

L'evento di allocazione **\_ \_ evento \_ heap ETW** è un evento di traccia di gestione della memoria per un'operazione di allocazione heap.


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle dell'heap in cui è stata allocata la memoria. Si tratta dell'heap che consente di gestire un'app passata alla funzione [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.

</dd> <dt>

*Dimensioni* 
</dt> <dd>

Dimensioni in byte allocate dall'heap.

</dd> <dt>

*Indirizzo* 
</dt> <dd>

Indirizzo della memoria allocata.

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
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **Memoria \_ da \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria da percorso lento.<br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**Memoria \_ di DA \_ 5 non valido**</dt> <dt></dt> </dl>                                             | Memoria non valida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**Memoria \_ di Dall' \_ \_ heap del segmento**</dt> <dt>6</dt> </dl>                             | Questo valore è riservato per un utilizzo futuro e non verrà mai restituito.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento di allocazione **\_ \_ evento \_ heap ETW** viene registrato per tutte le allocazioni di heap.

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

 

 
