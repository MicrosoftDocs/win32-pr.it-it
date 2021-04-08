---
title: Identificatori di callout predefiniti (Fwpmu. h)
description: Gli identificatori per le funzioni di callout compilate in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi identificatori sono definiti nel modo seguente.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964890"
---
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="22ba0-104">Identificatori di callout predefiniti</span><span class="sxs-lookup"><span data-stu-id="22ba0-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="22ba0-105">Gli identificatori per le funzioni di callout compilate in Windows Filtering Platform (WFP) sono rappresentati da un GUID.</span><span class="sxs-lookup"><span data-stu-id="22ba0-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="22ba0-106">Questi identificatori sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="22ba0-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="22ba0-107">I suffissi V4 e V6 alla fine degli identificatori di callout indicano se il callout è per lo stack di rete IPv4 o per lo stack di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="22ba0-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="22ba0-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM callout trasporto in ingresso IPSec di callout \_ \_ \_ \_ \_ V4/FWPM \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22ba0-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-109">Verifica che ogni pacchetto ricevuto che dovrebbe arrivare attraverso un'associazione di sicurezza in modalità trasporto arrivi in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="22ba0-110">Questo callout è applicabile a livello di trasporto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ callout IPSec trasporto in uscita \_ \_ V4/FWPM il trasporto in \_ \_ \_ \_ uscita IPSec in \_ uscita \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-112">Indica a IPsec il traffico in uscita che deve essere protetto sulle associazioni di sicurezza in modalità trasporto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="22ba0-113">Questo callout è applicabile a livello di trasporto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM callout tunnel in ingresso IPSec \_ \_ \_ \_ \_ V4/FWPM \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22ba0-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-115">Verifica che ogni pacchetto ricevuto che dovrebbe arrivare attraverso un'associazione di sicurezza in modalità tunnel arrivi in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="22ba0-116">Questo callout è applicabile a livello di trasporto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**Tunnel in uscita IPSec FWPM \_ callout \_ \_ \_ \_ V4/FWPM \_ callout IPSec in \_ \_ uscita \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-118">Indica a IPsec il traffico in uscita che deve essere protetto sulle associazioni di sicurezza in modalità tunnel.</span><span class="sxs-lookup"><span data-stu-id="22ba0-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="22ba0-119">Questo callout è applicabile a livello di trasporto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ callout \_ IPSec \_ inoltri tunnel in ingresso \_ \_ \_ V4/FWPM \_ callout \_ protocollo IPSec \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22ba0-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-121">Verifica che ogni pacchetto ricevuto che dovrebbe arrivare attraverso un'associazione di sicurezza in modalità tunnel arrivi in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="22ba0-122">Questo callout è applicabile a livello di inoltri.</span><span class="sxs-lookup"><span data-stu-id="22ba0-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ callout \_ IPSec \_ inoltri in uscita \_ \_ tunnel \_ V4/ \_ FWPM \_ callout \_ in \_ uscita del \_ tunnel \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-124">Indica a IPsec il traffico in uscita che deve essere protetto tramite un'associazione di sicurezza in modalità tunnel.</span><span class="sxs-lookup"><span data-stu-id="22ba0-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="22ba0-125">Questo callout è applicabile a livello di inoltri.</span><span class="sxs-lookup"><span data-stu-id="22ba0-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ callout \_ IPSec in \_ ingresso \_ avvio \_ Secure \_ V4/FWPM \_ callout IPSec in \_ \_ ingresso \_ avviare \_ Secure \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-127">Verifica che ogni connessione in ingresso che dovrebbe arrivare sicuro arrivi in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="22ba0-128">Questo callout è applicabile al livello di accettazione ALE.</span><span class="sxs-lookup"><span data-stu-id="22ba0-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ callout \_ IPSec in \_ ingresso \_ tunnel \_ ale \_ Accept \_ V4/FWPM \_ callout \_ in \_ ingresso \_ tunnel \_ ale \_ Accept \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-130">Consente i pacchetti IP-in modalità tunnel IPsec quando vengono classificati al livello di accettazione ALE.</span><span class="sxs-lookup"><span data-stu-id="22ba0-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ callout \_ IPSec \_ ale \_ Connect \_ V4/FWPM \_ callout \_ IPSec \_ ale \_ Connect \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-132">Applica i modificatori di criteri IPsec alle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="22ba0-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ callout \_ IPSec \_ DoSP \_ in poi \_ V4/FWPM \_ callout \_ IPSec \_ DoSP \_ in futuro \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-134">Segnala alla protezione DoS IPsec che il traffico deve essere verificato per le potenziali DoS e potrebbe essere necessario un limite di frequenza.</span><span class="sxs-lookup"><span data-stu-id="22ba0-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="22ba0-135">Disponibile solo in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="22ba0-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ callout \_ PAM \_ Transport \_ Layer \_ V4 \_ Silent \_ Drop/FWPM \_ callout \_ \_ Transport \_ Layer \_ V6 \_ Silent \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="22ba0-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-137">Implementa il filtro in modalità Stealth ignorando automaticamente tutti i pacchetti in ingresso per i quali TCP non dispone di un endpoint di ascolto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="22ba0-138">Questo callout è applicabile al livello di eliminazione del trasporto in ingresso.</span><span class="sxs-lookup"><span data-stu-id="22ba0-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V4/FWPM \_ callout \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-140">Abilita o disabilita TCP Chimney Offload per ogni connessione in uscita.</span><span class="sxs-lookup"><span data-stu-id="22ba0-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ callout \_ TCP \_ Chimney \_ Accept \_ Layer \_ V4/FWPM \_ callout \_ TCP \_ Chimney \_ Accept \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-142">Abilita o disabilita TCP Chimney Offload per ogni connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="22ba0-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**Opzioni \_ set di CALLOUT FWPM \_ \_ \_ autenticazione \_ connessione \_ Layer \_ V4/FWPM \_ callout \_ set \_ Opzioni \_ auth \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-144">Imposta le opzioni di classificazione nei flussi in uscita.</span><span class="sxs-lookup"><span data-stu-id="22ba0-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**\_Opzioni set di CALLOUT FWPM \_ \_ \_ auth \_ ricezione \_ Accept \_ Layer \_ V4/FWPM \_ callout \_ set \_ Options \_ auth \_ ricezione \_ Accept \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-146">Imposta le opzioni di classificazione nei flussi in ingresso.</span><span class="sxs-lookup"><span data-stu-id="22ba0-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="22ba0-147">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="22ba0-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ callout \_ riservato \_ auth \_ Connect \_ Layer \_ V4/FWPM \_ callout \_ reserved Authentication \_ \_ \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-149">Questo identificatore è riservato per uso interno.</span><span class="sxs-lookup"><span data-stu-id="22ba0-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ callout \_ Edge \_ attraversamento \_ ale \_ ascolto \_ V6/FWPM \_ callout \_ TEREDO \_ ale \_ ascolto \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-151">Segnala al servizio Teredo che un'applicazione richiede un indirizzo Teredo.</span><span class="sxs-lookup"><span data-stu-id="22ba0-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="22ba0-152">Per Windows 7 e versioni successive, usare **FWPM \_ CALLOUT \_ Edge \_ attraversamento \_ ale \_ ascolto \_ V6**.</span><span class="sxs-lookup"><span data-stu-id="22ba0-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**Assegnazione delle risorse ale del callout di FWPM di \_ \_ \_ \_ \_ \_ \_ FWPM V6/ \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22ba0-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-154">Segnala al servizio Teredo che un'applicazione richiede un indirizzo Teredo.</span><span class="sxs-lookup"><span data-stu-id="22ba0-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="22ba0-155">Per Windows 7 e versioni successive, usare l' **\_ \_ \_ \_ \_ assegnazione delle risorse \_ \_ di FWPM CALLOUT Edge attraversamento della birra V6**.</span><span class="sxs-lookup"><span data-stu-id="22ba0-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**\_ \_ \_ \_ \_ Assegnazione delle risorse ale del bordo di \_ CALLOUT FWPM \_ V4**</span><span class="sxs-lookup"><span data-stu-id="22ba0-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-157">Questo identificatore è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ \_ attraversamento bordo CALLOUT- \_ \_ ale \_ ascolto \_ V4**</span><span class="sxs-lookup"><span data-stu-id="22ba0-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-159">Questo identificatore è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ callout \_ i \_ modelli TCP \_ Connect \_ Layer \_ V4/FWPM \_ callout \_ TCP \_ Templates \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-161">Applica le impostazioni del modello TCP per la corrispondenza delle connessioni in uscita.</span><span class="sxs-lookup"><span data-stu-id="22ba0-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="22ba0-162">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="22ba0-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="22ba0-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**I \_ modelli TCP di CALLOUT FWPM \_ \_ accettano i \_ \_ modelli TCP di livello \_ V4/FWPM che \_ accettano il \_ \_ \_ \_ livello \_ V6**</span><span class="sxs-lookup"><span data-stu-id="22ba0-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="22ba0-164">Applica le impostazioni del modello TCP per la corrispondenza delle connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="22ba0-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="22ba0-165">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="22ba0-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22ba0-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22ba0-166">Requirements</span></span>



| <span data-ttu-id="22ba0-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ba0-167">Requirement</span></span> | <span data-ttu-id="22ba0-168">Valore</span><span class="sxs-lookup"><span data-stu-id="22ba0-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22ba0-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22ba0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="22ba0-170">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22ba0-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="22ba0-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22ba0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="22ba0-172">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22ba0-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="22ba0-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22ba0-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="22ba0-174"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="22ba0-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





