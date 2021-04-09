---
title: Condizioni di filtro disponibili a ogni livello di filtro (Fwpmu. h)
description: Il motore di filtro della piattaforma filtro Windows (WFP) supporta un set di condizioni di filtro diverso a ogni livello di filtro.
ms.assetid: 6faace21-44ec-49dd-8e77-e403c258c14a
topic_type:
- apiref
api_name:
- FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD
- FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD
- FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD
- FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6
- FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6
- FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD
- FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6
- FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6
- FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD
- FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6
- FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD
- FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD
- FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6
- FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6
- FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6
- FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6
- FWPM_LAYER_RPC_UM
- FWPM_LAYER_RPC_EPMAP
- FWPM_LAYER_RPC_EP_ADD
- FWPM_LAYER_RPC_PROXY_CONN
- FWPM_LAYER_RPC_PROXY_IF
- FWPM_LAYER_KM_AUTHORIZATION
- FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET
- FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE
- FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET
- FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0c3806c7c3c7a5fa7f10af0e5e11c212bd93e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963747"
---
# <a name="filtering-conditions-available-at-each-filtering-layer"></a><span data-ttu-id="639dd-103">Condizioni di filtro disponibili a ogni livello di filtro</span><span class="sxs-lookup"><span data-stu-id="639dd-103">Filtering Conditions Available at Each Filtering Layer</span></span>

<span data-ttu-id="639dd-104">Il motore di filtro della piattaforma filtro Windows (WFP) supporta un set di condizioni di filtro diverso a ogni livello di filtro.</span><span class="sxs-lookup"><span data-stu-id="639dd-104">The Windows Filtering Platform (WFP) filter engine supports a different set of filtering conditions at each of its filtering layers.</span></span>

<span data-ttu-id="639dd-105">Di seguito è riportato l'elenco delle condizioni di filtro disponibili a ogni livello.</span><span class="sxs-lookup"><span data-stu-id="639dd-105">The list of filtering conditions that are available at each layer are as follows.</span></span>

