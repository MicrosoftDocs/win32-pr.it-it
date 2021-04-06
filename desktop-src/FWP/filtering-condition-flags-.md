---
title: Flag di condizione di filtro (Fwptypes. h)
description: I flag della condizione di filtro della piattaforma filtro Windows (WFP) sono rappresentati da un bit.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743151"
---
# <a name="filtering-condition-flags"></a><span data-ttu-id="5a60f-103">Flag di condizione di filtro</span><span class="sxs-lookup"><span data-stu-id="5a60f-103">Filtering Condition Flags</span></span>

<span data-ttu-id="5a60f-104">I flag della condizione di filtro della piattaforma filtro Windows (WFP) sono rappresentati da un bit.</span><span class="sxs-lookup"><span data-stu-id="5a60f-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="5a60f-105">Questi flag e i livelli di filtro in cui possono essere usati sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="5a60f-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="5a60f-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**il \_ flag di condizione FWP \_ \_ è \_ loopback**</span><span class="sxs-lookup"><span data-stu-id="5a60f-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-107">Verifica se il traffico di rete è il traffico di loopback.</span><span class="sxs-lookup"><span data-stu-id="5a60f-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="5a60f-108">Filtraggio di livelli:</span><span class="sxs-lookup"><span data-stu-id="5a60f-108">Filtering layers:</span></span>

-   <span data-ttu-id="5a60f-109">FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-110">FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-111">FWPM \_ Layer \_ trasporto in \_ ingresso \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-112">FWPM \_ livello di \_ trasporto in uscita \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-113">\_Flusso di livello FWPM \_ \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-114">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-115">\_ \_ Errore ICMP in ingresso FWPM layer \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-116">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-117">\_ \_ Errore ICMP in uscita livello FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-118">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-119">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-120">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-121">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-122">Flusso di FWPM \_ Layer \_ ale \_ \_ stabilito \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-123">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**il \_ flag di condizione FWP \_ \_ è \_ protetto da IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-125">Verifica se il traffico di rete è protetto da IPsec.</span><span class="sxs-lookup"><span data-stu-id="5a60f-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="5a60f-126">Filtraggio di livelli:</span><span class="sxs-lookup"><span data-stu-id="5a60f-126">Filtering layers:</span></span>

-   <span data-ttu-id="5a60f-127">FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-128">FWPM \_ Layer \_ trasporto in \_ ingresso \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-129">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-130">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**il \_ flag di condizione FWP \_ \_ è stato \_ riautorizzato**</span><span class="sxs-lookup"><span data-stu-id="5a60f-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-132">Verifica la modifica di un criterio anziché una nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="5a60f-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="5a60f-133">Filtraggio di livelli:</span><span class="sxs-lookup"><span data-stu-id="5a60f-133">Filtering layers:</span></span>

-   <span data-ttu-id="5a60f-134">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-135">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**il \_ flag di condizione FWP \_ \_ è \_ associato a caratteri jolly \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-137">Verifica se l'applicazione ha specificato un indirizzo jolly durante l'associazione a un indirizzo di rete locale.</span><span class="sxs-lookup"><span data-stu-id="5a60f-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="5a60f-138">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-138">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-139">\_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**il \_ flag di condizione FWP \_ è un \_ \_ endpoint non elaborato \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-141">Verifica se l'endpoint locale che invia e riceve il traffico è un endpoint non elaborato.</span><span class="sxs-lookup"><span data-stu-id="5a60f-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="5a60f-142">Filtraggio di livelli:</span><span class="sxs-lookup"><span data-stu-id="5a60f-142">Filtering layers:</span></span>

