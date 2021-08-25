---
description: L'astrazione del socket di flusso include la nozione di dati fuori banda (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent dati fuori banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1918ba1525462f4352d76c989d7fb5d92beeb59766f92cdccbdda66a5b82744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860831"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent dati fuori banda

L'astrazione del socket di flusso include la nozione di dati fuori banda (OOB). Molti protocolli consentono di contrassegnate parti di dati in ingresso come speciali e questi blocchi di dati speciali possono essere recapitati all'utente fuori dalla sequenza normale. Ad esempio, i dati accelerati in X.25 e altri protocolli OSI e i dati urgenti in BSD UNIX'uso di TCP. La sezione seguente descrive la gestione dei dati OOB in modo indipendente dal protocollo. Una descrizione dei dati OOB implementati usando dati urgenti TCP segue la spiegazione indipendente dal protocollo. In ogni discussione, l'uso di [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) implica anche [**recvfrom,**](/windows/desktop/api/winsock/nf-winsock-recvfrom) [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)e i riferimenti a [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) si applicano anche a [**WSAEventSelect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)

## <a name="protocol-independent-oob-data"></a>Dati OOB indipendenti dal protocollo

I dati OOB sono un canale di trasmissione indipendente logicamente associato a ogni coppia di socket di flusso connessi. I dati OOB possono essere recapitati all'utente indipendentemente dai dati normali. L'astrazione definisce che le strutture di dati OOB devono supportare la distribuzione affidabile di almeno un blocco di dati OOB alla volta. Questo blocco di dati può contenere almeno un byte di dati e almeno un blocco di dati OOB può essere in attesa di recapito all'utente in qualsiasi momento. Per i protocolli di comunicazione che supportano la segnalazione in banda (ad esempio TCP, in cui i dati urgenti vengono recapitati in sequenza con i dati normali), il sistema in genere estrae i dati OOB dal flusso di dati normale e li archivia separatamente (lasciando un divario nel flusso di dati normale). In questo modo gli utenti possono scegliere tra la ricezione dei dati OOB in ordine e la ricezione fuori sequenza senza dover eseguire il buffer di tutti i dati. È possibile visualizzare in anteprima i dati fuori banda (OOB).

Un utente può determinare se i dati OOB sono in attesa di essere letti usando la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con **SIOCATMARK** IOCTL. Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo, ad esempio TCP, un provider di servizi Windows Sockets mantiene un marcatore concettuale che indica la posizione dell'ultimo byte di dati OOB all'interno del flusso di dati normale. Questa operazione non è necessaria per l'implementazione delle **funzioni ioctlsocket** o **WSAIoctl** che **supportano SIOCATMARK.** La presenza o l'assenza di dati OOB è necessaria.

Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo, un'applicazione potrebbe elaborare dati fuori banda inline, come parte del flusso di dati normale. A tale scopo, impostare l'opzione socket SO \_ OOBINLINE con [**la funzione setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt) Per altri protocolli in cui i blocchi di dati OOB sono realmente indipendenti dal normale flusso di dati, il tentativo di impostare SO \_ OOBINLINE causa un errore. Un'applicazione può usare la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con **SIOCATMARK** IOCTL per determinare se sono presenti dati OOB non letti che precedono il contrassegno. Ad esempio, può usare queste informazioni per risincronizzare con il peer assicurandosi che tutti i dati fino al contrassegno nel flusso di dati vengono eliminati quando appropriato.

Con SO \_ OOBINLINE disabilitato (impostazione predefinita):

