---
description: Le metriche vengono usate per misurare gli aspetti delle prestazioni di rete e protocollo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologia di rete (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751418"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="cc3ce-103">Terminologia di rete (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="cc3ce-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="cc3ce-104">Le metriche vengono usate per misurare gli aspetti delle prestazioni di rete e protocollo.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="cc3ce-105">I valori di tali metriche in diversi scenari indicano il livello di prestazioni di un'applicazione di rete.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="cc3ce-106">Questa sezione definisce i termini e le metriche usati a livello di settore per misurare le prestazioni delle applicazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="cc3ce-107">Questi termini vengono usati nel resto di questa guida.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="cc3ce-108">Tempo di round trip (RTT)</span><span class="sxs-lookup"><span data-stu-id="cc3ce-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="cc3ce-109">Tempo, in millisecondi, per cui una richiesta di eseguire un viaggio da un computer di origine a un computer di destinazione e viceversa.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="cc3ce-110">I valori più bassi indicano prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-110">Lower values indicate better performance.</span></span> <span data-ttu-id="cc3ce-111">I tempi di avanzamento e di ritorno del percorso non sono necessariamente uguali.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="cc3ce-112">I valori RTT sono interessati dall'infrastruttura di rete, dalla distanza tra i nodi, dalle condizioni della rete e dalle dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="cc3ce-113">Dimensioni del pacchetto, congestione e compressione del payload che incidono su RTT se misurato su collegamenti lenti, ad esempio connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="cc3ce-114">Altri fattori influiscono sull'RTT, inclusa la correzione degli errori in diretta e la compressione dei dati, che introducono buffer e code che aumentano RTT e pertanto diminuiscono le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="cc3ce-115">Goodput</span><span class="sxs-lookup"><span data-stu-id="cc3ce-115">Goodput</span></span>

    <span data-ttu-id="cc3ce-116">Misura dei dati di applicazione utili elaborati correttamente dal ricevitore, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="cc3ce-117">Goodput consente di misurare la velocità effettiva effettiva o utile e include solo i dati dell'applicazione. il pacchetto, il protocollo e le intestazioni multimediali sono considerati sovraccarico e non fanno parte di goodput.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="cc3ce-118">Overhead del protocollo</span><span class="sxs-lookup"><span data-stu-id="cc3ce-118">Protocol Overhead</span></span>

    <span data-ttu-id="cc3ce-119">Byte non applicazione, inclusi il protocollo e il frame multimediale, divisi per il numero totale di byte trasmessi.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="cc3ce-120">Il valore è espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="cc3ce-121">Valori più elevati indicano prestazioni più ridotte.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="cc3ce-122">Il sovraccarico viene calcolato per entrambe le direzioni in questa guida, ma può essere calcolato separatamente per ogni direzione.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="cc3ce-123">Prodotto Bandwidth-Delay</span><span class="sxs-lookup"><span data-stu-id="cc3ce-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="cc3ce-124">Prodotto della larghezza di banda di bit al secondo della rete e RTT (in secondi).</span><span class="sxs-lookup"><span data-stu-id="cc3ce-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="cc3ce-125">Questo valore equivale al numero di bit necessari per riempire la larghezza di banda di rete disponibile.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="cc3ce-126">Quando il valore per il ritardo della larghezza di banda è elevato, lo stack TCP/IP deve gestire grandi quantità di dati non riconosciuti per garantire la completa pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="cc3ce-127">Il prodotto con ritardo della larghezza di banda è una metrica end-to-end chiave per le applicazioni di streaming.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



