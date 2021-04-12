---
title: Livelli ALE
description: Application Layer Enforcement (ALE) è costituito da diversi livelli di filtro e molti livelli di scarto corrispondenti.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336926"
---
# <a name="ale-layers"></a><span data-ttu-id="92be7-103">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="92be7-103">ALE Layers</span></span>

<span data-ttu-id="92be7-104">L'applicazione a livello di applicazione (ALE) è costituita da diversi livelli di filtro e molti livelli di scarto corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="92be7-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="92be7-105">Tutti i livelli del motore di filtro della piattaforma filtro Windows (WFP), incluso ALE, sono descritti in [**filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md).</span><span class="sxs-lookup"><span data-stu-id="92be7-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="92be7-106">Questo argomento contiene una descrizione più dettagliata dei livelli di filtro che fanno parte di ALE.</span><span class="sxs-lookup"><span data-stu-id="92be7-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="92be7-107">assegnazione di risorse \_</span><span class="sxs-lookup"><span data-stu-id="92be7-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="92be7-108">Per le operazioni di binding di rete, esplicito o implicito, viene associato un filtro a livello di [**\_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) .</span><span class="sxs-lookup"><span data-stu-id="92be7-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="92be7-109">Se viene confrontato un filtro a questo livello per autorizzare la creazione di socket non elaborati, il [**flag di condizione FWP è il flag \_ \_ \_ \_ \_ endpoint non elaborato**](filtering-condition-flags-.md) verrà impostato.</span><span class="sxs-lookup"><span data-stu-id="92be7-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="92be7-110">Se per un filtro a questo livello viene stabilita una corrispondenza per autorizzare la ricezione in modalità promiscua, il campo della [**modalità di FWP \_ condizione \_ ale \_ \_**](filtering-condition-identifiers-.md) viene impostato su sio \_ RCVALL.</span><span class="sxs-lookup"><span data-stu-id="92be7-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="92be7-111">Per una descrizione di SIO \_ RCVALL, vedere [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span><span class="sxs-lookup"><span data-stu-id="92be7-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="92be7-112">Si tratta dell'unico livello in cui è possibile filtrare la modalità promiscua.</span><span class="sxs-lookup"><span data-stu-id="92be7-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="92be7-113">Se durante l'operazione **Bind ()** non viene specificata alcuna porta, ovvero se la porta è impostata su 0 (zero), lo stack TCP/IP selezionerà una porta dall'intervallo di porte dinamiche (19152 – 65535).</span><span class="sxs-lookup"><span data-stu-id="92be7-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="92be7-114">La porta selezionata verrà classificata a questo livello insieme al [**flag di condizione FWP è il flag di \_ \_ \_ \_ \_ binding con caratteri jolly**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="92be7-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="92be7-115">Se l'indirizzo locale non è specificato nella chiamata [**Bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) , il campo indirizzo locale è impostato su [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="92be7-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="92be7-116">AUTENTICAZIONE in \_ ascolto</span><span class="sxs-lookup"><span data-stu-id="92be7-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="92be7-117">Un filtro a livello di [**FWPM \_ Layer \_ ale \_ auth \_ Listen \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene associato alle chiamate di [**ascolto TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="92be7-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="92be7-118">\_accetta ricezione di autenticazione \_</span><span class="sxs-lookup"><span data-stu-id="92be7-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="92be7-119">Un filtro a livello di [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene abbinato per le chiamate TCP [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , per i primi pacchetti UDP (unicast) da una tupla di porta/indirizzo remoto univoca e per i primi messaggi ICMP non di errore in ingresso (unicast) con un tipo, un codice e un ID ICMP univoco.</span><span class="sxs-lookup"><span data-stu-id="92be7-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="92be7-120">I protocolli che non sono TCP o ICMP sono trattati come UDP.</span><span class="sxs-lookup"><span data-stu-id="92be7-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="92be7-121">I pacchetti TCP ricevuti dai socket non elaborati vengono gestiti in modo analogo al traffico UDP.</span><span class="sxs-lookup"><span data-stu-id="92be7-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="92be7-122">Ovvero solo la prima [**trasmissione TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e il primo [**ricezione TCP ()**](/windows/desktop/api/winsock/nf-winsock-recv) su socket non elaborati verranno filtrati.</span><span class="sxs-lookup"><span data-stu-id="92be7-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="92be7-123">\_Connetti autenticazione</span><span class="sxs-lookup"><span data-stu-id="92be7-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="92be7-124">Un filtro a livello di [**FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene associato per le chiamate TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , per i primi pacchetti UDP inviati a un indirizzo remoto univoco e una tupla di porta e per i primi messaggi ICMP non di errore in uscita con un tipo, un codice e un ID ICMP univoco.</span><span class="sxs-lookup"><span data-stu-id="92be7-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="92be7-125">I protocolli che non sono TCP o ICMP sono trattati come UDP.</span><span class="sxs-lookup"><span data-stu-id="92be7-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="92be7-126">I pacchetti TCP inviati da socket non elaborati vengono gestiti in modo analogo al traffico UDP.</span><span class="sxs-lookup"><span data-stu-id="92be7-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="92be7-127">Ovvero solo la prima [**trasmissione TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e il primo [**ricezione TCP ()**](/windows/desktop/api/winsock/nf-winsock-recv) su socket non elaborati verranno filtrati.</span><span class="sxs-lookup"><span data-stu-id="92be7-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="92be7-128">FLUSSO \_ stabilito</span><span class="sxs-lookup"><span data-stu-id="92be7-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="92be7-129">Al termine di un handshake TCP a tre vie, un filtro a livello di FWPM layer ale ha stabilito la corrispondenza del livello [**\_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) .</span><span class="sxs-lookup"><span data-stu-id="92be7-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="92be7-130">Per il traffico non TCP, il filtro viene associato immediatamente dopo che sono state soddisfatte le corrispondenze dei filtri dei livelli di **autenticazione \_ ricezione \_ Accept** o **auth \_ Connect** .</span><span class="sxs-lookup"><span data-stu-id="92be7-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="92be7-131">Un filtro a questo livello non deve restituire un blocco o un permesso.</span><span class="sxs-lookup"><span data-stu-id="92be7-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="92be7-132">Questo livello viene usato dai driver di callout per tenere traccia dello stato della connessione, descritto in dettaglio nella documentazione di [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="92be7-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="92be7-133">versione della risorsa \_</span><span class="sxs-lookup"><span data-stu-id="92be7-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="92be7-134">Un filtro a livello [**di \_ FWPM \_ livello \_ ale \_ versione \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene abbinato dopo che sono state liberate le risorse allocate tramite l' **\_ assegnazione di risorse** .</span><span class="sxs-lookup"><span data-stu-id="92be7-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="92be7-135">\_chiusura endpoint</span><span class="sxs-lookup"><span data-stu-id="92be7-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="92be7-136">Viene stabilita una corrispondenza tra un filtro a livello di [**FWPM \_ Layer ale che chiude il livello \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) quando si chiude un flusso TCP connesso o un endpoint socket UDP.</span><span class="sxs-lookup"><span data-stu-id="92be7-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="92be7-137">Connetti \_ Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="92be7-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="92be7-138">Un filtro a livello di [**FWPM \_ Layer \_ ale \_ Connect \_ Reindirizzamento \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) consente di modificare gli indirizzi e le porte remote.</span><span class="sxs-lookup"><span data-stu-id="92be7-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="92be7-139">La connessione in uscita verrà reindirizzata per la durata di tale connessione.</span><span class="sxs-lookup"><span data-stu-id="92be7-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="92be7-140">Reindirizzamento di binding \_</span><span class="sxs-lookup"><span data-stu-id="92be7-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="92be7-141">Un filtro a livello di [**FWPM \_ Layer \_ ale \_ Bind \_ Reindirizzamento \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) consente di modificare l'indirizzo locale e le porte del socket sottostante.</span><span class="sxs-lookup"><span data-stu-id="92be7-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="92be7-142">Il socket locale verrà reindirizzato per la durata del socket</span><span class="sxs-lookup"><span data-stu-id="92be7-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="92be7-143">Livelli di eliminazione ALE</span><span class="sxs-lookup"><span data-stu-id="92be7-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="92be7-144">Per ognuno dei livelli ALE descritti sopra, il motore di filtro contiene un livello di scarto corrispondente.</span><span class="sxs-lookup"><span data-stu-id="92be7-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="92be7-145">I livelli di eliminazione delle ALE vengono usati dai callout a scopo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="92be7-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="92be7-146">I pacchetti e le indicazioni che sono stati eliminati in uno dei livelli di filtro ALE sono indicati al livello di eliminazione delle ALE corrispondente.</span><span class="sxs-lookup"><span data-stu-id="92be7-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92be7-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92be7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92be7-148">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="92be7-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="92be7-149">Filtro con stato ALE</span><span class="sxs-lookup"><span data-stu-id="92be7-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="92be7-150">Traffico di broadcast/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="92be7-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="92be7-151">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="92be7-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="92be7-152">Personalizzazione del flusso di ALE</span><span class="sxs-lookup"><span data-stu-id="92be7-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="92be7-153">Flussi di pacchetti TCP</span><span class="sxs-lookup"><span data-stu-id="92be7-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="92be7-154">Flussi di pacchetti UDP</span><span class="sxs-lookup"><span data-stu-id="92be7-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="92be7-155">Funzioni Winsock</span><span class="sxs-lookup"><span data-stu-id="92be7-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="92be7-156">**Flag di condizione di filtro**</span><span class="sxs-lookup"><span data-stu-id="92be7-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="92be7-157">**Condizioni di filtro disponibili a ogni livello di filtro**</span><span class="sxs-lookup"><span data-stu-id="92be7-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 