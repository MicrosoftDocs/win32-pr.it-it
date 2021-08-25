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
ms.openlocfilehash: 3770029f732629f12d94c9304d144226d873f38cc1b8452036d39ca2abdd757a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909591"
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

Questo metodo aggiunge un esempio alla parte finale della coda. Mantenere la sezione critica prima di chiamare questo metodo e chiamarlo solo quando l'oggetto usa un thread per fornire esempi. Per determinare se l'oggetto usa un thread, chiamare il [**metodo COutputQueue::IsQueued.**](coutputqueue-isqueued.md)

Questo metodo può essere usato anche per inserire i messaggi di controllo nella coda. Un messaggio di controllo è una costante definita (cast a un tipo LONG PTR) che indica al thread di \_ eseguire un'azione. La **classe COutputQueue** definisce i messaggi di controllo illustrati nella tabella seguente.



| Etichetta | Valore |
|---------------|----------------------------------------|
| Message       | Azione                                 |
| PACCHETTO \_ EOS   | Recapitare una notifica di fine flusso. |
| NUOVO \_ SEGMENTO  | Distribuire un nuovo segmento.                 |
| REIMPOSTARE \_ IL PACCHETTO | Reimpostare lo stato della coda.          |
| INVIARE \_ UN PACCHETTO  | Inviare un batch parziale di esempi.       |



 

Si tratta di un metodo protetto, che la **classe COutputQueue** usa internamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




