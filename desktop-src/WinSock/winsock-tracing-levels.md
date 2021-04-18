---
description: 'Altre informazioni su: livelli di traccia Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Livelli di traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315753"
---
# <a name="winsock-tracing-levels"></a>Livelli di traccia Winsock

## <a name="levels-of-winsock-tracing"></a>Livelli di traccia Winsock

Nella traccia Winsock sono possibili due livelli di registrazione:

-   Informazioni
-   Dettagliato

Il livello informazioni analizza il socket creare e chiudere gli eventi, nonché gli eventuali errori che si verificano nel socket.

Il livello dettagliato include gli eventi a livello di informazioni e aggiunge ulteriori tracce per gli eventi di trasmissione e ricezione. La registrazione dettagliata verrebbe utilizzata per rilevare i problemi di danneggiamento del buffer e le applicazioni scritte in modo non corretto.

Con la traccia eventi di rete Winsock è possibile utilizzare il livello di informazioni o dettagliato. La traccia delle modifiche del catalogo Winsock supporta solo il livello di informazioni.

## <a name="information-event-tracing"></a>Traccia eventi informativi

Nell'elenco seguente vengono illustrate le operazioni di socket di eventi di rete Winsock tracciate a livello di informazioni:

-   Creazione socket

    Un evento viene registrato nella creazione del socket che può essere usato per tracciare la durata di un socket. Questi eventi includono anche socket creati accettando connessioni su un socket di ascolto.

-   Associazione

    L'indirizzo IP locale viene registrato per consentire la correlazione tra le informazioni di traccia di Winsock e le chiamate al socket di un'applicazione.

-   Connessione

    L'indirizzo IP remoto del socket connesso viene registrato per consentire la correlazione delle informazioni di traccia di Winsock alle chiamate socket di un'applicazione.

-   Interruzioni e annullamenti avviati da Winsock

    Quando Winsock interrompe attivamente o Annulla una richiesta, l'evento viene registrato.

-   Reimpostazioni avviate dal trasporto

    Ogni volta che il trasporto sottostante indica che la connessione è stata reimpostata, l'evento viene registrato.

-   Inviare e ricevere errori

    Ogni volta che una chiamata di trasmissione o ricezione al trasporto sottostante ha esito negativo, viene registrato l'evento.

-   Disconnetti e Chiudi socket

    Un evento viene registrato quando un handle di socket viene chiuso.

## <a name="verbose-event-tracing"></a>Traccia eventi dettagliati

Tutti gli eventi informativi vengono tracciati a livello dettagliato. Nell'elenco seguente vengono illustrate le operazioni aggiuntive del socket di eventi di rete Winsock tracciate a livello dettagliato:

-   Buffer di invio e ricezione

    Gli eventi vengono registrati negli indirizzi del buffer utente e le lunghezze quando le chiamate di invio e ricezione vengono inviate a Winsock, oltre al completamento di queste chiamate. Questa operazione è utile per la diagnosi dei problemi di riutilizzo del buffer, nonché per l'utilizzo inefficiente dei buffer.

-   Opzioni socket

    Un evento viene registrato quando un'applicazione modifica determinati valori di opzioni del socket. Alcune delle opzioni registrate includono \_ sndbuf, pertanto \_ RCVBUF, SIO Abilita l' \_ \_ \_ Accodamento circolare e FIONBIO.

-   WSAPoll e Select

    Un evento viene registrato nell'utilizzo di un'applicazione di [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e nelle chiamate [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) che possono essere usate per individuare i colli di bottiglia delle prestazioni.

-   Interruzioni e annullamenti avviati da Winsock

    Quando Winsock interrompe attivamente o Annulla una richiesta, l'evento viene registrato.

-   Maschera eventi

    Viene registrato un evento della maschera di eventi registrata da un'applicazione per l'utilizzo della funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

-   Datagram

    Un evento viene registrato ogni volta che viene ricevuto un datagramma e non è disponibile spazio nel buffer in cui copiarlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Dettagli traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
