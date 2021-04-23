---
description: Il metodo QueueSample accoda un esempio.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Metodo COutputQueue.QueueSample (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910069"
---
# <a name="coutputqueuequeuesample-method"></a>Metodo COutputQueue.QueueSample

Il `QueueSample` metodo accoda un esempio.

## <a name="syntax"></a>Sintassi


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo aggiunge un campione alla parte finale della coda. Mantenere la sezione critica prima di chiamare questo metodo e chiamarla solo quando l'oggetto usa un thread per distribuire i campioni. Per determinare se l'oggetto usa un thread, chiamare il [**metodo COutputQueue::IsQueued.**](coutputqueue-isqueued.md)

Questo metodo può essere usato anche per inserire i messaggi di controllo nella coda. Un messaggio di controllo è una costante definita (cast a un tipo PTR LONG) che indica al \_ thread di eseguire un'azione. La **classe COutputQueue** definisce i messaggi di controllo illustrati nella tabella seguente.



| Label | Valore |
|---------------|----------------------------------------|
| Message       | Azione                                 |
| PACCHETTO \_ EOS   | Recapitare una notifica di fine flusso. |
| NUOVO \_ SEGMENTO  | Distribuire un nuovo segmento.                 |
| REIMPOSTA \_ PACCHETTO | Reimpostare lo stato della coda.          |
| SEND \_ PACKET  | Inviare un batch parziale di campioni.       |



 

Si tratta di un metodo protetto, che la **classe COutputQueue usa** internamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




