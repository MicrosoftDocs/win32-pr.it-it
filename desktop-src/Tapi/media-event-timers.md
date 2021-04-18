---
description: Molte applicazioni dipendono dalla relazione temporale tra gli eventi multimediali (ad esempio, le cifre DTMF ricevute) per determinare la natura di un'operazione richiesta.
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: Timer eventi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320658"
---
# <a name="media-event-timers"></a>Timer eventi multimediali

Molte applicazioni dipendono dalla relazione temporale tra gli eventi multimediali (ad esempio, le cifre DTMF ricevute) per determinare la natura di un'operazione richiesta. Ad esempio, in un'applicazione di posta vocale, due cifre DTMF "1" consecutive possono significare "eseguire il backup di due segmenti" o "riprodurre dall'inizio del messaggio", a seconda della quantità di tempo trascorso tra le due cifre. In un ambiente client/server, se il rilevamento DTMF viene eseguito su un processore separato da quello in cui è in esecuzione l'applicazione, la latenza nella rete locale rende molto probabile che la relazione di intervallo tra gli eventi del supporto sia asimmetrica, con il risultato che queste differenze basate sulla temporizzazione potrebbero andare perse o diventare inaffidabili.

Per risolvere questo problema, è possibile che vengano visualizzati timestamp per più messaggi TAPI. Poiché si tratta dell'intervallo relativo tra questi eventi importanti, il "tempo di clock" dell'evento non è importante e la temporizzazione dei secondi è interrotta. Questi timestamp utilizzano la risoluzione dei millisecondi "tempo trascorso dall'avvio di Windows" restituito dalla funzione [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) . Le applicazioni devono tenere presente che si tratta del numero di cicli del server (o del computer in cui il provider di servizi gestisce direttamente l'hardware è in esecuzione) e non è necessariamente lo stesso computer in cui è in esecuzione l'applicazione. Pertanto, i timestamp in questi messaggi TAPI possono essere confrontati solo tra loro e non nel valore restituito da **GetTickCount** sul processore in cui è in esecuzione l'applicazione.

I messaggi TAPI che possono essere timestamp sono: [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md)e [**riga \_ MONITORTONE**](line-monitortone.md). Il numero di cicli viene inserito in *dwParam3* di questi messaggi. Se il timestamp non è supportato dal provider di servizi (che è indicato dall'impostazione del provider di servizi *dwParam3* in questi messaggi su 0), TAPI stesso inserisce il conteggio dei segni di inizializzazione in *dwParam3* di tutti questi messaggi. può essere leggermente inclinato, ma minore di se l'applicazione ha eseguito la stessa operazione dopo che i messaggi hanno attraversato uno schema di comunicazione interprocesso.

 

 
