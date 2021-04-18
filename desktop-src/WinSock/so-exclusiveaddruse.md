---
description: L' \_ opzione EXCLUSIVEADDRUSE socket impedisce ad altri socket di essere associati forzatamente allo stesso indirizzo e alla stessa porta.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Opzione socket SO_EXCLUSIVEADDRUSE (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306899"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="ef1f5-103">\_Opzione socket EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="ef1f5-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="ef1f5-104">L' \_ opzione EXCLUSIVEADDRUSE socket impedisce ad altri socket di essere associati forzatamente allo stesso indirizzo e alla stessa porta.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef1f5-105">Syntax</span></span>

<span data-ttu-id="ef1f5-106">L' \_ opzione EXCLUSIVEADDRUSE impedisce ad altri socket di essere associati forzatamente allo stesso indirizzo e alla stessa porta, una pratica abilitata dall' \_ opzione socket REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="ef1f5-107">Tale riutilizzo può essere eseguito da applicazioni dannose per compromettere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="ef1f5-108">L' \_ opzione EXCLUSIVEADDRUSE è molto utile per i servizi di sistema che richiedono una disponibilità elevata.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="ef1f5-109">Nell'esempio di codice riportato di seguito viene illustrata l'impostazione di questa opzione.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-109">The following code example illustrates setting this option.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



<span data-ttu-id="ef1f5-110">Per avere un effetto, l' \_ opzione EXCLUSIVADDRUSE deve essere impostata prima di chiamare la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) (questo vale anche per l' \_ opzione REUSEADDR).</span><span class="sxs-lookup"><span data-stu-id="ef1f5-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="ef1f5-111">Nella tabella 1 sono elencati gli effetti dell'impostazione dell' \_ opzione EXCLUSIVEADDRUSE.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="ef1f5-112">Il carattere jolly indica il binding all'indirizzo jolly, ad esempio 0.0.0.0 per IPv4 e:: per IPv6.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="ef1f5-113">Specifico indica l'associazione a un'interfaccia specifica, ad esempio l'associazione di un indirizzo IP assegnato a un adapter.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="ef1f5-114">Specific2 indica l'associazione a un indirizzo specifico diverso dall'indirizzo associato a nel caso specifico.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="ef1f5-115">Il caso Specific2 è applicabile solo quando viene eseguita la prima operazione di binding con un indirizzo specifico. per il caso in cui il primo socket è associato al carattere jolly, la voce per specifico copre tutti i case di indirizzi specifici.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="ef1f5-116">Si consideri, ad esempio, un computer con due interfacce IP: 10.0.0.1 e 10.99.99.99.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="ef1f5-117">Se la prima operazione di binding è 10.0.0.1 e la porta 5150 con il set di opzioni \_ EXCLUSIVEADDRUSE, il secondo binding a 10.99.99.99 e la porta 5150 con un set di opzioni any o no ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="ef1f5-118">Tuttavia, se il primo socket è associato all'indirizzo con caratteri jolly (0.0.0.0) e alla porta 5150 con \_ EXCLUSIVEADDRUSE impostato, qualsiasi associazione successiva alla stessa porta, indipendentemente dall'indirizzo IP, avrà esito negativo con WSAEADDRINUSE (10048) o WSAEACCESS (10013), a seconda delle opzioni impostate nel secondo socket di binding.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="ef1f5-119">Associa il comportamento con varie opzioni impostate</span><span class="sxs-lookup"><span data-stu-id="ef1f5-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="ef1f5-120">Seconda associazione</span><span class="sxs-lookup"><span data-stu-id="ef1f5-120">Second bind</span></span>

<span data-ttu-id="ef1f5-121">Prima associazione</span><span class="sxs-lookup"><span data-stu-id="ef1f5-121">First bind</span></span>

<span data-ttu-id="ef1f5-122">*\_EXCLUSIVEADDRUSE*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="ef1f5-123">*Nessuna opzione* o *così \_ REUSEADDR*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="ef1f5-124">*Jolly*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-124">*Wildcard*</span></span>

