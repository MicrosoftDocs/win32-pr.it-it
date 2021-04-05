---
title: Filtro con stato ALE
description: I filtri installati a livello di applicazione a livello di applicazione (ALE) di Windows Filtering Platform (WFP) eseguono un filtro di rete con stato.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046741"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="b8995-103">Filtro con stato ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="b8995-104">I filtri installati a livello di applicazione a livello di applicazione (ALE) di Windows Filtering Platform (WFP) eseguono un filtro di rete con stato.</span><span class="sxs-lookup"><span data-stu-id="b8995-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="b8995-105">Un *flusso ale* viene usato come base per il filtro con stato ale.</span><span class="sxs-lookup"><span data-stu-id="b8995-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="b8995-106">Un flusso ALE è un modo per classificare il traffico di rete mediante il raggruppamento in base a un indirizzo IP di origine, un indirizzo IP di destinazione, una porta di origine, una porta di destinazione e un protocollo.</span><span class="sxs-lookup"><span data-stu-id="b8995-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="b8995-107">Un flusso ALE potrebbe essere generico, ovvero uno o più descrittori potrebbero corrispondere a tutti gli elementi (o caratteri jolly \* ).</span><span class="sxs-lookup"><span data-stu-id="b8995-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="b8995-108">Ad esempio, un flusso UDP ALE generico viene descritto come indirizzo IP di origine = \* , indirizzo IP di destinazione = \* , porta di origine = \* , porta di destinazione = \* e protocollo = UDP.</span><span class="sxs-lookup"><span data-stu-id="b8995-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="b8995-109">Una volta autorizzata una connessione, le connessioni in ingresso sono autorizzate al livello [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) layer and Outbound Connections at the **FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}** Layer), viene creato un flusso ale, in modo tale che, a blocco di una modifica dei criteri, tutti i pacchetti, in ingresso e in uscita, che appartengono allo stesso</span><span class="sxs-lookup"><span data-stu-id="b8995-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="b8995-110">Poiché la modifica di un criterio potrebbe richiedere il blocco delle connessioni precedentemente consentite, è necessario [riautorizzare](ale-re-authorization.md) i flussi ale quando si verifica una modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b8995-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="b8995-111">Il filtro con stato di ALE riduce drasticamente il numero di classificazioni necessarie classificando solo il primo pacchetto che appartiene a un flusso ALE.</span><span class="sxs-lookup"><span data-stu-id="b8995-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="b8995-112">Per confronto, il filtro senza stato richiede la classificazione di ogni pacchetto che attraversa la rete.</span><span class="sxs-lookup"><span data-stu-id="b8995-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="b8995-113">Un flusso ALE ha una direzione associata, ovvero la direzione del primo pacchetto del flusso.</span><span class="sxs-lookup"><span data-stu-id="b8995-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="b8995-114">In questo modo è possibile disporre di criteri più flessibili, permettendo connessioni avviate in ingresso per avere criteri diversi dalle connessioni avviate in uscita.</span><span class="sxs-lookup"><span data-stu-id="b8995-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="b8995-115">Flusso TCP ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-115">TCP ALE Flow</span></span>