## <a name="fwpm_layer_inbound_ippacket_v4--fwpm_layer_inbound_ippacket_v4_discard--fwpm_layer_inbound_ippacket_v6--fwpm_layer_inbound_ippacket_v6_discard"></a><span data-ttu-id="639dd-106">FWPM_LAYER_INBOUND_IPPACKET_V4/FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_INBOUND_IPPACKET_V6/FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-106">FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-107">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-107">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-108">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-108">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-109">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-109">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-115">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-115">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_outbound_ippacket_v4--fwpm_layer_outbound_ippacket_v4_discard--fwpm_layer_outbound_ippacket_v6--fwpm_layer_outbound_ippacket_v6_discard"></a><span data-ttu-id="639dd-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4/FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_OUTBOUND_IPPACKET_V6/FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-117">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-117">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-118">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-118">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-119">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-119">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-125">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-125">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_ipforward_v4--fwpm_layer_ipforward_v4_discard--fwpm_layer_ipforward_v6--fwpm_layer_ipforward_v6_discard"></a><span data-ttu-id="639dd-126">FWPM_LAYER_IPFORWARD_V4/FWPM_LAYER_IPFORWARD_V4_DISCARD/FWPM_LAYER_IPFORWARD_V6/FWPM_LAYER_IPFORWARD_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-126">FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-127">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-127">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="639dd-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span></span>
- <span data-ttu-id="639dd-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="639dd-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-137">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-137">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span></span> 
- <span data-ttu-id="639dd-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="639dd-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_inbound_transport_v4--fwpm_layer_inbound_transport_v4_discard--fwpm_layer_inbound_transport_v6--fwpm_layer_inbound_transport_v6_discard"></a><span data-ttu-id="639dd-142">FWPM_LAYER_INBOUND_TRANSPORT_V4/FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_INBOUND_TRANSPORT_V6/FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-142">FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-143">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-143">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-144">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-144">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-145">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-145">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-149">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-149">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-150">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-150">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-152">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-152">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-154">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-154">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-155">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-155">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_transport_v4--fwpm_layer_outbound_transport_v4_discard--fwpm_layer_outbound_transport_v6--fwpm_layer_outbound_transport_v6_discard"></a><span data-ttu-id="639dd-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4/FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_OUTBOUND_TRANSPORT_V6/FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-158">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-158">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-159">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-159">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-160">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-160">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-165">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-165">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-166">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-166">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-168">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-168">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-170">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-170">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-171">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-171">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_stream_v4--fwpm_layer_stream_v4_discard--fwpm_layer_stream_v6--fwpm_layer_stream_v6_discard"></a><span data-ttu-id="639dd-173">FWPM_LAYER_STREAM_V4/FWPM_LAYER_STREAM_V4_DISCARD/FWPM_LAYER_STREAM_V6/FWPM_LAYER_STREAM_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-173">FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-174">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="639dd-174">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="639dd-175">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-175">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-178">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-178">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-180">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-180">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
## <a name="fwpm_layer_datagram_data_v4--fwpm_layer_datagram_data_v4_discard--fwpm_layer_datagram_data_v6--fwpm_layer_datagram_data_v6_discard"></a><span data-ttu-id="639dd-181">FWPM_LAYER_DATAGRAM_DATA_V4/FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD/FWPM_LAYER_DATAGRAM_DATA_V6/FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-181">FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-182">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="639dd-182">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="639dd-183">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-183">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-184">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-184">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-185">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-185">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-189">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-189">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-190">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-190">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-192">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-192">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-194">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-194">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_stream_packet-v4--fwpm_layer_stream_packet-v6"></a><span data-ttu-id="639dd-195">FWPM_LAYER_STREAM_PACKET V4/FWPM_LAYER_STREAM_PACKET V6</span><span class="sxs-lookup"><span data-stu-id="639dd-195">FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-196">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-196">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-197">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="639dd-197">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="639dd-198">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-198">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-199">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-199">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-200">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-200">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-203">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-203">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-205">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-205">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-207">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-207">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_inbound_icmp_error_v4--fwpm_layer_inbound_icmp_error_v4_discard--fwpm_layer_inbound_icmp_error_v6--fwpm_layer_inbound_icmp_error_v6_discard"></a><span data-ttu-id="639dd-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4/FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_INBOUND_ICMP_ERROR_V6/FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="639dd-213">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-213">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-214">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="639dd-214">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="639dd-215">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-215">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="639dd-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span></span>
- <span data-ttu-id="639dd-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-228">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-228">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_icmp_error_v4--fwpm_layer_outbound_icmp_error_v4_discard--fwpm_layer_outbound_icmp_error_v6--fwpm_layer_outbound_icmp_error_v6_discard"></a><span data-ttu-id="639dd-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-231">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-231">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-232">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="639dd-232">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="639dd-233">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-233">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="639dd-234">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-234">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-235">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-235">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-241">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-241">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-242">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-242">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_ale_bind_redirect_v4--fwpm_layer_ale_bind_redirect-v6"></a><span data-ttu-id="639dd-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4/FWPM_LAYER_ALE_BIND_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="639dd-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-245">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-245">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-246">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-246">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-247">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-247">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-248">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-248">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-251">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-251">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-252">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-252">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-253">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-253">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-254">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-254">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_assignment_v4--fwpm_layer_ale_resource_assignment_v4_discard--fwpm_layer_ale_resource_assignment_v6--fwpm_layer_ale_resource_assignment_v6_discard"></a><span data-ttu-id="639dd-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-256">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-256">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span><span class="sxs-lookup"><span data-stu-id="639dd-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span></span>
- <span data-ttu-id="639dd-258">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-258">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-259">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-259">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-260">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-260">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-264">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-264">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-265">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-265">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-266">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-266">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-267">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-267">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-270">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-270">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-271">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-271">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_release_v4--fwpm_layer_ale_resource_release_v6"></a><span data-ttu-id="639dd-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4/FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-273">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-273">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-274">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-274">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-275">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-275">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-276">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-276">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-280">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-280">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-281">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-281">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-282">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-282">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-283">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-283">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_endpoint_closure_v4--fwpm_layer_ale_endpoint_closure_v6"></a><span data-ttu-id="639dd-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4/FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-285">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-285">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-286">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-286">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-287">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-287">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-288">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-288">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-292">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-292">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-293">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-293">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-295">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-295">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-296">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-296">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-297">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-297">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_listen_v4--fwpm_layer_ale_auth_listen_v4_discard--fwpm_layer_ale_auth_listen_v6--fwpm_layer_ale_auth_listen_v6_discard"></a><span data-ttu-id="639dd-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4/FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD/FWPM_LAYER_ALE_AUTH_LISTEN_V6/FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-299">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-299">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-300">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-300">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-301">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-301">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-302">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-302">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-306">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-306">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-307">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-307">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-308">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-308">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-311">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-311">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-312">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-312">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_recv_accept_v4--fwpm_layer_ale_auth_recv_accept_v4_discard--fwpm_layer_ale_auth_recv_accept_v6--fwpm_layer_ale_auth_recv_accept_v6_discard"></a><span data-ttu-id="639dd-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-314">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-314">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="639dd-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span></span>
- <span data-ttu-id="639dd-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="639dd-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="639dd-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
- <span data-ttu-id="639dd-319">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-319">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="639dd-324">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-324">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-329">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-329">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-330">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-330">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-332">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-332">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-336">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-336">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="639dd-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="639dd-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-344">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="639dd-344">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="639dd-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-346">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-346">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-347">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-347">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_connect_redirect_v4--fwpm_layer_ale_connect_redirect-v6"></a><span data-ttu-id="639dd-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4/FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="639dd-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-349">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-349">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-350">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-350">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-351">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-351">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-352">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-352">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-355">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-355">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-356">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-356">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-357">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-357">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-360">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-360">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-361">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-361">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_connect_v4--fwpm_layer_ale_auth_connect_v4_discard--fwpm_layer_ale_auth_connect_v6--fwpm_layer_ale_auth_connect_v6_discard"></a><span data-ttu-id="639dd-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4/FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_CONNECT_V6/FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-363">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-363">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="639dd-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="639dd-366">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-366">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-367">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-367">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-368">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-368">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-373">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-373">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-374">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-374">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-376">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-376">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-378">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-378">FWPM_CONDITION_TUNNEL_TYPE</span></span>
- <span data-ttu-id="639dd-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="639dd-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX _sp1 e laterFWPM_CONDITION_INTERFACE_INDEX di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="639dd-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 and laterFWPM_CONDITION_INTERFACE_INDEX</span></span> 
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-383">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-383">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="639dd-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="639dd-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="639dd-391">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="639dd-391">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="639dd-392">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="639dd-392">FWPM_CONDITION_PEER_NAME</span></span>
- <span data-ttu-id="639dd-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-394">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-394">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-395">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-395">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_flow_established_v4--fwpm_layer_ale_flow_established_v4_discard--fwpm_layer_ale_flow_established_v6--fwpm_layer_ale_flow_established_v6_discard"></a><span data-ttu-id="639dd-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="639dd-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span></span>
- <span data-ttu-id="639dd-397">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-397">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="639dd-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="639dd-400">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-400">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-401">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="639dd-401">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="639dd-402">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-402">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="639dd-403">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-403">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-408">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-408">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-409">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-409">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-411">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-411">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="639dd-412">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-412">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-413">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-413">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-414">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-414">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_name_resolution_cache_v4--fwpm_layer_name_resolution_cache_v6"></a><span data-ttu-id="639dd-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4/FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-416">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-416">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-417">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-417">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="639dd-418">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-418">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="639dd-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-420">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="639dd-420">FWPM_CONDITION_PEER_NAME</span></span>
## <a name="fwpm_layer_ipsec_km_demux_v4--fwpm_layer_ipsec_km_demux_v6"></a><span data-ttu-id="639dd-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4/FWPM_LAYER_IPSEC_KM_DEMUX_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6</span></span>
- <span data-ttu-id="639dd-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
## <a name="fwpm_layer_ipsec_v4--fwpm_layer_ipsec_v6"></a><span data-ttu-id="639dd-424">FWPM_LAYER_IPSEC_V4/FWPM_LAYER_IPSEC_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-424">FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6</span></span>
- <span data-ttu-id="639dd-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-426">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-426">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-427">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-427">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-429">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-429">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-430">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-430">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_ikeext_v4--fwpm_layer_ikeext_v6"></a><span data-ttu-id="639dd-433">FWPM_LAYER_IKEEXT_V4/FWPM_LAYER_IKEEXT_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-433">FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6</span></span>
- <span data-ttu-id="639dd-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-436">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-436">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="639dd-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_rpc_um"></a><span data-ttu-id="639dd-439">FWPM_LAYER_RPC_UM</span><span class="sxs-lookup"><span data-stu-id="639dd-439">FWPM_LAYER_RPC_UM</span></span>
- <span data-ttu-id="639dd-440">FWPM_CONDITION_DCOM_APP_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-440">FWPM_CONDITION_DCOM_APP_ID</span></span>
- <span data-ttu-id="639dd-441">FWPM_CONDITION_IMAGE_NAME</span><span class="sxs-lookup"><span data-stu-id="639dd-441">FWPM_CONDITION_IMAGE_NAME</span></span>
- <span data-ttu-id="639dd-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="639dd-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="639dd-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="639dd-444">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-444">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="639dd-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="639dd-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>
- <span data-ttu-id="639dd-447">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="639dd-447">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="639dd-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="639dd-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="639dd-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="639dd-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="639dd-450">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-450">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="639dd-451">FWPM_CONDITION_RPC_IF_FLAG</span><span class="sxs-lookup"><span data-stu-id="639dd-451">FWPM_CONDITION_RPC_IF_FLAG</span></span>
- <span data-ttu-id="639dd-452">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="639dd-452">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="639dd-453">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="639dd-453">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="639dd-454">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-454">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="639dd-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="639dd-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="639dd-456">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="639dd-456">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_epmap"></a><span data-ttu-id="639dd-457">FWPM_LAYER_RPC_EPMAP</span><span class="sxs-lookup"><span data-stu-id="639dd-457">FWPM_LAYER_RPC_EPMAP</span></span>
- <span data-ttu-id="639dd-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="639dd-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="639dd-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="639dd-460">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-460">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="639dd-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="639dd-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="639dd-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>

