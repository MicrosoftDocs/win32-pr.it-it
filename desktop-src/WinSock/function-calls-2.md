---
description: Sono state introdotte nuove funzioni per l'interfaccia Windows Sockets progettata in modo specifico per semplificare Windows di programmazione dei socket. Uno dei vantaggi di queste nuove funzioni Windows Sockets è il supporto integrato per IPv6 e IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Chiamate di funzione per applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241db1f7e07264fe4f0c776834d17c48cff4780b06e6a42816d36a50fa22cef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051669"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>Chiamate di funzione per applicazioni Winsock IPv6

Sono state introdotte nuove funzioni per l'interfaccia Windows Sockets progettata in modo specifico per semplificare Windows di programmazione dei socket. Uno dei vantaggi di queste nuove funzioni Windows Sockets è il supporto integrato per IPv6 e IPv4.

Queste nuove Windows Sockets includono:

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   Famiglia di funzioni [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)e [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   [**Famiglia di funzioni getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**getnameinfo** e [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

Inoltre, sono state aggiunte nuove funzioni helper IP con supporto sia per IPv6 che per IPv4 per semplificare la programmazione Windows Sockets. Queste nuove funzioni helper IP includono quanto segue:

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Quando si aggiunge il supporto IPv6 a un'applicazione, è necessario usare le linee guida seguenti:

-   Usare [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) per stabilire una connessione a un endpoint in base a un nome host e a una porta. La **funzione WSAConnectByName** è disponibile in Windows Vista e versioni successive.
-   Usare [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) per stabilire una connessione a uno di una raccolta di possibili endpoint rappresentati da un set di indirizzi di destinazione (nomi host e porte). La **funzione WSAConnectByList** è disponibile in Windows Vista e versioni successive.
-   Sostituire [**le chiamate di funzione gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) con chiamate a una delle nuove funzioni [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets. La **funzione getaddrinfo** con supporto per il protocollo IPv6 è disponibile Windows XP e versioni successive. Il protocollo IPv6 è supportato anche in Windows 2000 quando viene installata L'anteprima della tecnologia IPv6 per Windows 2000.
-   Sostituire [**le chiamate di funzione gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) con chiamate a una delle nuove funzioni [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets. La **funzione getnameinfo** con supporto per il protocollo IPv6 è disponibile Windows XP e versioni successive. Il protocollo IPv6 è supportato anche in Windows 2000 quando viene installata L'anteprima della tecnologia IPv6 per Windows 2000.

## <a name="wsaconnectbyname"></a>WSAConnectByName

La [**funzione WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) semplifica la connessione a un endpoint usando un socket basato su flusso in base al nome host o all'indirizzo IP della destinazione (IPv4 o IPv6). Questa funzione riduce il codice sorgente necessario per creare un'applicazione IP indipendente dalla versione del protocollo IP usata. **WSAConnectByName** sostituisce i passaggi seguenti in una tipica applicazione TCP a una singola chiamata di funzione:

-   Risolvere un nome host in un set di indirizzi IP.
-   Per ogni indirizzo IP:
    -   Creare un socket della famiglia di indirizzi appropriata.
    -   Tenta di connettersi all'indirizzo IP remoto. Se la connessione ha esito positivo, restituisce ; in caso contrario, viene provato l'indirizzo IP remoto successivo per l'host.

La [**funzione WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va oltre la semplice risoluzione del nome e quindi il tentativo di connessione. La funzione usa tutti gli indirizzi remoti restituiti dalla risoluzione dei nomi e tutti gli indirizzi IP di origine del computer locale. Tenta prima di tutto di connettersi usando coppie di indirizzi con la massima probabilità di esito positivo. Pertanto, **WSAConnectByName** non solo garantisce che verrà stabilita una connessione, se possibile, ma riduce al minimo il tempo necessario per stabilire la connessione.

Per abilitare le comunicazioni IPv6 e IPv4, usare il metodo seguente:

-   La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere chiamata su un socket creato per la famiglia di indirizzi AF INET6 per disabilitare l'opzione socket \_ **IPV6 \_ V6ONLY** prima di chiamare [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea). A tale scopo, chiamare la funzione **setsockopt** nel socket con il parametro *level* impostato su **IPPROTO \_ IPV6** (vedere [Opzioni socket \_ IPV6 IPPROTO),](ipproto-ipv6-socket-options.md)il parametro *optname* impostato su **IPV6 \_ V6ONLY** e il valore del parametro *optvalue* impostato su zero.

Se un'applicazione deve essere associata a un indirizzo locale o a una porta specifica, non è possibile usare [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) perché il parametro socket per **WSAConnectByName** deve essere un socket non associato.

L'esempio di codice seguente mostra solo alcune righe di codice necessarie per usare questa funzione per implementare un'applicazione indipendente dalla versione IP.

Stabilire una connessione usando [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a>WSAConnectByList

La [**funzione WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) stabilisce una connessione a un host dato un set di possibili host (rappresentati da un set di porte e indirizzi IP di destinazione). La funzione accetta tutti gli indirizzi IP e le porte per l'endpoint e tutti gli indirizzi IP del computer locale e tenta una connessione usando tutte le possibili combinazioni di indirizzi.

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) è correlato alla [**funzione WSAConnectByName.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) Anziché accettare un singolo nome host, **WSAConnectByList** accetta un elenco di host (indirizzi di destinazione e coppie di porte) e si connette a uno degli indirizzi e delle porte nell'elenco fornito. Questa funzione è progettata per supportare scenari in cui un'applicazione deve connettersi a qualsiasi host disponibile in un elenco di potenziali host.

Analogamente a [**WSAConnectByName,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)la funzione [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) riduce significativamente il codice sorgente necessario per creare, associare e connettere un socket. Questa funzione rende molto più semplice implementare un'applicazione indipendente dalla versione IP. L'elenco di indirizzi per un host accettato da questa funzione può essere indirizzi IPv6 o IPv4.

Per consentire il pass di indirizzi IPv6 e IPv4 nel singolo elenco di indirizzi accettato dalla funzione, è necessario eseguire i passaggi seguenti prima di chiamare la funzione :

-   La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere chiamata su un socket creato per la famiglia di indirizzi AF INET6 per disabilitare l'opzione socket \_ **IPV6 \_ V6ONLY** prima di chiamare [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist). A tale scopo, chiamare la funzione **setsockopt** nel socket con il parametro *level* impostato su **IPPROTO \_ IPV6** (vedere [Opzioni socket \_ IPV6 IPPROTO),](ipproto-ipv6-socket-options.md)il parametro *optname* impostato su **IPV6 \_ V6ONLY** e il valore del parametro *optvalue* impostato su zero.
-   Tutti gli indirizzi IPv4 devono essere rappresentati nel formato di indirizzo IPv6 mappato IPv4 che consente a un'applicazione solo IPv6 di comunicare con un nodo IPv4. Il formato di indirizzo IPv6 mappato a IPv4 consente all'indirizzo IPv4 di un nodo IPv4 di essere rappresentato come indirizzo IPv6. L'indirizzo IPv4 viene codificato nei 32 bit meno elevati dell'indirizzo IPv6 e i 96 bit di ordine superiore contengono il prefisso fisso 0:0:0:0:0:0:FFFF. Il formato di indirizzo IPv6 mappato a IPv4 è specificato in RFC 4291. Per altre informazioni, [vedere ](https://tools.ietf.org/html/rfc4291)www.ietf.org/rfc/rfc4291.txt. La macro IN6ADDR \_ SETV4MAPPED in *Mstcpip.h* può essere usata per convertire un indirizzo IPv4 nel formato di indirizzo IPv6 con mapping IPv4 richiesto.

Stabilire una connessione tramite [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a>getaddrinfo

La **funzione getaddrinfo** esegue anche il lavoro di elaborazione di molte funzioni. In precedenza, le chiamate a una serie di Windows Sockets erano necessarie per creare, aprire e quindi associare un indirizzo a un socket. Con la **funzione getaddrinfo,** le righe di codice sorgente necessarie per eseguire tali operazioni possono essere notevolmente ridotte. I due esempi seguenti illustrano il codice sorgente necessario per eseguire queste attività con e senza la **funzione getaddrinfo.**

Eseguire un'operazione Open, Connessione e Bind usando **getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



Eseguire un'operazione Open, Connessione e Bind senza usare **getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



Si noti che entrambi questi esempi di codice sorgente eseguono le stesse attività, ma il primo esempio, usando la funzione **getaddrinfo,** richiede meno righe di codice sorgente e può gestire indirizzi IPv6 o IPv4. Il numero di righe di codice sorgente eliminate tramite la **funzione getaddrinfo** varia.

> [!Note]  
> Nel codice sorgente di produzione l'applicazione scorre il set di indirizzi restituito dalla [**funzione gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) [**o getaddrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Questi esempi omettono questo passaggio a favore della semplicità.

 

Un altro problema che è necessario risolvere quando si modifica un'applicazione IPv4 esistente per supportare IPv6 è associato all'ordine in cui vengono chiamate le funzioni. Sia [**getaddrinfo che**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) richiedono che una sequenza di chiamate di funzione sia effettuata in un ordine specifico.

Nelle piattaforme in cui vengono usati sia IPv4 che IPv6, la famiglia di indirizzi del nome host remoto non è nota in anticipo. È quindi necessario eseguire prima la risoluzione degli indirizzi usando la funzione [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per determinare l'indirizzo IP e la famiglia di indirizzi dell'host remoto. È quindi possibile chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) per aprire un socket della famiglia di indirizzi restituita da [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo). Si tratta di una modifica importante nel modo in cui vengono scritte Windows Sockets, poiché molte applicazioni IPv4 tendono a usare un ordine diverso di chiamate di funzione.

La maggior parte delle applicazioni IPv4 crea prima un socket per la famiglia di indirizzi AF INET, quindi esegue la risoluzione dei nomi e quindi usa il socket per connettersi \_ all'indirizzo IP risolto. Quando si rende tali applicazioni compatibili con IPv6, la chiamata di funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) deve essere posticipata fino alla risoluzione del nome dopo che la famiglia di indirizzi è stata dissuasa. Si noti che se la risoluzione dei nomi restituisce entrambi gli indirizzi IPv4 e IPv6, è necessario usare socket IPv4 e IPv6 separati per connettersi a questi indirizzi di destinazione. Tutte queste complessità possono essere evitate usando la funzione [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) in Windows Vista e versioni successive, pertanto gli sviluppatori di applicazioni sono invitati a usare questa nuova funzione.

Nell'esempio di codice seguente viene illustrata la sequenza appropriata per eseguire prima la risoluzione dei nomi (eseguita<sup></sup> nella quarta riga nell'esempio di codice sorgente seguente), quindi l'apertura di un socket (eseguita nella 19° riga nell'esempio di codice seguente). Questo esempio è un estratto del file Client.c disponibile nel codice client abilitato per [IPv6](ipv6-enabled-client-code-2.md) nell'appendice B. La funzione PrintError chiamata nell'esempio di codice seguente è elencata nell'esempio Client.c.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a>Funzioni dell'helper IP

Infine, le applicazioni che usano la funzione helper IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)e la struttura associata [**IP ADAPTER \_ \_ INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)devono riconoscere che sia questa funzione che la struttura sono limitate agli indirizzi IPv4. Le sostituzioni abilitate per IPv6 per questa funzione e struttura sono la [**funzione GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e la [**struttura IP ADAPTER \_ \_ ADDRESSES.**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) Le applicazioni abilitate per IPv6 che usano l'API helper IP devono usare la **funzione GetAdaptersAddresses** e la struttura IP **ADAPTER \_ \_ ADDRESSES** corrispondente abilitata per IPv6, entrambe definite in Microsoft Windows Software Development Kit (SDK).

## <a name="recommendations"></a>Consigli

L'approccio migliore per garantire che l'applicazione usi chiamate di funzione compatibili con IPv6 consiste nell'usare la [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per ottenere la conversione da host a indirizzo. A partire da Windows XP, la **funzione getaddrinfo** rende superflua la funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) e l'applicazione deve pertanto usare la **funzione getaddrinfo** per i progetti di programmazione futuri. Anche se Microsoft continuerà a **supportare gethostbyname,** questa funzione non verrà estesa per supportare IPv6. Per il supporto trasparente per ottenere informazioni sugli host IPv6 e IPv4, è necessario usare **getaddrinfo**.

L'esempio seguente illustra come usare al meglio **la funzione getaddrinfo.** Si noti che la funzione, se usata correttamente come illustrato in questo esempio, gestisce correttamente la conversione da host a indirizzo IPv6 e IPv4, ma ottiene anche altre informazioni utili sull'host, ad esempio il tipo di socket supportati. Questo esempio è un estratto dell'esempio Client.c disponibile nell'appendice B.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> La versione della [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che supporta IPv6 è una novità Windows versione XP di Windows.

 

Codice da evitare

La conversione degli indirizzi host è stata tradizionalmente ottenuta [**usando la funzione gethostbyname.**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) A partire da Windows XP:

-   La **funzione getaddrinfo** rende obsoleta **la funzione gethostbyname.**
-   Le applicazioni devono usare **la funzione getaddrinfo** anziché **la funzione gethostbyname.**

Attività di codifica

**Per modificare un'applicazione IPv4 esistente per aggiungere il supporto per IPv6**

1.  Acquisire l'Checkv4.exe di installazione. Questa utilità viene installata come parte di Windows SDK. L Windows SDK è disponibile tramite una sottoscrizione MSDN e può essere scaricato anche dal sito Web Microsoft ( https://msdn.microsoft.com) . Una versione precedente dello strumento *Checkv4.exe* è stata inclusa anche come parte di Microsoft IPv6 Technology Preview per Windows 2000.
2.  Eseguire *l'utilitàCheckv4.exe* sul codice. Vedere [Uso dell'utilità Checkv4.exe per](using-the-checkv4-exe-utility-2.md) informazioni sull'esecuzione dell'utilità della versione sui file.
3.  L'utilità segnala l'utilizzo di [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e altre funzioni solo IPv4 e fornisce indicazioni su come sostituirle con la funzione compatibile con IPv6, ad esempio [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).
4.  Sostituire le istanze della **funzione gethostbyname** e il codice associato in base alle esigenze, con la **funzione getaddrinfo.** In Windows Vista usare la [**funzione WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) o [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) quando appropriato.
5.  Sostituire le istanze della [**funzione gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e il codice associato in base alle esigenze, con la [**funzione getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)

In alternativa, è possibile cercare nella codebase le istanze delle funzioni **gethostbyname** e [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e modificare tutto questo utilizzo (e altro codice associato, in base alle esigenze) con le funzioni **getaddrinfo** [**e getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture dei dati per le applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack Sockets per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Uso di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interfaccia utente problemi relativi alle applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
