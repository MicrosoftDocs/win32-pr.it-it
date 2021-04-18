---
description: La classe CAMSchedule implementa un'utilità di pianificazione per gli orologi di riferimento.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Classe CAMSchedule (Dsschedule. h)
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
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330549"
---
# <a name="camschedule-class"></a>Classe CAMSchedule

La `CAMSchedule` classe implementa un'utilità di pianificazione per gli orologi di riferimento.



| Metodi pubblici                                             | Descrizione                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Metodo del costruttore.                                                                  |
| [**~ CAMSchedule**](camschedule--camschedule.md)           | Metodo del distruttore. Virtuale.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Recupera il numero di richieste di notifica in sospeso.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Recupera l'ora della successiva richiesta di notifica.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Aggiunge una richiesta di notifica all'elenco di richieste in sospeso.                              |
| [**Unadvise**](camschedule-unadvise.md)                   | Rimuove una richiesta di notifica.                                                           |
| [**Consigliare**](camschedule-advise.md)                       | Invia tutte le richieste pianificate per un periodo di tempo specificato o una versione precedente.          |
| [**GetEvent**](camschedule-getevent.md)                   | Recupera un handle di evento, che viene usato per segnalare una modifica nel tempo di notifica successivo. |



 

## <a name="remarks"></a>Commenti

Questo oggetto helper gestisce un elenco di richieste di notifica per un orologio di riferimento. La classe [**CBaseReferenceClock**](cbasereferenceclock.md) la utilizza per pianificare le richieste di notifica. Gli orologi usano questo oggetto nel modo seguente:

1.  Il clock crea un thread di lavoro per gestire la pianificazione.
2.  Il thread di lavoro chiama il metodo [**CAMSchedule:: GetEvent**](camschedule-getevent.md) per recuperare un handle di evento dall'utilità di pianificazione. Attende questo evento, inizialmente con un timeout infinito.
3.  Per pianificare una nuova richiesta di notifica, il clock chiama il metodo [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) . Una richiesta di notifica può essere monofase o periodica. L'utilità di pianificazione mantiene l'elenco di richieste in ordine temporale.
4.  Se una richiesta viene aggiunta all'inizio dell'elenco, l'utilità di pianificazione segnala l'evento. (L'elenco è inizialmente vuoto, quindi la prima richiesta viene garantita per segnalare l'evento).
5.  Quando l'evento viene segnalato, il thread di lavoro chiama il metodo [**CAMSchedule:: Advise**](camschedule-advise.md) , specificando l'ora di riferimento corrente. Se sono scadute richieste in sospeso, l'utilità di pianificazione li invia.
6.  Il metodo Advise restituisce l'ora della richiesta successiva. Il thread di lavoro utilizza questo valore per calcolare un nuovo valore di timeout.
7.  I passaggi 2 6 si ripetono per un periodo illimitato.
8.  Per terminare il thread di lavoro, il clock imposta un flag interno e segnala l'evento.

Nel passaggio 2, l'evento viene segnalato o il timeout dell'attesa. Se l'evento viene segnalato, significa che è stata aggiunta una nuova richiesta all'inizio dell'elenco. Il thread di lavoro deve calcolare un nuovo valore di timeout. D'altra parte, se si verifica il timeout dell'attesa, significa che una richiesta di notifica è dovuta e deve essere inviata. La chiamata a advise nel passaggio 5 gestisce entrambi i casi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Dsschedule. h (include Streams. h)</dt> </dl>                                                                                |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