- <span data-ttu-id="639dd-463">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="639dd-463">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="639dd-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="639dd-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="639dd-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="639dd-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="639dd-466">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-466">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="639dd-467">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="639dd-467">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="639dd-468">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="639dd-468">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="639dd-469">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-469">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="639dd-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="639dd-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="639dd-471">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="639dd-471">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_ep_add"></a><span data-ttu-id="639dd-472">FWPM_LAYER_RPC_EP_ADD</span><span class="sxs-lookup"><span data-stu-id="639dd-472">FWPM_LAYER_RPC_EP_ADD</span></span>
- <span data-ttu-id="639dd-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="639dd-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span></span>
- <span data-ttu-id="639dd-474">FWPM_CONDITION_RPC_EP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-474">FWPM_CONDITION_RPC_EP_FLAGS</span></span>
- <span data-ttu-id="639dd-475">FWPM_CONDITION_RPC_EP_VALUE</span><span class="sxs-lookup"><span data-stu-id="639dd-475">FWPM_CONDITION_RPC_EP_VALUE</span></span>
- <span data-ttu-id="639dd-476">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-476">FWPM_CONDITION_RPC_PROTOCOL</span></span>
## <a name="fwpm_layer_rpc_proxy_conn"></a><span data-ttu-id="639dd-477">FWPM_LAYER_RPC_PROXY_CONN</span><span class="sxs-lookup"><span data-stu-id="639dd-477">FWPM_LAYER_RPC_PROXY_CONN</span></span>
- <span data-ttu-id="639dd-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="639dd-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="639dd-479">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="639dd-479">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="639dd-480">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="639dd-480">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="639dd-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="639dd-482">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="639dd-482">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="639dd-483">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-483">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_rpc_proxy_if"></a><span data-ttu-id="639dd-484">FWPM_LAYER_RPC_PROXY_IF</span><span class="sxs-lookup"><span data-stu-id="639dd-484">FWPM_LAYER_RPC_PROXY_IF</span></span>
- <span data-ttu-id="639dd-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="639dd-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="639dd-486">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="639dd-486">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="639dd-487">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="639dd-487">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="639dd-488">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="639dd-488">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="639dd-489">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="639dd-489">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="639dd-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="639dd-491">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="639dd-491">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="639dd-492">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-492">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_km_authorization"></a><span data-ttu-id="639dd-493">FWPM_LAYER_KM_AUTHORIZATION</span><span class="sxs-lookup"><span data-stu-id="639dd-493">FWPM_LAYER_KM_AUTHORIZATION</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="639dd-494">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-494">Windows 7  and later</span></span>
- <span data-ttu-id="639dd-495">FWPM_CONDITION_REMOTE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-495">FWPM_CONDITION_REMOTE_ID</span></span>
- <span data-ttu-id="639dd-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span></span>
- <span data-ttu-id="639dd-497">FWPM_CONDITION_KM_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-497">FWPM_CONDITION_KM_TYPE</span></span>
- <span data-ttu-id="639dd-498">FWPM_CONDITION_KM_MODE</span><span class="sxs-lookup"><span data-stu-id="639dd-498">FWPM_CONDITION_KM_MODE</span></span>
- <span data-ttu-id="639dd-499">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="639dd-499">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="639dd-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span><span class="sxs-lookup"><span data-stu-id="639dd-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span></span>
## <a name="fwpm_layer_inbound_mac_frame_ethernet--fwpm_layer_outbound_mac_frame_ethernet"></a><span data-ttu-id="639dd-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET/FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="639dd-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-502">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-502">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span></span>
- <span data-ttu-id="639dd-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="639dd-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="639dd-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-508">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-508">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="639dd-509">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-509">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="639dd-510">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-510">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="639dd-511">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-511">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-512">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-512">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="639dd-513">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-513">FWPM_CONDITION_L2_FLAGS</span></span>
##  <a name="fwpm_layer_inbound_mac_frame_native--fwpm_layer_outbound_mac_frame_native"></a><span data-ttu-id="639dd-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE/FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span><span class="sxs-lookup"><span data-stu-id="639dd-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-515">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-515">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span></span>
- <span data-ttu-id="639dd-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span></span>
- <span data-ttu-id="639dd-518">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="639dd-518">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="639dd-519">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-519">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-520">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="639dd-520">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="639dd-521">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-521">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="639dd-522">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-522">FWPM_CONDITION_L2_FLAGS</span></span>
## <a name="fwpm_layer_egress_vswitch_ethernet--fwpm_layer_ingress_vswitch_ethernet"></a><span data-ttu-id="639dd-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET/FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="639dd-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-524">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-524">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="639dd-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="639dd-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="639dd-529">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-529">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="639dd-530">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-530">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="639dd-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="639dd-532">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-532">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="639dd-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="639dd-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="639dd-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="639dd-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>
##  <a name="fwpm_layer_egress_vswitch_transport_v4--fwpm_layer_ingress_vswitch_transport_v4--fwpm_layer_egressvswitch_transport_v6--fwpm_layer_ingress_vswitch_transport_v6"></a><span data-ttu-id="639dd-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span><span class="sxs-lookup"><span data-stu-id="639dd-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="639dd-539">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="639dd-539">Windows 8  and later</span></span>
- <span data-ttu-id="639dd-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="639dd-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="639dd-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="639dd-542">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="639dd-542">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="639dd-543">FWPM_CONDITION_IP_SOURCE_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-543">FWPM_CONDITION_IP_SOURCE_PORT</span></span>
- <span data-ttu-id="639dd-544">FWPM_CONDITION_IP_DESTINATION_PORT</span><span class="sxs-lookup"><span data-stu-id="639dd-544">FWPM_CONDITION_IP_DESTINATION_PORT</span></span>
- <span data-ttu-id="639dd-545">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-545">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="639dd-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="639dd-547">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-547">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="639dd-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="639dd-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="639dd-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="639dd-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="639dd-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span></span>
- <span data-ttu-id="639dd-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="639dd-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="639dd-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="639dd-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>



