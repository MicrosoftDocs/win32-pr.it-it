---
description: La classe CTransformFilter è una classe di base per l'implementazione di filtri di trasformazione.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: Classe CTransformFilter (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9d199a406fa1934fb63625cd258baee8d69c20c17992a7d1d3bbd2c83956a1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633896"
---
# <a name="ctransformfilter-class"></a>Classe CTransformFilter

![Gerarchia di classi ctransformfilter](images/tfrm03.png)

La `CTransformFilter` classe è una classe di base per l'implementazione di filtri di trasformazione. Questa classe è progettata per l'implementazione di un filtro di trasformazione con un pin di input e un pin di output. Usa allocatori separati per il pin di input e il pin di output. Per creare un filtro che elabora i dati sul posto, usare la [**classe CTransInPlaceFilter.**](ctransinplacefilter.md)

Questo filtro usa la [**classe CTransformInputPin**](ctransforminputpin.md) per il pin di input e la [**classe CTransformOutputPin**](ctransformoutputpin.md) per il pin di output. In genere, non è necessario eseguire l'override di queste classi pin. La maggior parte dei metodi pin chiama metodi corrispondenti sulla classe, quindi `CTransformFilter` è possibile eseguire l'override dei metodi di filtro, se necessario. Il filtro crea entrambi i pin nel [**metodo CTransformFilter::GetPin.**](ctransformfilter-getpin.md) Se si esegue l'override delle classi pin, è necessario eseguire l'override **di GetPin** per creare i pin personalizzati.

Per usare questa classe, derivare una nuova classe da `CTransformFilter` e implementare i metodi seguenti:

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter::Transform**](ctransformfilter-transform.md)

Potrebbe essere necessario eseguire l'override anche di altri metodi, a seconda dei requisiti del filtro.

## <a name="media-types"></a>Tipi di supporti

Il pin di input di questo filtro non propone alcun tipo di supporto. si basa sul filtro upstream per proporre i tipi di supporti per la connessione. Il motivo di questa progettazione è che nella maggior parte dei casi, il filtro upstream può fornire altre informazioni sul formato. Con i formati video, ad esempio, il filtro upstream conosce le dimensioni del video e la frequenza dei fotogrammi, mentre il filtro di trasformazione non è in grado di determinare queste informazioni. Per modificare questo comportamento, eseguire l'override del metodo [**GetMediaType**](ctransformfilter-getmediatype.md) del pin di input. Quando il filtro upstream propone un tipo di supporto, il pin di input chiama il metodo [**CheckInputType**](ctransformfilter-checkinputtype.md) del filtro (virtuale puro).

Finché il pin di input non viene connesso, il pin di output rifiuta tutte le connessioni e non restituisce alcun tipo di supporto preferito. Dopo aver connesso il pin di input, il pin di output restituisce un elenco di tipi preferiti chiamando il metodo [**GetMediaType del**](ctransformfilter-getmediatype.md) filtro. Controlla i tipi di output per la connessione tramite il metodo [**CheckTransform del**](ctransformfilter-checktransform.md) filtro. Entrambi i metodi sono virtuali puri. In genere, il tipo di input determinerà in parte i tipi di output accettabili.

A seconda del filtro, potrebbe essere necessario registrare alcuni dei tipi di supporti supportati del filtro, in modo che l'oggetto [Filter Mapper](filter-mapper.md) possa individuare il filtro. Per altre informazioni, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Streaming

Questa classe non accoda i dati di output. Ogni esempio di output viene recapitato [**all'interno del metodo IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Il **metodo Receive** chiama il metodo [**Transform**](ctransformfilter-transform.md) del filtro (anche virtuale puro) per elaborare i dati.

Per altre informazioni sull'uso di questa classe, vedere [Scrittura di filtri di trasformazione](writing-transform-filters.md).



| Variabili membro protette                                                | Descrizione                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | Flag che indica se il filtro ha inviato una notifica di fine flusso.                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | Flag che indica se l'esempio più recente è stato eliminato.                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | Flag che indica se la qualità è stata modificata.                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | Sezione critica che protegge lo stato del filtro.                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | Sezione critica che protegge lo stato di streaming.                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | Puntatore al pin di input.                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | Puntatore al pin di output.                                                                              |
| Metodi pubblici                                                            | Descrizione                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | Metodo del costruttore.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Metodo del distruttore.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Recupera il numero di pin nel filtro. Virtuale.                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | Recupera un segnaposto. Virtuale.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Trasforma un esempio di input per produrre un esempio di output. Virtuale.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Chiamato quando il filtro passa allo stato sospeso. Virtuale.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Chiamato quando il filtro passa allo stato arrestato. Virtuale.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Notifica al filtro che è richiesta una modifica della qualità. Virtuale.                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | Chiamato quando il tipo di supporto è impostato su uno dei pin del filtro. Virtuale.                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | Determina se una connessione pin è adatta. Virtuale.                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | Rilascia un pin da una connessione. Virtuale.                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | Completa una connessione pin. Virtuale.                                                                    |
| [**Ricevere**](ctransformfilter-receive.md)                               | Riceve un campione di supporti, lo elabora e recapita un esempio di output al filtro downstream. Virtuale. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Recupera un nuovo esempio di output e lo inizializza.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Notifica al filtro che non sono previsti dati aggiuntivi dal pin di input. Virtuale.                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | Avvia un'operazione di scaricamento. Virtuale.                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | Termina un'operazione di scaricamento. Virtuale.                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | Notifica al filtro che i campioni multimediali ricevuti dopo questa chiamata vengono raggruppati come segmento. Virtuale.      |
| Metodi virtuali puri                                                      | Descrizione                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | Controlla se un tipo di supporto specificato è accettabile per l'input.                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | Controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output.                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | Imposta i requisiti del buffer del pin di output.                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | Recupera un tipo di supporto preferito per il pin di output.                                                    |
| Metodi IMediaFilter                                                      | Descrizione                                                                                             |
| [**Fermare**](ctransformfilter-stop.md)                                     | Arresta il filtro.                                                                                       |
| [**Sospendi**](ctransformfilter-pause.md)                                   | Sospende il filtro.                                                                                      |
| Metodi IBaseFilter                                                       | Descrizione                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | Recupera il pin con l'identificatore specificato.                                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




