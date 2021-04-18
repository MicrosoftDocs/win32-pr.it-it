---
description: La classe CBaseOutputPin è una classe di base astratta che implementa un pin di output.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Classe CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330542"
---
# <a name="cbaseoutputpin-class"></a>Classe CBaseOutputPin

![gerarchia di classi cbaseoutputpin](images/filter06.png)

La `CBaseOutputPin` classe è una classe di base astratta che implementa un pin di output.

Questa classe deriva da [**CBasePin**](cbasepin.md). Si differenzia da **CBasePin** nei seguenti aspetti:

-   Si connette solo ai pin di input che supportano l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Supporta il trasporto di memoria locale tramite l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .
-   Rifiuta le notifiche di fine flusso, svuotamento e nuovo segmento. Questi non devono essere inviati a un pin di output.
-   Fornisce metodi per la distribuzione di esempi downstream.

Quando il pin si connette, richiede un allocatore di memoria dal pin di input. In caso contrario, viene creato un nuovo oggetto allocatore. Il pin di output è responsabile dell'impostazione delle proprietà dell'allocatore. Questa operazione viene eseguita tramite il metodo virtuale pure [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md). Eseguire l'override di questo metodo nella classe derivata. Se il pin di input presenta requisiti del buffer, questi vengono passati al metodo **DecideBufferSize** .

Chiamare il metodo [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) per ottenere un esempio di supporto vuoto. Chiamare il metodo [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) per fornire esempi downstream.

La classe derivata deve eseguire l'override del metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtuale pure per convalidare il tipo di supporto durante le connessioni pin.



| Variabili membro protette                                      | Descrizione                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**\_pAllocator m**](cbaseoutputpin-m-pallocator.md)            | Puntatore all'allocatore di memoria.                                           |
| [**\_pInputPin m**](cbaseoutputpin-m-pinputpin.md)              | Puntatore al pin di input connesso a questo pin.                            |
| Metodi pubblici                                                  | Descrizione                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Metodo del costruttore.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Completa una connessione a un pin di input. Virtuale.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Seleziona un allocatore di memoria. Virtuale.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Recupera un esempio multimediale che contiene un buffer vuoto. Virtuale.           |
| [**Distribuzione**](cbaseoutputpin-deliver.md)                       | Recapita un campione multimediale al pin di input connesso. Virtuale.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Crea un allocatore di memoria. Virtuale.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Determina se una connessione pin è adatta.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Rilascia il pin da una connessione.                                        |
| [**Attivo**](cbaseoutputpin-active.md)                         | Notifica al pin che il filtro è ora attivo.                            |
| [**Inattivo**](cbaseoutputpin-inactive.md)                     | Notifica al pin che il filtro non è più attivo.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Recapita una notifica di fine del flusso al pin di input connesso. Virtuale. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Richiede al pin di input connesso di iniziare un'operazione di svuotamento. Virtuale.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Richiede al pin di input connesso di terminare un'operazione di svuotamento. Virtuale.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Recapita una notifica del nuovo segmento al pin di input connesso. Virtuale.   |
| Metodi virtuali puri                                            | Descrizione                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Imposta i requisiti del buffer.                                              |
| Metodi IPin                                                    | Descrizione                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Avvia un'operazione di svuotamento.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Termina un'operazione di svuotamento.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Notifica al pin che non sono previsti dati aggiuntivi.                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




