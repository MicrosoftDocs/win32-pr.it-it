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
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="6889f-104">Chiamate di funzione per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="6889f-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="6889f-105">Sono state introdotte nuove funzioni per l'interfaccia Windows Sockets appositamente progettate per semplificare la programmazione di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="6889f-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="6889f-106">Uno dei vantaggi di queste nuove funzioni di Windows Sockets è il supporto integrato sia per IPv6 che per IPv4.</span><span class="sxs-lookup"><span data-stu-id="6889f-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="6889f-107">Di seguito sono riportate le nuove funzioni Windows Sockets:</span><span class="sxs-lookup"><span data-stu-id="6889f-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="6889f-108">**Con WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="6889f-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="6889f-109">**WSAConnectByList**</span><span class="sxs-lookup"><span data-stu-id="6889f-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="6889f-110">famiglia di funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**funzione getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**FreeAddrInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)e [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span><span class="sxs-lookup"><span data-stu-id="6889f-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="6889f-111">[**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) della famiglia di funzioni (**GetNameInfo** e [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span><span class="sxs-lookup"><span data-stu-id="6889f-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="6889f-112">Sono state inoltre aggiunte nuove funzioni helper IP con supporto per IPv6 e IPv4 per semplificare la programmazione di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="6889f-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="6889f-113">Di seguito sono riportate le nuove funzioni di supporto IP:</span><span class="sxs-lookup"><span data-stu-id="6889f-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="6889f-114">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="6889f-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="6889f-115">Quando si aggiunge il supporto IPv6 a un'applicazione, è necessario utilizzare le seguenti linee guida:</span><span class="sxs-lookup"><span data-stu-id="6889f-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="6889f-116">Usare [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) per stabilire una connessione a un endpoint dato un nome host e una porta.</span><span class="sxs-lookup"><span data-stu-id="6889f-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="6889f-117">La funzione **con WSAConnectByName** è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6889f-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="6889f-118">Utilizzare [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) per stabilire una connessione a un'uscita da una raccolta di possibili endpoint rappresentati da un set di indirizzi di destinazione (nomi host e porte).</span><span class="sxs-lookup"><span data-stu-id="6889f-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="6889f-119">La funzione **WSAConnectByList** è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6889f-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="6889f-120">Sostituire le chiamate di funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) con chiamate a una delle nuove funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="6889f-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="6889f-121">La funzione **funzione getaddrinfo** con supporto per il protocollo IPv6 è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6889f-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="6889f-122">Il protocollo IPv6 è supportato anche in Windows 2000 quando viene installata l'anteprima della tecnologia IPv6 per Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6889f-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="6889f-123">Sostituire le chiamate di funzione [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) con chiamate a una delle nuove funzioni [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="6889f-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="6889f-124">La funzione **GetNameInfo** con supporto per il protocollo IPv6 è disponibile in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6889f-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="6889f-125">Il protocollo IPv6 è supportato anche in Windows 2000 quando viene installata l'anteprima della tecnologia IPv6 per Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6889f-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="6889f-126">Con WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="6889f-126">WSAConnectByName</span></span>

