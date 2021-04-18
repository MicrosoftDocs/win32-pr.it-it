---
description: Sono state introdotte nuove funzioni per l'interfaccia Windows Sockets appositamente progettate per semplificare la programmazione di Windows Sockets. Uno dei vantaggi di queste nuove funzioni di Windows Sockets è il supporto integrato sia per IPv6 che per IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Chiamate di funzione per applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306979"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>Chiamate di funzione per applicazioni Winsock IPv6

Sono state introdotte nuove funzioni per l'interfaccia Windows Sockets appositamente progettate per semplificare la programmazione di Windows Sockets. Uno dei vantaggi di queste nuove funzioni di Windows Sockets è il supporto integrato sia per IPv6 che per IPv4.

Di seguito sono riportate le nuove funzioni Windows Sockets:

-   [**Con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   famiglia di funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**funzione getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**FreeAddrInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)e [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) della famiglia di funzioni (**GetNameInfo** e [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

Sono state inoltre aggiunte nuove funzioni helper IP con supporto per IPv6 e IPv4 per semplificare la programmazione di Windows Sockets. Di seguito sono riportate le nuove funzioni di supporto IP:

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Quando si aggiunge il supporto IPv6 a un'applicazione, è necessario utilizzare le seguenti linee guida:

-   Usare [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) per stabilire una connessione a un endpoint dato un nome host e una porta. La funzione **con WSAConnectByName** è disponibile in Windows Vista e versioni successive.
-   Utilizzare [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) per stabilire una connessione a un'uscita da una raccolta di possibili endpoint rappresentati da un set di indirizzi di destinazione (nomi host e porte). La funzione **WSAConnectByList** è disponibile in Windows Vista e versioni successive.
-   Sostituire le chiamate di funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) con chiamate a una delle nuove funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets. La funzione **funzione getaddrinfo** con supporto per il protocollo IPv6 è disponibile in Windows XP e versioni successive. Il protocollo IPv6 è supportato anche in Windows 2000 quando viene installata l'anteprima della tecnologia IPv6 per Windows 2000.
-   Sostituire le chiamate di funzione [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) con chiamate a una delle nuove funzioni [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets. La funzione **GetNameInfo** con supporto per il protocollo IPv6 è disponibile in Windows XP e versioni successive. Il protocollo IPv6 è supportato anche in Windows 2000 quando viene installata l'anteprima della tecnologia IPv6 per Windows 2000.

## <a name="wsaconnectbyname"></a>Con WSAConnectByName

La funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) semplifica la connessione a un endpoint usando un socket basato sul flusso, dato il nome host o l'indirizzo IP della destinazione (IPv4 o IPv6). Questa funzione riduce il codice sorgente necessario per creare un'applicazione IP indipendente dalla versione del protocollo IP usato. **Con WSAConnectByName** sostituisce i passaggi seguenti in un'applicazione TCP tipica a una singola chiamata di funzione:

-   Risolvere un nome host in un set di indirizzi IP.
-   Per ogni indirizzo IP:
    -   Creare un socket della famiglia di indirizzi appropriata.
    -   Tenta di connettersi all'indirizzo IP remoto. Se la connessione ha avuto esito positivo, restituisce; in caso contrario, viene eseguito un tentativo con l'indirizzo IP remoto successivo per l'host.

La funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va oltre la semplice risoluzione del nome e il tentativo di connessione. La funzione utilizza tutti gli indirizzi remoti restituiti dalla risoluzione dei nomi e tutti gli indirizzi IP di origine del computer locale. Tenta innanzitutto di connettersi utilizzando le coppie di indirizzi con la massima probabilità di successo. Pertanto, **con WSAConnectByName** non solo garantisce che venga stabilita una connessione, se possibile, ma riduce anche il tempo necessario per stabilire la connessione.

Per abilitare le comunicazioni sia IPv6 che IPv4, usare il metodo seguente:

-   La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere chiamata su un socket creato per la \_ famiglia di indirizzi AF INET6 per disabilitare l'opzione socket **\_ V6ONLY di IPv6** prima di chiamare [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea). Questa operazione viene eseguita chiamando la funzione **setsockopt** sul socket con il parametro *level* impostato su **IPPROTO \_ IPv6** (vedere [ \_ opzioni socket IPv6 IPPROTO](ipproto-ipv6-socket-options.md)), il parametro *optname* impostato su **IPv6 \_ V6ONLY** e il valore del parametro *optvalue* impostato su zero.

Se un'applicazione deve essere associata a una porta o a un indirizzo locale specifico, non è possibile usare [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) perché il parametro socket per **con WSAConnectByName** deve essere un socket non associato.

Nell'esempio di codice riportato di seguito vengono illustrate solo alcune righe di codice necessarie per utilizzare questa funzione per implementare un'applicazione indipendente dalla versione IP.

Stabilire una connessione tramite [ **con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


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

La funzione [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) stabilisce una connessione a un host in base a un set di possibili host, rappresentato da un set di porte e indirizzi IP di destinazione. La funzione accetta tutti gli indirizzi IP e le porte per l'endpoint e tutti gli indirizzi IP del computer locale e tenta una connessione utilizzando tutte le combinazioni di indirizzi possibili.

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) è correlato alla funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) . Anziché assumere un solo nome host, **WSAConnectByList** accetta un elenco di host (indirizzi di destinazione e coppie di porte) e si connette a uno degli indirizzi e delle porte nell'elenco fornito. Questa funzione è progettata per supportare scenari in cui un'applicazione deve connettersi a qualsiasi host disponibile da un elenco di potenziali host.

