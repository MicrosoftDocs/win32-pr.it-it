---
description: Dettagli traccia eventi di rete Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Dettagli traccia eventi di rete Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232789"
---
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="ece98-103">Dettagli traccia eventi di rete Winsock</span><span class="sxs-lookup"><span data-stu-id="ece98-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="ece98-104">Di seguito vengono illustrati tutti gli eventi di rete Winsock che possono essere tracciati e vengono descritti i parametri e le informazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="ece98-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="ece98-105">Creazione socket</span><span class="sxs-lookup"><span data-stu-id="ece98-105">Socket Creation</span></span>

<span data-ttu-id="ece98-106">ID evento = 1</span><span class="sxs-lookup"><span data-stu-id="ece98-106">Event ID = 1</span></span>

<span data-ttu-id="ece98-107">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-107">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-108">Per la creazione del socket vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="ece98-109">Handle di socket creati dalle chiamate alle funzioni [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="ece98-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="ece98-110">Handle di socket accettati sui socket in ascolto.</span><span class="sxs-lookup"><span data-stu-id="ece98-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="ece98-111">Handle di socket creati dalle chiamate alla funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="ece98-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="ece98-112">Gli handle di socket riutilizzati dalle chiamate alle funzioni [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) o [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .</span><span class="sxs-lookup"><span data-stu-id="ece98-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="ece98-113">Per un evento di creazione del socket vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="ece98-114">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="ece98-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="ece98-117">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="ece98-119">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span><span class="sxs-lookup"><span data-stu-id="ece98-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="ece98-121">Tipo di socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="ece98-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocollo</span><span class="sxs-lookup"><span data-stu-id="ece98-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="ece98-123">Protocollo del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="ece98-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span><span class="sxs-lookup"><span data-stu-id="ece98-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="ece98-125">ID processo in modalità utente che ha creato il socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="ece98-126">Binding socket</span><span class="sxs-lookup"><span data-stu-id="ece98-126">Socket Bind</span></span>

<span data-ttu-id="ece98-127">ID evento = 2 (IPv4), ID evento = 3 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="ece98-128">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-128">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-129">Per un'operazione di associazione vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="ece98-130">Associazione implicita o esplicita di un handle di socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="ece98-131">Per un evento di binding vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="ece98-132">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-132">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-135">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-137">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="ece98-139">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="ece98-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="ece98-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="ece98-141">Numero di porta IP locale.</span><span class="sxs-lookup"><span data-stu-id="ece98-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="ece98-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stato</span><span class="sxs-lookup"><span data-stu-id="ece98-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="ece98-143">Stato o codice di errore restituito per l'operazione di associazione.</span><span class="sxs-lookup"><span data-stu-id="ece98-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="ece98-144">Associazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="ece98-144">Failed Bind</span></span>

<span data-ttu-id="ece98-145">ID evento = 40</span><span class="sxs-lookup"><span data-stu-id="ece98-145">Event ID = 40</span></span>

<span data-ttu-id="ece98-146">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-146">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-147">Per un'operazione di associazione non riuscita vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="ece98-148">Associazione implicita o esplicita di un handle di socket che ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ece98-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="ece98-149">Vengono registrati i seguenti parametri per un evento di binding non riuscito:</span><span class="sxs-lookup"><span data-stu-id="ece98-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="ece98-150">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-150">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-153">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-155">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-157">Codice di errore restituito per l'operazione di associazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="ece98-158">Connessione socket</span><span class="sxs-lookup"><span data-stu-id="ece98-158">Socket Connect</span></span>

<span data-ttu-id="ece98-159">ID evento = 4 (IPv4), ID evento = 5 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="ece98-160">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-160">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-161">Gli eventi Winsock seguenti sono tracciati per una richiesta di operazione di connessione (una chiamata alla funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):</span><span class="sxs-lookup"><span data-stu-id="ece98-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="ece98-162">Connessione di un socket a una destinazione per un socket orientato alla connessione o senza connessione.</span><span class="sxs-lookup"><span data-stu-id="ece98-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="ece98-163">Per un evento Connect vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="ece98-164">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-164">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-167">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-169">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="ece98-171">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="ece98-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="ece98-173">Numero di porta IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="ece98-174">Connessione completata</span><span class="sxs-lookup"><span data-stu-id="ece98-174">Connect Completed</span></span>

<span data-ttu-id="ece98-175">ID evento = 6</span><span class="sxs-lookup"><span data-stu-id="ece98-175">Event ID = 6</span></span>

<span data-ttu-id="ece98-176">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-176">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-177">Per una connessione completata, vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="ece98-178">L'operazione di connessione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ece98-178">The connect operation is completed.</span></span>

<span data-ttu-id="ece98-179">I parametri seguenti vengono registrati per un evento di connessione completata:</span><span class="sxs-lookup"><span data-stu-id="ece98-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="ece98-180">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-180">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-183">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-185">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-187">Codice di errore restituito per l'operazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="ece98-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="ece98-188">Interruzione AFD-Initiated</span><span class="sxs-lookup"><span data-stu-id="ece98-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="ece98-189">ID evento = 7</span><span class="sxs-lookup"><span data-stu-id="ece98-189">Event ID = 7</span></span>

<span data-ttu-id="ece98-190">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-190">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-191">Gli eventi Winsock seguenti sono tracciati per le interruzioni avviate da Winsock o per le operazioni di annullamento:</span><span class="sxs-lookup"><span data-stu-id="ece98-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="ece98-192">Interruzione causata da dati di ricezione non letti memorizzati nel buffer dopo la chiusura.</span><span class="sxs-lookup"><span data-stu-id="ece98-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="ece98-193">Interruzione dopo una chiamata alla funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con il parametro *How* impostato su SD \_ Receive e una chiamata alla funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) con la ricezione dei dati in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ece98-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="ece98-194">Interruzione dopo un tentativo non riuscito di scaricare l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ece98-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="ece98-195">Si è verificata un'interruzione dopo un errore interno di Winsock.</span><span class="sxs-lookup"><span data-stu-id="ece98-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="ece98-196">Interruzione a causa di una connessione con errori e dell'applicazione che in precedenza richiedeva che la connessione venisse interrotta in determinate circostanze.</span><span class="sxs-lookup"><span data-stu-id="ece98-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="ece98-197">Un esempio di questo caso è costituito da un'applicazione che è stata impostata in modo che venga \_ sospesa con un timeout di zero e che nella connessione siano ancora presenti dati non riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="ece98-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="ece98-198">Interruzione su una connessione non completamente associata all'accettazione dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ece98-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="ece98-199">Interruzione di una chiamata non riuscita alla funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) o [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .</span><span class="sxs-lookup"><span data-stu-id="ece98-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="ece98-200">Interruzione a causa di un'operazione di ricezione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="ece98-201">Interruzione a causa di un evento Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="ece98-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="ece98-202">Interruzione a causa di una richiesta di scaricamento non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="ece98-203">Interruzione a causa di una richiesta di ricezione dati accelerata non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="ece98-204">Interruzione a causa di una richiesta di invio non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="ece98-205">Interruzione causata dalla richiesta di invio annullata.</span><span class="sxs-lookup"><span data-stu-id="ece98-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="ece98-206">Interruzione causata da un oggetto annullato chiamato sulla funzione [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .</span><span class="sxs-lookup"><span data-stu-id="ece98-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="ece98-207">I parametri seguenti vengono registrati per un'operazione di interruzione o annullamento avviata da Winsock:</span><span class="sxs-lookup"><span data-stu-id="ece98-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="ece98-208">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-208">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-211">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-213">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Motivo</span><span class="sxs-lookup"><span data-stu-id="ece98-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="ece98-215">Motivo dell'operazione di interruzione o annullamento.</span><span class="sxs-lookup"><span data-stu-id="ece98-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="ece98-216">Interruzione Transport-Initiated</span><span class="sxs-lookup"><span data-stu-id="ece98-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="ece98-217">ID evento = 8</span><span class="sxs-lookup"><span data-stu-id="ece98-217">Event ID = 8</span></span>

<span data-ttu-id="ece98-218">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-218">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-219">Gli eventi Winsock seguenti sono tracciati per le operazioni di interruzione o annullamento avviate dal trasporto:</span><span class="sxs-lookup"><span data-stu-id="ece98-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="ece98-220">Reimpostazione indicata dal trasporto.</span><span class="sxs-lookup"><span data-stu-id="ece98-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="ece98-221">I parametri seguenti vengono registrati per un'operazione di interruzione o annullamento avviata da Winsock:</span><span class="sxs-lookup"><span data-stu-id="ece98-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="ece98-222">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-222">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-223">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-225">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-227">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Motivo</span><span class="sxs-lookup"><span data-stu-id="ece98-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="ece98-229">Motivo dell'operazione di interruzione o annullamento.</span><span class="sxs-lookup"><span data-stu-id="ece98-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="ece98-230">Richiesta di invio non riuscita</span><span class="sxs-lookup"><span data-stu-id="ece98-230">Failed Send Request</span></span>

<span data-ttu-id="ece98-231">ID evento = 9</span><span class="sxs-lookup"><span data-stu-id="ece98-231">Event ID = 9</span></span>

<span data-ttu-id="ece98-232">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-232">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-233">Gli eventi Winsock seguenti sono tracciati per individuare eventuali errori nelle richieste [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :</span><span class="sxs-lookup"><span data-stu-id="ece98-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="ece98-234">Errori restituiti nelle richieste [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) non riuscite.</span><span class="sxs-lookup"><span data-stu-id="ece98-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="ece98-235">I parametri seguenti vengono registrati per le richieste di invio che generano un errore:</span><span class="sxs-lookup"><span data-stu-id="ece98-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="ece98-236">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-236">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-237">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-239">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-241">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-243">Codice di errore restituito per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ece98-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="ece98-244">Richiesta WsaSendMsg non riuscita</span><span class="sxs-lookup"><span data-stu-id="ece98-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="ece98-245">ID evento = 10</span><span class="sxs-lookup"><span data-stu-id="ece98-245">Event ID = 10</span></span>

<span data-ttu-id="ece98-246">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-246">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-247">Gli eventi Winsock seguenti sono tracciati per gli errori nelle richieste [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="ece98-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="ece98-248">Errori restituiti nelle richieste [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) non riuscite.</span><span class="sxs-lookup"><span data-stu-id="ece98-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="ece98-249">I parametri seguenti vengono registrati per le richieste di invio che generano un errore:</span><span class="sxs-lookup"><span data-stu-id="ece98-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="ece98-250">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-250">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-251">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-253">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-255">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-257">Codice di errore restituito per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ece98-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="ece98-258">Richiesta ricezione non riuscita</span><span class="sxs-lookup"><span data-stu-id="ece98-258">Failed Recv Request</span></span>

<span data-ttu-id="ece98-259">ID evento = 11</span><span class="sxs-lookup"><span data-stu-id="ece98-259">Event ID = 11</span></span>

<span data-ttu-id="ece98-260">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-260">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-261">Gli eventi Winsock seguenti sono tracciati per individuare eventuali errori nelle richieste [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)o [**chiamata WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :</span><span class="sxs-lookup"><span data-stu-id="ece98-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="ece98-262">Errori restituiti sulle richieste di ricezione non riuscite.</span><span class="sxs-lookup"><span data-stu-id="ece98-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="ece98-263">I parametri seguenti vengono registrati per le richieste di invio che generano un errore:</span><span class="sxs-lookup"><span data-stu-id="ece98-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="ece98-264">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-264">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-265">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-267">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-269">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-271">Codice di errore restituito per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ece98-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="ece98-272">Richiesta recvfrom non riuscita</span><span class="sxs-lookup"><span data-stu-id="ece98-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="ece98-273">ID evento = 12</span><span class="sxs-lookup"><span data-stu-id="ece98-273">Event ID = 12</span></span>

<span data-ttu-id="ece98-274">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-274">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-275">Gli eventi Winsock seguenti sono tracciati per gli errori nelle richieste [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :</span><span class="sxs-lookup"><span data-stu-id="ece98-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="ece98-276">Errori restituiti nelle richieste [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) non riuscite.</span><span class="sxs-lookup"><span data-stu-id="ece98-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="ece98-277">I parametri seguenti vengono registrati per una richiesta [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) che genera un errore:</span><span class="sxs-lookup"><span data-stu-id="ece98-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="ece98-278">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-278">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-279">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-281">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-283">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-285">Codice di errore restituito per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ece98-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="ece98-286">Chiusura socket</span><span class="sxs-lookup"><span data-stu-id="ece98-286">Socket Close</span></span>

<span data-ttu-id="ece98-287">ID evento = 13</span><span class="sxs-lookup"><span data-stu-id="ece98-287">Event ID = 13</span></span>

<span data-ttu-id="ece98-288">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-288">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-289">Gli eventi Winsock seguenti sono tracciati per le operazioni di chiusura del socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="ece98-290">Un handle socket è chiuso.</span><span class="sxs-lookup"><span data-stu-id="ece98-290">A socket handle is closed.</span></span>

<span data-ttu-id="ece98-291">I parametri seguenti vengono registrati per un evento di chiusura del socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="ece98-292">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-292">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-293">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-295">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-297">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-299">Valore restituito per l'operazione di chiusura del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="ece98-300">Pulitura socket</span><span class="sxs-lookup"><span data-stu-id="ece98-300">Socket Cleanup</span></span>

<span data-ttu-id="ece98-301">ID evento = 14</span><span class="sxs-lookup"><span data-stu-id="ece98-301">Event ID = 14</span></span>

<span data-ttu-id="ece98-302">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-302">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-303">Gli eventi Winsock seguenti sono tracciati per le operazioni di pulizia socket (Shutdown):</span><span class="sxs-lookup"><span data-stu-id="ece98-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="ece98-304">La funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) viene chiamata su un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="ece98-305">Il trasporto indica una disconnessione normale non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="ece98-306">I parametri seguenti vengono registrati per un evento di pulizia del socket (arresto) o di chiusura del socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="ece98-307">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-307">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-310">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-312">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-314">Valore restituito per l'operazione di pulizia del socket (arresto).</span><span class="sxs-lookup"><span data-stu-id="ece98-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="ece98-315">Accettazione socket</span><span class="sxs-lookup"><span data-stu-id="ece98-315">Socket Accept</span></span>

<span data-ttu-id="ece98-316">ID evento = 15 (IPv4), ID evento = 16 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="ece98-317">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-317">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-318">Gli eventi Winsock seguenti sono tracciati per una richiesta di funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :</span><span class="sxs-lookup"><span data-stu-id="ece98-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="ece98-319">Richiesta di funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) su un handle di socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="ece98-320">Per un evento Accept vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="ece98-321">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-321">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-322">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-324">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-326">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="ece98-328">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="ece98-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="ece98-330">Numero di porta IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="ece98-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stato</span><span class="sxs-lookup"><span data-stu-id="ece98-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="ece98-332">Stato o codice di errore restituito per l'operazione Accept.</span><span class="sxs-lookup"><span data-stu-id="ece98-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="ece98-333">Accettazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="ece98-333">Accept Failed</span></span>

<span data-ttu-id="ece98-334">ID evento = 17</span><span class="sxs-lookup"><span data-stu-id="ece98-334">Event ID = 17</span></span>

<span data-ttu-id="ece98-335">Livello = 4 (informazioni)</span><span class="sxs-lookup"><span data-stu-id="ece98-335">Level = 4 (Information)</span></span>

<span data-ttu-id="ece98-336">Gli eventi Winsock seguenti sono tracciati per un'operazione di accettazione non riuscita:</span><span class="sxs-lookup"><span data-stu-id="ece98-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="ece98-337">Richiesta [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) su un handle di socket che ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ece98-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="ece98-338">Per un evento Accept non riuscito vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="ece98-339">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-339">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-340">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-342">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-344">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-346">Codice di errore restituito per l'operazione di accettazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ece98-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="ece98-347">Invia inviato</span><span class="sxs-lookup"><span data-stu-id="ece98-347">Send Posted</span></span>

<span data-ttu-id="ece98-348">ID evento = 18</span><span class="sxs-lookup"><span data-stu-id="ece98-348">Event ID = 18</span></span>

<span data-ttu-id="ece98-349">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-350">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-351">Gli eventi Winsock seguenti sono tracciati per le operazioni post del buffer di invio e di ricezione del socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="ece98-352">Un'applicazione invia un messaggio di invio.</span><span class="sxs-lookup"><span data-stu-id="ece98-352">An application posts a send.</span></span>
-   <span data-ttu-id="ece98-353">Un'operazione di invio è stata completata in Winsock.</span><span class="sxs-lookup"><span data-stu-id="ece98-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="ece98-354">I parametri seguenti vengono registrati per le operazioni di invio del socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="ece98-355">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-356">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-358">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="ece98-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-360">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="ece98-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="ece98-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="ece98-362">Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.</span><span class="sxs-lookup"><span data-stu-id="ece98-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="ece98-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-364">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ece98-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-366">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-366">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-367">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-369">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-369">The length of the buffer.</span></span> <span data-ttu-id="ece98-370">Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="ece98-371">Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="ece98-372">Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="ece98-373">Ricezione inviata</span><span class="sxs-lookup"><span data-stu-id="ece98-373">Receive Posted</span></span>

<span data-ttu-id="ece98-374">ID evento = 19</span><span class="sxs-lookup"><span data-stu-id="ece98-374">Event ID = 19</span></span>

<span data-ttu-id="ece98-375">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-376">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-377">Gli eventi Winsock seguenti sono tracciati per le operazioni post del buffer di ricezione socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="ece98-378">Un'applicazione invia una ricezione.</span><span class="sxs-lookup"><span data-stu-id="ece98-378">An application posts a receive.</span></span>
-   <span data-ttu-id="ece98-379">Un'operazione di ricezione viene completata in Winsock.</span><span class="sxs-lookup"><span data-stu-id="ece98-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="ece98-380">Per le operazioni di ricezione socket vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="ece98-381">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-382">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-384">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="ece98-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-386">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="ece98-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="ece98-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="ece98-388">Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.</span><span class="sxs-lookup"><span data-stu-id="ece98-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="ece98-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-390">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ece98-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-392">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-392">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-393">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-395">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-395">The length of the buffer.</span></span> <span data-ttu-id="ece98-396">Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="ece98-397">Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="ece98-398">Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="ece98-399">RecvFrom pubblicato</span><span class="sxs-lookup"><span data-stu-id="ece98-399">RecvFrom Posted</span></span>

<span data-ttu-id="ece98-400">ID evento = 20</span><span class="sxs-lookup"><span data-stu-id="ece98-400">Event ID = 20</span></span>

<span data-ttu-id="ece98-401">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-402">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-403">Gli eventi Winsock seguenti sono tracciati per un'operazione post del buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) su un socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="ece98-404">Un'applicazione invia un'operazione di ricezione da.</span><span class="sxs-lookup"><span data-stu-id="ece98-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="ece98-405">Per l'operazione recvfrom vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="ece98-406">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-407">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-409">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="ece98-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-411">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="ece98-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="ece98-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="ece98-413">Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.</span><span class="sxs-lookup"><span data-stu-id="ece98-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="ece98-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-415">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ece98-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-417">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-417">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-418">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-420">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-420">The length of the buffer.</span></span> <span data-ttu-id="ece98-421">Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="ece98-422">Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="ece98-423">Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="ece98-424">SendTo inviato</span><span class="sxs-lookup"><span data-stu-id="ece98-424">SendTo Posted</span></span>

<span data-ttu-id="ece98-425">ID evento = 21 (IPv4), ID evento = 22 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="ece98-426">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-427">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-428">Gli eventi Winsock seguenti sono tracciati per un'operazione post sul buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) su un socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="ece98-429">Un'applicazione pubblica un invio da.</span><span class="sxs-lookup"><span data-stu-id="ece98-429">An application posts a send from.</span></span>

<span data-ttu-id="ece98-430">Per l'operazione [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="ece98-431">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-432">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-434">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="ece98-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-436">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="ece98-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="ece98-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="ece98-438">Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.</span><span class="sxs-lookup"><span data-stu-id="ece98-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="ece98-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-440">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ece98-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-442">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-442">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-443">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-445">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-445">The length of the buffer.</span></span> <span data-ttu-id="ece98-446">Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="ece98-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="ece98-448">Indirizzo IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="ece98-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="ece98-450">Numero di porta IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="ece98-451">Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="ece98-452">Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="ece98-453">Ricezione completato</span><span class="sxs-lookup"><span data-stu-id="ece98-453">Recv Completed</span></span>

<span data-ttu-id="ece98-454">ID evento = 23</span><span class="sxs-lookup"><span data-stu-id="ece98-454">Event ID = 23</span></span>

<span data-ttu-id="ece98-455">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-456">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-457">Gli eventi Winsock seguenti sono tracciati per le operazioni di ricezione socket completate:</span><span class="sxs-lookup"><span data-stu-id="ece98-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="ece98-458">Un'operazione di invio viene completata al trasporto.</span><span class="sxs-lookup"><span data-stu-id="ece98-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="ece98-459">Un'operazione di ricezione viene completata al trasporto.</span><span class="sxs-lookup"><span data-stu-id="ece98-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="ece98-460">Vengono registrati i seguenti parametri per un invio completato o una ricezione completata:</span><span class="sxs-lookup"><span data-stu-id="ece98-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="ece98-461">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-462">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-464">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="ece98-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-466">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="ece98-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-468">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-468">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-469">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="ece98-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-471">Lunghezza del buffer di byte ricevuti.</span><span class="sxs-lookup"><span data-stu-id="ece98-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="ece98-472">Per i buffer concatenati, questo parametro è il numero totale di byte ricevuti in tutti i buffer della catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="ece98-473">Invio completato</span><span class="sxs-lookup"><span data-stu-id="ece98-473">Send Completed</span></span>

<span data-ttu-id="ece98-474">ID evento = 24</span><span class="sxs-lookup"><span data-stu-id="ece98-474">Event ID = 24</span></span>

<span data-ttu-id="ece98-475">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-476">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-477">Gli eventi Winsock seguenti sono tracciati per le operazioni di invio socket completate:</span><span class="sxs-lookup"><span data-stu-id="ece98-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="ece98-478">Un'operazione di invio viene completata al trasporto.</span><span class="sxs-lookup"><span data-stu-id="ece98-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="ece98-479">Per un invio completato vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="ece98-480">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-481">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-483">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="ece98-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-485">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="ece98-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-487">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-487">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-488">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="ece98-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-490">Lunghezza del buffer di byte inviati.</span><span class="sxs-lookup"><span data-stu-id="ece98-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="ece98-491">Per i buffer concatenati, questo parametro è il numero totale di byte inviati da tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="ece98-492">SendMsg completato</span><span class="sxs-lookup"><span data-stu-id="ece98-492">SendMsg Completed</span></span>

<span data-ttu-id="ece98-493">ID evento = 25</span><span class="sxs-lookup"><span data-stu-id="ece98-493">Event ID = 25</span></span>

<span data-ttu-id="ece98-494">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-495">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-496">Quando un'operazione post del buffer [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) viene completata in un socket, vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="ece98-497">Un'applicazione completa un'operazione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="ece98-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="ece98-498">Per il completamento [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="ece98-499">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-500">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-502">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="ece98-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-504">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="ece98-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-506">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="ece98-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-508">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-508">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-509">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="ece98-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-511">Lunghezza del buffer di byte inviati.</span><span class="sxs-lookup"><span data-stu-id="ece98-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="ece98-512">Per i buffer concatenati, questo parametro è il numero totale di byte inviati da tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="ece98-514">Indirizzo IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="ece98-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="ece98-516">Numero di porta IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="ece98-517">RecvFrom completato</span><span class="sxs-lookup"><span data-stu-id="ece98-517">RecvFrom Completed</span></span>

<span data-ttu-id="ece98-518">ID evento = 26 (IPv4), ID evento = 27 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="ece98-519">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-520">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-521">Quando un'operazione post del buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) viene completata in un socket, vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="ece98-522">Un'applicazione completa un'operazione [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .</span><span class="sxs-lookup"><span data-stu-id="ece98-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="ece98-523">Per il completamento [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="ece98-524">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-525">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-527">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="ece98-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-529">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="ece98-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-531">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="ece98-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-533">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-533">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-534">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="ece98-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-536">Lunghezza del buffer di byte ricevuti.</span><span class="sxs-lookup"><span data-stu-id="ece98-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="ece98-537">Per i buffer concatenati, questo parametro è il numero totale di byte ricevuti in tutti i buffer della catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="ece98-539">Indirizzo IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="ece98-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="ece98-541">Numero di porta IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="ece98-542">SendTo completato</span><span class="sxs-lookup"><span data-stu-id="ece98-542">SendTo Completed</span></span>

<span data-ttu-id="ece98-543">ID evento = 28</span><span class="sxs-lookup"><span data-stu-id="ece98-543">Event ID = 28</span></span>

<span data-ttu-id="ece98-544">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-545">Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="ece98-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="ece98-546">Gli eventi Winsock seguenti vengono tracciati quando un'operazione post del buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) viene completata in un socket:</span><span class="sxs-lookup"><span data-stu-id="ece98-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="ece98-547">Un'applicazione completa un'operazione [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .</span><span class="sxs-lookup"><span data-stu-id="ece98-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="ece98-548">Per il completamento del [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="ece98-549">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="ece98-550">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="ece98-552">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="ece98-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="ece98-554">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="ece98-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="ece98-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="ece98-556">Numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="ece98-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span><span class="sxs-lookup"><span data-stu-id="ece98-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="ece98-558">Indirizzo virtuale del buffer.</span><span class="sxs-lookup"><span data-stu-id="ece98-558">The virtual address of the buffer.</span></span> <span data-ttu-id="ece98-559">Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="ece98-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="ece98-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="ece98-561">Lunghezza del buffer di byte inviati.</span><span class="sxs-lookup"><span data-stu-id="ece98-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="ece98-562">Per i buffer concatenati, questo parametro è il numero totale di byte inviati da tutti i buffer nella catena.</span><span class="sxs-lookup"><span data-stu-id="ece98-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="ece98-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="ece98-564">Indirizzo IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="ece98-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="ece98-566">Numero di porta IP remoto del socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="ece98-567">Set di opzioni socket</span><span class="sxs-lookup"><span data-stu-id="ece98-567">Socket Option Set</span></span>

<span data-ttu-id="ece98-568">ID evento = 29</span><span class="sxs-lookup"><span data-stu-id="ece98-568">Event ID = 29</span></span>

<span data-ttu-id="ece98-569">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-570">Ogni volta che un'applicazione modifica determinati valori di opzioni socket e IOCTL, i nuovi valori verranno registrati.</span><span class="sxs-lookup"><span data-stu-id="ece98-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="ece98-571">Le opzioni registrate possono essere usate per diagnosticare prestazioni insufficienti o comportamenti strani nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ece98-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="ece98-572">Per alcune opzioni socket e IOCTL sono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="ece98-573">QUINDI \_ sndbuf modifiche.</span><span class="sxs-lookup"><span data-stu-id="ece98-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="ece98-574">QUINDI \_ RCVBUF modifiche.</span><span class="sxs-lookup"><span data-stu-id="ece98-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="ece98-575">FIONBIO</span><span class="sxs-lookup"><span data-stu-id="ece98-575">FIONBIO</span></span>
-   <span data-ttu-id="ece98-576">SIO \_ Abilita \_ \_ Accodamento circolare</span><span class="sxs-lookup"><span data-stu-id="ece98-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="ece98-577">\_CONNRESET UDP \_ sio</span><span class="sxs-lookup"><span data-stu-id="ece98-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="ece98-578">\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="ece98-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="ece98-579">Vengono registrati i seguenti parametri per le chiamate di funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) che modificano uno dei valori precedenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="ece98-580">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-580">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-581">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-583">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-585">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Opzione</span><span class="sxs-lookup"><span data-stu-id="ece98-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="ece98-587">Opzione socket o IOCTL modificata.</span><span class="sxs-lookup"><span data-stu-id="ece98-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="ece98-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="ece98-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="ece98-589">Nuovo valore per l'opzione socket o IOCTL.</span><span class="sxs-lookup"><span data-stu-id="ece98-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="ece98-590">Selezione/polling pubblicato</span><span class="sxs-lookup"><span data-stu-id="ece98-590">Select/Poll Posted</span></span>

<span data-ttu-id="ece98-591">ID evento = 30</span><span class="sxs-lookup"><span data-stu-id="ece98-591">Event ID = 30</span></span>

<span data-ttu-id="ece98-592">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-593">Quando un'applicazione chiama la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="ece98-594">L'applicazione invia una richiesta [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="ece98-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="ece98-595">Per gli eventi [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="ece98-596">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="ece98-597">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="ece98-599">ID del processo proprietario.</span><span class="sxs-lookup"><span data-stu-id="ece98-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="ece98-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="ece98-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="ece98-601">Il numero di handle passati dall'applicazione (valido solo nell'evento di avvio).</span><span class="sxs-lookup"><span data-stu-id="ece98-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="ece98-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span><span class="sxs-lookup"><span data-stu-id="ece98-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="ece98-603">Tempo massimo di attesa per la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="ece98-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="ece98-604">Selezione/polling completato</span><span class="sxs-lookup"><span data-stu-id="ece98-604">Select/Poll Completed</span></span>

<span data-ttu-id="ece98-605">ID evento = 31</span><span class="sxs-lookup"><span data-stu-id="ece98-605">Event ID = 31</span></span>

<span data-ttu-id="ece98-606">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-607">Quando un'applicazione chiama la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="ece98-608">Winsock completa una chiamata [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="ece98-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="ece98-609">Quando viene completata un'operazione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="ece98-610">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-610">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-611">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-613">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="ece98-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-615">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="ece98-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore</span><span class="sxs-lookup"><span data-stu-id="ece98-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="ece98-617">Codice di errore restituito per l'operazione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="ece98-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="ece98-618">WSAEventSelect</span><span class="sxs-lookup"><span data-stu-id="ece98-618">WSAEventSelect</span></span>

<span data-ttu-id="ece98-619">ID evento = 32</span><span class="sxs-lookup"><span data-stu-id="ece98-619">Event ID = 32</span></span>

<span data-ttu-id="ece98-620">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-621">Quando un'applicazione chiama la funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="ece98-622">Registra la maschera eventi passata nella funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="ece98-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="ece98-623">Per le chiamate di funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) vengono registrati i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="ece98-624">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-624">Parameter</span></span>                                                                                                | <span data-ttu-id="ece98-625">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="ece98-627">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="ece98-629">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span><span class="sxs-lookup"><span data-stu-id="ece98-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="ece98-631">Valore per la maschera di evento.</span><span class="sxs-lookup"><span data-stu-id="ece98-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="ece98-632">Datagramma eliminato</span><span class="sxs-lookup"><span data-stu-id="ece98-632">Dropped Datagram</span></span>

<span data-ttu-id="ece98-633">ID evento = 33 (IPv4), ID evento = 34 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="ece98-634">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-635">Per semplificare la diagnosi dei problemi relativi alle applicazioni datagramma, vengono tracciati gli eventi Winsock seguenti:</span><span class="sxs-lookup"><span data-stu-id="ece98-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="ece98-636">Quando arriva un datagramma, questo viene eliminato allo spazio del buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ece98-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="ece98-637">In un datagramma connesso, se i dati arrivano da un'origine diversa dalla destinazione connessa.</span><span class="sxs-lookup"><span data-stu-id="ece98-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="ece98-638">Vengono registrati i seguenti parametri per i datagrammi eliminati:</span><span class="sxs-lookup"><span data-stu-id="ece98-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="ece98-639">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="ece98-640">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="ece98-642">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="ece98-644">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span><span class="sxs-lookup"><span data-stu-id="ece98-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="ece98-646">Dimensioni del pacchetto che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ece98-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="ece98-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="ece98-648">Indirizzo IP dell'origine del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ece98-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="ece98-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="ece98-650">Numero di porta IP dell'origine del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ece98-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="ece98-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Motivo</span><span class="sxs-lookup"><span data-stu-id="ece98-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="ece98-652">Il codice di errore o il motivo per cui il pacchetto è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ece98-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="ece98-653">Connessione indicata</span><span class="sxs-lookup"><span data-stu-id="ece98-653">Connection Indicated</span></span>

<span data-ttu-id="ece98-654">ID evento = 35 (IPv4), ID evento = 36 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="ece98-655">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-656">Gli eventi Winsock seguenti sono tracciati per le operazioni indicate per la connessione:</span><span class="sxs-lookup"><span data-stu-id="ece98-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="ece98-657">Un'applicazione riceve una richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="ece98-657">An application receives a connection request.</span></span>

<span data-ttu-id="ece98-658">Vengono registrati i seguenti parametri per le connessioni indicate dagli eventi di trasporto:</span><span class="sxs-lookup"><span data-stu-id="ece98-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="ece98-659">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-659">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-660">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-662">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-664">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="ece98-666">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="ece98-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="ece98-668">Numero di porta IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="ece98-669">Dati indicati</span><span class="sxs-lookup"><span data-stu-id="ece98-669">Data Indicated</span></span>

<span data-ttu-id="ece98-670">ID evento = 37</span><span class="sxs-lookup"><span data-stu-id="ece98-670">Event ID = 37</span></span>

<span data-ttu-id="ece98-671">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-672">Gli eventi Winsock seguenti sono tracciati per le operazioni di dati indicate:</span><span class="sxs-lookup"><span data-stu-id="ece98-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="ece98-673">Un'applicazione riceve i dati su un socket connesso.</span><span class="sxs-lookup"><span data-stu-id="ece98-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="ece98-674">I parametri seguenti vengono registrati per i dati indicati dagli eventi di trasporto:</span><span class="sxs-lookup"><span data-stu-id="ece98-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="ece98-675">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="ece98-676">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="ece98-678">ID del processo proprietario.</span><span class="sxs-lookup"><span data-stu-id="ece98-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="ece98-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="ece98-680">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Byte indicati</span><span class="sxs-lookup"><span data-stu-id="ece98-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="ece98-682">Numero di byte ricevuti sul socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="ece98-683">Dati indicati dal trasporto</span><span class="sxs-lookup"><span data-stu-id="ece98-683">Data Indicated from Transport</span></span>

<span data-ttu-id="ece98-684">ID evento = 38 (IPv4), ID evento = 39 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="ece98-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="ece98-685">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-686">Gli eventi Winsock seguenti sono tracciati per i dati indicati dalle operazioni di trasporto:</span><span class="sxs-lookup"><span data-stu-id="ece98-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="ece98-687">Un'applicazione invia una richiesta di ricezione e riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="ece98-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="ece98-688">I parametri seguenti vengono registrati per i dati indicati dagli eventi di trasporto:</span><span class="sxs-lookup"><span data-stu-id="ece98-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="ece98-689">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="ece98-690">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="ece98-692">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="ece98-694">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="ece98-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ece98-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="ece98-696">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="ece98-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</span><span class="sxs-lookup"><span data-stu-id="ece98-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="ece98-698">Numero di porta IP remoto.</span><span class="sxs-lookup"><span data-stu-id="ece98-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="ece98-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Byte indicati</span><span class="sxs-lookup"><span data-stu-id="ece98-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="ece98-700">Numero di byte ricevuti sul socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="ece98-701">Disconnessione indicata dal trasporto</span><span class="sxs-lookup"><span data-stu-id="ece98-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="ece98-702">ID evento = 41</span><span class="sxs-lookup"><span data-stu-id="ece98-702">Event ID = 41</span></span>

<span data-ttu-id="ece98-703">Livello = 5 (dettagliato)</span><span class="sxs-lookup"><span data-stu-id="ece98-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="ece98-704">Gli eventi Winsock seguenti sono tracciati per le operazioni di disconnessione indicate:</span><span class="sxs-lookup"><span data-stu-id="ece98-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="ece98-705">Un'applicazione riceve un'indicazione di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="ece98-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="ece98-706">I parametri seguenti vengono registrati per la disconnessione indicata dagli eventi di trasporto:</span><span class="sxs-lookup"><span data-stu-id="ece98-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="ece98-707">Parametro</span><span class="sxs-lookup"><span data-stu-id="ece98-707">Parameter</span></span>                                                                                            | <span data-ttu-id="ece98-708">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece98-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece98-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo</span><span class="sxs-lookup"><span data-stu-id="ece98-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="ece98-710">Indirizzo della struttura EPROCESS del kernel per il processo.</span><span class="sxs-lookup"><span data-stu-id="ece98-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="ece98-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="ece98-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="ece98-712">Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.</span><span class="sxs-lookup"><span data-stu-id="ece98-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ece98-713">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ece98-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ece98-714">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="ece98-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="ece98-715">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="ece98-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="ece98-716">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="ece98-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="ece98-717">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="ece98-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
