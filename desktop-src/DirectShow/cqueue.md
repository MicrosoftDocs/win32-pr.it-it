---
description: Il modello di classe CQueue implementa una coda semplice e a dimensione statica.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Classe CQueue (Wxutil. h)
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
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331322"
---
# <a name="cqueue-class"></a>Classe CQueue

Il modello di classe **CQueue** implementa una coda semplice e a dimensione statica.



| Metodi pubblici                                  | Descrizione                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Metodo del costruttore.                     |
| [**~ CQueue**](cqueue--cqueue.md)               | Metodo del distruttore.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Recupera l'elemento successivo dalla coda. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Inserisce un elemento nella coda.            |



 

## <a name="remarks"></a>Commenti

Il costruttore della classe specifica le dimensioni della coda. Usare [**CQueue::P utqueueobject**](cqueue-putqueueobject.md) per inserire un elemento nella coda e il metodo [**CQueue:: GetQueueObject**](cqueue-getqueueobject.md) per rimuovere dalla coda un elemento. Se la coda è piena, il metodo **PutQueueObject** si blocca fino a quando un elemento non viene rimosso dalla coda. Se la coda è vuota, il **GetQueueObject** si blocca fino a quando un elemento non viene accodato. Il parametro di modello specifica il tipo di elemento. Ad esempio:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



La classe usa due semafori per controllare le operazioni di Accodamento, un semaforo "Get" e un semaforo "put". Il metodo [**GetQueueObject**](cqueue-getqueueobject.md) attende il semaforo "Get" (usando la funzione **WaitForSingleObject** ) e rilascia il semaforo "put" (usando la funzione **ReleaseSemaphore** ). Il metodo [**PutQueueObject**](cqueue-putqueueobject.md) attende il semaforo "put" e rilascia il semaforo "Get". La classe utilizza una sezione critica per serializzare le operazioni di Accodamento tra più thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