Analogamente a [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), la funzione [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) riduce significativamente il codice sorgente necessario per creare, associare e connettere un socket. Questa funzione rende molto più semplice implementare un'applicazione indipendente dalla versione IP. L'elenco di indirizzi per un host accettato da questa funzione può essere indirizzi IPv6 o IPv4.

Per consentire il passaggio di indirizzi IPv6 e IPv4 nell'elenco di indirizzi singolo accettato dalla funzione, è necessario eseguire i passaggi seguenti prima di chiamare la funzione:

-   La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere chiamata su un socket creato per la \_ famiglia di indirizzi AF INET6 per disabilitare l'opzione socket **\_ V6ONLY di IPv6** prima di chiamare [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist). Questa operazione viene eseguita chiamando la funzione **setsockopt** sul socket con il parametro *level* impostato su **IPPROTO \_ IPv6** (vedere [ \_ opzioni socket IPv6 IPPROTO](ipproto-ipv6-socket-options.md)), il parametro *optname* impostato su **IPv6 \_ V6ONLY** e il valore del parametro *optvalue* impostato su zero.
-   Tutti gli indirizzi IPv4 devono essere rappresentati nel formato di indirizzo IPv6 mappato IPv4, che consente a un'applicazione solo IPv6 di comunicare con un nodo IPv4. Il formato di indirizzo IPv6 con mapping IPv4 consente di rappresentare l'indirizzo IPv4 di un nodo IPv4 come indirizzo IPv6. L'indirizzo IPv4 è codificato nei bit 32 di ordine inferiore dell'indirizzo IPv6 e i 96 bit di ordine superiore contengono il prefisso fisso 0:0: 0:0: 0: FFFF. Il formato di indirizzo IPv6 mappato a IPv4 è specificato nella RFC 4291. Per ulteriori informazioni, vedere [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La \_ macro IN6ADDR SETV4MAPPED in *MSTCPIP. h* può essere utilizzata per convertire un indirizzo IPv4 nel formato di indirizzo IPv6 con mapping IPv4 richiesto.

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



## <a name="getaddrinfo"></a>funzione getaddrinfo

La funzione **funzione getaddrinfo** esegue anche il lavoro di elaborazione di molte funzioni. In precedenza, le chiamate a una serie di funzioni di Windows Socket erano necessarie per creare, aprire e quindi associare un indirizzo a un socket. Con la funzione **funzione getaddrinfo** , le righe del codice sorgente necessarie per eseguire tale operazione possono essere notevolmente ridotte. Nei due esempi seguenti viene illustrato il codice sorgente necessario per eseguire queste attività con e senza la funzione **funzione getaddrinfo** .

Eseguire un'apertura, una connessione e un'associazione usando **funzione getaddrinfo**


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



Eseguire un'apertura, una connessione e un'associazione senza usare **funzione getaddrinfo**


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



Si noti che entrambi gli esempi di codice sorgente eseguono le stesse attività, ma il primo esempio, usando la funzione **funzione getaddrinfo** , richiede un minor numero di righe di codice sorgente e può gestire indirizzi IPv6 o IPv4. Il numero di righe di codice sorgente eliminate tramite la funzione **funzione getaddrinfo** varia.

> [!Note]  
> Nel codice sorgente di produzione, l'applicazione scorre il set di indirizzi restituito dalla funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) o [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . In questi esempi viene omesso il passaggio a favore della semplicità.

 

Un altro problema da affrontare quando si modifica un'applicazione IPv4 esistente per il supporto di IPv6 è associato all'ordine in cui le funzioni vengono chiamate. Sia [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) richiedono che una sequenza di chiamate di funzione venga eseguita in un ordine specifico.

Nelle piattaforme in cui vengono utilizzati sia IPv4 che IPv6, la famiglia di indirizzi del nome host remoto non è nota in anticipo. Pertanto, è necessario eseguire prima la risoluzione degli indirizzi utilizzando la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per determinare l'indirizzo IP e la famiglia di indirizzi dell'host remoto. È quindi possibile chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) per aprire un socket della famiglia di indirizzi restituita da [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo). Si tratta di una modifica importante nel modo in cui vengono scritte le applicazioni Windows Sockets, poiché molte applicazioni IPv4 tendono a usare un ordine diverso per le chiamate di funzione.

