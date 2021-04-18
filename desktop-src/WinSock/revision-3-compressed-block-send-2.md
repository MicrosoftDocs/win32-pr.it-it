---
description: In questa versione dell'applicazione viene utilizzato un blocco di invio dei dati compresso. Questa modifica comporta un miglioramento significativo delle prestazioni.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisione 3: invio blocco compresso'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310443"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="74046-104">Revisione 3: invio blocco compresso</span><span class="sxs-lookup"><span data-stu-id="74046-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="74046-105">In questa versione dell'applicazione viene utilizzato un blocco di invio dei dati compresso.</span><span class="sxs-lookup"><span data-stu-id="74046-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="74046-106">Questa modifica comporta un miglioramento significativo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="74046-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="74046-107">Modifiche in questa versione</span><span class="sxs-lookup"><span data-stu-id="74046-107">Changes in this Version</span></span>

<span data-ttu-id="74046-108">Questa versione riflette le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="74046-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="74046-109">Gli aggiornamenti delle celle non vengono più serializzati.</span><span class="sxs-lookup"><span data-stu-id="74046-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="74046-110">Poiché viene utilizzato un blocco Send, l'applicazione non è più in chat.</span><span class="sxs-lookup"><span data-stu-id="74046-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="74046-111">Viene utilizzata la compressione dei dati, causando un'applicazione meno FAT.</span><span class="sxs-lookup"><span data-stu-id="74046-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="74046-112">Si è verificato un problema con questa versione dell'applicazione. il rischio di deadlock esiste poiché viene utilizzata un'invio di grandi dimensioni con nessuna ricezione.</span><span class="sxs-lookup"><span data-stu-id="74046-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="74046-113">Il server invia un byte per ogni 3 byte ricevuti.</span><span class="sxs-lookup"><span data-stu-id="74046-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="74046-114">Questo potrebbe causare un deadlock se la dimensione del buffer di ricezione è inferiore a 1000 byte per questa applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="74046-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="74046-115">Metriche delle prestazioni chiave</span><span class="sxs-lookup"><span data-stu-id="74046-115">Key Performance Metrics</span></span>

<span data-ttu-id="74046-116">Le metriche delle prestazioni seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="74046-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="74046-117">Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="74046-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="74046-118">Questa versione riflette le metriche delle prestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="74046-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="74046-119">Tempo cella-. 002 \* RTT</span><span class="sxs-lookup"><span data-stu-id="74046-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="74046-120">Goodput-2 kilobyte/RTT</span><span class="sxs-lookup"><span data-stu-id="74046-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="74046-121">Overhead del protocollo: 14%</span><span class="sxs-lookup"><span data-stu-id="74046-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="74046-122">Del 14% di overhead, il 6% è dalle intestazioni Ethernet e l'altro l'8% viene dall'avvio della connessione e da teardown.</span><span class="sxs-lookup"><span data-stu-id="74046-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74046-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74046-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74046-124">Miglioramento di un'applicazione lenta</span><span class="sxs-lookup"><span data-stu-id="74046-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="74046-125">Terminologia di rete</span><span class="sxs-lookup"><span data-stu-id="74046-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="74046-126">Versione di base: applicazione con prestazioni molto scarsa</span><span class="sxs-lookup"><span data-stu-id="74046-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="74046-127">Revisione 1: pulizia dell'ovvia</span><span class="sxs-lookup"><span data-stu-id="74046-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="74046-128">Revisione 2: riprogettazione per un minor numero di connessioni</span><span class="sxs-lookup"><span data-stu-id="74046-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="74046-129">Miglioramenti futuri</span><span class="sxs-lookup"><span data-stu-id="74046-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



