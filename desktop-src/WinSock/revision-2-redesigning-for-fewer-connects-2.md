---
description: In questa revisione, l'applicazione di esempio viene riprogettata per eliminare le connessioni non necessarie.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revisione due: riprogettazione per un minor numero di connessioni'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131027"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="44d9f-103">Revisione due: riprogettazione per un minor numero di connessioni</span><span class="sxs-lookup"><span data-stu-id="44d9f-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="44d9f-104">In questa revisione, l'applicazione di esempio viene riprogettata per eliminare le connessioni non necessarie.</span><span class="sxs-lookup"><span data-stu-id="44d9f-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="44d9f-105">Questo esempio di applicazione fornisce anche prestazioni insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="44d9f-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="44d9f-106">Non usare questo esempio di codice nell'applicazione. è solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="44d9f-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="44d9f-107">Problemi rimanenti</span><span class="sxs-lookup"><span data-stu-id="44d9f-107">Remaining Problems</span></span>

<span data-ttu-id="44d9f-108">Le modifiche apportate alla revisione due hanno riprogettato l'applicazione per effettuare una sola connessione per ogni aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="44d9f-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="44d9f-109">L'applicazione include ancora i seguenti problemi di prestazioni:</span><span class="sxs-lookup"><span data-stu-id="44d9f-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="44d9f-110">L'applicazione è ancora serializzata e loquace.</span><span class="sxs-lookup"><span data-stu-id="44d9f-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="44d9f-111">L'applicazione ha ancora una progettazione Fat; sono presenti molti invii che non richiedono alcuna operazione in questa progettazione.</span><span class="sxs-lookup"><span data-stu-id="44d9f-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="44d9f-112">Gli invii sono ancora di 3 byte, che è un flusso insufficiente.</span><span class="sxs-lookup"><span data-stu-id="44d9f-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="44d9f-113">Metriche delle prestazioni chiave</span><span class="sxs-lookup"><span data-stu-id="44d9f-113">Key Performance Metrics</span></span>

<span data-ttu-id="44d9f-114">Le metriche delle prestazioni seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="44d9f-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="44d9f-115">Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="44d9f-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="44d9f-116">Questa versione riflette le metriche delle prestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="44d9f-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="44d9f-117">Tempo cella: 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="44d9f-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="44d9f-118">Goodput-4 byte/RTT</span><span class="sxs-lookup"><span data-stu-id="44d9f-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="44d9f-119">Overhead del protocollo-96,8%</span><span class="sxs-lookup"><span data-stu-id="44d9f-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="44d9f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44d9f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44d9f-121">Miglioramento di un'applicazione lenta</span><span class="sxs-lookup"><span data-stu-id="44d9f-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="44d9f-122">Terminologia di rete</span><span class="sxs-lookup"><span data-stu-id="44d9f-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="44d9f-123">Versione di base: applicazione con prestazioni molto scarsa</span><span class="sxs-lookup"><span data-stu-id="44d9f-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="44d9f-124">Revisione 1: pulizia dell'ovvia</span><span class="sxs-lookup"><span data-stu-id="44d9f-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="44d9f-125">Revisione 3: invio blocco compresso</span><span class="sxs-lookup"><span data-stu-id="44d9f-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="44d9f-126">Miglioramenti futuri</span><span class="sxs-lookup"><span data-stu-id="44d9f-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



