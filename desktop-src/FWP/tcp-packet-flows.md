---
title: Flussi di pacchetti TCP
description: Ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione TCP.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955641"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="0b953-103">Flussi di pacchetti TCP</span><span class="sxs-lookup"><span data-stu-id="0b953-103">TCP Packet Flows</span></span>

<span data-ttu-id="0b953-104">In questa sezione viene descritto l'ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione TCP.</span><span class="sxs-lookup"><span data-stu-id="0b953-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="0b953-105">I flussi di pacchetti TCP per IPv6 seguono lo stesso modello di IPv4.</span><span class="sxs-lookup"><span data-stu-id="0b953-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b953-106">I flussi di pacchetti non TCP seguono lo stesso modello dei [flussi di pacchetti UDP](udp-packet-flows.md).</span><span class="sxs-lookup"><span data-stu-id="0b953-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="0b953-107">Creazione connessione TCP</span><span class="sxs-lookup"><span data-stu-id="0b953-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="0b953-108">Il server (ricevitore) esegue l'apertura passiva</span><span class="sxs-lookup"><span data-stu-id="0b953-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="0b953-109">Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="0b953-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="0b953-110">Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="0b953-111">ascolto: FWPM \_ Layer \_ ale \_ auth \_ Listen \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="0b953-112">Il client (mittente) esegue l'apertura attiva</span><span class="sxs-lookup"><span data-stu-id="0b953-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="0b953-113">Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="0b953-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="0b953-114">Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="0b953-115">Connetti: FWPM \_ Layer \_ ale \_ Connect \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="0b953-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="0b953-116">connessione: FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="0b953-117">SYN: FWPM \_ livello di \_ trasporto in uscita \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-118">SYN: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="0b953-119">Server</span><span class="sxs-lookup"><span data-stu-id="0b953-119">Server</span></span>

-   <span data-ttu-id="0b953-120">SYN: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-121">SYN: FWPM \_ livello di \_ trasporto in ingresso \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-122">SYN: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="0b953-123">SYN-ACK: \_ trasporto in \_ uscita livello FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-124">SYN-ACK: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="0b953-125">Client</span><span class="sxs-lookup"><span data-stu-id="0b953-125">Client</span></span>

-   <span data-ttu-id="0b953-126">SYN-ACK: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-127">SYN-ACK: FWPM \_ livello di \_ trasporto in ingresso \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-128">FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="0b953-129">ACK: \_ trasporto in \_ uscita livello FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-130">ACK: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="0b953-131">Server</span><span class="sxs-lookup"><span data-stu-id="0b953-131">Server</span></span>

-   <span data-ttu-id="0b953-132">ACK: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-133">ACK: FWPM \_ Layer \_ trasporto in \_ ingresso \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-134">FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="0b953-135">Ascolto completato.</span><span class="sxs-lookup"><span data-stu-id="0b953-135">Listen completes.</span></span> <span data-ttu-id="0b953-136">Il server può eseguire un'accettazione.</span><span class="sxs-lookup"><span data-stu-id="0b953-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="0b953-137">TCP SYN ricevuto senza un ascolto sulla porta o sul protocollo</span><span class="sxs-lookup"><span data-stu-id="0b953-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="0b953-138">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="0b953-138">Server (receiver)</span></span>

-   <span data-ttu-id="0b953-139">SYN: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-140">SYN: FWPM \_ Layer \_ trasporto in \_ ingresso \_ V4 \_ Elimina</span><span class="sxs-lookup"><span data-stu-id="0b953-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="0b953-141">RST: \_ trasporto in uscita del livello FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-142">RST: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="0b953-143">Il protocollo SYN TCP senza endpoint è indicato al momento dell'eliminazione del trasporto con una condizione di errore specifica.</span><span class="sxs-lookup"><span data-stu-id="0b953-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="0b953-144">Blocca questo pacchetto all'eliminazione del trasporto per evitare che lo stack invii l'evento corrispondente (RST).</span><span class="sxs-lookup"><span data-stu-id="0b953-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="0b953-145">Per un esempio di filtro in modalità Stealth, vedere [Impedisci l'analisi delle porte](preventing-port-scanning.md).</span><span class="sxs-lookup"><span data-stu-id="0b953-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="0b953-146">Dati trasmessi tramite una connessione TCP</span><span class="sxs-lookup"><span data-stu-id="0b953-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="0b953-147">Client (mittente)</span><span class="sxs-lookup"><span data-stu-id="0b953-147">Client (sender)</span></span>

-   <span data-ttu-id="0b953-148">trasmissione</span><span class="sxs-lookup"><span data-stu-id="0b953-148">send</span></span>
-   <span data-ttu-id="0b953-149">dati: \_ flusso di livello FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="0b953-150">Segmenti TCP: \_ trasporto in uscita del livello FWPM \_ \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-151">IP datagrammi: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="0b953-152">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="0b953-152">Server (receiver)</span></span>

-   <span data-ttu-id="0b953-153">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-154">Segmenti TCP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-155">dati: \_ flusso di livello FWPM \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="0b953-156">I dati sono disponibili per la lettura.</span><span class="sxs-lookup"><span data-stu-id="0b953-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="0b953-157">Ricreazione di un pacchetto TCP riuscita</span><span class="sxs-lookup"><span data-stu-id="0b953-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="0b953-158">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="0b953-158">Server (receiver)</span></span>

-   <span data-ttu-id="0b953-159">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-160">Segmento TCP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-161">Segmento TCP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="0b953-162">dati: \_ flusso di livello FWPM \_ \_ V4 (in ingresso)</span><span class="sxs-lookup"><span data-stu-id="0b953-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="0b953-163">Non è stato possibile riautorizzare un pacchetto TCP</span><span class="sxs-lookup"><span data-stu-id="0b953-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="0b953-164">Server (ricevitore)</span><span class="sxs-lookup"><span data-stu-id="0b953-164">Server (receiver)</span></span>

-   <span data-ttu-id="0b953-165">IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="0b953-166">Segmento TCP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="0b953-167">Segmento TCP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4</span><span class="sxs-lookup"><span data-stu-id="0b953-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="0b953-168">Segmento TCP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4 \_ scartate</span><span class="sxs-lookup"><span data-stu-id="0b953-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="0b953-169">Terminazione connessione TCP</span><span class="sxs-lookup"><span data-stu-id="0b953-169">TCP Connection Termination</span></span>

<span data-ttu-id="0b953-170">La chiusura della connessione TCP non è indicata a nessun livello di Pam.</span><span class="sxs-lookup"><span data-stu-id="0b953-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b953-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b953-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b953-172">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="0b953-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="0b953-173">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="0b953-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