<span data-ttu-id="b8995-116">Un flusso di ALE per il traffico TCP è identificato dalle cinque tuple di TCP/IP (indirizzo IP di origine, indirizzo IP di destinazione, porta di origine, porta di destinazione e protocollo).</span><span class="sxs-lookup"><span data-stu-id="b8995-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="b8995-117">Un flusso TCP ALE ha la stessa durata di un socket TCP connesso.</span><span class="sxs-lookup"><span data-stu-id="b8995-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="b8995-118">Un socket TCP connesso può essere un socket creato con [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) o un socket creato in seguito a una chiamata [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .</span><span class="sxs-lookup"><span data-stu-id="b8995-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="b8995-119">ALE mantiene una relazione uno-a-uno tra un flusso TCP ALE e un blocco di controllo TCP (TCB).</span><span class="sxs-lookup"><span data-stu-id="b8995-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="b8995-120">Flusso UDP ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="b8995-121">I protocolli che non sono TCP o ICMP sono trattati come UDP.</span><span class="sxs-lookup"><span data-stu-id="b8995-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="b8995-122">Un flusso di ALE per il traffico UDP è identificato dalle cinque tuple di TCP/IP (indirizzo IP di origine, indirizzo IP di destinazione, porta di origine, porta di destinazione e protocollo).</span><span class="sxs-lookup"><span data-stu-id="b8995-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="b8995-123">Un flusso UDP ALE viene creato in base a un socket UDP e rappresenta il peer remoto con cui l'applicazione sta comunicando.</span><span class="sxs-lookup"><span data-stu-id="b8995-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="b8995-124">Un peer remoto è identificato da una tupla (indirizzo IP di destinazione e porta di destinazione).</span><span class="sxs-lookup"><span data-stu-id="b8995-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="b8995-125">Esiste una relazione uno-a-molti tra un socket UDP e i peer remoti a cui comunica.</span><span class="sxs-lookup"><span data-stu-id="b8995-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="b8995-126">Quando il socket UDP locale viene chiuso, verranno eliminati tutti i flussi ALE associati.</span><span class="sxs-lookup"><span data-stu-id="b8995-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="b8995-127">In assenza di chiusure socket, i flussi di ALE unicast UDP hanno un timeout di inattività [configurabile](ale-flow-customization.md) che per impostazione predefinita è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="b8995-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="b8995-128">Se non viene inviato o ricevuto alcun pacchetto all'interno di questa finestra, il flusso di ALE verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="b8995-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="b8995-129">Questo timeout predefinito viene abbreviato progressivamente quando il numero di ALE fluisce a livello di sistema fino a una determinata soglia.</span><span class="sxs-lookup"><span data-stu-id="b8995-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="b8995-130">Flusso ICMP ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-130">ICMP ALE Flow</span></span>

<span data-ttu-id="b8995-131">Un flusso di ALE per il traffico ICMP è identificato dalle sei Tuple (indirizzo IP di origine, indirizzo IP di destinazione, tipo ICMP, codice ICMP, protocollo e ID ICMP).</span><span class="sxs-lookup"><span data-stu-id="b8995-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="b8995-132">L'ID ICMP fa parte del flusso di ALE solo per il traffico Echo/Reply ICMP.</span><span class="sxs-lookup"><span data-stu-id="b8995-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="b8995-133">In assenza di chiusure socket, i flussi di ALE unicast ICMP hanno un timeout di inattività [configurabile](ale-flow-customization.md) che per impostazione predefinita è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="b8995-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="b8995-134">Se non viene inviato o ricevuto alcun pacchetto all'interno di questa finestra, il flusso di ALE verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="b8995-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="b8995-135">Questo timeout predefinito viene abbreviato progressivamente quando il numero di ALE fluisce a livello di sistema fino a una determinata soglia.</span><span class="sxs-lookup"><span data-stu-id="b8995-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="b8995-136">Solo i messaggi non di errore ICMP sono indicati ai livelli ALE.</span><span class="sxs-lookup"><span data-stu-id="b8995-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="b8995-137">I messaggi di errore ICMP possono essere controllati nei \_ livelli di errore ICMP.</span><span class="sxs-lookup"><span data-stu-id="b8995-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8995-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8995-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8995-139">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="b8995-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="b8995-140">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="b8995-141">Traffico di broadcast/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="b8995-142">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="b8995-143">Personalizzazione del flusso di ALE</span><span class="sxs-lookup"><span data-stu-id="b8995-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="b8995-144">Flussi di pacchetti TCP</span><span class="sxs-lookup"><span data-stu-id="b8995-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="b8995-145">Flussi di pacchetti UDP</span><span class="sxs-lookup"><span data-stu-id="b8995-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="b8995-146">Funzioni Winsock</span><span class="sxs-lookup"><span data-stu-id="b8995-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 