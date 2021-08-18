---
description: La classe CBaseOutputPin è una classe di base astratta che implementa un pin di output.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Classe CBaseOutputPin (Amfilter.h)
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
ms.openlocfilehash: 67a4051f904b27b75273d553e1d0604b068b3910fbfb322b5a2df716c996a1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872587"
---
# <a name="cbaseoutputpin-class"></a>Classe CBaseOutputPin

![Gerarchia di classi cbaseoutputpin](images/filter06.png)

La `CBaseOutputPin` classe è una classe di base astratta che implementa un pin di output.

Questa classe deriva da [**CBasePin.**](cbasepin.md) Si differenzia da **CBasePin** per i seguenti aspetti:

-   Si connette solo ai pin di input che supportano [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   Supporta il trasporto della memoria locale tramite [**l'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)
-   Rifiuta le notifiche di fine flusso, scaricamento e nuovo segmento. Non devono essere inviati a un pin di output.
-   Fornisce metodi per la distribuzione di campioni a valle.

Quando il pin si connette, richiede un allocatore di memoria dal pin di input. In caso contrario, viene creato un nuovo oggetto allocatore. Il pin di output è responsabile dell'impostazione delle proprietà dell'allocatore. Esegue questa operazione tramite il metodo virtuale [**puro CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md). Eseguire l'override di questo metodo nella classe derivata. Se il pin di input ha requisiti di buffer, vengono passati al **metodo DecideBufferSize.**

Chiamare il [**metodo CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) per ottenere un esempio di supporto vuoto. Chiamare il [**metodo CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) per distribuire gli esempi a valle.

La classe derivata deve eseguire l'override del metodo [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtuale puro per convalidare il tipo di supporto durante le connessioni pin.



| Variabili membro protette                                      | Descrizione                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseoutputpin-m-pallocator.md)            | Puntatore all'allocatore di memoria.                                           |
| [**m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md)              | Puntatore al pin di input connesso a questo pin.                            |
| Metodi pubblici                                                  | Descrizione                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Metodo del costruttore.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Completa una connessione a un pin di input. Virtuale.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Seleziona un allocatore di memoria. Virtuale.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Recupera un campione di supporti che contiene un buffer vuoto. Virtuale.           |
| [**Distribuzione**](cbaseoutputpin-deliver.md)                       | Recapita un campione multimediale al pin di input connesso. Virtuale.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Crea un allocatore di memoria. Virtuale.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Determina se una connessione pin è adatta.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Rilascia il pin da una connessione.                                        |
| [**Attivo**](cbaseoutputpin-active.md)                         | Notifica al segnaposto che il filtro è ora attivo.                            |
| [**Inattivo**](cbaseoutputpin-inactive.md)                     | Notifica al segnaposto che il filtro non è più attivo.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Recapita una notifica di fine flusso al pin di input connesso. Virtuale. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Richiede al pin di input connesso di iniziare un'operazione di scaricamento. Virtuale.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Richiede al pin di input connesso di terminare un'operazione di scaricamento. Virtuale.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Recapita una notifica di nuovo segmento al pin di input connesso. Virtuale.   |
| Metodi virtuali puri                                            | Descrizione                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Imposta i requisiti del buffer.                                              |
| Metodi IPin                                                    | Descrizione                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Avvia un'operazione di scaricamento.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Termina un'operazione di scaricamento.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Notifica al pin che non sono previsti dati aggiuntivi.                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




