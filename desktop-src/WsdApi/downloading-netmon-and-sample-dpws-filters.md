---
description: Microsoft Network Monitor 3 (Netmon) è un analizzatore di pacchetti usato per controllare il traffico di rete.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Download dei filtri Netmon e DPWS di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310312"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="d8cca-103">Download dei filtri Netmon e DPWS di esempio</span><span class="sxs-lookup"><span data-stu-id="d8cca-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="d8cca-104">Microsoft Network Monitor 3 (Netmon) è un analizzatore di pacchetti usato per controllare il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="d8cca-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="d8cca-105">È necessario scaricare Netmon prima di eseguire le procedure di risoluzione dei problemi fornite nel [controllo delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) ed [esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="d8cca-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="d8cca-106">Dopo aver scaricato Netmon, è possibile usare i filtri DPWS per isolare il traffico di interesse.</span><span class="sxs-lookup"><span data-stu-id="d8cca-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="d8cca-107">Download di Netmon</span><span class="sxs-lookup"><span data-stu-id="d8cca-107">Downloading Netmon</span></span>

<span data-ttu-id="d8cca-108">Per scaricare Netmon, passare a [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) e seguire le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="d8cca-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="d8cca-109">Per ulteriori informazioni su Netmon, vedere "informazioni su Network Monitor 3,0" nella Knowledge base relativa alla guida e al supporto tecnico all'indirizzo [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="d8cca-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="d8cca-110">Filtri DPWS di esempio</span><span class="sxs-lookup"><span data-stu-id="d8cca-110">Sample DPWS Filters</span></span>

<span data-ttu-id="d8cca-111">In alcuni casi, la risoluzione dei problemi relativi a WS-Discovery e scambio di metadati deve essere eseguita in una rete occupata.</span><span class="sxs-lookup"><span data-stu-id="d8cca-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="d8cca-112">I filtri di esempio possono essere usati per limitare l'output di Netmon al traffico di interesse.</span><span class="sxs-lookup"><span data-stu-id="d8cca-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="d8cca-113">Per ulteriori informazioni sull'utilizzo dei filtri Netmon, vedere [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="d8cca-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="d8cca-114">Nell'esempio seguente viene illustrato un filtro che limita l'output a tutto il traffico di trasmissione WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="d8cca-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="d8cca-115">Questo filtro non acquisisce il traffico da stack che non rispondono a multicast WS-Discovery messaggi originati dalla porta 3702.</span><span class="sxs-lookup"><span data-stu-id="d8cca-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="d8cca-116">Se viene utilizzato uno stack di questo tipo, è necessario modificare questo filtro di esempio prima dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="d8cca-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="d8cca-117">Nell'esempio seguente viene illustrato un filtro che limita l'output ai messaggi HTTP inviati agli stack WSDAPI sulla porta predefinita.</span><span class="sxs-lookup"><span data-stu-id="d8cca-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="d8cca-118">I servizi possono inviare messaggi HTTP rilevanti da porte diverse da 5357.</span><span class="sxs-lookup"><span data-stu-id="d8cca-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="d8cca-119">Se il traffico da altre porte è di interesse, questo filtro di esempio deve essere modificato prima dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="d8cca-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="d8cca-120">Nell'esempio seguente viene illustrato un filtro che limita l'output al traffico multicast IPv4.</span><span class="sxs-lookup"><span data-stu-id="d8cca-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="d8cca-121">Nell'esempio seguente viene illustrato un filtro che limita l'output al traffico multicast IPv6.</span><span class="sxs-lookup"><span data-stu-id="d8cca-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="d8cca-122">È possibile combinare alcuni filtri per limitare ulteriormente i risultati.</span><span class="sxs-lookup"><span data-stu-id="d8cca-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="d8cca-123">Nell'esempio seguente viene illustrato un filtro che limita l'output al traffico multicast IPv4 WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="d8cca-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="d8cca-124">Quando si utilizzano questi filtri, il traffico pertinente può essere escluso dai risultati di Netmon.</span><span class="sxs-lookup"><span data-stu-id="d8cca-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="d8cca-125">L'esclusione può verificarsi quando i servizi si trovano in porte diverse dalle porte predefinite (5357/5358) e quando uno stack DPWS non risponde ai messaggi utilizzando la porta predefinita.</span><span class="sxs-lookup"><span data-stu-id="d8cca-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="d8cca-126">In questi casi, è necessario modificare i filtri prima dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="d8cca-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8cca-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8cca-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8cca-128">Procedure di diagnostica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d8cca-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="d8cca-129">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d8cca-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



