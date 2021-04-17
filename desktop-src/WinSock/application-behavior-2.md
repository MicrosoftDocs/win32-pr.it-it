---
description: Un altro aspetto dello sviluppo di applicazioni da considerare è la differenza nel comportamento tra le operazioni locali o tra computer e il comportamento quando le operazioni avvengono tra due computer in rete.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamento dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526214"
---
# <a name="application-behavior"></a><span data-ttu-id="d95f0-103">Comportamento dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d95f0-103">Application Behavior</span></span>

<span data-ttu-id="d95f0-104">Un altro aspetto dello sviluppo di applicazioni da considerare è la differenza nel comportamento tra le operazioni locali o tra computer e il comportamento quando le operazioni avvengono tra due computer in rete.</span><span class="sxs-lookup"><span data-stu-id="d95f0-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="d95f0-105">Esistono comportamenti dell'applicazione che possono funzionare correttamente in un computer locale, ma quando vengono eseguiti in una rete, provoca un calo significativo delle prestazioni e l'utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d95f0-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="d95f0-106">Quando si sviluppano applicazioni Windows Sockets, è consigliabile evitare i comportamenti seguenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d95f0-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="d95f0-107">Comportamenti da evitare</span><span class="sxs-lookup"><span data-stu-id="d95f0-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="d95f0-108">Applicazioni loquaci.</span><span class="sxs-lookup"><span data-stu-id="d95f0-108">Chatty Applications.</span></span>

    <span data-ttu-id="d95f0-109">Alcune applicazioni eseguono molte transazioni di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d95f0-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="d95f0-110">In combinazione con il sovraccarico di rete associato a ogni transazione di questo tipo, l'effetto viene moltiplicato.</span><span class="sxs-lookup"><span data-stu-id="d95f0-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="d95f0-111">Nelle reti, le transazioni di piccole dimensioni possono utilizzare tutte le risorse e il tempo di transazioni di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d95f0-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="d95f0-112">Un approccio migliore consiste nel combinare molte piccole transazioni in un'unica transazione di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d95f0-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="d95f0-113">Transazioni serializzate.</span><span class="sxs-lookup"><span data-stu-id="d95f0-113">Serialized Transactions.</span></span>

    <span data-ttu-id="d95f0-114">La serializzazione delle transazioni non necessaria può comportare una riduzione delle prestazioni e influire sulla scalabilità.</span><span class="sxs-lookup"><span data-stu-id="d95f0-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="d95f0-115">Ad esempio, 1000 transazioni serializzate accettano almeno 1000 \* RTT per il completamento.</span><span class="sxs-lookup"><span data-stu-id="d95f0-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="d95f0-116">Un approccio migliore consiste nell'eseguire transazioni non correlate in parallelo.</span><span class="sxs-lookup"><span data-stu-id="d95f0-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="d95f0-117">Quando le applicazioni serializzate vengono combinate con le applicazioni chattate, la velocità di risposta può essere gravemente ostacolata.</span><span class="sxs-lookup"><span data-stu-id="d95f0-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="d95f0-118">La deserializzazione corretta di un'applicazione può essere difficile.</span><span class="sxs-lookup"><span data-stu-id="d95f0-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="d95f0-119">Se il passaggio da serializzato a parallelo risulta troppo complesso, provare a combinare più transazioni in un minor numero di transazioni di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d95f0-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="d95f0-120">Transazioni FAT.</span><span class="sxs-lookup"><span data-stu-id="d95f0-120">Fat Transactions.</span></span>

    <span data-ttu-id="d95f0-121">Le applicazioni che inviano byte superflui sulla rete sono considerate applicazioni FAT.</span><span class="sxs-lookup"><span data-stu-id="d95f0-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="d95f0-122">Le applicazioni che inviano byte superflui sulla rete aumentano il sovraccarico della rete e le prestazioni sono ostacolate.</span><span class="sxs-lookup"><span data-stu-id="d95f0-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="d95f0-123">Questa situazione deriva spesso da strutture di dati inefficienti o da flussi di dati inefficienti.</span><span class="sxs-lookup"><span data-stu-id="d95f0-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="d95f0-124">Per risolvere questo problema, ottimizzare le strutture dei dati o prendere in considerazione l'utilizzo della compressione.</span><span class="sxs-lookup"><span data-stu-id="d95f0-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="d95f0-125">Le sezioni seguenti affrontano gli aspetti dello sviluppo di applicazioni da considerare.</span><span class="sxs-lookup"><span data-stu-id="d95f0-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="d95f0-126">Problemi specifici di TCP/IP</span><span class="sxs-lookup"><span data-stu-id="d95f0-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="d95f0-127">Riconoscimento di applicazioni lente</span><span class="sxs-lookup"><span data-stu-id="d95f0-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="d95f0-128">Calcolo del sovraccarico con netstat</span><span class="sxs-lookup"><span data-stu-id="d95f0-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="d95f0-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d95f0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d95f0-130">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="d95f0-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



