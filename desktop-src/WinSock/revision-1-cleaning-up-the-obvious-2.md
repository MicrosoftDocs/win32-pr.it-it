---
description: In questa versione del programma di esempio, sono state apportate alcune modifiche ovvie che porteranno a un miglioramento delle prestazioni.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revisione uno: pulizia ovvia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310445"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="53855-103">Revisione uno: pulizia ovvia</span><span class="sxs-lookup"><span data-stu-id="53855-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="53855-104">In questa versione del programma di esempio, sono state apportate alcune modifiche ovvie che porteranno a un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="53855-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="53855-105">Questa versione del codice è distante da quella ottimizzata per le prestazioni, ma è un passaggio incrementale che consente di esaminare gli effetti degli approcci migliori in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="53855-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="53855-106">Questo esempio di applicazione fornisce prestazioni intenzionalmente insoddisfacenti, per illustrare i miglioramenti delle prestazioni possibili con le modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="53855-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="53855-107">Non usare questo esempio di codice nell'applicazione. è solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="53855-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="53855-108">Modifiche in questa versione</span><span class="sxs-lookup"><span data-stu-id="53855-108">Changes in this Version</span></span>

<span data-ttu-id="53855-109">Questa versione riflette le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="53855-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="53855-110">Rimosso SNDBUF = 0.</span><span class="sxs-lookup"><span data-stu-id="53855-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="53855-111">I ritardi 200 millisecondi causati da invii non memorizzati nel buffer e riconoscimenti ritardati vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="53855-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="53855-112">Rimosso il comportamento di trasmissione-invio-ricezione.</span><span class="sxs-lookup"><span data-stu-id="53855-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="53855-113">Questa modifica elimina i ritardi di 200 millisecondi a causa delle interazioni Nagle e ACK ritardate.</span><span class="sxs-lookup"><span data-stu-id="53855-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="53855-114">È stato rimosso il presupposto little-endian.</span><span class="sxs-lookup"><span data-stu-id="53855-114">Removed little-endian assumption.</span></span> <span data-ttu-id="53855-115">I byte sono ora in ordine.</span><span class="sxs-lookup"><span data-stu-id="53855-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="53855-116">Problemi rimanenti</span><span class="sxs-lookup"><span data-stu-id="53855-116">Remaining Problems</span></span>

<span data-ttu-id="53855-117">In questa versione, rimangono i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="53855-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="53855-118">L'applicazione è ancora in stato di connessione pesante.</span><span class="sxs-lookup"><span data-stu-id="53855-118">The application is still connect heavy.</span></span> <span data-ttu-id="53855-119">Poiché i ritardi di 600 millisecondi vengono rimossi, l'applicazione raggiunge ora la velocità sostenuta di 12 connessioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="53855-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="53855-120">Molte connessioni simultanee ora diventano un problema.</span><span class="sxs-lookup"><span data-stu-id="53855-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="53855-121">L'applicazione è ancora grassa; le celle non modificate vengono comunque propagate al server.</span><span class="sxs-lookup"><span data-stu-id="53855-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="53855-122">L'applicazione presenta ancora un flusso scarso; gli invii da 3 byte sono ancora di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="53855-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="53855-123">L'applicazione invia ora 2 byte/RTT, che è uguale a 4 KB/s sull'Ethernet direttamente connessa.</span><span class="sxs-lookup"><span data-stu-id="53855-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="53855-124">Questa operazione non è troppo veloce, ma il tempo di attesa potrebbe causare problemi.</span><span class="sxs-lookup"><span data-stu-id="53855-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="53855-125">L'overhead è inferiore al 99,3%, che non è ancora una percentuale di overhead corretta.</span><span class="sxs-lookup"><span data-stu-id="53855-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="53855-126">Metriche delle prestazioni chiave</span><span class="sxs-lookup"><span data-stu-id="53855-126">Key Performance Metrics</span></span>

<span data-ttu-id="53855-127">Le metriche delle prestazioni chiave seguenti sono espresse in tempo di round trip (RTT), Goodput e sovraccarico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="53855-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="53855-128">Per una spiegazione di questi termini, vedere l'argomento [terminologia di rete](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="53855-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="53855-129">Questa versione riflette le metriche delle prestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="53855-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="53855-130">Tempo cella: 2 × RTT</span><span class="sxs-lookup"><span data-stu-id="53855-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="53855-131">Goodput-2 byte/RTT</span><span class="sxs-lookup"><span data-stu-id="53855-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="53855-132">Overhead del protocollo: 99.3 percent</span><span class="sxs-lookup"><span data-stu-id="53855-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="53855-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53855-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53855-134">Miglioramento di un'applicazione lenta</span><span class="sxs-lookup"><span data-stu-id="53855-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="53855-135">Terminologia di rete</span><span class="sxs-lookup"><span data-stu-id="53855-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="53855-136">Versione di base: applicazione con prestazioni molto scarsa</span><span class="sxs-lookup"><span data-stu-id="53855-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="53855-137">Revisione 2: riprogettazione per un minor numero di connessioni</span><span class="sxs-lookup"><span data-stu-id="53855-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="53855-138">Revisione 3: invio blocco compresso</span><span class="sxs-lookup"><span data-stu-id="53855-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="53855-139">Miglioramenti futuri</span><span class="sxs-lookup"><span data-stu-id="53855-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



