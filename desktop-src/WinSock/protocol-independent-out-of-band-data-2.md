---
description: L'astrazione del socket di flusso include il concetto di dati fuori banda (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent dati fuori banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a929f4273d9cc9f268a296b711649406622ca9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343471"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent dati fuori banda

L'astrazione del socket di flusso include il concetto di dati fuori banda (OOB). Molti protocolli consentono di contrassegnare le parti dei dati in arrivo come speciali e possono essere recapitati all'utente fuori dalla sequenza normale. Gli esempi includono i dati accelerati in X. 25 e altri protocolli OSI e i dati urgenti nell'uso di TCP in BSD UNIX. Nella sezione seguente viene descritta la gestione dei dati di OOB in modo indipendente dal protocollo. Una descrizione dei dati di OOB implementati con i dati urgenti TCP segue la spiegazione indipendente dal protocollo. In ogni discussione, l'uso di [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) implica anche [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)e i riferimenti a [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) si applicano anche a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect).

## <a name="protocol-independent-oob-data"></a>Dati OOB indipendenti dal protocollo

I dati OOB sono un canale di trasmissione logicamente indipendente associato a ogni coppia di socket di flusso connessi. I dati di OOB possono essere recapitati all'utente indipendentemente dai dati normali. L'astrazione definisce che le funzionalità dei dati OOB devono supportare il recapito affidabile di almeno un blocco di dati OOB alla volta. Questo blocco di dati può contenere almeno un byte di dati e almeno un blocco di dati OOB può essere recapitato all'utente in un qualsiasi momento. Per i protocolli di comunicazione che supportano la segnalazione in banda (ad esempio TCP, in cui i dati urgenti vengono recapitati in sequenza con i dati normali), il sistema estrae in genere i dati OOB dal flusso di dati normale e li archivia separatamente (lasciando un gap nel flusso di dati normale). Ciò consente agli utenti di scegliere tra la ricezione dei dati di OOB nell'ordine e la ricezione fuori sequenza senza dover memorizzare nel buffer tutti i dati interessati. È possibile leggere i dati fuori banda (OOB).

Un utente può determinare se i dati di OOB sono in attesa di essere letti tramite la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con il comando IOCTL **SIOCATMARK** . Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo, ad esempio TCP, un provider di servizi Windows Sockets mantiene un marcatore concettuale che indica la posizione dell'ultimo byte dei dati OOB all'interno del flusso di dati normale. Questa operazione non è necessaria per l'implementazione delle funzioni **ioctlsocket** o **WSAIoctl** che supportano **SIOCATMARK**. La presenza o l'assenza di dati OOB è obbligatoria.

Per i protocolli in cui il concetto di posizione del blocco di dati OOB all'interno del flusso di dati normale è significativo, un'applicazione potrebbe elaborare dati fuori banda inline, come parte del normale flusso di dati. Questa operazione viene eseguita impostando l'opzione socket in modo che \_ OOBINLINE con la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Per altri protocolli in cui i blocchi di dati OOB sono realmente indipendenti dal flusso di dati normale, il tentativo di impostare questo \_ OOBINLINE genera un errore. Un'applicazione può usare la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con l'IOCTL **SIOCATMARK** per determinare se sono presenti dati OOB non letti che precedono il contrassegno. Ad esempio, può utilizzare queste informazioni per risincronizzare con il relativo peer garantendo che tutti i dati fino al contrassegno nel flusso di dati vengano eliminati quando appropriato.

Con \_ OOBINLINE disabilitato (impostazione predefinita):

