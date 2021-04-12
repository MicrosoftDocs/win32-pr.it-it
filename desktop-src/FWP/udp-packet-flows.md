---
title: Flussi di pacchetti UDP
description: Ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione UDP.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331308"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="3ae17-103">Flussi di pacchetti UDP</span><span class="sxs-lookup"><span data-stu-id="3ae17-103">UDP Packet Flows</span></span>

<span data-ttu-id="3ae17-104">In questa sezione viene descritto l'ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione UDP.</span><span class="sxs-lookup"><span data-stu-id="3ae17-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="3ae17-105">I flussi di pacchetti UDP per IPv6 seguono lo stesso modello di IPv4.</span><span class="sxs-lookup"><span data-stu-id="3ae17-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="3ae17-106">Tutti i flussi di pacchetti non TCP seguono lo stesso modello dei flussi di pacchetti UDP.</span><span class="sxs-lookup"><span data-stu-id="3ae17-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="3ae17-107">Creazione connessione UDP</span><span class="sxs-lookup"><span data-stu-id="3ae17-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="3ae17-108">Il server (ricevitore) esegue l'apertura passiva</span><span class="sxs-lookup"><span data-stu-id="3ae17-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="3ae17-109">Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="3ae17-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="3ae17-110">Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="3ae17-111">Il client (mittente) esegue l'apertura attiva</span><span class="sxs-lookup"><span data-stu-id="3ae17-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="3ae17-112">Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="3ae17-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="3ae17-113">Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="3ae17-114">SendTo: FWPM \_ Layer \_ ale \_ Connect \_ Reindirizzamento \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="3ae17-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="3ae17-115">SendTo: FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="3ae17-116">FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="3ae17-117">dati: \_ \_ dati datagramma FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="3ae17-118">Messaggio UDP: \_ trasporto in uscita del livello FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="3ae17-119">IP datagrammi: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="3ae17-120">Server</span><span class="sxs-lookup"><span data-stu-id="3ae17-120">Server</span></span>

-   <span data-ttu-id="3ae17-121">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="3ae17-122">Messaggio UDP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="3ae17-123">Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="3ae17-124">FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="3ae17-125">dati: \_ \_ dati datagramma FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="3ae17-126">Messaggio UDP ricevuto senza un ascolto sulla porta o sul protocollo</span><span class="sxs-lookup"><span data-stu-id="3ae17-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="3ae17-127">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="3ae17-127">Server (receiver)</span></span>

-   <span data-ttu-id="3ae17-128">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="3ae17-129">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4 \_</span><span class="sxs-lookup"><span data-stu-id="3ae17-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="3ae17-130">Destinazione ICMP non raggiungibile: \_ \_ errore ICMP in uscita livello \_ FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="3ae17-131">Destinazione ICMP non raggiungibile: FWPM \_ livello di \_ trasporto in \_ uscita \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="3ae17-132">Destinazione ICMP non raggiungibile: livello FWPM \_ in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="3ae17-133">UDP senza endpoint è indicato in IPPACKET scarti con una condizione di errore specifica.</span><span class="sxs-lookup"><span data-stu-id="3ae17-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="3ae17-134">Blocca questo pacchetto in IPPACKET scarta per evitare che lo stack invii l'evento corrispondente (errore ICMP).</span><span class="sxs-lookup"><span data-stu-id="3ae17-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="3ae17-135">La riautorizzazione di un pacchetto UDP è stata completata</span><span class="sxs-lookup"><span data-stu-id="3ae17-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="3ae17-136">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="3ae17-136">Server (receiver)</span></span>

-   <span data-ttu-id="3ae17-137">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="3ae17-138">Messaggio UDP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="3ae17-139">Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="3ae17-140">Messaggio UDP: \_ \_ dati datagramma FWPM livello \_ \_ V4 (in ingresso)</span><span class="sxs-lookup"><span data-stu-id="3ae17-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="3ae17-141">Non è stato possibile riautorizzare un pacchetto UDP</span><span class="sxs-lookup"><span data-stu-id="3ae17-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="3ae17-142">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="3ae17-142">Server (receiver)</span></span>

-   <span data-ttu-id="3ae17-143">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="3ae17-144">Messaggio UDP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="3ae17-145">Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4</span><span class="sxs-lookup"><span data-stu-id="3ae17-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="3ae17-146">Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4 \_ scartate</span><span class="sxs-lookup"><span data-stu-id="3ae17-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="3ae17-147">Terminazione connessione UDP</span><span class="sxs-lookup"><span data-stu-id="3ae17-147">UDP Connection Termination</span></span>

<span data-ttu-id="3ae17-148">La chiusura della connessione UDP non è indicata a nessun livello di Pam.</span><span class="sxs-lookup"><span data-stu-id="3ae17-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ae17-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ae17-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ae17-150">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="3ae17-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="3ae17-151">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="3ae17-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




