---
description: Versione di base di un'applicazione con prestazioni molto scarse in Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Versione di base: applicazione con prestazioni molto scarsa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313230"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="dda6d-103">Versione di base: applicazione con prestazioni molto scarsa</span><span class="sxs-lookup"><span data-stu-id="dda6d-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="dda6d-104">Di seguito è riportato l'esempio di codice iniziale, che consente di eseguire il calcolo degli aggiornamenti:</span><span class="sxs-lookup"><span data-stu-id="dda6d-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="dda6d-105">Per semplicità, negli esempi seguenti non è disponibile alcuna gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="dda6d-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="dda6d-106">Qualsiasi applicazione di produzione controlla sempre i valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="dda6d-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="dda6d-107">I primi esempi dell'applicazione forniscono prestazioni intenzionalmente insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="dda6d-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="dda6d-108">Non usare questi esempi di codice nell'applicazione. sono solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="dda6d-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="dda6d-109">In questo stato, l'applicazione presenta le peggiori prestazioni di rete possibili.</span><span class="sxs-lookup"><span data-stu-id="dda6d-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="dda6d-110">I problemi relativi a questa versione dell'applicazione di esempio includono:</span><span class="sxs-lookup"><span data-stu-id="dda6d-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="dda6d-111">L'applicazione è in chat.</span><span class="sxs-lookup"><span data-stu-id="dda6d-111">The application is chatty.</span></span> <span data-ttu-id="dda6d-112">Ogni transazione è troppo piccola: le celle non devono essere aggiornate una alla volta.</span><span class="sxs-lookup"><span data-stu-id="dda6d-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="dda6d-113">Le transazioni vengono serializzate rigorosamente, anche se le celle potrebbero essere aggiornate contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="dda6d-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="dda6d-114">Il buffer di invio è impostato su zero e l'applicazione comporta un ritardo di 200 millisecondi per ogni invio, tre volte per cella.</span><span class="sxs-lookup"><span data-stu-id="dda6d-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="dda6d-115">L'applicazione è molto connessa, connettendosi una volta per ogni cella.</span><span class="sxs-lookup"><span data-stu-id="dda6d-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="dda6d-116">Le applicazioni sono limitate al numero di connessioni al secondo per una determinata destinazione a causa dello stato di attesa del tempo, ma questo non è un problema, poiché ogni transazione impiega più di 600 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="dda6d-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="dda6d-117">L'applicazione è FAT; molte transazioni non hanno alcun effetto sullo stato del server, perché molte celle non cambiano da Update a Update.</span><span class="sxs-lookup"><span data-stu-id="dda6d-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="dda6d-118">L'applicazione presenta un flusso scarso; i piccoli invii utilizzano una quantità elevata di CPU e RAM.</span><span class="sxs-lookup"><span data-stu-id="dda6d-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="dda6d-119">L'applicazione presuppone una rappresentazione little-endian per le relative invii.</span><span class="sxs-lookup"><span data-stu-id="dda6d-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="dda6d-120">Si tratta di un presupposto naturale per la piattaforma Windows corrente, ma può essere pericoloso per il codice di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="dda6d-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="dda6d-121">Metriche delle prestazioni chiave</span><span class="sxs-lookup"><span data-stu-id="dda6d-121">Key Performance Metrics</span></span>

<span data-ttu-id="dda6d-122">Le metriche delle prestazioni seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="dda6d-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="dda6d-123">Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="dda6d-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="dda6d-124">Tempo della cella, tempo di rete per un aggiornamento a cella singola, richiede 4 \* RTT + 600 millisecondi per Nagle e interazioni con ACK ritardati.</span><span class="sxs-lookup"><span data-stu-id="dda6d-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="dda6d-125">Goodput è inferiore a 6 byte.</span><span class="sxs-lookup"><span data-stu-id="dda6d-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="dda6d-126">Il sovraccarico del protocollo è pari al 99,6%.</span><span class="sxs-lookup"><span data-stu-id="dda6d-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dda6d-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dda6d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dda6d-128">Miglioramento di un'applicazione lenta</span><span class="sxs-lookup"><span data-stu-id="dda6d-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="dda6d-129">Terminologia di rete</span><span class="sxs-lookup"><span data-stu-id="dda6d-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="dda6d-130">Revisione 1: pulizia dell'ovvia</span><span class="sxs-lookup"><span data-stu-id="dda6d-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="dda6d-131">Revisione 2: riprogettazione per un minor numero di connessioni</span><span class="sxs-lookup"><span data-stu-id="dda6d-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="dda6d-132">Revisione 3: invio blocco compresso</span><span class="sxs-lookup"><span data-stu-id="dda6d-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="dda6d-133">Miglioramenti futuri</span><span class="sxs-lookup"><span data-stu-id="dda6d-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



