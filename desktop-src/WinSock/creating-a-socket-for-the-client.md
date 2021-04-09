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
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="f671c-103">Creazione di un socket per il client</span><span class="sxs-lookup"><span data-stu-id="f671c-103">Creating a socket for the client</span></span>

<span data-ttu-id="f671c-104">Dopo l'inizializzazione, è necessario creare un'istanza di un oggetto **socket** per l'uso da parte del client.</span><span class="sxs-lookup"><span data-stu-id="f671c-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="f671c-105">**Per creare un socket**</span><span class="sxs-lookup"><span data-stu-id="f671c-105">**To create a socket**</span></span>

1.  <span data-ttu-id="f671c-106">Dichiarare un oggetto [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) che contiene una struttura [**sockaddr**](sockaddr-2.md) e inizializzare questi valori.</span><span class="sxs-lookup"><span data-stu-id="f671c-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="f671c-107">Per questa applicazione, la famiglia di indirizzi Internet non è specificata in modo che sia possibile restituire un indirizzo IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="f671c-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="f671c-108">L'applicazione richiede che il tipo di socket sia un socket di flusso per il protocollo TCP.</span><span class="sxs-lookup"><span data-stu-id="f671c-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="f671c-109">Chiamare la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che richiede l'indirizzo IP per il nome del server passato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f671c-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="f671c-110">La porta TCP sul server a cui il client si connetterà viene definita per impostazione predefinita \_ come 27015 in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="f671c-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="f671c-111">La funzione **funzione getaddrinfo** restituisce il relativo valore come intero che viene controllato per verificare la presenza di errori.</span><span class="sxs-lookup"><span data-stu-id="f671c-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
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

    

3.  <span data-ttu-id="f671c-112">Creare un oggetto **socket** denominato ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="f671c-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="f671c-113">Chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e restituire il relativo valore alla variabile ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="f671c-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="f671c-114">Per questa applicazione, usare il primo indirizzo IP restituito dalla chiamata a [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che corrisponde alla famiglia di indirizzi, al tipo di socket e al protocollo specificati nel parametro *hints* .</span><span class="sxs-lookup"><span data-stu-id="f671c-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="f671c-115">In questo esempio è stato specificato un socket del flusso TCP con un tipo di socket del flusso di SOCK \_ e un protocollo di IPPROTO \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="f671c-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="f671c-116">La famiglia di indirizzi non è stata specificata (AF \_ UNspecte), quindi l'indirizzo IP restituito può essere un indirizzo IPv6 o IPv4 per il server.</span><span class="sxs-lookup"><span data-stu-id="f671c-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="f671c-117">Se l'applicazione client desidera connettersi usando solo IPv6 o IPv4, la famiglia di indirizzi deve essere impostata su AF \_ INET6 per IPv6 o AF \_ inet per IPv4 nel parametro *hints* .</span><span class="sxs-lookup"><span data-stu-id="f671c-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="f671c-118">Verificare la presenza di errori per verificare che il socket sia un socket valido.</span><span class="sxs-lookup"><span data-stu-id="f671c-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="f671c-119">I parametri passati alla funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) possono essere modificati per implementazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="f671c-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="f671c-120">Il rilevamento degli errori è una parte fondamentale del codice di rete corretto.</span><span class="sxs-lookup"><span data-stu-id="f671c-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="f671c-121">Se la chiamata al [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) non riesce, viene restituito un socket non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="f671c-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="f671c-122">L'istruzione **if** del codice precedente viene utilizzata per intercettare eventuali errori che si sono verificati durante la creazione del socket.</span><span class="sxs-lookup"><span data-stu-id="f671c-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="f671c-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce un numero di errore associato all'ultimo errore che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="f671c-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="f671c-124">Potrebbe essere necessario un controllo degli errori più ampio a seconda dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f671c-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="f671c-125">Ad esempio, l'impostazione di *hints.ai_family* su **AF_UNSPEC** può causare l'esito negativo della chiamata Connect.</span><span class="sxs-lookup"><span data-stu-id="f671c-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="f671c-126">In tal caso, usare invece un valore IPv4 (**AF_INET**) o IPv6 (**AF_INET6**) specifico.</span><span class="sxs-lookup"><span data-stu-id="f671c-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="f671c-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) viene usato per terminare l'uso della DLL WS2 \_ 32.</span><span class="sxs-lookup"><span data-stu-id="f671c-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="f671c-128">Passaggio successivo: [connessione a un socket](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="f671c-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f671c-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f671c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f671c-130">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="f671c-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="f671c-131">Inizializzazione di Winsock</span><span class="sxs-lookup"><span data-stu-id="f671c-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="f671c-132">Applicazione client Winsock</span><span class="sxs-lookup"><span data-stu-id="f671c-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 
