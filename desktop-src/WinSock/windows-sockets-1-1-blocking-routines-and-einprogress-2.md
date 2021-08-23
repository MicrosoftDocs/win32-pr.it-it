---
description: Un problema importante nella portabilità delle applicazioni da un ambiente Berkeley Sockets a un ambiente Windows comporta il blocco; in altri, richiamando una funzione che non restituisce finché non viene completata l'operazione associata.
ms.assetid: 13aedad7-5f3b-4d73-b8e5-be3a095294bc
title: Windows Routine di blocco di Sockets 1.1 ed EINPROGRESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4028549862412b80d1343851fb2a147da804095821fdefab4b6aae0eb6ec5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641221"
---
# <a name="windows-sockets-11-blocking-routines-and-einprogress"></a>Windows Routine di blocco di Sockets 1.1 ed EINPROGRESS

Un problema importante nella portabilità delle applicazioni da un ambiente Berkeley Sockets a un ambiente Windows comporta il blocco; in altri, richiamando una funzione che non restituisce finché non viene completata l'operazione associata. Un problema si verifica quando il completamento dell'operazione richiede un tempo arbitrariamente lungo: un esempio è una funzione [**recv,**](/windows/desktop/api/winsock/nf-winsock-recv) che potrebbe bloccarsi fino a quando i dati non vengono ricevuti dal sistema peer. Il comportamento predefinito all'interno del modello Berkeley Sockets è che un socket funzioni in modalità di blocco, a meno che il programmatore non richiede in modo esplicito che le operazioni vengano considerate non bloccanti. Windows Gli ambienti Sockets 1.1 non potevano presupporre la pianificazione preventiva. Pertanto, è consigliabile che i programmatori usino le operazioni non bloccanti (asincrone) se possibile con Windows Sockets 1.1. Poiché questo non era sempre possibile, sono state fornite le funzionalità di pseudo-blocco descritte di seguito.

> [!Note]  
> Windows Sockets 2 viene eseguito solo in sistemi operativi a 32 bit preemptive in cui i deadlock non sono un problema. Le procedure di programmazione consigliate Windows Sockets 1.1 non sono necessarie in Windows Sockets 2.

 

Anche in un socket di blocco, alcune funzioni, ad esempio [**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)e [**getpeername,**](/windows/desktop/api/winsock/nf-winsock-getpeername) vengono completate immediatamente. Non esiste alcuna differenza tra un'operazione di blocco e un'operazione non di blocco per tali funzioni. Altre operazioni, ad esempio [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), possono essere completate immediatamente o richiedere un tempo arbitrario, a seconda delle diverse condizioni di trasporto. Se applicate a un socket di blocco, queste operazioni vengono definite operazioni di blocco. Le funzioni seguenti possono bloccarsi:

-   [**Recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**Invia**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)

Con Sockets 1.1 Windows 1.1 a 16 bit, un'operazione di blocco che non può essere completata immediatamente viene gestita tramite pseudo-blocco come indicato di seguito.

Il provider di servizi avvia l'operazione, quindi entra in un ciclo in cui invia tutti i messaggi Windows (generando il processore a un altro thread, se necessario) e quindi verifica il completamento della funzione Windows Sockets. Se la funzione è stata completata o se È stato richiamato [**WSACancelBlockingCall,**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) la funzione di blocco viene completata con un risultato appropriato.

Un provider di servizi deve consentire l'installazione di una funzione hook di blocco che non elabora i messaggi per evitare la possibilità di nuovi messaggi mentre un'operazione di blocco è in sospeso. La funzione hook di blocco più semplice restituirebbe **FALSE.** Se una DLL Windows Sockets dipende dai messaggi per operazioni interne, può eseguire **PeekMessage**(**hMyWnd**...) prima di eseguire l'hook di blocco dell'applicazione in modo che possa ottenere i messaggi senza influire sul resto del sistema.

In un ambiente Windows Sockets 1.1 a 16 bit, se viene ricevuto un messaggio Windows per un processo per cui è in corso un'operazione di blocco, esiste il rischio che l'applicazione tenti di eseguire un'altra chiamata Windows Sockets. A causa della difficoltà di gestire questa condizione in modo sicuro, Windows Sockets 1.1 non supporta tale comportamento dell'applicazione. Un'applicazione non è autorizzata a eseguire più chiamate di funzione Windows Sockets annidate. Per una determinata attività è consentita una sola chiamata di funzione in sospeso. Le uniche eccezioni sono due funzioni fornite per assistere il programmatore in questa situazione: [**WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) e [**WSACancelBlockingCall.**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)

La [**funzione WSAIsBlocking**](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) può essere chiamata in qualsiasi momento per determinare se è in corso o meno una chiamata Windows Sockets 1.1. Analogamente, la [**funzione WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) può essere chiamata in qualsiasi momento per annullare una chiamata di blocco in corso. Qualsiasi altro annidamento delle Windows Sockets ha esito negativo con l'errore WSAEINPROGRESS.

È opportuno sottolineare che questa restrizione si applica sia alle operazioni di blocco che di non blocco. Per Windows applicazioni Sockets 2 che negoziano la versione 2.0 o successiva al momento della chiamata a [**WSAStartup,**](/windows/desktop/api/winsock/nf-winsock-wsastartup)non viene chiusa alcuna restrizione per l'annidamento delle operazioni. Le operazioni possono essere annidate in rare circostanze, ad esempio durante un callback di accettazione condizionale [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) o se un provider di servizi a sua volta richiama una funzione Windows Sockets 2.

Anche se questo meccanismo è sufficiente per le applicazioni semplici, non può supportare i complessi requisiti di invio dei messaggi di applicazioni più avanzate, ad esempio quelle che usano il modello MDI. Per tali applicazioni, l'API Windows Sockets include la funzione [**WSASetBlockingHook**](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook), che consente all'applicazione di specificare una routine speciale che può essere chiamata anziché la routine di invio di messaggi predefinita descritta nella discussione precedente.

Il provider Windows Sockets chiama l'hook di blocco solo se sono vere tutte le condizioni seguenti:

-   La routine è una routine definita come in grado di bloccare.
-   Il socket specificato è un socket di blocco.
-   La richiesta non può essere completata immediatamente.

Un socket è impostato sul blocco per impostazione predefinita, ma la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) con **FIONBIO** IOCTL o la funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) può impostare un socket sulla modalità non di blocco.

L'hook di blocco non viene mai chiamato e l'applicazione non deve preoccuparsi dei problemi di ricorsività che l'hook di blocco può introdurre, se un'applicazione segue queste linee guida:

-   Usa solo socket non di blocco.
-   Usa le routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e/o **WSAAsyncGetXByY** anziché [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e le routine **getXbyY.**

Se un'applicazione Windows Sockets 1.1 richiama un'operazione asincrona o non bloccante che accetta un puntatore a un oggetto di memoria (ad esempio un buffer o una variabile globale), è responsabilità dell'applicazione garantire che l'oggetto sia disponibile per i socket Windows durante l'operazione. L'applicazione non deve richiamare Windows funzione che potrebbe influire sulla vitalità del mapping o dell'indirizzo della memoria coinvolta.

 

 