-   Windows I socket notificano a un'applicazione un evento OOB FD, se l'applicazione è registrata per la notifica con \_ [**WSAAsyncSelect,**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)esattamente nello stesso modo in cui viene usato FD READ per notificare la presenza di dati \_ normali. Ciò significa che L'OOB FD viene inviato quando i dati OOB arrivano senza dati \_ OOB accodati in precedenza. L'OOB FD viene pubblicato anche quando i dati vengono letti usando il \_ flag MSG OOB mentre alcuni dati OOB rimangono in coda dopo la restituita dell'operazione \_ di lettura. I messaggi \_ FD READ non vengono inviati per i dati OOB.
-   Windows I socket vengono [**restituiti da select**](/windows/desktop/api/Winsock2/nf-winsock2-select) con il socket *exceptfds* appropriato impostato se i dati OOB vengono accodati nel socket.
-   L'applicazione può chiamare [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) con MSG \_ OOB per leggere il blocco di dati urgenti in qualsiasi momento. Il blocco di dati OOB passa alla coda.
-   L'applicazione può chiamare [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) senza MSG \_ OOB per leggere il flusso di dati normale. Il blocco di dati OOB non viene visualizzato nel flusso di dati con dati normali. Se i dati OOB rimangono dopo qualsiasi chiamata a **recv**, Windows Sockets invia una notifica all'applicazione con FD \_ OOB o con *exceptfds* quando si usa [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Per i protocolli in cui i dati OOB hanno una posizione all'interno del flusso di dati normale, una singola [**operazione recv**](/windows/desktop/api/winsock/nf-winsock-recv) non si estende su tale posizione. Un **recv** restituisce i dati normali prima del contrassegno e un secondo **recv** è necessario per iniziare a leggere i dati dopo il contrassegno.

Con SO \_ OOBINLINE abilitato:

-   I messaggi \_ OOB FD non vengono inviati per i dati OOB. I dati OOB vengono considerati come normali ai fini delle funzioni [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e indicati impostando il socket in *readfds* o inviando rispettivamente un messaggio FD \_ READ.
-   L'applicazione non può [**chiamare recv**](/windows/desktop/api/winsock/nf-winsock-recv) con il \_ flag MSG OOB impostato per leggere il blocco di dati OOB. Viene restituito il codice di errore WSAEINVAL.
-   L'applicazione può [**chiamare recv**](/windows/desktop/api/winsock/nf-winsock-recv) senza il \_ flag MSG OOB impostato. Tutti i dati OOB vengono recapitati nell'ordine corretto all'interno del flusso di dati normale. I dati OOB non vengono mai misti ai dati normali. Per superare i dati OOB, devono essere presenti tre richieste di lettura. La prima restituisce i dati normali prima del blocco di dati OOB, la seconda restituisce i dati OOB, la terza restituisce i dati normali dopo i dati OOB. In altre parole, i limiti del blocco di dati OOB vengono mantenuti.

La routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) è particolarmente adatta per la gestione della notifica della presenza di dati fuori banda quando SO \_ OOBINLINE è disattivato.

## <a name="oob-data-in-tcp"></a>Dati OOB in TCP

> [!IMPORTANT]
> La discussione seguente sui dati fuori banda (OOB), implementati usando dati urgenti TCP, segue il modello usato nella distribuzione software di Berkeley. Gli utenti e gli implementatori devono tenere presente che:

 

-   Attualmente esistono due interpretazioni in conflitto di [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (in cui viene introdotto il concetto).
-   L'implementazione dei dati OOB in Berkeley Software Distribution (BSD) non è conforme ai requisiti host specificati in [RFC 1122.](https://www.ietf.org/rfc/rfc1122.txt)

    In particolare, il puntatore TCP urgente in BSD punta al byte dopo il byte di dati urgenti e un puntatore URGENT TCP conforme a RFC punta al byte di dati urgenti. Di conseguenza, se un'applicazione invia dati urgenti da un'implementazione compatibile con BSD a un'implementazione compatibile con RFC 1122, il ricevitore legge il byte di dati urgenti errato (legge il byte che si trova dopo il byte corretto nel flusso di dati come byte di dati urgenti).

    Per ridurre al minimo i problemi di interoperabilità, è consigliabile che i writer di applicazioni non usino i dati OOB, a meno che non sia necessario per interagire con un servizio esistente. Windows I fornitori di socket sono in grado di documentare la semantica OOB (BSD o RFC 1122) implementata dal prodotto.

L'arrivo di un segmento TCP con il flag RSI (per urgenti) impostato indica l'esistenza di un singolo byte di dati OOB all'interno del flusso di dati TCP. Le dimensioni del blocco di dati OOB sono di un byte. Il puntatore urgente è un offset positivo dal numero di sequenza corrente nell'intestazione TCP che indica la posizione del blocco di dati OOB (in modo ambiguo, come indicato in precedenza). Potrebbe quindi puntare a dati che non sono ancora stati ricevuti.

Se SO OOBINLINE è disabilitato (impostazione predefinita) quando arriva il segmento TCP contenente il byte a cui punta il puntatore urgente, il blocco di dati OOB (un byte) viene rimosso dal flusso di dati e memorizzato nel \_ buffer. Se un segmento TCP successivo arriva con il flag urgente impostato (e un nuovo puntatore urgente), il byte OOB attualmente in coda può essere perso perché viene sostituito dal nuovo blocco di dati OOB (come avviene in Berkeley Software Distribution). Tuttavia, non viene mai sostituito nel flusso di dati.

Con SO \_ OOBINLINE abilitato, i dati urgenti rimangono nel flusso di dati. Di conseguenza, il blocco di dati OOB non viene mai perso quando arriva un nuovo segmento TCP contenente dati urgenti. Il contrassegno dati OOB esistente viene aggiornato alla nuova posizione.

> [!Note]  
> Quando è impostata \_ l'opzione socket SO OOBINLINE, SIOCATMARK IOCTL restituisce sempre **TRUE** e i dati OOB vengono restituiti all'utente come dati normali.

 

 

 



