---
description: I dati fuori banda (OOB) sono un canale di trasmissione logicamente indipendente associato a una coppia di socket di flusso connessi.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Dati indipendenti dal protocollo in banda in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e5c7c5c8c8ad7a5985ec101dd157370c5f32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526113"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Dati indipendenti dal protocollo in banda in SPI

I dati fuori banda (OOB) sono un canale di trasmissione logicamente indipendente associato a una coppia di socket di flusso connessi. I dati di OOB possono essere recapitati all'utente indipendentemente dai dati normali. L'astrazione definisce che le funzionalità dei dati OOB devono supportare il recapito affidabile di almeno un blocco di dati OOB alla volta. Questo blocco di dati può contenere almeno un byte di dati e almeno un blocco di dati OOB potrebbe essere recapitato in attesa all'utente in qualsiasi momento. Per i protocolli di comunicazione che supportano la segnalazione in banda (ovvero TCP, in cui i dati urgenti vengono recapitati in sequenza con i dati normali), il sistema estrae in genere i dati OOB dal flusso di dati normale e li archivia separatamente (lasciando un gap nel flusso di dati normale). Ciò consente agli utenti di scegliere tra la ricezione dei dati di OOB nell'ordine e la ricezione fuori sequenza senza dover memorizzare nel buffer tutti i dati interessati. È possibile leggere i dati di OOB.

Un utente può determinare se sono presenti dati OOB in attesa di essere letti tramite la funzione [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK). Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo (ovvero TCP), un provider di servizi Windows Sockets manterrà un marcatore concettuale che indica la posizione dell'ultimo byte dei dati OOB all'interno del flusso di dati normale. Questa operazione non è necessaria per l'implementazione della funzionalità **WSPIoctl** (SIOCATMARK), ovvero la presenza o l'assenza di dati OOB è sufficiente.

Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo, un'applicazione può preferire elaborare dati fuori banda inline, come parte del normale flusso di dati. Questa operazione viene eseguita impostando l'opzione socket in modo da \_ OOBINLINE (vedere la sezione [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). Per altri protocolli in cui i blocchi di dati OOB sono realmente indipendenti dal flusso di dati normale, il tentativo di impostare in modo che \_ OOBINLINE provochi un errore. Un'applicazione può usare il comando SIOCATMARK WSPIoctl per determinare se sono presenti dati OOB non letti che precedono il contrassegno. Ad esempio, può utilizzare questo oggetto per risincronizzare con il relativo peer garantendo che tutti i dati fino al contrassegno nel flusso di dati vengano eliminati quando appropriato.

Con \_ OOBINLINE disabilitato (per impostazione predefinita):

-   Il provider di servizi Winsock invia una notifica a un client di un \_ evento OOB FD, se il client registrato per la notifica con [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), nello stesso modo in \_ cui viene usato FD Read per notificare la presenza di dati normali. Ovvero, FD \_ OOB viene pubblicato all'arrivo dei dati OOB e non sono presenti dati OOB accodati in precedenza e anche quando i dati vengono letti utilizzando il \_ flag msg OOB e alcuni dati OOB restano da leggere dopo che è stata restituita l'operazione di lettura. \_I messaggi di lettura FD non vengono inviati per i dati OOB.
-   Il provider di servizi Winsock restituisce da [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) con il set di socket *exceptfds* appropriato se i dati OOB sono accodati nel socket.
-   Il client può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con msg \_ OOB per leggere il blocco di dati urgente in qualsiasi momento. Il blocco dei dati di OOB salta la coda.
-   Il client può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) senza MSG \_ OOB per leggere il flusso di dati normale. Il blocco di dati OOB non verrà visualizzato nel flusso di dati con dati normali. Se i dati OOB rimangono dopo una chiamata a **WSPRecv**, il provider di servizi invia una notifica al client con FD \_ OOB o tramite *exceptfds* quando si usa [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   Per i protocolli in cui i dati di OOB hanno una posizione all'interno del flusso di dati normale, una singola operazione [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) non si estenderà a tale posizione. Un **WSPRecv** restituirà i dati normali prima del contrassegno e una seconda **WSPRecv** sarà necessaria per iniziare a leggere i dati dopo il contrassegno.

Con \_ OOBINLINE abilitato:

-   I \_ messaggi FD OOB non vengono inviati per i dati OOB: ai fini delle funzioni [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) e [**WSPASYNCSELECT**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , i dati OOB vengono considerati come dati normali e indicati impostando il socket in *readfds* o inviando rispettivamente un \_ messaggio di lettura FD.
-   Il client non può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con il \_ flag msg OOB impostato per leggere il blocco di dati OOB. verrà restituito il codice di errore WSAEINVAL.
-   Il client può chiamare [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) senza il \_ set di flag OOB msg. Tutti i dati di OOB verranno recapitati nell'ordine corretto nel flusso di dati normale. I dati di OOB non verranno mai combinati con i dati normali. devono essere presenti tre richieste di lettura per superare i dati di OOB. Il primo restituisce i dati normali prima del blocco di dati OOB, il secondo restituisce i dati OOB, il terzo restituisce i dati normali che seguono i dati OOB. In altre parole, vengono conservati i limiti dei blocchi di dati OOB.

La routine [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) è particolarmente adatta per la gestione della notifica della presenza di dati OOB quando \_ OOBINLINE è disattivato.

 

 
