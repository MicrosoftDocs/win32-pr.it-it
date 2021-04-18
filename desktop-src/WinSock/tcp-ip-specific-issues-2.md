---
description: Alcune tecniche di programmazione si verificano in problemi di prestazioni collegati all'implementazione di TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problemi specifici di TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313231"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="7ceea-103">Problemi specifici di TCP/IP</span><span class="sxs-lookup"><span data-stu-id="7ceea-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="7ceea-104">Alcune tecniche di programmazione si verificano in problemi di prestazioni collegati all'implementazione di TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7ceea-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="7ceea-105">Tali problemi di prestazioni non indicano che TCP/IP è inefficiente o un collo di bottiglia delle prestazioni. questi problemi si verificano invece quando le operazioni TCP/IP non vengono riconosciute.</span><span class="sxs-lookup"><span data-stu-id="7ceea-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="7ceea-106">I problemi seguenti identificano scenari comuni in cui la combinazione di opzioni per lo sviluppo di applicazioni di rete e di operazioni TCP/IP comporta una riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7ceea-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="7ceea-107">Applicazioni con utilizzo intensivo della connessione.</span><span class="sxs-lookup"><span data-stu-id="7ceea-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="7ceea-108">Alcune applicazioni creano un'istanza di una nuova connessione TCP per ogni transazione.</span><span class="sxs-lookup"><span data-stu-id="7ceea-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="7ceea-109">La creazione della connessione TCP richiede tempo, contribuisce a RTTs aggiuntivi ed è soggetta a un avvio lento.</span><span class="sxs-lookup"><span data-stu-id="7ceea-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="7ceea-110">Inoltre, le connessioni chiuse sono soggette a tempo di attesa, che utilizza le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ceea-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="7ceea-111">Le applicazioni con un elevato numero di connessioni sono molto comuni perché sono facili da creare; la gestione dei test e degli errori è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="7ceea-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="7ceea-112">Il rilevamento degli errori in una connessione permanente può richiedere un codice e un impegno considerevoli e, pertanto, a volte non viene completato.</span><span class="sxs-lookup"><span data-stu-id="7ceea-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="7ceea-113">Risolvere questa situazione riutilizzando la connessione TCP.</span><span class="sxs-lookup"><span data-stu-id="7ceea-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="7ceea-114">Questa operazione può causare la serializzazione sulla connessione TCP, a meno che le transazioni non siano multiplexate su più connessioni.</span><span class="sxs-lookup"><span data-stu-id="7ceea-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="7ceea-115">Se si adotta questo approccio, il numero di connessioni deve essere limitato a due e l'inquadramento a livello di applicazione e la gestione avanzata degli errori sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="7ceea-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="7ceea-116">Buffer di invio a lunghezza zero e invii di blocco.</span><span class="sxs-lookup"><span data-stu-id="7ceea-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="7ceea-117">La disattivazione del buffer tramite la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare il buffer di invio (in modo che \_ sndbuf) su zero è simile alla disattivazione della memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="7ceea-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="7ceea-118">Quando si imposta il buffer di invio su zero e si emette un blocco inviato, un'applicazione ha una probabilità del 50% di raggiungere un riconoscimento ritardato di 200 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="7ceea-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="7ceea-119">Non disattivare il buffer di invio, a meno che l'utente non abbia preso in considerazione l'effetto in tutti gli ambienti di rete.</span><span class="sxs-lookup"><span data-stu-id="7ceea-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="7ceea-120">Un'eccezione: i dati di streaming con I/O sovrapposti devono impostare il buffer di invio su zero.</span><span class="sxs-lookup"><span data-stu-id="7ceea-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="7ceea-121">Modello di programmazione Send-Send-Receive.</span><span class="sxs-lookup"><span data-stu-id="7ceea-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="7ceea-122">La strutturazione di un'applicazione per l'esecuzione di Send-Send-Receive consente di aumentare le probabilità di riscontrare l'algoritmo Nagle, che causa un ritardo di RTT + 200 ms.</span><span class="sxs-lookup"><span data-stu-id="7ceea-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="7ceea-123">L'algoritmo Nagle può essere rilevato se l'ultimo invio è inferiore alle dimensioni del segmento massimo TCP (MSS, i dati massimi in un singolo datagramma).</span><span class="sxs-lookup"><span data-stu-id="7ceea-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="7ceea-124">MSS può essere un valore di grandi dimensioni (64K in IPv4 e anche più grande in IPv6), quindi non contare su un MSS di solito piccolo.</span><span class="sxs-lookup"><span data-stu-id="7ceea-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="7ceea-125">Un'opzione migliore consiste nel combinare i due invii in una singola trasmissione usando la funzione [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o **memcpy** .</span><span class="sxs-lookup"><span data-stu-id="7ceea-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="7ceea-126">Un numero elevato di connessioni simultanee.</span><span class="sxs-lookup"><span data-stu-id="7ceea-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="7ceea-127">Le connessioni simultanee non devono superare due, ad eccezione delle applicazioni per scopi specifici.</span><span class="sxs-lookup"><span data-stu-id="7ceea-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="7ceea-128">Il superamento di due connessioni simultanee comporta una perdita di risorse.</span><span class="sxs-lookup"><span data-stu-id="7ceea-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="7ceea-129">Una regola efficace consiste nel disporre di un massimo di quattro connessioni di breve durata o di due connessioni permanenti per destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ceea-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ceea-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ceea-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ceea-131">Comportamento dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7ceea-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="7ceea-132">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="7ceea-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="7ceea-133">Algoritmo Nagle</span><span class="sxs-lookup"><span data-stu-id="7ceea-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



