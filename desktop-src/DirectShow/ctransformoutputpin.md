---
description: La classe CTransformOutputPin implementa un pin di output usato dalla classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Classe CTransformOutputPin (Transfrm. h)
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
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332985"
---
# <a name="ctransformoutputpin-class"></a>Classe CTransformOutputPin

![gerarchia di classi ctransformoutputpin](images/tfrm02.png)

La `CTransformOutputPin` classe implementa un pin di output usato dalla classe [**CTransformFilter**](ctransformfilter.md) .

In genere, non è necessario derivare da questa classe. La maggior parte dei metodi di questa classe chiama i metodi corrispondenti sulla classe **CTransformFilter** , che è possibile sottoscrivere. Se si deriva da questa classe, è necessario eseguire l'override del metodo [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro per creare istanze della classe derivata.

Questa classe espone le interfacce **IMediaSeeking** e **IMediaPosition** tramite l'oggetto [**CPosPassThru**](cpospassthru.md) . Passa tutte le richieste Seek al filtro successivo upstream.



| Variabili membro protette                                               | Descrizione                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**\_pTransformFilter m**](ctransformoutputpin-m-ptransformfilter.md)    | Puntatore al filtro proprietario.                            |
| Variabili membro pubblico                                                  | Descrizione                                              |
| [**\_pPosition m**](ctransformoutputpin-m-pposition.md)                  | Oggetto helper per passare i comandi Seek upstream.            |
| Metodi pubblici                                                           | Descrizione                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Metodo del costruttore.                                      |
| [**~ CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Metodo del distruttore.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Determina se una connessione pin è adatta.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Rilascia il pin da una connessione.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Completa una connessione a un altro pin.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Determina se il pin accetta un tipo di supporto specifico.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Imposta il tipo di supporto per la connessione.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Imposta i requisiti del buffer.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Recupera un tipo di supporto preferito, in base al valore di indice.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Recupera il tipo di supporto per la connessione al pin corrente. |
| Metodi IPin                                                             | Descrizione                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Recupera un identificatore per il PIN.                     |
| Metodi IQualityControl                                                  | Descrizione                                              |
| [**Notifica**](ctransformoutputpin-notify.md)                             | Notifica al pin che è richiesta una modifica di qualità.     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