<span data-ttu-id="6889f-127">La funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) semplifica la connessione a un endpoint usando un socket basato sul flusso, dato il nome host o l'indirizzo IP della destinazione (IPv4 o IPv6).</span><span class="sxs-lookup"><span data-stu-id="6889f-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="6889f-128">Questa funzione riduce il codice sorgente necessario per creare un'applicazione IP indipendente dalla versione del protocollo IP usato.</span><span class="sxs-lookup"><span data-stu-id="6889f-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="6889f-129">**Con WSAConnectByName** sostituisce i passaggi seguenti in un'applicazione TCP tipica a una singola chiamata di funzione:</span><span class="sxs-lookup"><span data-stu-id="6889f-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="6889f-130">Risolvere un nome host in un set di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="6889f-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="6889f-131">Per ogni indirizzo IP:</span><span class="sxs-lookup"><span data-stu-id="6889f-131">For each IP address:</span></span>
    -   <span data-ttu-id="6889f-132">Creare un socket della famiglia di indirizzi appropriata.</span><span class="sxs-lookup"><span data-stu-id="6889f-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="6889f-133">Tenta di connettersi all'indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="6889f-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="6889f-134">Se la connessione ha avuto esito positivo, restituisce; in caso contrario, viene eseguito un tentativo con l'indirizzo IP remoto successivo per l'host.</span><span class="sxs-lookup"><span data-stu-id="6889f-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="6889f-135">La funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) va oltre la semplice risoluzione del nome e il tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="6889f-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="6889f-136">La funzione utilizza tutti gli indirizzi remoti restituiti dalla risoluzione dei nomi e tutti gli indirizzi IP di origine del computer locale.</span><span class="sxs-lookup"><span data-stu-id="6889f-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="6889f-137">Tenta innanzitutto di connettersi utilizzando le coppie di indirizzi con la massima probabilità di successo.</span><span class="sxs-lookup"><span data-stu-id="6889f-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="6889f-138">Pertanto, **con WSAConnectByName** non solo garantisce che venga stabilita una connessione, se possibile, ma riduce anche il tempo necessario per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="6889f-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="6889f-139">Per abilitare le comunicazioni sia IPv6 che IPv4, usare il metodo seguente:</span><span class="sxs-lookup"><span data-stu-id="6889f-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="6889f-140">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere chiamata su un socket creato per la \_ famiglia di indirizzi AF INET6 per disabilitare l'opzione socket **\_ V6ONLY di IPv6** prima di chiamare [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span><span class="sxs-lookup"><span data-stu-id="6889f-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="6889f-141">Questa operazione viene eseguita chiamando la funzione **setsockopt** sul socket con il parametro *level* impostato su **IPPROTO \_ IPv6** (vedere [ \_ opzioni socket IPv6 IPPROTO](ipproto-ipv6-socket-options.md)), il parametro *optname* impostato su **IPv6 \_ V6ONLY** e il valore del parametro *optvalue* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="6889f-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="6889f-142">Se un'applicazione deve essere associata a una porta o a un indirizzo locale specifico, non è possibile usare [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) perché il parametro socket per **con WSAConnectByName** deve essere un socket non associato.</span><span class="sxs-lookup"><span data-stu-id="6889f-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="6889f-143">Nell'esempio di codice riportato di seguito vengono illustrate solo alcune righe di codice necessarie per utilizzare questa funzione per implementare un'applicazione indipendente dalla versione IP.</span><span class="sxs-lookup"><span data-stu-id="6889f-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="6889f-144">Stabilire una connessione tramite [ **con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="6889f-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


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



## <a name="wsaconnectbylist"></a><span data-ttu-id="6889f-145">WSAConnectByList</span><span class="sxs-lookup"><span data-stu-id="6889f-145">WSAConnectByList</span></span>

<span data-ttu-id="6889f-146">La funzione [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) stabilisce una connessione a un host in base a un set di possibili host, rappresentato da un set di porte e indirizzi IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6889f-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="6889f-147">La funzione accetta tutti gli indirizzi IP e le porte per l'endpoint e tutti gli indirizzi IP del computer locale e tenta una connessione utilizzando tutte le combinazioni di indirizzi possibili.</span><span class="sxs-lookup"><span data-stu-id="6889f-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="6889f-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) è correlato alla funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) .</span><span class="sxs-lookup"><span data-stu-id="6889f-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="6889f-149">Anziché assumere un solo nome host, **WSAConnectByList** accetta un elenco di host (indirizzi di destinazione e coppie di porte) e si connette a uno degli indirizzi e delle porte nell'elenco fornito.</span><span class="sxs-lookup"><span data-stu-id="6889f-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="6889f-150">Questa funzione è progettata per supportare scenari in cui un'applicazione deve connettersi a qualsiasi host disponibile da un elenco di potenziali host.</span><span class="sxs-lookup"><span data-stu-id="6889f-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="6889f-151">Analogamente a [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), la funzione [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) riduce significativamente il codice sorgente necessario per creare, associare e connettere un socket.</span><span class="sxs-lookup"><span data-stu-id="6889f-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="6889f-152">Questa funzione rende molto più semplice implementare un'applicazione indipendente dalla versione IP.</span><span class="sxs-lookup"><span data-stu-id="6889f-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="6889f-153">L'elenco di indirizzi per un host accettato da questa funzione può essere indirizzi IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="6889f-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="6889f-154">Per consentire il passaggio di indirizzi IPv6 e IPv4 nell'elenco di indirizzi singolo accettato dalla funzione, è necessario eseguire i passaggi seguenti prima di chiamare la funzione:</span><span class="sxs-lookup"><span data-stu-id="6889f-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="6889f-155">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere chiamata su un socket creato per la \_ famiglia di indirizzi AF INET6 per disabilitare l'opzione socket **\_ V6ONLY di IPv6** prima di chiamare [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span><span class="sxs-lookup"><span data-stu-id="6889f-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="6889f-156">Questa operazione viene eseguita chiamando la funzione **setsockopt** sul socket con il parametro *level* impostato su **IPPROTO \_ IPv6** (vedere [ \_ opzioni socket IPv6 IPPROTO](ipproto-ipv6-socket-options.md)), il parametro *optname* impostato su **IPv6 \_ V6ONLY** e il valore del parametro *optvalue* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="6889f-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="6889f-157">Tutti gli indirizzi IPv4 devono essere rappresentati nel formato di indirizzo IPv6 mappato IPv4, che consente a un'applicazione solo IPv6 di comunicare con un nodo IPv4.</span><span class="sxs-lookup"><span data-stu-id="6889f-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="6889f-158">Il formato di indirizzo IPv6 con mapping IPv4 consente di rappresentare l'indirizzo IPv4 di un nodo IPv4 come indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="6889f-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="6889f-159">L'indirizzo IPv4 è codificato nei bit 32 di ordine inferiore dell'indirizzo IPv6 e i 96 bit di ordine superiore contengono il prefisso fisso 0:0: 0:0: 0: FFFF.</span><span class="sxs-lookup"><span data-stu-id="6889f-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="6889f-160">Il formato di indirizzo IPv6 mappato a IPv4 è specificato nella RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="6889f-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="6889f-161">Per ulteriori informazioni, vedere [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span><span class="sxs-lookup"><span data-stu-id="6889f-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="6889f-162">La \_ macro IN6ADDR SETV4MAPPED in *MSTCPIP. h* può essere utilizzata per convertire un indirizzo IPv4 nel formato di indirizzo IPv6 con mapping IPv4 richiesto.</span><span class="sxs-lookup"><span data-stu-id="6889f-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="6889f-163">Stabilire una connessione tramite [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="6889f-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


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



## <a name="getaddrinfo"></a><span data-ttu-id="6889f-164">funzione getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="6889f-164">getaddrinfo</span></span>

<span data-ttu-id="6889f-165">La funzione **funzione getaddrinfo** esegue anche il lavoro di elaborazione di molte funzioni.</span><span class="sxs-lookup"><span data-stu-id="6889f-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="6889f-166">In precedenza, le chiamate a una serie di funzioni di Windows Socket erano necessarie per creare, aprire e quindi associare un indirizzo a un socket.</span><span class="sxs-lookup"><span data-stu-id="6889f-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="6889f-167">Con la funzione **funzione getaddrinfo** , le righe del codice sorgente necessarie per eseguire tale operazione possono essere notevolmente ridotte.</span><span class="sxs-lookup"><span data-stu-id="6889f-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="6889f-168">Nei due esempi seguenti viene illustrato il codice sorgente necessario per eseguire queste attività con e senza la funzione **funzione getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="6889f-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="6889f-169">Eseguire un'apertura, una connessione e un'associazione usando **funzione getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="6889f-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


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



<span data-ttu-id="6889f-170">Eseguire un'apertura, una connessione e un'associazione senza usare **funzione getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="6889f-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


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



<span data-ttu-id="6889f-171">Si noti che entrambi gli esempi di codice sorgente eseguono le stesse attività, ma il primo esempio, usando la funzione **funzione getaddrinfo** , richiede un minor numero di righe di codice sorgente e può gestire indirizzi IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="6889f-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="6889f-172">Il numero di righe di codice sorgente eliminate tramite la funzione **funzione getaddrinfo** varia.</span><span class="sxs-lookup"><span data-stu-id="6889f-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="6889f-173">Nel codice sorgente di produzione, l'applicazione scorre il set di indirizzi restituito dalla funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) o [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="6889f-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="6889f-174">In questi esempi viene omesso il passaggio a favore della semplicità.</span><span class="sxs-lookup"><span data-stu-id="6889f-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="6889f-175">Un altro problema da affrontare quando si modifica un'applicazione IPv4 esistente per il supporto di IPv6 è associato all'ordine in cui le funzioni vengono chiamate.</span><span class="sxs-lookup"><span data-stu-id="6889f-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="6889f-176">Sia [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) richiedono che una sequenza di chiamate di funzione venga eseguita in un ordine specifico.</span><span class="sxs-lookup"><span data-stu-id="6889f-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="6889f-177">Nelle piattaforme in cui vengono utilizzati sia IPv4 che IPv6, la famiglia di indirizzi del nome host remoto non è nota in anticipo.</span><span class="sxs-lookup"><span data-stu-id="6889f-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="6889f-178">Pertanto, è necessario eseguire prima la risoluzione degli indirizzi utilizzando la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per determinare l'indirizzo IP e la famiglia di indirizzi dell'host remoto.</span><span class="sxs-lookup"><span data-stu-id="6889f-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="6889f-179">È quindi possibile chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) per aprire un socket della famiglia di indirizzi restituita da [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span><span class="sxs-lookup"><span data-stu-id="6889f-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="6889f-180">Si tratta di una modifica importante nel modo in cui vengono scritte le applicazioni Windows Sockets, poiché molte applicazioni IPv4 tendono a usare un ordine diverso per le chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="6889f-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="6889f-181">La maggior parte delle applicazioni IPv4 crea prima un socket per la \_ famiglia di indirizzi AF inet, quindi esegue la risoluzione dei nomi e quindi usa il socket per connettersi all'indirizzo IP risolto.</span><span class="sxs-lookup"><span data-stu-id="6889f-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="6889f-182">Quando queste applicazioni sono in grado di supportare IPv6, è necessario ritardare la chiamata di funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) fino al termine della risoluzione dei nomi quando la famiglia di indirizzi è stata deteremined.</span><span class="sxs-lookup"><span data-stu-id="6889f-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="6889f-183">Si noti che se la risoluzione dei nomi restituisce indirizzi IPv4 e IPv6, per la connessione a questi indirizzi di destinazione devono essere utilizzati socket IPv4 e IPv6 distinti.</span><span class="sxs-lookup"><span data-stu-id="6889f-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="6889f-184">È possibile evitare tutte queste complessità utilizzando la funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) in Windows Vista e versioni successive, in modo che gli sviluppatori di applicazioni siano invitati a utilizzare questa nuova funzione.</span><span class="sxs-lookup"><span data-stu-id="6889f-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="6889f-185">Nell'esempio di codice seguente viene illustrata la sequenza corretta per eseguire prima la risoluzione dei nomi (eseguita nella quarta riga nell'esempio di codice sorgente seguente), quindi aprendo un socket (eseguito<sup>nella riga 19</sup> dell'esempio di codice seguente).</span><span class="sxs-lookup"><span data-stu-id="6889f-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="6889f-186">Questo esempio è un estratto dal file client. c trovato nel [codice client abilitato per IPv6](ipv6-enabled-client-code-2.md) nell'Appendice B. La funzione PrintError chiamata nell'esempio di codice seguente è elencata nell'esempio client. c.</span><span class="sxs-lookup"><span data-stu-id="6889f-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


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



## <a name="ip-helper-functions"></a><span data-ttu-id="6889f-187">Funzioni dell'helper IP</span><span class="sxs-lookup"><span data-stu-id="6889f-187">IP Helper Functions</span></span>

<span data-ttu-id="6889f-188">Infine, le applicazioni che usano la funzione helper IP [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)e le informazioni relative alla [**\_ scheda \_ IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)della struttura associata devono riconoscere che la funzione e la struttura sono limitate agli indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="6889f-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="6889f-189">Le sostituzioni abilitate per IPv6 per questa funzione e struttura sono la funzione [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e la struttura degli [**\_ \_ indirizzi degli adapter IP**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) .</span><span class="sxs-lookup"><span data-stu-id="6889f-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="6889f-190">Le applicazioni abilitate per IPv6 che usano l'API helper IP devono usare la funzione **GetAdaptersAddresses** e la struttura di **\_ \_ indirizzi IP** abilitata per IPv6 corrispondente, entrambe definite nel Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6889f-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="6889f-191">Consigli</span><span class="sxs-lookup"><span data-stu-id="6889f-191">Recommendations</span></span>

<span data-ttu-id="6889f-192">L'approccio migliore per garantire che l'applicazione usi chiamate di funzione compatibili con IPv6 consiste nell'usare la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) per ottenere la traduzione da host a indirizzo.</span><span class="sxs-lookup"><span data-stu-id="6889f-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="6889f-193">A partire da Windows XP, la funzione **funzione getaddrinfo** rende superflua la funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) e quindi l'applicazione deve utilizzare la funzione **funzione getaddrinfo** per progetti di programmazione futuri.</span><span class="sxs-lookup"><span data-stu-id="6889f-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="6889f-194">Sebbene Microsoft continuerà a supportare **gethostbyname**, questa funzione non verrà estesa per supportare IPv6.</span><span class="sxs-lookup"><span data-stu-id="6889f-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="6889f-195">Per il supporto trasparente per ottenere informazioni sull'host IPv4 e IPv6, è necessario usare **funzione getaddrinfo**.</span><span class="sxs-lookup"><span data-stu-id="6889f-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="6889f-196">Nell'esempio seguente viene illustrato come utilizzare al meglio la funzione **funzione getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="6889f-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="6889f-197">Si noti che la funzione, se utilizzata correttamente come illustrato in questo esempio, gestisce correttamente la conversione da host a indirizzo IPv6 e IPv4, ma ottiene anche altre informazioni utili sull'host, ad esempio il tipo di socket supportati.</span><span class="sxs-lookup"><span data-stu-id="6889f-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="6889f-198">Questo esempio è un estratto dall'esempio client. c disponibile nell'Appendice B.</span><span class="sxs-lookup"><span data-stu-id="6889f-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


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
> <span data-ttu-id="6889f-199">La versione della funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che supporta IPv6 è una novità per la versione Windows XP di Windows.</span><span class="sxs-lookup"><span data-stu-id="6889f-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="6889f-200">Codice da evitare</span><span class="sxs-lookup"><span data-stu-id="6889f-200">Code to Avoid</span></span>

<span data-ttu-id="6889f-201">La conversione degli indirizzi host è stata eseguita tradizionalmente tramite la funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) .</span><span class="sxs-lookup"><span data-stu-id="6889f-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="6889f-202">A partire da Windows XP:</span><span class="sxs-lookup"><span data-stu-id="6889f-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="6889f-203">La funzione **funzione getaddrinfo** rende obsoleta la funzione **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="6889f-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="6889f-204">Le applicazioni devono usare la funzione **funzione getaddrinfo** invece della funzione **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="6889f-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="6889f-205">Attività di codifica</span><span class="sxs-lookup"><span data-stu-id="6889f-205">Coding Tasks</span></span>