<span data-ttu-id="ef1f5-125">*Specifica*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-125">*Specific*</span></span>

<span data-ttu-id="ef1f5-126">*Jolly*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-126">*Wildcard*</span></span>

<span data-ttu-id="ef1f5-127">*Specifica*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-127">*Specific*</span></span>

<span data-ttu-id="ef1f5-128">$ {ROWSPAN3} $*così \_ EXCLUSIVEADDRUSE*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ef1f5-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="ef1f5-129">*Jolly*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-129">*Wildcard*</span></span>

<span data-ttu-id="ef1f5-130">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-130">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-131">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-131">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-132">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-132">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-133">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-133">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-134">*Specifica*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-134">*Specific*</span></span>

<span data-ttu-id="ef1f5-135">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-135">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-136">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-136">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-137">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-137">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-138">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-138">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-139">*Specific2*</span></span>

<span data-ttu-id="ef1f5-140">n/d</span><span class="sxs-lookup"><span data-stu-id="ef1f5-140">n/a</span></span>

<span data-ttu-id="ef1f5-141">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-141">Success</span></span>

<span data-ttu-id="ef1f5-142">n/d</span><span class="sxs-lookup"><span data-stu-id="ef1f5-142">n/a</span></span>

<span data-ttu-id="ef1f5-143">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-143">Success</span></span>

<span data-ttu-id="ef1f5-144">$ {ROWSPAN3} $*Nessuna opzione*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ef1f5-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="ef1f5-145">*Jolly*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-145">*Wildcard*</span></span>

<span data-ttu-id="ef1f5-146">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-146">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-147">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-147">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-148">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-148">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-149">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-149">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-150">*Specifica*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-150">*Specific*</span></span>

<span data-ttu-id="ef1f5-151">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-151">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-152">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-152">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-153">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-153">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-154">Non riuscito (10048)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-154">Fail (10048)</span></span>

<span data-ttu-id="ef1f5-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-155">*Specific2*</span></span>

<span data-ttu-id="ef1f5-156">n/d</span><span class="sxs-lookup"><span data-stu-id="ef1f5-156">n/a</span></span>

<span data-ttu-id="ef1f5-157">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-157">Success</span></span>

<span data-ttu-id="ef1f5-158">n/d</span><span class="sxs-lookup"><span data-stu-id="ef1f5-158">n/a</span></span>

<span data-ttu-id="ef1f5-159">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-159">Success</span></span>

<span data-ttu-id="ef1f5-160">$ {ROWSPAN3} $*così \_ REUSEADDR*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ef1f5-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="ef1f5-161">*Jolly*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-161">*Wildcard*</span></span>

<span data-ttu-id="ef1f5-162">Non riuscito (10013)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-162">Fail (10013)</span></span>

<span data-ttu-id="ef1f5-163">Non riuscito (10013)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-163">Fail (10013)</span></span>

<span data-ttu-id="ef1f5-164">Operazione completata\*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-164">Success\*</span></span>

<span data-ttu-id="ef1f5-165">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-165">Success</span></span>

<span data-ttu-id="ef1f5-166">*Specifica*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-166">*Specific*</span></span>

<span data-ttu-id="ef1f5-167">Non riuscito (10013)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-167">Fail (10013)</span></span>

<span data-ttu-id="ef1f5-168">Non riuscito (10013)</span><span class="sxs-lookup"><span data-stu-id="ef1f5-168">Fail (10013)</span></span>

<span data-ttu-id="ef1f5-169">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-169">Success</span></span>

<span data-ttu-id="ef1f5-170">Operazione completata\*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-170">Success\*</span></span>

<span data-ttu-id="ef1f5-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="ef1f5-171">*Specific2*</span></span>

<span data-ttu-id="ef1f5-172">n/d</span><span class="sxs-lookup"><span data-stu-id="ef1f5-172">n/a</span></span>

<span data-ttu-id="ef1f5-173">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-173">Success</span></span>

<span data-ttu-id="ef1f5-174">n/d</span><span class="sxs-lookup"><span data-stu-id="ef1f5-174">n/a</span></span>