La maggior parte delle applicazioni IPv4 crea prima un socket per la \_ famiglia di indirizzi AF inet, quindi esegue la risoluzione dei nomi e quindi usa il socket per connettersi all'indirizzo IP risolto. Quando queste applicazioni sono in grado di supportare IPv6, è necessario ritardare la chiamata di funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) fino al termine della risoluzione dei nomi quando la famiglia di indirizzi è stata deteremined. Si noti che se la risoluzione dei nomi restituisce indirizzi IPv4 e IPv6, per la connessione a questi indirizzi di destinazione devono essere utilizzati socket IPv4 e IPv6 distinti. È possibile evitare tutte queste complessità utilizzando la funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) in Windows Vista e versioni successive, in modo che gli sviluppatori di applicazioni siano invitati a utilizzare questa nuova funzione.

Nell'esempio di codice seguente viene illustrata la sequenza corretta per eseguire prima la risoluzione dei nomi (eseguita nella quarta riga nell'esempio di codice sorgente seguente), quindi aprendo un socket (eseguito<sup>nella riga 19</sup> dell'esempio di codice seguente). Questo esempio è un estratto dal file client. c trovato nel [codice client abilitato per IPv6](ipv6-enabled-client-code-2.md) nell'Appendice B. La funzione PrintError chiamata nell'esempio di codice seguente è elencata nell'esempio client. c.


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

Infine, le applicazioni che usano la funzione helper IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)e le informazioni relative alla [**\_ scheda \_ IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)della struttura associata devono riconoscere che la funzione e la struttura sono limitate agli indirizzi IPv4. Le sostituzioni abilitate per IPv6 per questa funzione e struttura sono la funzione [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e la struttura degli [**\_ \_ indirizzi degli adapter IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) . Le applicazioni abilitate per IPv6 che usano l'API helper IP devono usare la funzione **GetAdaptersAddresses** e la struttura di **\_ \_ indirizzi IP** abilitata per IPv6 corrispondente, entrambe definite nel Software Development Kit (SDK) di Microsoft Windows.

## <a name="recommendations"></a>Consigli

L'approccio migliore per garantire che l'applicazione usi chiamate di funzione compatibili con IPv6 consiste nell'usare la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per ottenere la traduzione da host a indirizzo. A partire da Windows XP, la funzione **funzione getaddrinfo** rende superflua la funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) e quindi l'applicazione deve utilizzare la funzione **funzione getaddrinfo** per progetti di programmazione futuri. Sebbene Microsoft continuerà a supportare **gethostbyname**, questa funzione non verrà estesa per supportare IPv6. Per il supporto trasparente per ottenere informazioni sull'host IPv4 e IPv6, è necessario usare **funzione getaddrinfo**.

Nell'esempio seguente viene illustrato come utilizzare al meglio la funzione **funzione getaddrinfo** . Si noti che la funzione, se utilizzata correttamente come illustrato in questo esempio, gestisce correttamente la conversione da host a indirizzo IPv6 e IPv4, ma ottiene anche altre informazioni utili sull'host, ad esempio il tipo di socket supportati. Questo esempio è un estratto dall'esempio client. c disponibile nell'Appendice B.


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
> La versione della funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che supporta IPv6 è una novità per la versione Windows XP di Windows.

 

Codice da evitare

La conversione degli indirizzi host è stata eseguita tradizionalmente tramite la funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) . A partire da Windows XP:

-   La funzione **funzione getaddrinfo** rende obsoleta la funzione **gethostbyname** .
-   Le applicazioni devono usare la funzione **funzione getaddrinfo** invece della funzione **gethostbyname** .

Attività di codifica

**Per modificare un'applicazione IPv4 esistente per aggiungere il supporto per IPv6**

1.  Acquisire l'utilità Checkv4.exe. Questa utilità viene installata come parte del Windows SDK. Il Windows SDK è disponibile tramite un abbonamento MSDN e può essere scaricato anche dal sito Web Microsoft ( https://msdn.microsoft.com) . Una versione precedente dello strumento *Checkv4.exe* era inclusa anche come parte di Microsoft IPv6 Technology Preview per Windows 2000.
2.  Eseguire l'utilità *Checkv4.exe* sul codice. Per informazioni sull'esecuzione dell'utilità di versione nei file, vedere [uso dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md) .
3.  Tramite l'utilità viene visualizzato un avviso per l'utilizzo di [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e altre funzioni solo IPv4 e vengono fornite indicazioni su come sostituirli con la funzione compatibile con IPv6, ad esempio [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).
4.  Sostituire tutte le istanze della funzione **gethostbyname** e il codice associato in modo appropriato con la funzione **funzione getaddrinfo** . In Windows Vista, utilizzare la funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) o [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) quando appropriato.
5.  Sostituire tutte le istanze della funzione [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e il codice associato in modo appropriato con la funzione [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

In alternativa, è possibile eseguire una ricerca nella codebase per le istanze delle funzioni **gethostbyname** e [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e modificare tutto questo utilizzo (e altro codice associato, a seconda delle esigenze) per le funzioni **funzione getaddrinfo** e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture di dati per applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Socket dual stack per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Utilizzo di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemi dell'interfaccia utente per le applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