<span data-ttu-id="6889f-206">**Per modificare un'applicazione IPv4 esistente per aggiungere il supporto per IPv6**</span><span class="sxs-lookup"><span data-stu-id="6889f-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="6889f-207">Acquisire l'utilità Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="6889f-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="6889f-208">Questa utilità viene installata come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6889f-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="6889f-209">Il Windows SDK è disponibile tramite un abbonamento MSDN e può essere scaricato anche dal sito Web Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="6889f-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="6889f-210">Una versione precedente dello strumento *Checkv4.exe* era inclusa anche come parte di Microsoft IPv6 Technology Preview per Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6889f-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="6889f-211">Eseguire l'utilità *Checkv4.exe* sul codice.</span><span class="sxs-lookup"><span data-stu-id="6889f-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="6889f-212">Per informazioni sull'esecuzione dell'utilità di versione nei file, vedere [uso dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md) .</span><span class="sxs-lookup"><span data-stu-id="6889f-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="6889f-213">Tramite l'utilità viene visualizzato un avviso per l'utilizzo di [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e altre funzioni solo IPv4 e vengono fornite indicazioni su come sostituirli con la funzione compatibile con IPv6, ad esempio [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span><span class="sxs-lookup"><span data-stu-id="6889f-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="6889f-214">Sostituire tutte le istanze della funzione **gethostbyname** e il codice associato in modo appropriato con la funzione **funzione getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="6889f-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="6889f-215">In Windows Vista, utilizzare la funzione [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) o [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="6889f-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="6889f-216">Sostituire tutte le istanze della funzione [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e il codice associato in modo appropriato con la funzione [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="6889f-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="6889f-217">In alternativa, è possibile eseguire una ricerca nella codebase per le istanze delle funzioni **gethostbyname** e [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) e modificare tutto questo utilizzo (e altro codice associato, a seconda delle esigenze) per le funzioni **funzione getaddrinfo** e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="6889f-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6889f-218">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6889f-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6889f-219">Guida a IPv6 per le applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6889f-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="6889f-220">Modifica delle strutture di dati per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="6889f-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="6889f-221">Socket dual stack per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="6889f-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="6889f-222">Utilizzo di indirizzi IPv4 hardcoded</span><span class="sxs-lookup"><span data-stu-id="6889f-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="6889f-223">Problemi dell'interfaccia utente per le applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="6889f-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="6889f-224">Protocolli sottostanti per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="6889f-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
