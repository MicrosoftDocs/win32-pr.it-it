---
description: Il metodo QueueSample Accoda un campione.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Metodo COutputQueue. QueueSample (Outputq. h)
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
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324682"
---
# <a name="coutputqueuequeuesample-method"></a>COutputQueue. QueueSample, metodo

Il `QueueSample` Metodo Accoda un campione.

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

Questo metodo aggiunge un campione alla parte finale della coda. Mantenere la sezione critica prima di chiamare questo metodo e chiamarla solo quando l'oggetto utilizza un thread per recapitare esempi. Per determinare se l'oggetto utilizza un thread, chiamare il metodo [**COutputQueue:: di Accodamento**](coutputqueue-isqueued.md) .

Questo metodo può essere utilizzato anche per inserire i messaggi di controllo nella coda. Un messaggio di controllo è una costante definita (di cui viene eseguito il cast a un \_ tipo Long PTR) che indica al thread di eseguire un'azione. La classe **COutputQueue** definisce i messaggi di controllo mostrati nella tabella seguente.



|               |                                        |
|---------------|----------------------------------------|
| Message       | Azione                                 |
| \_pacchetto EOS   | Recapitare una notifica di fine del flusso. |
| NUOVO \_ segmento  | Recapitare un nuovo segmento.                 |
| Reimposta \_ pacchetto | Reimpostare lo stato della coda.          |
| Invia \_ pacchetto  | Inviare un batch parziale di campioni.       |



 

Si tratta di un metodo protetto, che la classe **COutputQueue** utilizza internamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




