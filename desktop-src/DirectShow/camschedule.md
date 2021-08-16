---
description: La classe CAMSchedule implementa un'utilità di pianificazione per gli orologi di riferimento.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Classe CAMSchedule (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2236eb66086bb590892401cab052f39d81a41941db38d2a73dedd5edb4c53ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955410"
---
# <a name="camschedule-class"></a>Classe CAMSchedule

La `CAMSchedule` classe implementa un'utilità di pianificazione per gli orologi di riferimento.



| Metodi pubblici                                             | Descrizione                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Metodo del costruttore.                                                                  |
| [**~CAMSchedule**](camschedule--camschedule.md)           | Metodo del distruttore. Virtuale.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Recupera il numero di richieste di consulenza in sospeso.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Recupera l'ora della richiesta di consulenza successiva.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Aggiunge una richiesta di consulenza all'elenco delle richieste in sospeso.                              |
| [**Non supervisione**](camschedule-unadvise.md)                   | Rimuove una richiesta di consulenza.                                                           |
| [**Consigliare**](camschedule-advise.md)                       | Invia tutte le richieste pianificate per un orario specificato o in precedenza.          |
| [**GetEvent**](camschedule-getevent.md)                   | Recupera un handle di evento, che viene usato per segnalare una modifica al successivo consiglio. |



 

## <a name="remarks"></a>Commenti

Questo oggetto helper gestisce un elenco di richieste di consulenza per un clock di riferimento. La [**classe CBaseReferenceClock**](cbasereferenceclock.md) la usa per pianificare le richieste di consulenza. Gli orologi usano questo oggetto nel modo seguente:

1.  L'orologio crea un thread di lavoro per gestire la pianificazione.
2.  Il thread di lavoro chiama il [**metodo CAMSchedule::GetEvent**](camschedule-getevent.md) per recuperare un handle di evento dall'utilità di pianificazione. Attende questo evento, inizialmente con un timeout infinito.
3.  Per pianificare una nuova richiesta di consulenza, l'orologio chiama il [**metodo CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md) Una richiesta di consulenza può essere una sola volta o periodica. L'utilità di pianificazione mantiene l'elenco delle richieste in ordine temporale.
4.  Se una richiesta viene aggiunta all'inizio dell'elenco, l'utilità di pianificazione segnala l'evento. L'elenco è vuoto all'inizio, quindi la prima richiesta è garantita per segnalare l'evento.
5.  Quando l'evento viene segnalato, il thread di lavoro chiama il [**metodo CAMSchedule::Advise,**](camschedule-advise.md) specificando l'ora di riferimento corrente. Se le richieste in sospeso sono scadute, l'utilità di pianificazione le invia.
6.  Il metodo Advise restituisce l'ora della richiesta successiva. Il thread di lavoro usa questo valore per calcolare un nuovo valore di timeout.
7.  I passaggi 2 6 si ripetono per un periodo illimitato.
8.  Per terminare il thread di lavoro, il clock imposta un flag interno e segnala l'evento.

Nel passaggio 2 l'evento viene segnalato o si verifica il timeout dell'attesa. Se l'evento viene segnalato, significa che è stata aggiunta una nuova richiesta all'inizio dell'elenco. Il thread di lavoro deve calcolare un nuovo valore di timeout. D'altra parte, se si verifica il timeout dell'attesa, significa che una richiesta di consulenza è scaduta e deve essere inviata. La chiamata a Advise nel passaggio 5 gestisce entrambi i casi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule.h (includere Flussi.h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




