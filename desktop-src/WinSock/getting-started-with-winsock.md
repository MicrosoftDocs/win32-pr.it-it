---
description: Di seguito è riportata una guida dettagliata per iniziare a usare la programmazione Windows Sockets.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Introduzione con Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43751663a637fafb2eec453a48c329ff8e4499f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306957"
---
# <a name="getting-started-with-winsock"></a>Introduzione con Winsock

Di seguito è riportata una guida dettagliata per iniziare a usare la programmazione Windows Sockets. È progettato per fornire informazioni sulle funzioni e sulle strutture di dati di base di Winsock e sul modo in cui interagiscono.

L'applicazione client e Server usata per l'illustrazione è un client e un server molto semplici. Negli esempi inclusi nel Software Development Kit (SDK) di Microsoft Windows sono inclusi esempi di codice più avanzati.

I primi passaggi sono gli stessi per le applicazioni client e server.

-   [Informazioni su server e client](about-clients-and-servers.md)
-   [Creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)
-   [Inizializzazione di Winsock](initializing-winsock.md)

Nelle sezioni seguenti vengono descritti i passaggi rimanenti per la creazione di un'applicazione client Winsock.

-   [Creazione di un socket per il client](creating-a-socket-for-the-client.md)
-   [Connessione a un socket](connecting-to-a-socket.md)
-   [Invio e ricezione di dati sul client](sending-and-receiving-data-on-the-client.md)
-   [Disconnessione del client](disconnecting-the-client.md)

Nelle sezioni seguenti vengono descritti i passaggi rimanenti per la creazione di un'applicazione server Winsock.

-   [Creazione di un socket per il server](creating-a-socket-for-the-server.md)
-   [Associazione di un socket](binding-a-socket.md)
-   [Ascolto su un socket](listening-on-a-socket.md)
-   [Accettazione di una connessione](accepting-a-connection.md)
-   [Ricezione e invio di dati sul server](receiving-and-sending-data-on-the-server.md)
-   [Disconnessione del server](disconnecting-the-server.md)

Il codice sorgente completo per questi esempi di base.

-   [Esecuzione dell'esempio di codice server e client Winsock](finished-server-and-client-code.md)
-   [Codice client Winsock completo](complete-client-code.md)
-   [Codice server Winsock completo](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Esempi avanzati di Winsock

Con il Windows SDK sono inclusi diversi esempi di client e server Winsock più avanzati. Per impostazione predefinita, il codice sorgente di esempio Winsock viene installato nella directory seguente dalla Windows SDK per Windows 7:

*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ Winsock*

Nelle versioni precedenti del Windows SDK, il numero di versione nel percorso precedente verrebbe modificato. Ad esempio, il codice sorgente di esempio Winsock viene installato nella directory predefinita seguente dalla Windows SDK per Windows Vista

*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ esempi \\ NetDs \\ Winsock*

Gli esempi più avanzati elencati di seguito in ordine da prestazioni superiori a quelle più basse sono disponibili nelle directory seguenti:

-   IOCP

    Questa directory contiene tre programmi di esempio che utilizzano le porte di completamento I/O. I programmi includono un server Winsock (iocpserver) che usa la funzione [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , un server Winsock (iocpserverex) che usa la funzione [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) e un client Winsock con multithreading semplice (iocpclient) usato per testare uno di questi server. I programmi server supportano più client che si connettono tramite TCP/IP e inviano buffer di dati di dimensioni arbitrari che il server restituisce al client. Per praticità, è stato sviluppato un semplice programma client, iocpclient, per connettersi e inviare continuamente i dati al server per sottolinearli con più thread. I server Winsock che utilizzano le porte di completamento I/O offrono la funzionalità di prestazioni più elevate.

-   sovrapposizione

    Questa directory contiene un programma server di esempio che usa l'I/O sovrapposto. Il programma di esempio utilizza la funzione [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) e l'i/O sovrapposto per gestire più richieste di connessione asincrone dai client in modo efficace. Il server utilizza la funzione **AcceptEx** per eseguire il multiplexing di connessioni client diverse in un'applicazione Win32 a thread singolo. L'utilizzo di I/O sovrapposti consente una maggiore scalabilità.

-   WSAPoll

    Questa directory contiene un programma di esempio di base che illustra l'uso della funzione [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . Il programma client e server combinato non è bloccato e utilizza la funzione **WSAPoll** per determinare quando è possibile inviare o ricevere senza blocco. Questo esempio è più per illustrazione e non è un server a prestazioni elevate.

-   simple

    Questa directory contiene tre programmi di esempio di base che illustrano l'utilizzo di più thread da parte di un server. I programmi includono un semplice server TCP/UDP (semplici), un server solo TCP (Simple \_ IOCTL) che usa la funzione [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) in un'applicazione console Win32 per supportare più richieste client e un programma TCP/UDP client (SIMPLEC) per il test dei server. Nei server viene illustrato l'utilizzo di più thread per gestire più richieste client. Questo metodo presenta problemi di scalabilità, poiché viene creato un thread separato per ogni richiesta del client.

-   accettare

    Questa directory contiene un programma client e un server di esempio di base. Il server illustra l'uso di Accept non di blocco mediante la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o l'accettazione asincrona mediante la funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Questo esempio è più per illustrazione e non è un server a prestazioni elevate.

 

 
