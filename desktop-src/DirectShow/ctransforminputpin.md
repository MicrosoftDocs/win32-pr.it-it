---
description: La classe CTransformInputPin implementa un pin di input usato dalla classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Classe CTransformInputPin (Transfrm.h)
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
ms.openlocfilehash: 3df5da0ee6e80dd1da147563ef698a520222531de5cee9656ec52cb14301f66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087016"
---
# <a name="ctransforminputpin-class"></a>Classe CTransformInputPin

![Gerarchia di classi ctransforminputpin](images/tfrm01.png)

La `CTransformInputPin` classe implementa un pin di input usato dalla classe [**CTransformFilter.**](ctransformfilter.md)

In genere, non è necessario derivare da questa classe. La maggior parte dei metodi in questa classe chiama metodi corrispondenti nella **classe CTransformFilter,** di cui è possibile eseguire l'override. Se si deriva da questa classe, è necessario eseguire l'override del metodo [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) del filtro per creare istanze della classe derivata.



| Variabili membro protette                                           | Descrizione                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransforminputpin-m-ptransformfilter.md) | Puntatore al filtro proprietario.                                                          |
| Metodi pubblici                                                       | Descrizione                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Metodo del costruttore.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Determina se una connessione pin è adatta.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Rilascia il pin da una connessione.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Completa una connessione a un altro pin.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Determina se il pin accetta un tipo di supporto specifico.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Imposta il tipo di supporto per la connessione.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Determina se il pin può accettare campioni. Virtuale.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Recupera il tipo di supporto per la connessione del pin corrente.                               |
| Metodi IPin                                                         | Descrizione                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Recupera un identificatore per il pin.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Notifica al pin che non sono previsti dati aggiuntivi.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Avvia un'operazione di scaricamento.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Termina un'operazione di scaricamento.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Notifica al pin che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento. |
| Metodi di IMemInputPin                                                 | Descrizione                                                                            |
| [**Ricevere**](ctransforminputpin-receive.md)                        | Riceve l'esempio multimediale successivo nel flusso.                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




