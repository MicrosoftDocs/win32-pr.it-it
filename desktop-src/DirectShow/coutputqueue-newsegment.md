---
description: Il metodo NewSegment recapita un nuovo segmento al pin di input.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Metodo COutputQueue. NewSegment (Outputq. h)
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
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329521"
---
# <a name="coutputqueuenewsegment-method"></a>COutputQueue. NewSegment, metodo

Il `NewSegment` Metodo recapita un nuovo segmento al pin di input.

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

Posizione iniziale del supporto del segmento, in unità di 100 nanosecondi.

</dd> <dt>

*tStop* 
</dt> <dd>

Posizione media finale del segmento, in unità da 100 nanosecondi.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocità di elaborazione del segmento, espresso come percentuale della frequenza originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Se l'oggetto utilizza un thread, Accoda gli elementi seguenti in ordine:

-   NUOVO \_ messaggio di controllo del segmento.
-   Dati del segmento.

Il \_ messaggio nuovo segmento notifica al thread che l'elemento successivo nella coda conterrà i dati del segmento. I dati del segmento vengono aggregati in una struttura, dichiarati come segue:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



Il thread chiama il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input, usando i dati forniti nella struttura.

Se l'oggetto non utilizza un thread, viene chiamato il metodo [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) per recapitare eventuali esempi in sospeso. Chiama quindi **Ipin:: NewSegment** sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




