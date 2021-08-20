---
description: I dati fuori banda (OOB) sono un canale di trasmissione indipendente logicamente associato a una coppia di socket di flusso connessi.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Protocol IndependentOut-of-Band Data in the SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55e186e34e401e56017097271d5f036f2666bdc51f8bc27c6692be7e12874e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993611"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Protocol IndependentOut-of-Band Data in the SPI

I dati fuori banda (OOB) sono un canale di trasmissione indipendente logicamente associato a una coppia di socket di flusso connessi. I dati OOB possono essere recapitati all'utente indipendentemente dai dati normali. L'astrazione definisce che le strutture di dati OOB devono supportare la distribuzione affidabile di almeno un blocco di dati OOB alla volta. Questo blocco di dati può contenere almeno un byte di dati e almeno un blocco di dati OOB potrebbe essere in attesa di recapito all'utente in qualsiasi momento. Per i protocolli di comunicazione che supportano la segnalazione in banda (ovvero TCP, in cui i dati urgenti vengono recapitati in sequenza con i dati normali), il sistema estrae in genere i dati OOB dal flusso di dati normale e li archivia separatamente (lasciando un divario nel flusso di dati normale). In questo modo gli utenti possono scegliere tra la ricezione dei dati OOB in ordine e la ricezione fuori sequenza senza dover eseguire il buffer di tutti i dati. È possibile visualizzare in anteprima i dati OOB.

Un utente può determinare se sono presenti dati OOB in attesa di essere letti usando la funzione [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK). Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo (ovvero TCP), un provider di servizi Windows Sockets manterrà un marcatore concettuale che indica la posizione dell'ultimo byte di dati OOB all'interno del flusso di dati normale. Questa operazione non è necessaria per l'implementazione della funzionalità **WSPIoctl** (SIOCATMARK): la presenza o l'assenza di dati OOB è tutto ciò che è necessario.

Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo, un'applicazione potrebbe preferire l'elaborazione inline di dati fuori banda come parte del flusso di dati normale. A tale scopo, impostare l'opzione socket SO \_ OOBINLINE (vedere la [**sezione WSPIoctl).**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) Per altri protocolli in cui i blocchi di dati OOB sono realmente indipendenti dal normale flusso di dati, il tentativo di impostare SO \_ OOBINLINE restituirà un errore. Un'applicazione può usare il comando SIOCATMARK WSPIoctl per determinare se sono presenti dati OOB non letti che precedono il contrassegno. Ad esempio, potrebbe usarlo per risincronizzare con il relativo peer assicurando che tutti i dati fino al contrassegno nel flusso di dati vengono eliminati quando appropriato.

Con SO \_ OOBINLINE disabilitato (per impostazione predefinita):

-   Il provider di servizi Winsock notifica a un client un evento OOB FD, se il client è registrato per la notifica con \_ [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))esattamente nello stesso modo in cui viene usato FD READ per notificare la presenza di dati \_ normali. In altre informazioni, L'OOB FD viene inviato all'arrivo dei dati OOB e non sono stati precedentemente accodati dati OOB, ma anche quando i dati vengono letti usando il \_ flag MSG OOB e alcuni dati OOB rimangono da leggere dopo la restituita dell'operazione di \_ lettura. I messaggi \_ FD READ non vengono inviati per i dati OOB.
-   Il provider di servizi Winsock restituisce da [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) con il socket *exceptfds* appropriato impostato se i dati OOB vengono accodati nel socket.
-   Il client può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con MSG \_ OOB per leggere il blocco di dati urgenti in qualsiasi momento. Il blocco di dati OOB passa alla coda.
-   Il client può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) senza MSG \_ OOB per leggere il flusso di dati normale. Il blocco di dati OOB non verrà visualizzato nel flusso di dati con dati normali. Se i dati OOB rimangono dopo qualsiasi chiamata a **WSPRecv,** il provider di servizi invia una notifica al client con FD \_ OOB o tramite *exceptfds* quando si usa [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   Per i protocolli in cui i dati OOB hanno una posizione all'interno del flusso di dati normale, una singola [**operazione WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) non estenderà tale posizione. Un **WSPRecv** restituirà i dati normali prima del contrassegno e un secondo **WSPRecv** è necessario per iniziare a leggere i dati dopo il contrassegno.

Con SO \_ OOBINLINE abilitato:

-   I messaggi OOB FD non vengono inviati per i dati OOB. Ai fini delle funzioni \_ [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) e [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) i dati OOB vengono trattati come dati normali e indicati impostando il socket in *readfds* o inviando rispettivamente un messaggio FD \_ READ.
-   Il client non può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con il flag MSG OOB impostato per leggere il blocco di dati OOB. Verrà restituito il codice di \_ errore WSAEINVAL.
-   Il client può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) senza il \_ flag MSG OOB impostato. Tutti i dati OOB verranno recapitati nell'ordine corretto all'interno del flusso di dati normale. I dati OOB non verranno mai misti ai dati normali. Per superare i dati OOB, è necessario che siano presenti tre richieste di lettura. La prima restituisce i dati normali prima del blocco di dati OOB, la seconda restituisce i dati OOB, la terza restituisce i dati normali dopo i dati OOB. In altre parole, i limiti del blocco di dati OOB vengono mantenuti.

La routine [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) è particolarmente adatta per la gestione della notifica della presenza di dati OOB quando SO \_ OOBINLINE è disattivato.

 

 
