---
description: Calcolo del sovraccarico con netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calcolo del sovraccarico con netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307034"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="ba02d-103">Calcolo del sovraccarico con netstat</span><span class="sxs-lookup"><span data-stu-id="ba02d-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="ba02d-104">Il calcolo del sovraccarico con netstat deve essere eseguito in una rete non interattiva per evitare che il traffico di rete possa inclinare i dati, ad esempio il traffico broadcast o multicast.</span><span class="sxs-lookup"><span data-stu-id="ba02d-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="ba02d-105">**Per calcolare l'overhead di rete di un'applicazione con netstat**</span><span class="sxs-lookup"><span data-stu-id="ba02d-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="ba02d-106">Recuperare le statistiche dell'interfaccia corrente usando netstat.</span><span class="sxs-lookup"><span data-stu-id="ba02d-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="ba02d-107">Eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-107">Execute the application.</span></span>
3.  <span data-ttu-id="ba02d-108">Ottenere le statistiche dell'interfaccia usando nuovamente netstat.</span><span class="sxs-lookup"><span data-stu-id="ba02d-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="ba02d-109">Calcolare il numero di byte ricevuti tra le due misure netstat.</span><span class="sxs-lookup"><span data-stu-id="ba02d-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="ba02d-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ba02d-110">Example</span></span>

<span data-ttu-id="ba02d-111">Nell'esempio seguente vengono illustrati questi passaggi, utilizzando TTCP per inviare 10 byte di dati, un byte alla volta.</span><span class="sxs-lookup"><span data-stu-id="ba02d-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="ba02d-112">In primo luogo, viene calcolato un sovraccarico teorico per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba02d-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="ba02d-113">Per questo test, tutti i pacchetti sono 60 byte (valore minimo Ethernet).</span><span class="sxs-lookup"><span data-stu-id="ba02d-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="ba02d-114">Questo trasferimento richiede tre pacchetti per configurare la connessione, 10 pacchetti di dati, 10 pacchetti di riconoscimento (ACK ritardati viene attivato quasi ogni volta) e quattro pacchetti per chiudere la connessione normalmente.</span><span class="sxs-lookup"><span data-stu-id="ba02d-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="ba02d-115">Questa operazione equivale a 27 pacchetti di 60 byte ciascuno o 1620 byte (3 + 4 + 10 + 10) \* 60 = 1620).</span><span class="sxs-lookup"><span data-stu-id="ba02d-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="ba02d-116">Poiché vengono trasferiti solo 10 byte di dati, l'overhead è di 1610 byte, che è superiore al 99% del sovraccarico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ba02d-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="ba02d-117">Comandi</span><span class="sxs-lookup"><span data-stu-id="ba02d-117">Commands</span></span>

<span data-ttu-id="ba02d-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="ba02d-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="ba02d-119">**ttcp-t-H0-D-L1-N10-P9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="ba02d-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="ba02d-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="ba02d-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="ba02d-121">Calcoli</span><span class="sxs-lookup"><span data-stu-id="ba02d-121">Calculations</span></span>

<span data-ttu-id="ba02d-122">**Inviati:** 816 byte</span><span class="sxs-lookup"><span data-stu-id="ba02d-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="ba02d-123">**Ricevuti:** 674 byte</span><span class="sxs-lookup"><span data-stu-id="ba02d-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="ba02d-124">**Byte totali:** 1490</span><span class="sxs-lookup"><span data-stu-id="ba02d-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="ba02d-125">**Byte utente:** 10</span><span class="sxs-lookup"><span data-stu-id="ba02d-125">**User bytes:** 10</span></span>

<span data-ttu-id="ba02d-126">**Overhead:** 1480/1490 = 99,3%</span><span class="sxs-lookup"><span data-stu-id="ba02d-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="ba02d-127">\* \* Goodput: \* \* = 5 byte al secondo (o 40 bit/sec)</span><span class="sxs-lookup"><span data-stu-id="ba02d-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="ba02d-128">I byte effettivi trasferiti non corrispondono ai valori teorici a causa dei byte di riempimento non contabilizzati nei valori netstat.</span><span class="sxs-lookup"><span data-stu-id="ba02d-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ba02d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba02d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba02d-130">Comportamento dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="ba02d-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="ba02d-131">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="ba02d-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