## <a name="remarks"></a><span data-ttu-id="639dd-555">Commenti</span><span class="sxs-lookup"><span data-stu-id="639dd-555">Remarks</span></span>

<span data-ttu-id="639dd-556">I suffissi V4 e V6 alla fine degli identificatori di livello indicano se il livello si trova nello stack di rete IPv4 o nello stack di rete IPv6.</span><span class="sxs-lookup"><span data-stu-id="639dd-556">The V4 and V6 suffixes at the end of the layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="639dd-557">Requisiti</span><span class="sxs-lookup"><span data-stu-id="639dd-557">Requirements</span></span>



| <span data-ttu-id="639dd-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="639dd-558">Requirement</span></span> | <span data-ttu-id="639dd-559">Valore</span><span class="sxs-lookup"><span data-stu-id="639dd-559">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="639dd-560">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="639dd-560">Minimum supported client</span></span><br/> | <span data-ttu-id="639dd-561">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="639dd-561">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="639dd-562">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="639dd-562">Minimum supported server</span></span><br/> | <span data-ttu-id="639dd-563">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="639dd-563">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="639dd-564">Intestazione</span><span class="sxs-lookup"><span data-stu-id="639dd-564">Header</span></span><br/>                   | <dl> <span data-ttu-id="639dd-565"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="639dd-565"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





