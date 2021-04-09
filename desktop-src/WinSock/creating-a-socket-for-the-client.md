---
description: Dopo l'inizializzazione, è necessario creare un'istanza di un oggetto SOCKET per l'uso da parte del client.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Creazione di un socket per il client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879221"
---
# <a name="creating-a-socket-for-the-client"></a>Creazione di un socket per il client

Dopo l'inizializzazione, è necessario creare un'istanza di un oggetto **socket** per l'uso da parte del client.

**Per creare un socket**

1.  Dichiarare un oggetto [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) che contiene una struttura [**sockaddr**](sockaddr-2.md) e inizializzare questi valori. Per questa applicazione, la famiglia di indirizzi Internet non è specificata in modo che sia possibile restituire un indirizzo IPv6 o IPv4. L'applicazione richiede che il tipo di socket sia un socket di flusso per il protocollo TCP.
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  Chiamare la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che richiede l'indirizzo IP per il nome del server passato nella riga di comando. La porta TCP sul server a cui il client si connetterà viene definita per impostazione predefinita \_ come 27015 in questo esempio. La funzione **funzione getaddrinfo** restituisce il relativo valore come intero che viene controllato per verificare la presenza di errori.
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  Creare un oggetto **socket** denominato ConnectSocket.
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  Chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e restituire il relativo valore alla variabile ConnectSocket. Per questa applicazione, usare il primo indirizzo IP restituito dalla chiamata a [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che corrisponde alla famiglia di indirizzi, al tipo di socket e al protocollo specificati nel parametro *hints* . In questo esempio è stato specificato un socket del flusso TCP con un tipo di socket del flusso di SOCK \_ e un protocollo di IPPROTO \_ TCP. La famiglia di indirizzi non è stata specificata (AF \_ UNspecte), quindi l'indirizzo IP restituito può essere un indirizzo IPv6 o IPv4 per il server.

    Se l'applicazione client desidera connettersi usando solo IPv6 o IPv4, la famiglia di indirizzi deve essere impostata su AF \_ INET6 per IPv6 o AF \_ inet per IPv4 nel parametro *hints* .

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  Verificare la presenza di errori per verificare che il socket sia un socket valido.
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

I parametri passati alla funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) possono essere modificati per implementazioni diverse.

Il rilevamento degli errori è una parte fondamentale del codice di rete corretto. Se la chiamata al [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) non riesce, viene restituito un socket non valido \_ . L'istruzione **if** del codice precedente viene utilizzata per intercettare eventuali errori che si sono verificati durante la creazione del socket. [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce un numero di errore associato all'ultimo errore che si è verificato.

> [!Note]  
> Potrebbe essere necessario un controllo degli errori più ampio a seconda dell'applicazione.
>
> Ad esempio, l'impostazione di *hints.ai_family* su **AF_UNSPEC** può causare l'esito negativo della chiamata Connect. In tal caso, usare invece un valore IPv4 (**AF_INET**) o IPv6 (**AF_INET6**) specifico.

[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) viene usato per terminare l'uso della DLL WS2 \_ 32.

Passaggio successivo: [connessione a un socket](connecting-to-a-socket.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inizializzazione di Winsock](initializing-winsock.md)
</dt> <dt>

[Applicazione client Winsock](winsock-client-application.md)
</dt> </dl>

 

 