-   <span data-ttu-id="5a60f-143">FWPM \_ Layer \_ trasporto in \_ ingresso \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-144">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-145">FWPM \_ livello di \_ trasporto in uscita \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-146">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-147">\_ \_ Dati datagramma FWPM layer \_ \_ {V4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="5a60f-148">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="5a60f-149">\_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-150">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-151">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**il \_ flag di condizione FWP \_ è un \_ \_ frammento**</span><span class="sxs-lookup"><span data-stu-id="5a60f-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-153">Verifica se la \_ struttura dell' \_ elenco di buffer NET passata a un driver di callout è un frammento di pacchetto IP.</span><span class="sxs-lookup"><span data-stu-id="5a60f-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="5a60f-154">Filtraggio di livelli:</span><span class="sxs-lookup"><span data-stu-id="5a60f-154">Filtering layers:</span></span>

-   <span data-ttu-id="5a60f-155">FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-156">FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6} \_ Elimina</span><span class="sxs-lookup"><span data-stu-id="5a60f-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**il \_ flag di condizione FWP \_ è un \_ \_ gruppo di frammenti \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-158">Verifica se la \_ struttura dell' \_ elenco di buffer NET passata a un driver di callout descrive un elenco collegato di frammenti di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5a60f-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="5a60f-159">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-159">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-160">FWPM \_ livello \_ IPFORWARD \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**il \_ flag di condizione FWP \_ \_ è la \_ \_ \_ riclassificazione Natt IPSec**</span><span class="sxs-lookup"><span data-stu-id="5a60f-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-162">Indica che lo stesso pacchetto viene nuovamente classificato a livello di trasporto, quando lo shim NAT IPsec converte il valore della porta remota.</span><span class="sxs-lookup"><span data-stu-id="5a60f-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**il \_ flag di condizione FWP \_ richiede la \_ \_ \_ classificazione ale**</span><span class="sxs-lookup"><span data-stu-id="5a60f-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-164">Indica che il pacchetto verrà riclassificato al livello di ricezione/accettazione ALE.</span><span class="sxs-lookup"><span data-stu-id="5a60f-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**il \_ flag di condizione FWP \_ è un' \_ \_ associazione implicita \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-166">Verifica se i socket di Windows eseguono un'associazione implicita.</span><span class="sxs-lookup"><span data-stu-id="5a60f-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="5a60f-167">Disponibile solo in Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5a60f-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**il \_ flag di condizione FWP \_ \_ è stato \_ riassemblato**</span><span class="sxs-lookup"><span data-stu-id="5a60f-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-169">Verifica se il pacchetto è stato riassemblato.</span><span class="sxs-lookup"><span data-stu-id="5a60f-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-170">Disponibile solo in Windows Server 2008, Windows Vista con SP1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="5a60f-171">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-171">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-172">FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**il \_ flag di condizione FWP \_ è l' \_ \_ \_ app nome \_ specificata**</span><span class="sxs-lookup"><span data-stu-id="5a60f-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-174">Verifica se il nome del computer peer a cui è prevista l'applicazione si connette è stato ricevuto tramite un'API, ad esempio [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) , e non è stato ottenuto tramite l'euristica di Caching.</span><span class="sxs-lookup"><span data-stu-id="5a60f-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-175">Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="5a60f-176">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-176">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-177">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**il \_ flag di condizione FWP \_ \_ è \_ promiscuo**</span><span class="sxs-lookup"><span data-stu-id="5a60f-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-179">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a60f-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**il \_ flag di condizione FWP \_ \_ è \_ auth \_ FW**</span><span class="sxs-lookup"><span data-stu-id="5a60f-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-181">Verifica se la connessione è autenticata end-to-end, anche se i singoli pacchetti non sono stati verificati.</span><span class="sxs-lookup"><span data-stu-id="5a60f-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-182">Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="5a60f-183">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-183">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-184">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-185">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**il \_ flag di condizione FWP \_ \_ viene \_ riclassificato**</span><span class="sxs-lookup"><span data-stu-id="5a60f-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-187">Verifica se il motore di filtro sta riclassificando una richiesta di binding o ascolto precedente.</span><span class="sxs-lookup"><span data-stu-id="5a60f-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-188">Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="5a60f-189">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-189">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-190">FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-191">\_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**il \_ flag di condizione FWP \_ è una \_ \_ \_ connessione proxy**</span><span class="sxs-lookup"><span data-stu-id="5a60f-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-193">Verifica se la connessione utilizza un proxy.</span><span class="sxs-lookup"><span data-stu-id="5a60f-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-194">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5a60f-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback appcontainer**</span><span class="sxs-lookup"><span data-stu-id="5a60f-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-196">Verifica se il traffico di rete è il traffico di loopback del contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="5a60f-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-197">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5a60f-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback non appcontainer \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-199">Verifica se il traffico di rete è il traffico di loopback del contenitore non app.</span><span class="sxs-lookup"><span data-stu-id="5a60f-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-200">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5a60f-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**il \_ flag di condizione FWP \_ \_ è \_ riservato**</span><span class="sxs-lookup"><span data-stu-id="5a60f-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-202">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5a60f-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**il \_ flag di condizione FWP \_ \_ sta \_ rispettando l' \_ \_ autorizzazione per i criteri**</span><span class="sxs-lookup"><span data-stu-id="5a60f-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-204">Indica che è in corso l'esecuzione della classificazione corrente per rispettare l'intenzione di un'app di Windows Store reindirizzata di connettersi a un host specificato.</span><span class="sxs-lookup"><span data-stu-id="5a60f-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="5a60f-205">Tale classificazione conterrà gli stessi valori di campo classificabili come se l'app non venisse mai reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="5a60f-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="5a60f-206">Il flag indica inoltre che verrà richiamata una futura classificazione in modo che corrisponda alla destinazione reindirizzata effettiva.</span><span class="sxs-lookup"><span data-stu-id="5a60f-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="5a60f-207">Se l'app viene reindirizzata a un servizio proxy per l'ispezione, significa anche che verrà richiamata una futura classificazione sulla connessione proxy.</span><span class="sxs-lookup"><span data-stu-id="5a60f-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="5a60f-208">In genere, i driver di callout devono consentire questa classificazione.</span><span class="sxs-lookup"><span data-stu-id="5a60f-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-209">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5a60f-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="5a60f-210">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-210">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-211">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="5a60f-212">I flag seguenti specificano il motivo per la riautorizzazione di una connessione precedentemente autorizzata.</span><span class="sxs-lookup"><span data-stu-id="5a60f-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="5a60f-213">Questi flag e i livelli di filtro in cui possono essere usati sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="5a60f-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-214">Queste condizioni di filtro sono disponibili solo in Windows Server 2008 R2, Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="5a60f-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**\_modifica dei \_ \_ criteri per il motivo della Riautorizzazione della \_ condizione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="5a60f-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-216">Indica che la connessione è stata riautorizzata a causa dell'aggiunta o della rimozione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="5a60f-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="5a60f-217">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-217">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-218">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-219">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**\_condizione FWP \_ nuova autorizzazione \_ motivo \_ nuova \_ interfaccia di arrivo \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-221">Indica che il pacchetto è arrivato da un'interfaccia sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="5a60f-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="5a60f-222">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-222">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-223">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-224">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**condizione di FWP \_ \_ \_ nuova autorizzazione \_ motivo \_ nuova \_ interfaccia NEXTHOP**</span><span class="sxs-lookup"><span data-stu-id="5a60f-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-226">Indica che il pacchetto verrà ripartito da un'interfaccia sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="5a60f-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="5a60f-227">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-227">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-228">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-229">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP \_ condizione di \_ riautorizzazione del \_ profilo motivo- \_ \_ incrocio**</span><span class="sxs-lookup"><span data-stu-id="5a60f-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-231">Indica che il pacchetto ha attraversato interfacce di più di una categoria di rete.</span><span class="sxs-lookup"><span data-stu-id="5a60f-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="5a60f-232">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-232">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-233">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-234">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ condizione di \_ Riautorizzazione \_ per la classificazione del \_ \_ completamento**</span><span class="sxs-lookup"><span data-stu-id="5a60f-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-236">Indica che è ora possibile completare una connessione precedentemente mantenuta.</span><span class="sxs-lookup"><span data-stu-id="5a60f-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="5a60f-237">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-237">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-238">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-239">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ condizione di \_ riautorizzazione del \_ motivo \_ \_ Proprietà IPSec \_ modificate**</span><span class="sxs-lookup"><span data-stu-id="5a60f-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-241">Indica che le proprietà IPsec sono state modificate o che la connessione è cambiata da testo non crittografato a una connessione protetta.</span><span class="sxs-lookup"><span data-stu-id="5a60f-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="5a60f-242">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-242">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-243">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-244">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ condizione di \_ riautorizzazione del \_ motivo \_ Mid- \_ ispezione del flusso \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-246">Indica che è in corso l'ispezione di una connessione TCP stabilita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5a60f-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="5a60f-247">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-247">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-248">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-249">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_proprietà del \_ socket del motivo di Riautorizzazione della condizione FWP \_ \_ \_ \_ modificata**</span><span class="sxs-lookup"><span data-stu-id="5a60f-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-251">Indica che le proprietà del socket sono state impostate dopo che è stata autorizzata e stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="5a60f-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="5a60f-252">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-252">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-253">FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-254">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_condizione FWP \_ riautorizzare il \_ \_ nuovo \_ \_ pacchetto mcast in ingresso \_ gettati \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-256">Indica che i nuovi pacchetti broadcast o multicast in ingresso vengono riautorizzati in ALE \_ ricezione \_ accettano i callout.</span><span class="sxs-lookup"><span data-stu-id="5a60f-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="5a60f-257">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-257">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-258">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="5a60f-259">I flag seguenti specificano le proprietà del socket correlate a se un'applicazione vuole ricevere traffico di attraversamento perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5a60f-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="5a60f-260">Questi flag e i livelli di filtro in cui possono essere usati sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="5a60f-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-261">Queste condizioni di filtro sono disponibili solo in Windows Server 2008 R2, Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5a60f-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="5a60f-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**il \_ flag della proprietà Socket della condizione FWP \_ \_ \_ \_ è RPC per la \_ porta di sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-263">Indica che l'applicazione sta comunicando con una porta RPC dinamica.</span><span class="sxs-lookup"><span data-stu-id="5a60f-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="5a60f-264">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-264">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-265">FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-266">\_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_flag della proprietà Socket della condizione FWP che consente il \_ \_ \_ \_ \_ traffico perimetrale \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-268">Indica che l'applicazione vuole ricevere traffico specifico di attraversamento del perimetro.</span><span class="sxs-lookup"><span data-stu-id="5a60f-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="5a60f-269">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-269">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-270">FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-271">\_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_flag della proprietà Socket della condizione FWP che nega il \_ \_ \_ \_ \_ traffico perimetrale \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-273">Indica che l'applicazione non vuole ricevere o elaborare traffico specifico di attraversamento del perimetro.</span><span class="sxs-lookup"><span data-stu-id="5a60f-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="5a60f-274">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-274">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-275">FWPM \_ Layer \_ ale \_ auth \_ ascolto \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="5a60f-276">\_ \_ \_ Assegnazione delle risorse FWPM layer ale \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="5a60f-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="5a60f-277">I flag seguenti specificano i dettagli della connessione correlati al filtro L2.</span><span class="sxs-lookup"><span data-stu-id="5a60f-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="5a60f-278">Queste condizioni di filtro sono disponibili solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5a60f-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="5a60f-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**\_La condizione \_ FWP \_ L2 \_ è \_ Ethernet nativa**</span><span class="sxs-lookup"><span data-stu-id="5a60f-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-280">Indica che la connessione è Ethernet nativa.</span><span class="sxs-lookup"><span data-stu-id="5a60f-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="5a60f-281">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-281">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-282">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-283">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-284">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-285">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**\_La condizione FWP \_ L2 \_ è \_ Wi-Fi**</span><span class="sxs-lookup"><span data-stu-id="5a60f-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-287">Indica che la connessione è Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5a60f-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="5a60f-288">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-288">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-289">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-290">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-291">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-292">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**\_La condizione FWP \_ L2 \_ è \_ mobile \_ Broadband**</span><span class="sxs-lookup"><span data-stu-id="5a60f-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-294">Indica che la connessione è Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="5a60f-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="5a60f-295">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-295">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-296">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-297">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-298">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-299">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**\_La condizione \_ FWP \_ L2 \_ è \_ dati diretti Wi-Fi \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-301">Indica che la connessione è Wi-Fi diretta.</span><span class="sxs-lookup"><span data-stu-id="5a60f-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="5a60f-302">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-302">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-303">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-304">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-305">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-306">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**\_La condizione FWP \_ L2 \_ è \_ VM2VM**</span><span class="sxs-lookup"><span data-stu-id="5a60f-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-308">Indica che la connessione è tra macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="5a60f-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="5a60f-309">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-309">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-310">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-311">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-312">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-313">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**\_La condizione FWP \_ L2 è un \_ \_ pacchetto in formato non valido \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-315">Indica che un pacchetto sembra non essere corretto.</span><span class="sxs-lookup"><span data-stu-id="5a60f-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="5a60f-316">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-316">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-317">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-318">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-319">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-320">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**\_La condizione FWP \_ L2 è un gruppo di \_ \_ \_ frammenti IP \_**</span><span class="sxs-lookup"><span data-stu-id="5a60f-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-322">Indica un gruppo di frammenti di pacchetti IP.</span><span class="sxs-lookup"><span data-stu-id="5a60f-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="5a60f-323">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-323">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-324">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-325">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-326">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-327">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a60f-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_Condizione FWP \_ L2 \_ se \_ connettore \_ presente**</span><span class="sxs-lookup"><span data-stu-id="5a60f-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5a60f-329">Indica che è presente un connettore.</span><span class="sxs-lookup"><span data-stu-id="5a60f-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="5a60f-330">Livello filtro:</span><span class="sxs-lookup"><span data-stu-id="5a60f-330">Filtering layer:</span></span>

-   <span data-ttu-id="5a60f-331">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-332">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="5a60f-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="5a60f-333">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="5a60f-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="5a60f-334">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="5a60f-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a60f-335">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a60f-335">Requirements</span></span>



| <span data-ttu-id="5a60f-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a60f-336">Requirement</span></span> | <span data-ttu-id="5a60f-337">Valore</span><span class="sxs-lookup"><span data-stu-id="5a60f-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a60f-338">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a60f-338">Minimum supported client</span></span><br/> | <span data-ttu-id="5a60f-339">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a60f-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a60f-340">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a60f-340">Minimum supported server</span></span><br/> | <span data-ttu-id="5a60f-341">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a60f-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a60f-342">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a60f-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a60f-343"><dt>Fwptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a60f-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a60f-344">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a60f-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a60f-345">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="5a60f-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

