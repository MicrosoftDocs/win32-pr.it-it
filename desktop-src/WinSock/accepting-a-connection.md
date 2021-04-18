---
description: Quando il socket è in ascolto di una connessione, il programma deve gestire le richieste di connessione su tale socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Accettazione di una connessione (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307058"
---
# <a name="accepting-a-connection-windows-sockets-2"></a>Accettazione di una connessione (Windows Sockets 2)

Quando il socket è in ascolto di una connessione, il programma deve gestire le richieste di connessione su tale socket.

**Per accettare una connessione in un socket**

1.  Creare un oggetto **socket** temporaneo denominato ClientSocket per l'accettazione delle connessioni dai client.
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  Normalmente un'applicazione server è progettata per restare in ascolto delle connessioni da più client. Per i server a prestazioni elevate, in genere vengono usati più thread per gestire più connessioni client.

    Sono disponibili diverse tecniche di programmazione con Winsock che possono essere usate per restare in ascolto di più connessioni client. Una tecnica di programmazione consiste nel creare un ciclo continuo che verifica la presenza di richieste di connessione tramite la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (vedere [ascolto su un socket](listening-on-a-socket.md)). Se si verifica una richiesta di connessione, l'applicazione chiama la funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) e passa il lavoro a un altro thread per gestire la richiesta. Sono possibili diverse altre tecniche di programmazione.

    Si noti che questo esempio di base è molto semplice e non usa più thread. L'esempio è anche semplicemente in ascolto e accetta solo una singola connessione.

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  Quando la connessione client è stata accettata, un'applicazione server passa normalmente il socket client accettato (la variabile ClientSocket nel codice di esempio precedente) a un thread di lavoro o a una porta di completamento di I/O e continua ad accettare connessioni aggiuntive. In questo esempio di base, il server continua con il passaggio successivo.

    Sono disponibili diverse altre tecniche di programmazione che possono essere usate per ascoltare e accettare più connessioni. Questi includono l'uso delle funzioni [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . Esempi di alcune di queste diverse tecniche di programmazione sono illustrate negli [esempi di Winsock avanzati](getting-started-with-winsock.md) inclusi in Microsoft Windows Software Development Kit (SDK).

    > [!Note]  
    > Nei sistemi UNIX, una tecnica di programmazione comune per i server era che un'applicazione potesse restare in ascolto delle connessioni. Quando è stata accettata una connessione, il processo padre chiama la funzione **fork** per creare un nuovo processo figlio per gestire la connessione client, ereditando il socket dall'elemento padre. Questa tecnica di programmazione non è supportata in Windows, perché la funzione **fork** non è supportata. Questa tecnica non è in genere adatta ai server ad alte prestazioni, perché le risorse necessarie per creare un nuovo processo sono molto più grandi di quelle necessarie per un thread.

     

Passaggio successivo: [ricezione e invio di dati sul server](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Ascolto su un socket](listening-on-a-socket.md)
</dt> </dl>

 

 
