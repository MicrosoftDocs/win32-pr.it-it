---
description: La classe CBaseInputPin è una classe di base astratta per l'implementazione di pin di input. Questa classe aggiunge il supporto per l'interfaccia IMemInputPin, oltre al supporto dell'interfaccia IPin fornito da CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Classe CBaseInputPin (Amfilter. h)
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
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328689"
---
# <a name="cbaseinputpin-class"></a>Classe CBaseInputPin

![gerarchia di classi cbaseinputpin](images/filter07.png)

La `CBaseInputPin` classe è una classe di base astratta per l'implementazione di pin di input. Questa classe aggiunge il supporto per l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , oltre al supporto dell'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) fornito da [**CBasePin**](cbasepin.md).

Per usare questa classe, derivare una nuova classe ed eseguire l'override di almeno i metodi seguenti:

-   [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

A seconda della funzione del PIN, potrebbe essere necessario eseguire l'override di metodi aggiuntivi in `CBaseInputPin` o **CBasePin**.



| Variabili membro protette                                                 | Descrizione                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**\_pAllocator m**](cbaseinputpin-m-pallocator.md)                        | Puntatore all'allocatore di memoria.                                                                            |
| [**\_bReadOnly m**](cbaseinputpin-m-breadonly.md)                          | Flag che indica se l'allocatore produce esempi di supporti di sola lettura.                                 |
| [**\_bFlushing m**](cbaseinputpin-m-bflushing.md)                          | Flag che indica se il PIN sta attualmente scaricando.                                                  |
| [**\_SampleProps m**](cbaseinputpin-m-sampleprops.md)                      | Proprietà dell'esempio più recente.                                                                       |
| Metodi pubblici                                                             | Descrizione                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Metodo del costruttore.                                                                                         |
| [**~ CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Metodo del distruttore.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Rilascia il pin da una connessione.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Esegue una query se l'allocatore usa esempi di supporti di sola lettura.                                                 |
| [**Scaricamento**](cbaseinputpin-isflushing.md)                             | Esegue una query per determinare se il filtro sta attualmente scaricando.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Determina se il pin può accettare esempi. Virtuale.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Passa un messaggio di controllo di qualità all'oggetto appropriato.                                                 |
| [**Inattivo**](cbaseinputpin-inactive.md)                                 | Notifica al pin che il filtro non è più attivo. Virtuale.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Recupera le proprietà dell'esempio più recente.                                                         |
| Metodi IPin                                                               | Descrizione                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Avvia un'operazione di svuotamento.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Termina un'operazione di svuotamento.                                                                                     |
| Metodi IMemInputPin                                                       | Descrizione                                                                                                 |
| [**Getallocator**](cbaseinputpin-getallocator.md)                         | Recupera l'allocatore di memoria proposto da questo pin.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Specifica un allocatore per la connessione.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Recupera le proprietà dell'allocatore richieste dal pin di input.                                              |
| [**Ricevere**](cbaseinputpin-receive.md)                                   | Riceve il campione multimediale successivo nel flusso.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Riceve più campioni nel flusso.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Determina se le chiamate al metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) potrebbero bloccarsi. |
| Metodi IQualityControl                                                    | Descrizione                                                                                                 |
| [**Notifica**](cbaseinputpin-notify.md)                                     | Riceve un messaggio di controllo di qualità.                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




