---
description: Un problema principale del porting di applicazioni da un ambiente Berkeley Sockets a un ambiente Windows prevede il blocco. ovvero richiamando una funzione che non restituisce un valore fino a quando l'operazione associata non viene completata.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Routine di blocco di Windows Sockets 1,1 e EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea6d45b4d25578505a3cb4ab4beb7c2c2fe90e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308869"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Routine di blocco di Windows Sockets 1,1 e EINPROGRESS

Un problema principale del porting di applicazioni da un ambiente Berkeley Sockets a un ambiente Windows prevede il blocco. ovvero richiamando una funzione che non restituisce un valore fino a quando l'operazione associata non viene completata. Un problema si verifica quando l'operazione richiede un tempo arbitrariamente lungo per il completamento: un esempio è una funzione [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) che può bloccarsi fino a quando i dati non sono stati ricevuti dal sistema peer. Il comportamento predefinito all'interno del modello di socket Berkeley prevede che un socket funzioni in modalità di blocco a meno che il programmatore non richieda esplicitamente che le operazioni vengano considerate come non bloccanti. Gli ambienti Windows Sockets 1,1 non possono presupporre la pianificazione di tipo preemptive. Pertanto, è consigliabile che i programmatori usino le operazioni non bloccanti (asincrone) se possibile con Windows Sockets 1,1. Poiché questo non è sempre possibile, sono state fornite le funzionalità di pseudo-blocco descritte nei seguenti elementi.

> [!Note]  
> Windows Sockets 2 viene eseguito solo su sistemi operativi a 32 bit preemptive in cui i deadlock non rappresentano un problema. Le procedure di programmazione consigliate per Windows Sockets 1,1 non sono necessarie in Windows Sockets 2.

 

Anche in un socket di blocco, alcune funzioni, ovvero [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)e [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , ad esempio, vengono completate immediatamente. Non esiste alcuna differenza tra un blocco e un'operazione non di blocco per queste funzioni. Altre operazioni, ad esempio [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv), possono essere completate immediatamente o richiedere un tempo arbitrario per il completamento, a seconda delle diverse condizioni di trasporto. Quando vengono applicati a un socket di blocco, queste operazioni sono denominate operazioni di blocco. Le funzioni seguenti possono bloccare:

-   [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Invia**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)

Con Windows Sockets 1,1 a 16 bit, un'operazione di blocco che non può essere completata immediatamente viene gestita dallo pseudo-blocco come indicato di seguito.

Il provider di servizi avvia l'operazione, quindi immette un ciclo in cui invia tutti i messaggi di Windows (cedendo il processore a un altro thread, se necessario), quindi controlla il completamento della funzione Windows Sockets. Se la funzione è stata completata o se [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) è stato richiamato, la funzione di blocco viene completata con un risultato appropriato.

Un provider di servizi deve consentire l'installazione di una funzione hook di blocco che non elabora i messaggi per evitare la possibilità di messaggi rientranti mentre un'operazione di blocco è in attesa. La funzione di hook di blocco più semplice restituisce **false**. Se una DLL Windows Sockets dipende dai messaggi per l'operazione interna, può eseguire **PeekMessage**(**hMyWnd**...) prima di eseguire l'hook di blocco dell'applicazione in modo che possa ricevere i messaggi senza influire sul resto del sistema.

In un ambiente Windows Sockets 1,1 a 16 bit, se viene ricevuto un messaggio di Windows per un processo per cui è in corso un'operazione di blocco, esiste il rischio che l'applicazione tenti di emettere un'altra chiamata di Windows Sockets. A causa della difficoltà nella gestione sicura di questa condizione, Windows Sockets 1,1 non supporta tale comportamento dell'applicazione. Un'applicazione non è autorizzata a eseguire più di una chiamata di funzione Windows Sockets nidificata. Per una determinata attività è consentita una sola chiamata di funzione in attesa. Le uniche eccezioni sono due funzioni fornite per supportare il programmatore in questa situazione: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) e [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).

La funzione [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) può essere chiamata in qualsiasi momento per determinare se è in corso una chiamata di blocco di Windows sockets 1,1. Analogamente, la funzione [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) può essere chiamata in qualsiasi momento per annullare una chiamata di blocco in corso. Qualsiasi altra annidamento di funzioni Windows Sockets ha esito negativo con l'errore WSAEINPROGRESS.

È opportuno sottolineare che questa restrizione si applica alle operazioni di blocco e non blocco. Per le applicazioni Windows Sockets 2 che negoziano la versione 2,0 o una versione successiva al momento della chiamata a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup), non viene chiusa alcuna restrizione sull'annidamento delle operazioni. Le operazioni possono essere annidate in rare circostanze, ad esempio durante un callback di accettazione condizionale [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , o se un provider di servizi richiama a sua volta una funzione di Windows Sockets 2.

Sebbene questo meccanismo sia sufficiente per le applicazioni semplici, non può supportare i requisiti complessi per l'invio di messaggi di applicazioni più avanzate, ad esempio quelli che usano il modello MDI. Per tali applicazioni, l'API di Windows Sockets include la funzione [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), che consente all'applicazione di specificare una routine speciale che può essere chiamata al posto della routine di invio dei messaggi predefinita descritta nella discussione precedente.

Il provider Windows Sockets chiama l'hook di blocco solo se si verificano tutte le condizioni seguenti:

-   La routine è quella definita come in grado di bloccarsi.
-   Il socket specificato è un socket di blocco.
-   La richiesta non può essere completata immediatamente.

Un socket è impostato su blocking per impostazione predefinita, ma la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) con l'IOCTL **FIONBIO** o la funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) può impostare un socket sulla modalità di non blocco.

L'hook di blocco non viene mai chiamato e non è necessario che l'applicazione sia interessata dai problemi di riapertura che possono essere introdotti dall'hook di blocco, se un'applicazione rispetta le linee guida seguenti:

-   USA solo socket non bloccati.
-   Usa le routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e/o **WSAAsyncGetXByY** anziché le routine [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e **getXbyY** .

Se un'applicazione Windows Sockets 1,1 richiama un'operazione asincrona o non bloccata che accetta un puntatore a un oggetto memoria (ad esempio, un buffer o una variabile globale), è responsabilità dell'applicazione garantire che l'oggetto sia disponibile per Windows Sockets durante l'operazione. L'applicazione non deve richiamare alcuna funzione di Windows che potrebbe influire sul mapping o affrontare la redditività della memoria in questione.

 

 



