---
description: Il metodo NewSegment recapita un nuovo segmento al pin di input.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Metodo COutputQueue.NewSegment (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768141"
---
# <a name="coutputqueuenewsegment-method"></a>Metodo COutputQueue.NewSegment

Il `NewSegment` metodo recapita un nuovo segmento al pin di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Posizione media iniziale del segmento, in unità da 100 nanosecondi.

</dd> <dt>

*tStop* 
</dt> <dd>

Posizione media finale del segmento, in unità da 100 nanosecondi.

</dd> <dt>

*dRate* 
</dt> <dd>

Frequenza con cui deve essere elaborato questo segmento, come percentuale della tariffa originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Se l'oggetto usa un thread, accoda gli elementi seguenti, nell'ordine indicato:

-   Messaggio di \_ controllo NEW SEGMENT.
-   Dati del segmento.

Il messaggio NEW \_ SEGMENT notifica al thread che l'elemento successivo nella coda conterrà i dati del segmento. I dati del segmento vengono aggregati in una struttura , dichiarati come segue:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



Il thread chiama il [**metodo IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input, usando i dati dati nella struttura .

Se l'oggetto non usa un thread, chiama il metodo [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) per recapitare eventuali esempi in sospeso. Chiama quindi **IPin::NewSegment** sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




