---
description: La classe CTransformInputPin implementa un pin di input usato dalla classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Classe CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333309"
---
# <a name="ctransforminputpin-class"></a>Classe CTransformInputPin

![gerarchia di classi ctransforminputpin](images/tfrm01.png)

La `CTransformInputPin` classe implementa un pin di input usato dalla classe [**CTransformFilter**](ctransformfilter.md) .

In genere, non è necessario derivare da questa classe. La maggior parte dei metodi di questa classe chiama i metodi corrispondenti sulla classe **CTransformFilter** , che è possibile sottoscrivere. Se si deriva da questa classe, è necessario eseguire l'override del metodo [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro per creare istanze della classe derivata.



| Variabili membro protette                                           | Descrizione                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_pTransformFilter m**](ctransforminputpin-m-ptransformfilter.md) | Puntatore al filtro proprietario.                                                          |
| Metodi pubblici                                                       | Descrizione                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Metodo del costruttore.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Determina se una connessione pin è adatta.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Rilascia il pin da una connessione.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Completa una connessione a un altro pin.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Determina se il pin accetta un tipo di supporto specifico.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Imposta il tipo di supporto per la connessione.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Determina se il pin può accettare esempi. Virtuale.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Recupera il tipo di supporto per la connessione al pin corrente.                               |
| Metodi IPin                                                         | Descrizione                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Recupera un identificatore per il PIN.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Notifica al pin che non sono previsti dati aggiuntivi.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Avvia un'operazione di svuotamento.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Termina un'operazione di svuotamento.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento. |
| Metodi IMemInputPin                                                 | Descrizione                                                                            |
| [**Ricevere**](ctransforminputpin-receive.md)                        | Riceve il campione multimediale successivo nel flusso.                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




