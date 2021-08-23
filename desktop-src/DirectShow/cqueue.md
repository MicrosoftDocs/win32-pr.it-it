---
description: Il modello di classe CQueue implementa una coda semplice con dimensioni statiche.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Classe CQueue (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c6225a393f8f6ff1848acc66c68b6d260b0c839f2cc9f1e24d06a11e88219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953980"
---
# <a name="cqueue-class"></a>Classe CQueue

Il **modello di classe CQueue** implementa una coda semplice con dimensioni statiche.



| Metodi pubblici                                  | Descrizione                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Metodo del costruttore.                     |
| [**~CQueue**](cqueue--cqueue.md)               | Metodo del distruttore.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Recupera l'elemento successivo dalla coda. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Inserisce un elemento nella coda.            |



 

## <a name="remarks"></a>Commenti

Il costruttore della classe specifica le dimensioni della coda. Usare [**CQueue::P utQueueObject**](cqueue-putqueueobject.md) per inserire un elemento nella coda e il metodo [**CQueue::GetQueueObject per dequeues**](cqueue-getqueueobject.md) un elemento. Se la coda è piena, il **metodo PutQueueObject** si blocca fino a quando non viene deaccodato un elemento. Se la coda è vuota, **GetQueueObject** si blocca fino a quando un elemento non viene accodato. Il parametro del modello specifica il tipo di elemento. Esempio:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



La classe usa due semafori per controllare le operazioni di accodamento, un semaforo "get" e un semaforo "put". Il [**metodo GetQueueObject**](cqueue-getqueueobject.md) attende il semaforo "get" (usando la funzione **WaitForSingleObject)** e rilascia il semaforo "put" (usando la funzione **ReleaseSemaphore).** Il [**metodo PutQueueObject**](cqueue-putqueueobject.md) attende il semaforo "put" e rilascia il semaforo "get". La classe usa una sezione critica per serializzare le operazioni di accodamento tra più thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




