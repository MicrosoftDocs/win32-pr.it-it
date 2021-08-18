---
description: Di seguito è riportata una guida dettagliata per iniziare a Windows programmazione socket.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Attività iniziali con Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcce956d7dcb142e4a51ac3a461868dfa055acc9a2d1624b6a6dff5132f86ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132154"
---
# <a name="getting-started-with-winsock"></a>Attività iniziali con Winsock

Di seguito è riportata una guida dettagliata per iniziare a Windows programmazione socket. È progettato per offrire una conoscenza delle funzioni e delle strutture di dati Di base di Winsock e del modo in cui funzionano insieme.

L'applicazione client e server utilizzata a scopo illustrativo è un client e un server di base. Esempi di codice più avanzati sono inclusi negli esempi inclusi in Microsoft Windows Software Development Kit (SDK).

I primi passaggi sono gli stessi per le applicazioni client e server.

-   [Informazioni su server e client](about-clients-and-servers.md)
-   [Creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)
-   [Inizializzazione di Winsock](initializing-winsock.md)

Le sezioni seguenti descrivono i passaggi rimanenti per la creazione di un'applicazione client Winsock.

-   [Creazione di un socket per il client](creating-a-socket-for-the-client.md)
-   [Connessione a un socket](connecting-to-a-socket.md)
-   [Invio e ricezione di dati nel client](sending-and-receiving-data-on-the-client.md)
-   [Disconnessione del client](disconnecting-the-client.md)

Le sezioni seguenti descrivono i passaggi rimanenti per la creazione di un'applicazione server Winsock.

-   [Creazione di un socket per il server](creating-a-socket-for-the-server.md)
-   [Associazione di un socket](binding-a-socket.md)
-   [Ascolto su un socket](listening-on-a-socket.md)
-   [Accettazione di una connessione](accepting-a-connection.md)
-   [Ricezione e invio di dati nel server](receiving-and-sending-data-on-the-server.md)
-   [Disconnessione del server](disconnecting-the-server.md)

Codice sorgente completo per questi esempi di base.

-   [Esecuzione dell'esempio di codice del client e del server Winsock](finished-server-and-client-code.md)
-   [Completare il codice client Winsock](complete-client-code.md)
-   [Completare il codice del server Winsock](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Esempi avanzati di Winsock

In Windows SDK sono inclusi diversi esempi di client e server Winsock più avanzati. Per impostazione predefinita, il codice sorgente di esempio di Winsock viene installato nella directory seguente da Windows SDK per Windows 7:

*C: \\ Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples \\ NetDs \\ winsock*

Nelle versioni precedenti di Windows SDK, il numero di versione nel percorso precedente cambierebbe. Ad esempio, il codice sorgente di esempio winsock viene installato nella directory predefinita seguente da Windows SDK per Windows Vista

*C: \\ Programmi \\ Microsoft SDKs \\ Windows \\ v6.0 \\ Samples \\ NetDs \\ winsock*

Gli esempi più avanzati elencati di seguito, in ordine da prestazioni più elevate a prestazioni inferiori, sono disponibili nelle directory seguenti:

-   Iocp

    Questa directory contiene tre programmi di esempio che usano le porte di completamento I/O. I programmi includono un server Winsock (iocpserver) che usa la funzione [**WSAAccept,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) un server Winsock (iocpserverex) che usa la funzione [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) e un semplice client Winsock multithread (iocpclient) usato per testare uno di questi server. I programmi server supportano più client che si connettono tramite TCP/IP e inviano buffer di dati di dimensioni arbitrarie che il server invia al client. Per praticità, è stato sviluppato un semplice programma client, iocpclient, per connettersi e inviare continuamente dati al server per stressarlo usando più thread. I server Winsock che usano le porte di completamento I/O offrono la maggiore capacità di prestazioni.

-   Sovrapposizione

    Questa directory contiene un programma server di esempio che usa operazioni di I/O sovrapposte. Il programma di esempio usa la [**funzione AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) e le operazioni di I/O sovrapposte per gestire in modo efficace più richieste di connessione asincrone dai client. Il server usa la **funzione AcceptEx** per eseguire il multiplex di connessioni client diverse in un'applicazione Win32 a thread singolo. L'uso di operazioni di I/O sovrapposte consente una maggiore scalabilità.

-   WSAPoll

    Questa directory contiene un programma di esempio di base che illustra l'uso [**della funzione WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) Il programma client e server combinato non blocca e usa la funzione **WSAPoll** per determinare quando è possibile inviare o ricevere senza blocco. Questo esempio è più a scopo illustrativo e non è un server ad alte prestazioni.

-   simple

    Questa directory contiene tre programmi di esempio di base che illustrano l'uso di più thread da parte di un server. I programmi includono un semplice server TCP/UDP (semplici), un server solo TCP (simples ioctl) che usa la funzione select in un'applicazione console Win32 per supportare più richieste client e un \_ programma client TCP/UDP [](/windows/desktop/api/Winsock2/nf-winsock2-select) (simplec) per testare i server. I server illustrano l'uso di più thread per gestire più richieste client. Questo metodo presenta problemi di scalabilità perché viene creato un thread separato per ogni richiesta del client.

-   Accettare

    Questa directory contiene un programma client e un server di esempio di base. Il server dimostra l'uso dell'accettazione non bloccante usando la [**funzione select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o l'accettazione asincrona tramite [**la funzione WSAAsyncSelect.**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) Questo esempio è più a scopo illustrativo e non è un server ad alte prestazioni.

 

 
