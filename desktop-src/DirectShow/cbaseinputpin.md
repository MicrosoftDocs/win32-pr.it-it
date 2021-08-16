---
description: La classe CBaseInputPin è una classe di base astratta per l'implementazione dei pin di input. Questa classe aggiunge il supporto per l'interfaccia IMemInputPin, oltre al supporto dell'interfaccia IPin fornito da CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Classe CBaseInputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab98a2dcb1503e7593912df0e5dff51539855611311d4704e4045816fd6380e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823886"
---
# <a name="cbaseinputpin-class"></a>Classe CBaseInputPin

![Gerarchia di classi cbaseinputpin](images/filter07.png)

La `CBaseInputPin` classe è una classe di base astratta per l'implementazione dei pin di input. Questa classe aggiunge il supporto per [**l'interfaccia IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) oltre al supporto [**dell'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) fornito da [**CBasePin**](cbasepin.md).

Per usare questa classe, derivare una nuova classe ed eseguire l'override almeno dei metodi seguenti:

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin::Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

A seconda della funzione del pin, potrebbe essere necessario eseguire l'override di metodi aggiuntivi in `CBaseInputPin` o **CBasePin**.



| Variabili membro protette                                                 | Descrizione                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | Puntatore all'allocatore di memoria.                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | Flag che indica se l'allocatore produce esempi di supporti di sola lettura.                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | Flag che indica se il pin è attualmente in fase di scaricamento.                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | Proprietà dell'esempio più recente.                                                                       |
| Metodi pubblici                                                             | Descrizione                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Metodo del costruttore.                                                                                         |
| [**~CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Metodo del distruttore.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Rilascia il pin da una connessione.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Esegue una query se l'allocatore usa esempi di supporti di sola lettura.                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | Esegue una query per determinare se il filtro è attualmente in fase di scaricamento.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Determina se il pin può accettare campioni. Virtuale.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Passa un messaggio di controllo di qualità all'oggetto appropriato.                                                 |
| [**Inattivo**](cbaseinputpin-inactive.md)                                 | Notifica al pin che il filtro non è più attivo. Virtuale.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Recupera le proprietà dell'esempio più recente.                                                         |
| Metodi IPin                                                               | Descrizione                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Avvia un'operazione di scaricamento.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Termina un'operazione di scaricamento.                                                                                     |
| Metodi di IMemInputPin                                                       | Descrizione                                                                                                 |
| [**GetAllocator**](cbaseinputpin-getallocator.md)                         | Recupera l'allocatore di memoria proposto da questo pin.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Specifica un allocatore per la connessione.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Recupera le proprietà dell'allocatore richieste dal pin di input.                                              |
| [**Ricevere**](cbaseinputpin-receive.md)                                   | Riceve l'esempio multimediale successivo nel flusso.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Riceve più esempi nel flusso.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Determina se le chiamate al [**metodo CBaseInputPin::Receive possono**](cbaseinputpin-receive.md) bloccarsi. |
| Metodi di IQualityControl                                                    | Descrizione                                                                                                 |
| [**Notificare**](cbaseinputpin-notify.md)                                     | Riceve un messaggio di controllo qualità.                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




