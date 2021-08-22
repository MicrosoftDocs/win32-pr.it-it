---
description: Evento di traccia di gestione della memoria per un'operazione di riallocazione dell'heap.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC eventi (Ntwmi.h)
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
ms.openlocfilehash: 705f31eaf403c4edd608c0b3347713e43ec3c81746b5efde90e14b7213425963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067871"
---
# <a name="etw_heap_event_realloc-event"></a>EVENTO \_ \_ REALLOC DELL'HEAP ETW \_

**L'evento ETW \_ HEAP EVENT \_ \_ REALLOC è** un evento di traccia di gestione della memoria per un'operazione di riallocazione heap.


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HeapHandle* 
</dt> <dd>

Handle dell'heap in cui è stata allocata la memoria. Si tratta dell'handle dell'heap passato a un'app alla [**funzione AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.

</dd> <dt>

*NewAddress* 
</dt> <dd>

Nuovo indirizzo della memoria allocata.

</dd> <dt>

*Indirizzo precedente* 
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

Nella tabella seguente sono elencati i valori possibili per *il parametro Source* come definito nel file di intestazione *ntetw.h:*



| Valore                                                                                                                                                                                                                                                                               | Significato                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <dt>**MEMORY \_ DA \_ LOOKASIDE**</dt> <dt>1</dt> </dl>                                       | Memoria dall'elenco lookaside.<br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <dt>**MEMORY \_ FROM \_ LOWFRAG**</dt> <dt>2</dt> </dl>                                             | Memoria dall'heap a bassa frammentazione.<br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <dt>**MEMORY \_ FROM \_ MAINPATH**</dt> <dt>3</dt> </dl>                                          | Memoria dal percorso del codice principale.<br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <dt> **MEMORIA \_ DA \_ SLOWPATH**</dt> <dt>4</dt> </dl> | Memoria da c lenta.<br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <dt>**MEMORY \_ FROM \_ INVALID**</dt> <dt>5</dt> </dl>                                             | Memoria non valida.<br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <dt>**MEMORY \_ FROM \_ SEGMENT \_ HEAP**</dt> <dt>6</dt> </dl>                             | Questo valore è riservato per un uso futuro e non verrà mai restituito.<br/> |



 

</dd> </dl>

Questo evento non ha parametri.

## <a name="remarks"></a>Commenti

**L'evento ETW \_ HEAP EVENT \_ \_ REALLOC** viene registrato in tutte le riallocazioni dell'heap.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Ntwmi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di traccia di gestione della memoria](memory-management-tracing-events.md)
</dt> </dl>

 

 
