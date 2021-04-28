---
description: 'Costruttore COutputQueue.COutputQueue : metodo del costruttore.'
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Costruttore COutputQueue.COutputQueue (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095329"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Costruttore COutputQueue.COutputQueue

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInputPin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input. L'oggetto consegnerà esempi a questo segnaposto.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **codice restituito HRESULT.** Impostare il valore su S \_ OK prima di chiamare questo metodo. In caso di restituzione, *phr* riceve un valore che indica l'esito positivo o negativo del metodo.

</dd> <dt>

*bAuto* 
</dt> <dd>

Flag che specifica se l'oggetto decide quando creare una coda. Se **TRUE,** l'oggetto crea una coda solo se il pin di input potrebbe bloccarsi. Se **FALSE,** il *parametro bQueue* specifica se creare una coda.

</dd> <dt>

*bQueue* 
</dt> <dd>

Se *bAuto* è **TRUE,** questo parametro viene ignorato. Se *bAuto* è **FALSE,** questo flag specifica se creare una coda.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Numero massimo di campioni da distribuire in un batch.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Flag che specifica se usare dimensioni esatte dei batch. Se **TRUE,** l'oggetto attende gli *esempi lBatchSize* prima di recapitarli al pin di input. Se **FALSE,** l'oggetto recapita gli esempi quando li riceve.

</dd> <dt>

*lListSize* 
</dt> <dd>

Dimensioni della cache per la coda. Il valore predefinito, DEFAULTCACHE, è una costante definita per la [**classe CBaseList.**](cbaselist.md)

</dd> <dt>

*dwPriority* 
</dt> <dd>

Priorità del thread che recapita gli esempi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *bAuto* è **TRUE,** l'oggetto chiama il metodo [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) sul pin downstream. Se **ReceiveCanBlock restituisce** S OK (ovvero il pin potrebbe bloccarsi nelle chiamate \_ [**IMemInputPin::Receive),**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) l'oggetto crea un thread per la distribuzione degli esempi. In caso contrario, non crea un thread.

Se *bAuto* è **FALSE,** il valore di *bQueue* determina se creare un thread.

Se l'oggetto crea un thread, assegna l'handle del thread alla variabile membro [**COutputQueue::m \_ hThread.**](coutputqueue-m-hthread.md) La routine del thread [**è COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md)e il parametro thread è un puntatore a questo. L'oggetto crea anche una coda per contenere gli esempi, specificata dalla variabile membro [**COutputQueue::m \_ List.**](coutputqueue-m-list.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