<span data-ttu-id="ef1f5-175">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef1f5-175">Success</span></span>

<span data-ttu-id="ef1f5-176">\* Il comportamento non è definito per il socket che riceverà i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="ef1f5-177">Nel caso in cui la prima operazione di binding non imposti opzioni \_ , quindi REUSEADDR e la seconda operazione di binding esegua una \_ REUSEADDR, il secondo socket avrà la porta e il comportamento che riguardano il socket che riceverà i pacchetti non è determinato.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="ef1f5-178">QUINDI \_ , EXCLUSIVEADDRUSE è stato introdotto per risolvere questa situazione.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="ef1f5-179">\_Non è sempre possibile riutilizzare un socket con tale set EXCLUSIVEADDRUSE immediatamente dopo la chiusura del socket.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="ef1f5-180">Se, ad esempio, un socket di ascolto con il flag esclusivo impostato accetta una connessione dopo la quale il socket di ascolto viene chiuso, un altro socket non può essere associato alla stessa porta del primo socket di ascolto con il flag esclusivo fino a quando non è più attiva la connessione accettata.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="ef1f5-181">Questa situazione può essere piuttosto complessa. anche se il socket è stato chiuso, è possibile che il trasporto sottostante non termini la connessione.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="ef1f5-182">Anche dopo la chiusura del socket, il sistema deve inviare tutti i dati memorizzati nel buffer, trasmettere una disconnessione normale al peer e attendere una disconnessione normale dal peer.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="ef1f5-183">È pertanto possibile che il trasporto sottostante non rilasci mai la connessione, ad esempio quando il peer annuncia una finestra di dimensioni pari a zero o altri attacchi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="ef1f5-184">Nell'esempio precedente, il socket in ascolto è stato chiuso dopo l'accettazione di una connessione client.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="ef1f5-185">A questo punto, anche se la connessione client viene chiusa, è possibile che la porta non venga riutilizzata se la connessione client rimane in uno stato attivo a causa di dati non riconosciuti e così via.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="ef1f5-186">Per evitare questa situazione, le applicazioni devono garantire un arresto normale: chiamare [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con il \_ flag di invio SD, quindi attendere il completamento di un ciclo [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) fino a quando non vengono restituiti zero byte.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="ef1f5-187">In questo modo si evita il problema associato al riutilizzo delle porte, garantisce che tutti i dati siano stati ricevuti dal peer e assicura al peer che tutti i dati sono stati ricevuti correttamente.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="ef1f5-188">L' \_ opzione così Linger può essere impostata su un socket per impedire che la porta si trovi in uno degli Stati di attesa attivi. Tuttavia, questa operazione è sconsigliata perché può causare effetti indesiderati, poiché può causare la reimpostazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="ef1f5-189">Se, ad esempio, i dati sono stati ricevuti ma non ancora riconosciuti dal peer e il computer locale chiude il socket con il \_ set Linger, la connessione viene reimpostata e il peer ignora i dati non riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="ef1f5-190">Inoltre, la scelta di un tempo appropriato per l'indugio è difficile. un valore troppo piccolo genera molte connessioni interrotte, mentre un timeout di grandi dimensioni può lasciare il sistema vulnerabile agli attacchi di tipo Denial of Service stabilendo molte connessioni e bloccando così numerosi thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="ef1f5-191">Un socket che utilizza l' \_ opzione EXCLUSIVEADDRUSE deve essere arrestato correttamente prima di chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="ef1f5-192">In caso contrario, è possibile che si verifichi un attacco Denial of Service se il servizio associato deve essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="ef1f5-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef1f5-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef1f5-193">Requirements</span></span>



| <span data-ttu-id="ef1f5-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1f5-194">Requirement</span></span> | <span data-ttu-id="ef1f5-195">Valore</span><span class="sxs-lookup"><span data-stu-id="ef1f5-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1f5-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef1f5-196">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1f5-197">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef1f5-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ef1f5-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef1f5-198">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1f5-199">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef1f5-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef1f5-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef1f5-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1f5-201"><dt>Winsock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1f5-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 




