---
description: La classe CTransformOutputPin implementa un pin di output usato dalla classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Classe CTransformOutputPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f99b0d03eb3b2b1ac63c69620346e4db663c75730ff773de2fb1429b268aefb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756787"
---
# <a name="ctransformoutputpin-class"></a>Classe CTransformOutputPin

![Gerarchia di classi ctransformoutputpin](images/tfrm02.png)

La `CTransformOutputPin` classe implementa un pin di output usato dalla classe [**CTransformFilter.**](ctransformfilter.md)

In genere, non è necessario derivare da questa classe. La maggior parte dei metodi in questa classe chiama metodi corrispondenti nella **classe CTransformFilter,** di cui è possibile eseguire l'override. Se si deriva da questa classe, è necessario eseguire l'override del metodo [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) del filtro per creare istanze della classe derivata.

Questa classe espone le **interfacce IMediaSeeking** e **IMediaPosition** tramite l'oggetto [**CPosPassThru.**](cpospassthru.md) Passa tutte le richieste di ricerca al filtro successivo a monte.



| Variabili membro protette                                               | Descrizione                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransformoutputpin-m-ptransformfilter.md)    | Puntatore al filtro proprietario.                            |
| Variabili membro pubbliche                                                  | Descrizione                                              |
| [**m \_ pPosition**](ctransformoutputpin-m-pposition.md)                  | Oggetto helper per passare i comandi seek a monte.            |
| Metodi pubblici                                                           | Descrizione                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Metodo del costruttore.                                      |
| [**~CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Metodo del distruttore.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Determina se una connessione pin è adatta.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Rilascia il pin da una connessione.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Completa una connessione a un altro pin.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Determina se il pin accetta un tipo di supporto specifico.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Imposta il tipo di supporto per la connessione.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Imposta i requisiti del buffer.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Recupera un tipo di supporto preferito, in base al valore di indice.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Recupera il tipo di supporto per la connessione del pin corrente. |
| Metodi IPin                                                             | Descrizione                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Recupera un identificatore per il pin.                     |
| Metodi di IQualityControl                                                  | Descrizione                                              |
| [**Notificare**](ctransformoutputpin-notify.md)                             | Notifica al pin che è richiesta una modifica di qualità.     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




