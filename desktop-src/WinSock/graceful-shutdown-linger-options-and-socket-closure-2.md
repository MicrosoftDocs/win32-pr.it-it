---
description: Il materiale seguente viene fornito come spiegazione per l'oggetto dell'arresto delle connessioni socket che chiudono i socket. È importante distinguere la differenza tra l'arresto di una connessione socket e la chiusura di un socket.
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: Arresto normale, opzioni Linger e chiusura del socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226090"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>Arresto normale, opzioni Linger e chiusura del socket

Il materiale seguente viene fornito come spiegazione per l'oggetto dell'arresto delle connessioni socket che chiudono i socket. È importante distinguere la differenza tra l'arresto di una connessione socket e la chiusura di un socket.

L'arresto di una connessione socket comporta uno scambio di messaggi di protocollo tra i due endpoint, in seguito definito sequenza di arresto. Sono definite due classi generali di sequenze di arresto: aggraziate e interrotte (chiamate anche rigide). In una sequenza di arresto normale, tutti i dati che sono stati accodati ma non ancora trasmessi possono essere inviati prima della chiusura della connessione. In caso di arresto anomalo, tutti i dati non inviati andranno perduti. L'occorrenza di una sequenza di arresto (normale o abortica) può essere usata anche per fornire un' \_ indicazione di chiusura FD alle applicazioni associate, a indicare che è in corso un arresto.

La chiusura di un socket, d'altra parte, causa la deallocazione dell'handle del socket, in modo che l'applicazione non possa più fare riferimento o utilizzare il socket in alcun modo.

In Windows Sockets è possibile usare sia la funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) che la funzione [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) per avviare una sequenza di arresto, mentre la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) viene usata per deallocare gli handle di socket e liberare le risorse associate. Tuttavia, si verifica una certa confusione dal fatto che la funzione **chiamata closesocket** causa implicitamente la generazione di una sequenza di arresto, se non è già avvenuta. In realtà, si tratta di una pratica di programmazione piuttosto comune che si basa su questa funzionalità e per usare **chiamata closesocket** per avviare la sequenza di arresto e deallocare l'handle del socket.

Per semplificare questo utilizzo, l'interfaccia Sockets fornisce i controlli tramite il meccanismo di opzione del socket che consente al programmatore di indicare se la sequenza di arresto implicita deve essere normale o interrotta e anche se la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) deve rimanere sospesa (non immediatamente completata) per consentire il completamento di una sequenza di arresto normale. Queste distinzioni importanti e le ramificazioni dell'utilizzo di **chiamata closesocket** in questo modo non sono ancora ampiamente comprese.

Se si stabiliscono i valori appropriati per le opzioni del socket in modo \_ che vengano sospesi e quindi \_ DONTLINGER, è possibile ottenere i tipi di comportamento seguenti con la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) :

-   Sequenza di arresto interrotta, ritorno immediato da [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).
-   Arresto normale, ritardo della restituzione fino al completamento della sequenza di arresto o scadenza di un intervallo di tempo specificato. Se l'intervallo di tempo scade prima del completamento della sequenza di arresto normale, si verifica una sequenza di arresto interrotta e [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) restituisce.
-   Arresto normale, restituzione immediata, che consente di completare la sequenza di arresto in background. Sebbene questo sia il comportamento predefinito, l'applicazione non ha modo di sapere quando (o se) la sequenza di arresto normale viene effettivamente completata.

L'uso delle opzioni per il \_ socket DONTLINGER e così via e \_ la struttura [**Linger**](/windows/desktop/api/winsock/ns-winsock-linger) associata viene descritto più dettagliatamente nelle sezioni di riferimento sulle [**Opzioni del socket di \_ socket Sol**](sol-socket-socket-options.md) e sulla struttura **Linger** .

Una tecnica che può essere usata per ridurre al minimo la possibilità di problemi che si verificano durante la connessione teardown consiste nell'evitare di basarsi su un arresto implicito avviato da [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket). Usare invece una delle due funzioni di arresto esplicite, [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) o [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect). Questa operazione a sua volta causa \_ la ricezione di un'indicazione di chiusura FD da parte dell'applicazione peer, a indicare che tutti i dati in sospeso sono stati ricevuti. Per illustrare questo problema, nella tabella seguente vengono illustrate le funzioni che verrebbero richiamate dai componenti client e server di un'applicazione, in cui il client è responsabile dell'avvio di un arresto normale.

| Lato client                                                                                                                | Sul lato server                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| (1) richiama [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) per segnalare la fine della sessione e il client non ha più dati da inviare. |                                                                                                       |
|                                                                                                                            | (2) riceve \_ la chiusura FD, che indica l'arresto normale in corso e la ricezione di tutti i dati. |
|                                                                                                                            | (3) Invia tutti i dati di risposta rimanenti.                                                                |
| (solo per importanza temporale locale) Ottiene FD \_ Read e chiama [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) per ottenere tutti i dati di risposta inviati dal server.  | (4) richiama [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)(s, SD \_ Send) per indicare che il server non ha più dati da inviare.  |
| (5) riceve l' \_ indicazione di chiusura FD.                                                                                         | (solo per importanza temporale locale) Richiama [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .                       |
| (6) richiama [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                          |                                                                                                       |



 

 

 



