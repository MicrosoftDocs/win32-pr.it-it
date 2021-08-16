---
description: Dopo l'inizializzazione, è necessario creare un'istanza di un oggetto SOCKET per l'uso da parte del server.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Creazione di un socket per il server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e71d6ee0117153b00a9ab77c53bd7555aa031b3fa9d1f7a425ea9aaf0e358f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322201"
---
# <a name="creating-a-socket-for-the-server"></a>Creazione di un socket per il server

Dopo **l'inizializzazione, è** necessario creare un'istanza di un oggetto SOCKET per l'uso da parte del server.

**Per creare un socket per il server**

1.  La [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) viene usata per determinare i valori nella [**struttura sockaddr:**](sockaddr-2.md)

    -   **Af \_ INET** viene usato per specificare la famiglia di indirizzi IPv4.
    -   **SOCK \_ STREAM** viene usato per specificare un socket di flusso.
    -   **IPPROTO \_ TCP** viene usato per specificare il protocollo TCP .
    -   **Intelligenza artificiale \_ Il** flag PASSIVE indica che il chiamante intende usare la struttura di indirizzi socket restituita in una chiamata alla [**funzione di**](/windows/desktop/api/winsock/nf-winsock-bind) associazione. Quando il flag **AI \_ PASSIVE** è impostato e il parametro *nodename* per la funzione [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) è un puntatore **NULL,** la parte dell'indirizzo IP della struttura di indirizzi socket viene impostata su **INADDR \_ ANY** per gli indirizzi IPv4 o **IN6ADDR \_ ANY \_ INIT** per gli indirizzi IPv6.
    -   27015 è il numero di porta associato al server a cui si connetterà il client.

    La [**struttura addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) viene usata dalla [**funzione getaddrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Creare un **oggetto SOCKET** denominato ListenSocket perché il server sia in ascolto delle connessioni client.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Chiamare la [**funzione socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e restituirne il valore alla variabile ListenSocket. Per questa applicazione server, usare il primo indirizzo IP restituito dalla chiamata a [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) corrispondente alla famiglia di indirizzi, al tipo di socket e al protocollo specificati nel *parametro hints.* In questo esempio è stato richiesto un socket di flusso TCP per IPv4 con una famiglia di indirizzi IPv4, un tipo di socket SOCK STREAM e un protocollo \_ IPPROTO \_ TCP. Viene quindi richiesto un indirizzo IPv4 per ListenSocket.

    Se l'applicazione server vuole restare in ascolto su IPv6, la famiglia di indirizzi deve essere impostata su AF \_ INET6 nel *parametro hints.* Se un server vuole essere in ascolto sia su IPv6 che su IPv4, è necessario creare due socket di ascolto, uno per IPv6 e uno per IPv4. Questi due socket devono essere gestiti separatamente dall'applicazione.

    Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 che viene messo in modalità dual stack per l'ascolto sia su IPv6 che su IPv4. Per altre informazioni su questa funzionalità, vedere [Dual-Stack Sockets.](dual-stack-sockets.md)

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  Verificare la presenza di errori per assicurarsi che il socket sia un socket valido.
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Passaggio successivo: [Associazione di un socket](binding-a-socket.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inizializzazione di Winsock](initializing-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> </dl>

 

 
