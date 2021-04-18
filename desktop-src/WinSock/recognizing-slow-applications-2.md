---
description: Questa guida identifica un'applicazione lenta come applicazione Microsoft Windows con prestazioni non associate.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Riconoscimento di applicazioni lente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316999"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="53397-103">Riconoscimento di applicazioni lente</span><span class="sxs-lookup"><span data-stu-id="53397-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="53397-104">Questa guida identifica un'applicazione *lenta* come applicazione Microsoft Windows con prestazioni non associate.</span><span class="sxs-lookup"><span data-stu-id="53397-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="53397-105">Un'applicazione lenta presenta uno o più dei seguenti sintomi:</span><span class="sxs-lookup"><span data-stu-id="53397-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="53397-106">L'utilizzo della CPU e della rete è basso.</span><span class="sxs-lookup"><span data-stu-id="53397-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="53397-107">Il computer sembra essere in attesa di qualcosa.</span><span class="sxs-lookup"><span data-stu-id="53397-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="53397-108">Spesso, l'applicazione è in attesa sulla rete.</span><span class="sxs-lookup"><span data-stu-id="53397-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="53397-109">La disattivazione dell'algoritmo Nagle tramite l' \_ opzione socket TCP NoDelay aumenta le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="53397-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="53397-110">Ciò indica altri problemi e non deve essere considerato una soluzione.</span><span class="sxs-lookup"><span data-stu-id="53397-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="53397-111">La disattivazione dell'algoritmo Nagle aumenta l'overhead del protocollo.</span><span class="sxs-lookup"><span data-stu-id="53397-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="53397-112">Non usare questo metodo come correzione per le applicazioni interrotte, solo per indicare che l'applicazione necessita di altro lavoro per la risoluzione dei problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="53397-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="53397-113">L'applicazione presenta un sovraccarico elevato.</span><span class="sxs-lookup"><span data-stu-id="53397-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="53397-114">Per calcolare il sovraccarico delle applicazioni, determinare la quantità di dati che si intende trasferire in ogni direzione.</span><span class="sxs-lookup"><span data-stu-id="53397-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="53397-115">Usare quindi netstat e aggiungere (per Ethernet) 60 byte per ogni pacchetto e 500 byte per ogni connessione.</span><span class="sxs-lookup"><span data-stu-id="53397-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="53397-116">Il sovraccarico migliore che è possibile prevedere per lo streaming tramite Ethernet è circa il 6%.</span><span class="sxs-lookup"><span data-stu-id="53397-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="53397-117">Per una connessione modem, il sovraccarico migliore è approssimativamente del 2%, a causa del fatto che un collegamento PPP usa la compressione di intestazione.</span><span class="sxs-lookup"><span data-stu-id="53397-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="53397-118">Per ulteriori informazioni, vedere [calcolo del sovraccarico con netstat](calculating-overhead-with-netstat-2.md) .</span><span class="sxs-lookup"><span data-stu-id="53397-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="53397-119">La risposta dell'applicazione rallenta quando la connessione ha un RTT di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="53397-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="53397-120">Supponendo che l'applicazione non si avvicini alla larghezza di banda del collegamento, un RTT di grandi dimensioni deve avere un effetto minimo o nullo.</span><span class="sxs-lookup"><span data-stu-id="53397-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="53397-121">Un notevole rallentamento con un RTT di grandi dimensioni è un segno chiaro dell'elaborazione serializzata e di molte transazioni di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="53397-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="53397-122">Ogni applicazione deve essere testata in un ambiente con un RTT di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="53397-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="53397-123">In questo modo viene visualizzata la maggior parte delle applicazioni che soffrono di scelte di sviluppo scarse.</span><span class="sxs-lookup"><span data-stu-id="53397-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="53397-124">Questo test può essere eseguito in diversi ambienti, tra cui una rete LAN wireless, un simulatore di ritardo del collegamento o una rete satellite.</span><span class="sxs-lookup"><span data-stu-id="53397-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53397-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53397-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53397-126">Comportamento dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="53397-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="53397-127">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="53397-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="53397-128">Algoritmo Nagle</span><span class="sxs-lookup"><span data-stu-id="53397-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