-   Windows Sockets Invia una notifica all'applicazione di un \_ evento FD OOB, se l'applicazione registrata per la notifica con [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect), nello stesso modo in \_ cui FD Read viene utilizzata per notificare la presenza di dati normali. Ovvero, l' \_ OOB FD viene pubblicato quando i dati di OOB arrivano senza dati OOB accodati in precedenza. Il \_ OOB FD viene pubblicato anche quando i dati vengono letti usando il \_ flag msg OOB mentre alcuni dati OOB rimangono in coda dopo che è stata restituita l'operazione di lettura. \_I messaggi di lettura FD non vengono inviati per i dati OOB.
-   Windows Sockets restituisce da [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) con il set di socket *exceptfds* appropriato se i dati OOB sono accodati nel socket.
-   L'applicazione può chiamare [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) con msg \_ OOB per leggere il blocco di dati urgente in qualsiasi momento. Il blocco dei dati di OOB salta la coda.
-   L'applicazione può chiamare [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) senza MSG \_ OOB per leggere il flusso di dati normale. Il blocco di dati OOB non viene visualizzato nel flusso di dati con dati normali. Se i dati OOB rimangono dopo qualsiasi chiamata a **ricezione**, Windows Sockets Invia una notifica all'applicazione con FD \_ OOB o con *exceptfds* quando si usa [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Per i protocolli in cui i dati di OOB hanno una posizione all'interno del flusso di dati normale, una singola operazione [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) non si estende in tale posizione. Un **ricezione** restituisce i dati normali prima del contrassegno e un secondo **ricezione** è necessario per iniziare a leggere i dati dopo il contrassegno.

Con \_ OOBINLINE abilitato:

-   \_I messaggi FD OOB non vengono inviati per i dati OOB. I dati OOB vengono considerati normali allo scopo delle funzioni [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e indicati impostando il socket in *readfds* o inviando rispettivamente un messaggio di \_ lettura FD.
-   L'applicazione non può chiamare [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) con il \_ flag msg OOB impostato per leggere il blocco di dati OOB. Viene restituito il codice di errore WSAEINVAL.
-   L'applicazione può chiamare [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) senza il \_ set di flag OOB msg. Tutti i dati di OOB vengono recapitati nell'ordine corretto nel flusso di dati normale. I dati di OOB non vengono mai combinati con i dati normali. Devono essere presenti tre richieste di lettura per superare i dati OOB. Il primo restituisce i dati normali prima del blocco di dati OOB, il secondo restituisce i dati OOB, il terzo restituisce i dati normali che seguono i dati OOB. In altre parole, vengono conservati i limiti dei blocchi di dati OOB.

La routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) è particolarmente adatta per la gestione della notifica della presenza di dati fuori banda quando \_ OOBINLINE è disattivato.

## <a name="oob-data-in-tcp"></a>OOB dati in TCP

> [!IMPORTANT]
> La seguente discussione sui dati fuori banda (OOB), implementati con i dati urgenti TCP, segue il modello usato nella distribuzione del software Berkeley. Gli utenti e gli implementatori devono tenere presente quanto segue:

 

-   Attualmente sono presenti due interpretazioni in conflitto di [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (in cui è stato introdotto il concetto).
-   L'implementazione dei dati di OOB in Berkeley Software Distribution (BSD) non è conforme ai requisiti dell'host specificati nella [specifica RFC 1122](https://www.ietf.org/rfc/rfc1122.txt).

    In particolare, il puntatore urgente TCP in BSD punta al byte dopo il byte di dati urgente e un puntatore di urgenza TCP conforme a RFC punta al byte di dati urgente. Di conseguenza, se un'applicazione invia dati urgenti da un'implementazione compatibile con BSD a un'implementazione compatibile con RFC 1122, il ricevitore legge il byte di dati urgente errato (legge il byte posizionato dopo il byte corretto nel flusso di dati come byte di dati urgente).

    Per ridurre al minimo i problemi di interoperabilità, è consigliabile che i writer di applicazioni non usino i dati OOB a meno che non sia necessario per interagire con un servizio esistente. I fornitori di Windows Sockets vengono invitati a documentare la semantica di OOB (BSD o RFC 1122) implementata dal prodotto.

L'arrivo di un segmento TCP con il flag URG (per urgente) impostato indica l'esistenza di un singolo byte di dati OOB all'interno del flusso di dati TCP. Le dimensioni del blocco di dati OOB sono pari a un byte. Il puntatore urgente è un offset positivo rispetto al numero di sequenza corrente nell'intestazione TCP che indica la posizione del blocco di dati OOB (in modo ambiguo, come indicato nel precedente). Potrebbe, quindi, puntare a dati che non sono ancora stati ricevuti.

Se quindi \_ OOBINLINE è disabilitato (impostazione predefinita) quando arriva il segmento TCP contenente il byte a cui punta il puntatore urgente, il blocco di dati OOB (un byte) viene rimosso dal flusso di dati e memorizzato nel buffer. Se viene ricevuto un segmento TCP successivo con il flag urgente impostato (e un nuovo puntatore urgente), il byte OOB attualmente in coda può andare perduto perché viene sostituito dal nuovo blocco di dati OOB (come si verifica in Berkeley Software Distribution). Tuttavia, non viene mai sostituito nel flusso di dati.

Con \_ l'abilitazione di OOBINLINE, i dati urgenti rimangono nel flusso di dati. Di conseguenza, il blocco di dati OOB non viene mai perso quando arriva un nuovo segmento TCP contenente dati urgenti. Il contrassegno di dati OOB esistente viene aggiornato alla nuova posizione.

> [!Note]  
> Quando \_ è impostata l'opzione di socket OOBINLINE, il IOCTL SIOCATMARK restituisce sempre **true** e i dati OOB vengono restituiti all'utente come dati normali.

 

 

 



