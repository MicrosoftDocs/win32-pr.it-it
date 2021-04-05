---
title: Filtraggio degli identificatori di condizione (Fwpmu. h)
description: Gli identificatori della condizione di filtro Windows Filtering Platform (WFP) sono rappresentati da un GUID.
ms.assetid: 4f0b970a-e511-4107-8023-22a8775905b9
topic_type:
- apiref
api_name:
- FWPM_CONDITION_INTERFACE_MAC_ADDRESS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS
- FWPM_CONDITION_MAC_REMOTE_ADDRESS
- FWPM_CONDITION_ETHER_TYPE
- FWPM_CONDITION_VLAN_ID
- FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID
- FWPM_CONDITION_NDIS_PORT
- FWPM_CONDITION_NDIS_MEDIA_TYPE
- FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE
- FWPM_CONDITION_L2_FLAGS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_SOURCE_ADDRESS
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS
- FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_SOURCE_PORT
- FWPM_CONDITION_VSWITCH_ICMP_TYPE
- FWPM_CONDITION_IP_DESTINATION_PORT
- FWPM_CONDITION_VSWITCH_ICMP_CODE
- FWPM_CONDITION_VSWITCH_ID
- FWPM_CONDITION_VSWITCH_NETWORK_TYPE
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_SOURCE_VM_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE
- FWPM_CONDITION_INTERFACE
- FWPM_CONDITION_ALE_PACKAGE_ID
- FWPM_CONDITION_ALE_ORIGINAL_APP_ID
- FWPM_CONDITION_IP_NEXTHOP_ADDRESS
- FWPM_CONDITION_IP_NEXTHOP_INTERFACE
- FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE
- FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE
- FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX
- FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ORIGINAL_PROFILE_ID
- FWPM_CONDITION_CURRENT_PROFILE_ID
- FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID
- FWPM_CONDITION_REAUTHORIZE_REASON
- FWPM_CONDITION_ALE_REAUTH_REASON
- FWPM_CONDITION_ORIGINAL_ICMP_TYPE
- FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE
- FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE
- FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH
- FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY
- FWPM_CONDITION_IP_ARRIVAL_INTERFACE
- FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE
- FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE
- FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX
- FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_TYPE
- FWPM_CONDITION_LOCAL_TUNNEL_TYPE
- FWPM_CONDITION_IP_LOCAL_ADDRESS
- FWPM_CONDITION_IP_REMOTE_ADDRESS
- FWPM_CONDITION_IP_SOURCE_ADDRESS
- FWPM_CONDITION_IP_DESTINATION_ADDRESS
- FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_LOCAL_INTERFACE
- FWPM_CONDITION_INTERFACE_TYPE
- FWPM_CONDITION_TUNNEL_TYPE
- FWPM_CONDITION_IP_FORWARD_INTERFACE
- FWPM_CONDITION_IP_PROTOCOL
- FWPM_CONDITION_IP_LOCAL_PORT
- FWPM_CONDITION_ICMP_TYPE
- FWPM_CONDITION_IP_REMOTE_PORT
- FWPM_CONDITION_ICMP_CODE
- FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS
- FWPM_CONDITION_EMBEDDED_PROTOCOL
- FWPM_CONDITION_EMBEDDED_LOCAL_PORT
- FWPM_CONDITION_EMBEDDED_REMOTE_PORT
- FWPM_CONDITION_FLAGS
- FWPM_CONDITION_DIRECTION
- FWPM_CONDITION_INTERFACE_INDEX
- FWPM_CONDITION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ALE_APP_ID
- FWPM_CONDITION_ALE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_MACHINE_ID
- FWPM_CONDITION_ALE_PROMISCUOUS_MODE
- FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT
- FWPM_CONDITION_ALE_NAP_CONTEXT
- FWPM_CONDITION_QM_MODE
- FWPM_CONDITION_KM_AUTH_NAP_CONTEXT
- FWPM_CONDITION_PEER_NAME
- FWPM_CONDITION_REMOTE_ID
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_KM_TYPE
- FWPM_CONDITION_KM_MODE
- FWPM_CONDITION_IPSEC_POLICY_KEY
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_REMOTE_USER_TOKEN
- FWPM_CONDITION_RPC_IF_UUID
- FWPM_CONDITION_RPC_IF_VERSION
- FWPM_CONDITION_RPC_IF_FLAG
- FWPM_CONDITION_DCOM_APP_ID
- FWPM_CONDITION_IMAGE_NAME
- FWPM_CONDITION_RPC_PROTOCOL
- FWPM_CONDITION_RPC_AUTH_TYPE
- FWPM_CONDITION_RPC_AUTH_LEVEL
- FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM
- FWPM_CONDITION_SEC_KEY_SIZE
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V4
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V6
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V4
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V6
- FWPM_CONDITION_PIPE
- FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID
- FWPM_CONDITION_RPC_EP_VALUE
- FWPM_CONDITION_RPC_EP_FLAGS
- FWPM_CONDITION_CLIENT_TOKEN
- FWPM_CONDITION_RPC_SERVER_NAME
- FWPM_CONDITION_RPC_SERVER_PORT
- FWPM_CONDITION_RPC_PROXY_AUTH_TYPE
- FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH
- FWPM_CONDITION_CLIENT_CERT_OID
- FWPM_CONDITION_NET_EVENT_TYPE
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617946e5708bb982f96edcad155bcbf2509596dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739847"
---
# <a name="filtering-condition-identifiers"></a><span data-ttu-id="f6e95-103">Filtraggio degli identificatori di condizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-103">Filtering Condition Identifiers</span></span>

<span data-ttu-id="f6e95-104">Gli identificatori della condizione di filtro Windows Filtering Platform (WFP) sono rappresentati da un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="f6e95-104">The Windows Filtering Platform (WFP) filtering condition identifiers are each represented by a **GUID**.</span></span> <span data-ttu-id="f6e95-105">Il tipo di dati per il valore della condizione per ogni condizione di filtro viene specificato come [**\_ \_ tipo di dati FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="f6e95-105">The data type for the condition value for each filtering condition is specified as an [**FWP\_DATA\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="f6e95-106">Questi identificatori e i relativi tipi di dati sono definiti qui.</span><span class="sxs-lookup"><span data-stu-id="f6e95-106">These identifiers and their data types are defined here.</span></span>

<span data-ttu-id="f6e95-107">Le condizioni standard sono elencate per prime, seguite dalle condizioni specifiche per la modalità utente.</span><span class="sxs-lookup"><span data-stu-id="f6e95-107">The standard conditions are listed first, followed by the conditions specific to user mode.</span></span> <span data-ttu-id="f6e95-108">Le condizioni sono raggruppate in base al sistema operativo supportato, in modo che sia possibile stabilire facilmente quali condizioni sono supportate per un determinato sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f6e95-108">Conditions are grouped by supported operating system, so that you can easily tell which conditions are supported for a given OS.</span></span>

> [!Note]  
> <span data-ttu-id="f6e95-109">Ognuna delle seguenti condizioni di filtro è disponibile solo in un subset dei livelli di filtro WFP.</span><span class="sxs-lookup"><span data-stu-id="f6e95-109">Each of the following filtering conditions is available only at a subset of the WFP filtering layers.</span></span> <span data-ttu-id="f6e95-110">Per altre informazioni sulla disponibilità di ogni condizione a un determinato livello, vedere [**condizioni di filtro disponibili a ogni livello di filtro**](filtering-conditions-available-at-each-filtering-layer.md).</span><span class="sxs-lookup"><span data-stu-id="f6e95-110">For more information on each condition's availability at any given layer, see [**Filtering Conditions Available at Each Filtering Layer**](filtering-conditions-available-at-each-filtering-layer.md).</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f6e95-111">Condizioni disponibili per Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6e95-111">Conditions available for Windows 8 and Windows Server 2012</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f6e95-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <span data-ttu-id="f6e95-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-114">Indirizzo MAC di una particolare interfaccia locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-114">The MAC address of a particular local interface.</span></span><br/> <span data-ttu-id="f6e95-115"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-115"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <span data-ttu-id="f6e95-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-117">Indirizzo di destinazione di un frame in ingresso o indirizzo di origine di un frame in uscita.</span><span class="sxs-lookup"><span data-stu-id="f6e95-117">Destination address of an inbound frame, or source address of an outbound frame.</span></span><br/> <span data-ttu-id="f6e95-118"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-118"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <span data-ttu-id="f6e95-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-120">Indirizzo di origine di un frame in ingresso o indirizzo di destinazione di un frame in uscita.</span><span class="sxs-lookup"><span data-stu-id="f6e95-120">Source address of an inbound frame, or destination address of an outbound frame.</span></span><br/> <span data-ttu-id="f6e95-121"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-121"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <span data-ttu-id="f6e95-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-123">Tipo di dati del payload di rete Ethernet V2.</span><span class="sxs-lookup"><span data-stu-id="f6e95-123">The Ethernet V2 network payload data type.</span></span> <span data-ttu-id="f6e95-124">(Vedere ETHERNET_TYPE_IPV4 e così via in netiodef. h).</span><span class="sxs-lookup"><span data-stu-id="f6e95-124">(See ETHERNET_TYPE_IPV4, etc. in netiodef.h.)</span></span><br/> <span data-ttu-id="f6e95-125"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-125"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <span data-ttu-id="f6e95-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-127">L'intestazione della VLAN a 16 bit, inclusi i campi VID, CFI e Priority, in base allo standard 802.1 q (vedere VLAN_TAG in netiodef. h per le posizioni del campi).</span><span class="sxs-lookup"><span data-stu-id="f6e95-127">The 16-bits of VLAN header including the VID, CFI, and Priority fields as per the 802.1q standard (see VLAN_TAG in netiodef.h for the positions of the bitfields).</span></span><br/> <span data-ttu-id="f6e95-128"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-128"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <span data-ttu-id="f6e95-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-130">Identificatore univoco per la rete vSwitch.</span><span class="sxs-lookup"><span data-stu-id="f6e95-130">Unique identifier for the vSwitch network.</span></span> <span data-ttu-id="f6e95-131">Non può essere usato in combinazione con VLAN_IDs.</span><span class="sxs-lookup"><span data-stu-id="f6e95-131">Cannot be used in conjunction with VLAN_IDs.</span></span><br/> <span data-ttu-id="f6e95-132"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-132"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <span data-ttu-id="f6e95-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-134">Numero di porta della porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="f6e95-134">The port number of the NDIS port.</span></span><br/> <span data-ttu-id="f6e95-135"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-135"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <span data-ttu-id="f6e95-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-137">Tipo di supporto della porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="f6e95-137">The media type of the NDIS port.</span></span><br/> <span data-ttu-id="f6e95-138"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-138"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="f6e95-139"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>NDIS_MEDIUM</strong> .</span><span class="sxs-lookup"><span data-stu-id="f6e95-139"><strong>Possible values:</strong> Any of the <strong>NDIS_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="f6e95-140">(Vedere Ntddndis. h).</span><span class="sxs-lookup"><span data-stu-id="f6e95-140">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <span data-ttu-id="f6e95-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-142">Tipo di supporto fisico della porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="f6e95-142">The physical media type of the NDIS port.</span></span><br/> <span data-ttu-id="f6e95-143"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-143"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="f6e95-144"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>NDIS_PHYSICAL_MEDIUM</strong> .</span><span class="sxs-lookup"><span data-stu-id="f6e95-144"><strong>Possible values:</strong> Any of the <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="f6e95-145">(Vedere Ntddndis. h).</span><span class="sxs-lookup"><span data-stu-id="f6e95-145">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <span data-ttu-id="f6e95-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-147">OR bit per bit di una combinazione di flag di condizione di filtro.</span><span class="sxs-lookup"><span data-stu-id="f6e95-147">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="f6e95-148"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-148"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="f6e95-149"><strong>Valori possibili:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-149"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span><span class="sxs-lookup"><span data-stu-id="f6e95-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span></span></li>
<li><span data-ttu-id="f6e95-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="f6e95-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span></span></li>
<li><span data-ttu-id="f6e95-152">FWP_CONDITION_L2_IS_WIFI</span><span class="sxs-lookup"><span data-stu-id="f6e95-152">FWP_CONDITION_L2_IS_WIFI</span></span></li>
<li><span data-ttu-id="f6e95-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span><span class="sxs-lookup"><span data-stu-id="f6e95-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <span data-ttu-id="f6e95-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-155">Tipo di indirizzo dell'indirizzo locale fisico.</span><span class="sxs-lookup"><span data-stu-id="f6e95-155">The address type of the physical local address.</span></span><br/> <span data-ttu-id="f6e95-156"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-156"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="f6e95-157"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-157"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-158">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-158">DlUnicast</span></span></li>
<li><span data-ttu-id="f6e95-159">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-159">DlMulticast</span></span></li>
<li><span data-ttu-id="f6e95-160">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-160">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <span data-ttu-id="f6e95-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-162">Tipo di indirizzo dell'indirizzo remoto fisico.</span><span class="sxs-lookup"><span data-stu-id="f6e95-162">The address type of the physical remote address.</span></span><br/> <span data-ttu-id="f6e95-163"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-163"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="f6e95-164"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-164"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-165">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-165">DlUnicast</span></span></li>
<li><span data-ttu-id="f6e95-166">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-166">DlMulticast</span></span></li>
<li><span data-ttu-id="f6e95-167">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-167">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <span data-ttu-id="f6e95-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-169">Indirizzo di origine fisico di un frame.</span><span class="sxs-lookup"><span data-stu-id="f6e95-169">The physical source address of a frame.</span></span><br/> <span data-ttu-id="f6e95-170"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-170"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <span data-ttu-id="f6e95-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-172">Indirizzo di destinazione fisico di un frame.</span><span class="sxs-lookup"><span data-stu-id="f6e95-172">The physical destination address of a frame.</span></span><br/> <span data-ttu-id="f6e95-173"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-173"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <span data-ttu-id="f6e95-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-175">Tipo di indirizzo dell'indirizzo di destinazione fisico.</span><span class="sxs-lookup"><span data-stu-id="f6e95-175">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="f6e95-176"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-176"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="f6e95-177"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-177"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-178">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-178">DlUnicast</span></span></li>
<li><span data-ttu-id="f6e95-179">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-179">DlMulticast</span></span></li>
<li><span data-ttu-id="f6e95-180">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-180">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <span data-ttu-id="f6e95-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-182">Tipo di indirizzo dell'indirizzo di destinazione fisico.</span><span class="sxs-lookup"><span data-stu-id="f6e95-182">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="f6e95-183"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-183"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="f6e95-184"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-184"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-185">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-185">DlUnicast</span></span></li>
<li><span data-ttu-id="f6e95-186">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-186">DlMulticast</span></span></li>
<li><span data-ttu-id="f6e95-187">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-187">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <span data-ttu-id="f6e95-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-189">Porta di origine del trasporto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-189">The source port of the packet's transport.</span></span><br/> <span data-ttu-id="f6e95-190"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-190"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <span data-ttu-id="f6e95-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-192">Il campo di tipo ICMP, come specificato nella RFC 792.</span><span class="sxs-lookup"><span data-stu-id="f6e95-192">The ICMP type field, as specified in RFC 792.</span></span><br/> <span data-ttu-id="f6e95-193"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-193"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <span data-ttu-id="f6e95-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-195">Porta di destinazione del trasporto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-195">The destination port of the packet's transport.</span></span><br/> <span data-ttu-id="f6e95-196"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-196"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <span data-ttu-id="f6e95-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-198">Il campo del codice ICMP, come specificato nella RFC 792.</span><span class="sxs-lookup"><span data-stu-id="f6e95-198">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="f6e95-199"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-199"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <span data-ttu-id="f6e95-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-201">Identificatore univoco di un'istanza di vSwitch.</span><span class="sxs-lookup"><span data-stu-id="f6e95-201">Unique identifier of an vSwitch instance.</span></span><br/> <span data-ttu-id="f6e95-202"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-202"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <span data-ttu-id="f6e95-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-204">Specifica se l'istanza di vSwitch fa parte di una rete virtuale esterna, interna o privata.</span><span class="sxs-lookup"><span data-stu-id="f6e95-204">Specifies whether the vSwitch instance is part of an external, internal, or private virtual network.</span></span><br/> <span data-ttu-id="f6e95-205"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-205"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <span data-ttu-id="f6e95-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-207">Identificatore univoco dell'origine del pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="f6e95-207">Unique identifier of the source of the current packet.</span></span> <span data-ttu-id="f6e95-208">(Il nome di una VM-NIC, P-NIC o V-NIC).</span><span class="sxs-lookup"><span data-stu-id="f6e95-208">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="f6e95-209"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-209"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <span data-ttu-id="f6e95-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-211">Identificatore univoco della destinazione del pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="f6e95-211">Unique identifier of the destination of the current packet.</span></span> <span data-ttu-id="f6e95-212">(Il nome di una VM-NIC, P-NIC o V-NIC).</span><span class="sxs-lookup"><span data-stu-id="f6e95-212">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="f6e95-213"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-213"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <span data-ttu-id="f6e95-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-215">Identificatore univoco della macchina virtuale di origine vSwitch.</span><span class="sxs-lookup"><span data-stu-id="f6e95-215">Unique identifier of the vSwitch source virtual machine.</span></span><br/> <span data-ttu-id="f6e95-216"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-216"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <span data-ttu-id="f6e95-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-218">Identificatore univoco della macchina virtuale di destinazione vSwitch.</span><span class="sxs-lookup"><span data-stu-id="f6e95-218">Unique identifier of the vSwitch destination virtual machine.</span></span><br/> <span data-ttu-id="f6e95-219"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-219"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <span data-ttu-id="f6e95-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-221">Tipo di interfaccia dell'origine del pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="f6e95-221">Interface type of the source of the current packet.</span></span><br/> <span data-ttu-id="f6e95-222"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-222"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="f6e95-223"><strong>Valori possibili:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-223"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-224">SwitchNicSyntheticNic (quando il tipo di interfaccia è VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="f6e95-224">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="f6e95-225">SwitchNicEmulatedNic (quando il tipo di interfaccia è VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="f6e95-225">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="f6e95-226">SwitchNicPhysicalNic (quando il tipo di interfaccia è P-NIC)</span><span class="sxs-lookup"><span data-stu-id="f6e95-226">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="f6e95-227">SwitchNicVNic (quando il tipo di interfaccia è V-NIC, connesso alla partizione host)</span><span class="sxs-lookup"><span data-stu-id="f6e95-227">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <span data-ttu-id="f6e95-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-229">Tipo di interfaccia della destinazione del pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="f6e95-229">Interface type of the destination of the current packet.</span></span><br/> <span data-ttu-id="f6e95-230"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-230"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="f6e95-231"><strong>Valori possibili:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-231"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-232">SwitchNicSyntheticNic (quando il tipo di interfaccia è VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="f6e95-232">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="f6e95-233">SwitchNicEmulatedNic (quando il tipo di interfaccia è VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="f6e95-233">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="f6e95-234">SwitchNicPhysicalNic (quando il tipo di interfaccia è P-NIC)</span><span class="sxs-lookup"><span data-stu-id="f6e95-234">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="f6e95-235">SwitchNicVNic (quando il tipo di interfaccia è V-NIC, connesso alla partizione host)</span><span class="sxs-lookup"><span data-stu-id="f6e95-235">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <span data-ttu-id="f6e95-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-237">LUID per l'interfaccia di rete associata all'indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-237">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="f6e95-238"><strong>Tipo di dati:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="f6e95-238"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <span data-ttu-id="f6e95-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-240">ID di sicurezza (SID) di un contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="f6e95-240">The security identifier (SID) of an app container.</span></span><br/> <span data-ttu-id="f6e95-241"><strong>Tipo di dati:</strong> FWP_SID</span><span class="sxs-lookup"><span data-stu-id="f6e95-241"><strong>Data type:</strong> FWP_SID</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <span data-ttu-id="f6e95-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-243">Percorso completo del dispositivo dell'applicazione, ad esempio &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="f6e95-243">The fully qualified device path of the application, such as &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.</span></span> <span data-ttu-id="f6e95-244">Quando una connessione è stata reindirizzata, questo sarà l'identificatore dell'app di origine. in caso contrario, sarà uguale a <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span><span class="sxs-lookup"><span data-stu-id="f6e95-244">When a connection has been redirected, this will be the identifier of the originating app; otherwise this will be the same as <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span></span><br/> <span data-ttu-id="f6e95-245"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-245"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
</tbody>
</table>





| <span data-ttu-id="f6e95-246">Condizioni disponibili per Windows 7, Windows Server 2008 R2 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f6e95-246">Conditions available for Windows 7, Windows Server 2008 R2, and later</span></span>                                                                                                                                                                                                    | <span data-ttu-id="f6e95-247">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-247">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <span data-ttu-id="f6e95-248"><dt>**\_ \_ \_ Indirizzo NEXTHOP IP della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-248"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_ADDRESS**</dt></span></span> </dl>                                             | <span data-ttu-id="f6e95-249">Indirizzo IP dell'interfaccia hop successiva.</span><span class="sxs-lookup"><span data-stu-id="f6e95-249">The IP address of the next-hop interface.</span></span><br/> <span data-ttu-id="f6e95-250">**Tipo di dati:** \_Maschera FWP V4 \_ addr \_</span><span class="sxs-lookup"><span data-stu-id="f6e95-250">**Data type:** FWP\_V4\_ADDR\_MASK</span></span><br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <span data-ttu-id="f6e95-251"><dt>**interfaccia NEXTHOP di FWPM \_ Condition \_ IP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-251"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>                                       | <span data-ttu-id="f6e95-252">Interfaccia hop successiva da cui il pacchetto verrà ripartito.</span><span class="sxs-lookup"><span data-stu-id="f6e95-252">The next-hop interface from which the packet will be departing.</span></span> <br/> <span data-ttu-id="f6e95-253">**Tipo di dati:** FWP \_ UInt64</span><span class="sxs-lookup"><span data-stu-id="f6e95-253">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <span data-ttu-id="f6e95-254"><dt>**FWPM \_ Condition \_ NEXTHOP \_ - \_ tipo interfaccia**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-254"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_TYPE**</dt></span></span> </dl>                                 | <span data-ttu-id="f6e95-255">Tipo di interfaccia dell'interfaccia hop successiva.</span><span class="sxs-lookup"><span data-stu-id="f6e95-255">The interface type of the next-hop interface.</span></span><br/> <span data-ttu-id="f6e95-256">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-256">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <span data-ttu-id="f6e95-257"><dt>**\_tipo di \_ \_ tunnel NEXTHOP della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-257"><dt>**FWPM\_CONDITION\_NEXTHOP\_TUNNEL\_TYPE**</dt></span></span> </dl>                                          | <span data-ttu-id="f6e95-258">Tipo di tunnel dell'interfaccia hop successiva.</span><span class="sxs-lookup"><span data-stu-id="f6e95-258">The tunnel type of the next-hop interface.</span></span><br/> <span data-ttu-id="f6e95-259">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-259">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <span data-ttu-id="f6e95-260"><dt>**\_indice dell' \_ \_ interfaccia NEXTHOP della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-260"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_INDEX**</dt></span></span> </dl>                              | <span data-ttu-id="f6e95-261">Indice di interfaccia dell'interfaccia hop successiva.</span><span class="sxs-lookup"><span data-stu-id="f6e95-261">The interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="f6e95-262">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-262">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <span data-ttu-id="f6e95-263"><dt>**FWPM \_ Condition \_ NEXTHOP \_ \_ indice secondario interfaccia \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-263"><dt>**FWPM\_CONDITION\_NEXTHOP\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl>                 | <span data-ttu-id="f6e95-264">Indice dell'interfaccia secondaria dell'interfaccia hop successiva.</span><span class="sxs-lookup"><span data-stu-id="f6e95-264">The sub-interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="f6e95-265">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-265">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <span data-ttu-id="f6e95-266"><dt>**\_ \_ \_ ID profilo originale della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-266"><dt>**FWPM\_CONDITION\_ORIGINAL\_PROFILE\_ID**</dt></span></span> </dl>                                          | <span data-ttu-id="f6e95-267">Categoria di rete dell'interfaccia di arrivo o di hop successivo tramite la quale viene creato il flusso di ALE (in entrata o in uscita).</span><span class="sxs-lookup"><span data-stu-id="f6e95-267">The network category of the arrival or next-hop interface through which the ALE flow (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="f6e95-268">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-268">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <span data-ttu-id="f6e95-269"><dt>**\_ \_ \_ ID profilo corrente della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-269"><dt>**FWPM\_CONDITION\_CURRENT\_PROFILE\_ID**</dt></span></span> </dl>                                             | <span data-ttu-id="f6e95-270">Categoria di rete dell'interfaccia di arrivo o di hop successivo tramite la quale viene creato il pacchetto corrente (in entrata o in uscita).</span><span class="sxs-lookup"><span data-stu-id="f6e95-270">The network category of the arrival or next-hop interface through which the current packet (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="f6e95-271">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-271">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <span data-ttu-id="f6e95-272"><dt>**\_ \_ \_ \_ ID profilo interfaccia locale della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-272"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>                    | <span data-ttu-id="f6e95-273">Categoria di rete dell'interfaccia di recapito.</span><span class="sxs-lookup"><span data-stu-id="f6e95-273">The network category of the delivery interface.</span></span><br/> <span data-ttu-id="f6e95-274">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-274">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <span data-ttu-id="f6e95-275"><dt>**\_ \_ \_ \_ ID profilo interfaccia arrivo condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-275"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="f6e95-276">Categoria di rete dell'interfaccia di arrivo.</span><span class="sxs-lookup"><span data-stu-id="f6e95-276">The network category of the arrival interface.</span></span><br/> <span data-ttu-id="f6e95-277">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-277">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <span data-ttu-id="f6e95-278"><dt>**FWPM \_ Condition \_ NEXTHOP \_ \_ ID profilo \_ interfaccia**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-278"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="f6e95-279">Categoria di rete dell'interfaccia hop successiva.</span><span class="sxs-lookup"><span data-stu-id="f6e95-279">The network category of the next-hop interface.</span></span><br/> <span data-ttu-id="f6e95-280">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-280">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <span data-ttu-id="f6e95-281"><dt>**\_motivo della \_ Riautorizzazione della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-281"><dt>**FWPM\_CONDITION\_REAUTHORIZE\_REASON**</dt></span></span> </dl>                                              | <span data-ttu-id="f6e95-282">Motivo della Riautorizzazione di una connessione precedentemente autorizzata.</span><span class="sxs-lookup"><span data-stu-id="f6e95-282">The reason for reauthorizing a previously authorized connection.</span></span><br/> <span data-ttu-id="f6e95-283">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-283">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <span data-ttu-id="f6e95-284"><dt>**\_motivo della \_ \_ riautenticazione ale della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-284"><dt>**FWPM\_CONDITION\_ALE\_REAUTH\_REASON**</dt></span></span> </dl>                                                | <span data-ttu-id="f6e95-285">Il motivo per cui è stata riautorizzata una connessione precedentemente autorizzata, ad esempio la **\_ \_ \_ \_ \_ modifica del criterio di Riautorizzazione della condizione FWP** (o uno degli altri valori elencati nei flag di condizione di [**filtro**](filtering-condition-flags-.md)).</span><span class="sxs-lookup"><span data-stu-id="f6e95-285">The reason for reauthorizing a previously authorized connection, such as **FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE** (or one of the other values listed in [**Filtering Condition Flags**](filtering-condition-flags-.md)).</span></span><br/> <span data-ttu-id="f6e95-286">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-286">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <span data-ttu-id="f6e95-287"><dt>**\_ \_ \_ tipo ICMP originale della condizione FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-287"><dt>**FWPM\_CONDITION\_ORIGINAL\_ICMP\_TYPE**</dt></span></span> </dl>                                             | <span data-ttu-id="f6e95-288">Tipo ICMP con cui è stato creato il flusso.</span><span class="sxs-lookup"><span data-stu-id="f6e95-288">The ICMP type with which the flow was created.</span></span><br/> <span data-ttu-id="f6e95-289">**Tipo di dati:** FWP \_ UInt16</span><span class="sxs-lookup"><span data-stu-id="f6e95-289">**Data type:** FWP\_UINT16</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <span data-ttu-id="f6e95-290"><dt>**\_interfaccia di \_ \_ arrivo fisica \_ IP \_ della condizione FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-290"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="f6e95-291">LUID dell'interfaccia fisica associata all'indirizzo IP di arrivo.</span><span class="sxs-lookup"><span data-stu-id="f6e95-291">The LUID of the physical interface associated with the arrival IP address.</span></span><br/> <span data-ttu-id="f6e95-292">**Tipo di dati:** FWP \_ UInt64</span><span class="sxs-lookup"><span data-stu-id="f6e95-292">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <span data-ttu-id="f6e95-293"><dt>**FWPM \_ Condition \_ IP \_ - \_ interfaccia NEXTHOP fisica \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-293"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="f6e95-294">LUID dell'interfaccia fisica dell'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="f6e95-294">The LUID of the physical interface of the next hop.</span></span><br/> <span data-ttu-id="f6e95-295">**Tipo di dati:** FWP \_ UInt64</span><span class="sxs-lookup"><span data-stu-id="f6e95-295">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <span data-ttu-id="f6e95-296"><dt>**\_epoca di \_ quarantena dell'interfaccia della condizione FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-296"><dt>**FWPM\_CONDITION\_INTERFACE\_QUARANTINE\_EPOCH**</dt></span></span> </dl>                     | <span data-ttu-id="f6e95-297">Numero di Epoch associato a un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f6e95-297">The epoch count associated with an interface.</span></span> <span data-ttu-id="f6e95-298">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f6e95-298">Reserved.</span></span><br/> <span data-ttu-id="f6e95-299">**Tipo di dati:** FWP \_ UInt64</span><span class="sxs-lookup"><span data-stu-id="f6e95-299">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <span data-ttu-id="f6e95-300"><dt>**\_proprietà del socket del firewall della condizione FWPM \_ ale \_ sio \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-300"><dt>**FWPM\_CONDITION\_ALE\_SIO\_FIREWALL\_SOCKET\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="f6e95-301">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-301">Reserved for internal use.</span></span> <br/> <span data-ttu-id="f6e95-302">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-302">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                              |





| <span data-ttu-id="f6e95-303">Costanti disponibili per Windows Vista con SP1, Windows Server 2008 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f6e95-303">Constants available for Windows Vista with SP1, Windows Server 2008, and later</span></span>                                                                                                                                                                           | <span data-ttu-id="f6e95-304">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-304">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <span data-ttu-id="f6e95-305"><dt>**\_interfaccia di \_ \_ arrivo IP della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-305"><dt>**FWPM\_CONDITION\_IP\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>                       | <span data-ttu-id="f6e95-306">LUID per l'interfaccia di rete associata all'indirizzo IP di arrivo.</span><span class="sxs-lookup"><span data-stu-id="f6e95-306">The LUID for the network interface associated with the arrival IP address.</span></span> <br/> <span data-ttu-id="f6e95-307">**Tipo di dati:** FWP \_ UInt64</span><span class="sxs-lookup"><span data-stu-id="f6e95-307">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <span data-ttu-id="f6e95-308"><dt>**\_tipo di \_ interfaccia di arrivo della condizione FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-308"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                 | <span data-ttu-id="f6e95-309">Tipo di interfaccia di rete di arrivo come definito da IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="f6e95-309">The type of the arrival network interface as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="f6e95-310">Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="f6e95-310">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="f6e95-311">**Valori possibili:** Valori del tipo di interfaccia elencati nel file di intestazione Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="f6e95-311">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="f6e95-312">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-312">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <span data-ttu-id="f6e95-313"><dt>**FWPM \_ \_tipo di \_ tunnel \_ di arrivo della condizione**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-313"><dt> **FWPM\_CONDITION\_ARRIVAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="f6e95-314">Metodo di incapsulamento usato da un tunnel associato all'interfaccia di rete di arrivo se il membro del tipo è se il \_ tunnel del tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="f6e95-314">The encapsulation method used by a tunnel associated with the arrival network interface if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="f6e95-315">Il tipo di tunnel è definito da IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="f6e95-315">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="f6e95-316">Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="f6e95-316">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="f6e95-317">**Valori possibili:** Valori del \_ tipo di enumerazione del tipo di tunnel elencati nel file di intestazione ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="f6e95-317">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="f6e95-318">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-318">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <span data-ttu-id="f6e95-319"><dt>**\_ \_ indice dell'interfaccia di arrivo della condizione FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-319"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_INDEX**</dt></span></span> </dl>              | <span data-ttu-id="f6e95-320">Indice dell'interfaccia di rete di arrivo, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-320">The index of the arrival network interface, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="f6e95-321">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-321">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <span data-ttu-id="f6e95-322"><dt>**\_ \_ \_ indice dell'interfaccia secondaria \_ di arrivo della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-322"><dt>**FWPM\_CONDITION\_ARRIVAL\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl> | <span data-ttu-id="f6e95-323">Indice dell'interfaccia di rete di arrivo, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-323">The index of the arrival network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-324">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-324">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <span data-ttu-id="f6e95-325"><dt>**\_indice dell' \_ \_ interfaccia locale della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-325"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_INDEX**</dt></span></span> </dl>                    | <span data-ttu-id="f6e95-326">Indice dell'interfaccia di rete, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-326">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-327">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-327">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <span data-ttu-id="f6e95-328"><dt>**\_tipo di \_ \_ interfaccia locale della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-328"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="f6e95-329">Il tipo di interfaccia definito da IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="f6e95-329">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="f6e95-330">Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="f6e95-330">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="f6e95-331">**Valori possibili:** Valori del tipo di interfaccia elencati nel file di intestazione Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="f6e95-331">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="f6e95-332">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-332">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <span data-ttu-id="f6e95-333"><dt>**\_tipo di \_ \_ tunnel locale della condizione \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-333"><dt>**FWPM\_CONDITION\_LOCAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                                | <span data-ttu-id="f6e95-334">Metodo di incapsulamento usato da un tunnel se il membro del tipo è se il \_ tunnel del tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="f6e95-334">The encapsulation method used by a tunnel if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="f6e95-335">Il tipo di tunnel è definito da IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="f6e95-335">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="f6e95-336">Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="f6e95-336">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="f6e95-337">**Valori possibili:** Valori del \_ tipo di enumerazione del tipo di tunnel elencati nel file di intestazione ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="f6e95-337">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="f6e95-338">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-338">**Data type:** FWP\_UINT32</span></span> <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f6e95-339">Costanti disponibili per Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f6e95-339">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f6e95-340">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-340">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <span data-ttu-id="f6e95-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-342">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-342">The local IP address.</span></span> <br/> <span data-ttu-id="f6e95-343"><strong>Tipo di dati:</strong> Per un indirizzo IPv4</span><span class="sxs-lookup"><span data-stu-id="f6e95-343"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-344">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-344">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-345">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-345">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-346"><strong>Tipo di dati:</strong> Per un indirizzo IPv6</span><span class="sxs-lookup"><span data-stu-id="f6e95-346"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-347">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-347">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-348">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-348">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <span data-ttu-id="f6e95-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-350">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-350">The remote IP address.</span></span> <br/> <span data-ttu-id="f6e95-351"><strong>Tipo di dati:</strong> Per un indirizzo IPv4</span><span class="sxs-lookup"><span data-stu-id="f6e95-351"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-352">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-352">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-353">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-353">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-354"><strong>Tipo di dati:</strong> Per un indirizzo IPv6</span><span class="sxs-lookup"><span data-stu-id="f6e95-354"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-355">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-355">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-356">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-356">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <span data-ttu-id="f6e95-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-358">Indirizzo IP di origine per i pacchetti inoltrati.</span><span class="sxs-lookup"><span data-stu-id="f6e95-358">The source IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="f6e95-359"><strong>Tipo di dati:</strong> Per un indirizzo IPv4</span><span class="sxs-lookup"><span data-stu-id="f6e95-359"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-360">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-360">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-361">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-361">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-362"><strong>Tipo di dati:</strong> Per un indirizzo IPv6</span><span class="sxs-lookup"><span data-stu-id="f6e95-362"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-363">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-363">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-364">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-364">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <span data-ttu-id="f6e95-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-366">Indirizzo IP di destinazione per i pacchetti inoltrati.</span><span class="sxs-lookup"><span data-stu-id="f6e95-366">The destination IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="f6e95-367"><strong>Tipo di dati:</strong> Per un indirizzo IPv4</span><span class="sxs-lookup"><span data-stu-id="f6e95-367"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-368">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-368">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-369">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-369">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-370"><strong>Tipo di dati:</strong> Per un indirizzo IPv6</span><span class="sxs-lookup"><span data-stu-id="f6e95-370"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-371">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-371">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-372">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-372">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <span data-ttu-id="f6e95-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-374">Tipo di indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-374">The local IP address type.</span></span> <br/> <span data-ttu-id="f6e95-375"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-375"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-376">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="f6e95-376">NlatUnspecified</span></span></li>
<li><span data-ttu-id="f6e95-377">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-377">NlatUnicast</span></span></li>
<li><span data-ttu-id="f6e95-378">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="f6e95-378">NlatAnycast</span></span></li>
<li><span data-ttu-id="f6e95-379">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-379">NlatMulticast</span></span></li>
<li><span data-ttu-id="f6e95-380">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-380">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-381"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-381"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <span data-ttu-id="f6e95-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-383">Tipo di indirizzo IP di destinazione per i pacchetti inoltrati.</span><span class="sxs-lookup"><span data-stu-id="f6e95-383">The destination IP address type for forwarded packets.</span></span> <br/> <span data-ttu-id="f6e95-384"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-384"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-385">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="f6e95-385">NlatUnspecified</span></span></li>
<li><span data-ttu-id="f6e95-386">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-386">NlatUnicast</span></span></li>
<li><span data-ttu-id="f6e95-387">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="f6e95-387">NlatAnycast</span></span></li>
<li><span data-ttu-id="f6e95-388">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-388">NlatMulticast</span></span></li>
<li><span data-ttu-id="f6e95-389">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-389">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-390"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-390"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <span data-ttu-id="f6e95-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-392">LUID per l'interfaccia di rete associata all'indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-392">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="f6e95-393"><strong>Tipo di dati:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="f6e95-393"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <span data-ttu-id="f6e95-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-395">Il tipo di interfaccia definito da IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="f6e95-395">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="f6e95-396">Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="f6e95-396">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="f6e95-397"><strong>Valori possibili:</strong> Valori del tipo di interfaccia elencati nel file di intestazione Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="f6e95-397"><strong>Possible values:</strong> The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="f6e95-398"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-398"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <span data-ttu-id="f6e95-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-400">Metodo di incapsulamento utilizzato da un tunnel se il membro del tipo è IF_TYPE_TUNNEL.</span><span class="sxs-lookup"><span data-stu-id="f6e95-400">The encapsulation method used by a tunnel if the Type member is IF_TYPE_TUNNEL.</span></span> <span data-ttu-id="f6e95-401">Il tipo di tunnel è definito da IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="f6e95-401">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="f6e95-402">Per altre informazioni, vedere <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span><span class="sxs-lookup"><span data-stu-id="f6e95-402">For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span></span> <br/> <span data-ttu-id="f6e95-403"><strong>Valori possibili:</strong> I valori del tipo di enumerazione TUNNEL_TYPE elencati nel file di intestazione ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="f6e95-403"><strong>Possible values:</strong> The TUNNEL_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="f6e95-404"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-404"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <span data-ttu-id="f6e95-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-406">LUID per l'interfaccia di rete in cui deve essere inviato il pacchetto inoltrato.</span><span class="sxs-lookup"><span data-stu-id="f6e95-406">The LUID for the network interface on which the packet being forwarded is to be sent out.</span></span> <br/> <span data-ttu-id="f6e95-407"><strong>Tipo di dati:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="f6e95-407"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <span data-ttu-id="f6e95-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-409">Il numero di protocollo IP, come specificato nella RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="f6e95-409">The IP protocol number, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="f6e95-410"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-410"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <span data-ttu-id="f6e95-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-412">Numero di porta del protocollo di trasporto locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-412">The local transport protocol port number.</span></span><br/> <span data-ttu-id="f6e95-413"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-413"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <span data-ttu-id="f6e95-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-415">Il campo di tipo ICMP, come specificato nella RFC 792.</span><span class="sxs-lookup"><span data-stu-id="f6e95-415">The ICMP type field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="f6e95-416"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-416"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <span data-ttu-id="f6e95-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-418">Numero di porta del protocollo di trasporto remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-418">The remote transport protocol port number.</span></span> <br/> <span data-ttu-id="f6e95-419"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-419"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <span data-ttu-id="f6e95-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-421">Il campo del codice ICMP, come specificato nella RFC 792.</span><span class="sxs-lookup"><span data-stu-id="f6e95-421">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="f6e95-422"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-422"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <span data-ttu-id="f6e95-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-424">Tipo di indirizzo IP locale incorporato nel pacchetto ICMP.</span><span class="sxs-lookup"><span data-stu-id="f6e95-424">The local IP address type that is embedded in the ICMP packet.</span></span><br/> <span data-ttu-id="f6e95-425"><strong>Valori possibili:</strong> Uno dei valori di enumerazione <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6e95-425"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="f6e95-426">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="f6e95-426">NlatUnspecified</span></span></li>
<li><span data-ttu-id="f6e95-427">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="f6e95-427">NlatUnicast</span></span></li>
<li><span data-ttu-id="f6e95-428">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="f6e95-428">NlatAnycast</span></span></li>
<li><span data-ttu-id="f6e95-429">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="f6e95-429">NlatMulticast</span></span></li>
<li><span data-ttu-id="f6e95-430">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="f6e95-430">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-431"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-431"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <span data-ttu-id="f6e95-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-433">Indirizzo IP remoto incorporato nel pacchetto ICMP.</span><span class="sxs-lookup"><span data-stu-id="f6e95-433">The remote IP address that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="f6e95-434"><strong>Tipo di dati:</strong> Per un indirizzo IPv4</span><span class="sxs-lookup"><span data-stu-id="f6e95-434"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-435">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-435">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-436">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-436">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-437"><strong>Tipo di dati:</strong> Per un indirizzo IPv6</span><span class="sxs-lookup"><span data-stu-id="f6e95-437"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="f6e95-438">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-438">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-439">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-439">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <span data-ttu-id="f6e95-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-441">Il numero di protocollo IP incorporato nel pacchetto ICMP, come specificato nella RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="f6e95-441">The IP protocol number that is embedded in the ICMP packet, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="f6e95-442"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-442"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <span data-ttu-id="f6e95-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-444">Numero di porta del protocollo di trasporto locale incorporato nel pacchetto ICMP.</span><span class="sxs-lookup"><span data-stu-id="f6e95-444">The local transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="f6e95-445"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-445"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <span data-ttu-id="f6e95-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-447">Numero di porta del protocollo di trasporto remoto incorporato nel pacchetto ICMP.</span><span class="sxs-lookup"><span data-stu-id="f6e95-447">The remote transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="f6e95-448"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-448"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <span data-ttu-id="f6e95-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-450">OR bit per bit di una combinazione di flag di condizione di filtro.</span><span class="sxs-lookup"><span data-stu-id="f6e95-450">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="f6e95-451"><strong>Valori possibili:</strong> Vedere <a href="filtering-condition-flags-.md"> <strong>flag della condizione di filtro</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6e95-451"><strong>Possible values:</strong> See <a href="filtering-condition-flags-.md"><strong>Filtering Condition Flags</strong></a></span></span><br/> <span data-ttu-id="f6e95-452"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-452"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <span data-ttu-id="f6e95-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-454">Direzione del traffico o del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="f6e95-454">The direction of the traffic or data flow.</span></span> <br/> <span data-ttu-id="f6e95-455"><strong>Valori possibili:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-455"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-456">FWP_DIRECTION_INBOUND</span><span class="sxs-lookup"><span data-stu-id="f6e95-456">FWP_DIRECTION_INBOUND</span></span></li>
<li><span data-ttu-id="f6e95-457">FWP_DIRECTION_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="f6e95-457">FWP_DIRECTION_OUTBOUND</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-458">Per i livelli di datagramma (FWPM_LAYER_DATAGRAM_DATA_ *) e i livelli di pacchetti di flusso (FWPM_LAYER_STREAM_PACKET_*), il valore sarà uguale a quello della direzione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-458">For datagram layers (FWPM_LAYER_DATAGRAM_DATA_ *) and stream packet layers (FWPM_LAYER_STREAM_PACKET_*), the value will be the same as the direction of the packet.</span></span> <br/> <span data-ttu-id="f6e95-459">Per i livelli di flusso (FWPM_LAYER_STREAM_ *) e i livelli stabiliti dal flusso (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), il valore sarà uguale alla direzione della connessione.</span><span class="sxs-lookup"><span data-stu-id="f6e95-459">For stream layers (FWPM_LAYER_STREAM_ *) and flow established layers (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), the value will be the same as direction of the connection.</span></span> <span data-ttu-id="f6e95-460">Ad esempio, quando un'applicazione locale avvia la connessione, un pacchetto in ingresso ha <strong>FWPM_CONDITION_DIRECTION</strong> impostato su <strong>FWP_DIRECTION_OUTBOUND</strong>.</span><span class="sxs-lookup"><span data-stu-id="f6e95-460">(For example, when a local application initiates the connection, an inbound packet has <strong>FWPM_CONDITION_DIRECTION</strong> set to <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span></span> <br/> <span data-ttu-id="f6e95-461"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-461"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <span data-ttu-id="f6e95-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-463">Indice dell'interfaccia di rete, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-463">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-464"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-464"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <span data-ttu-id="f6e95-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-466">Indice dell'interfaccia di rete logica, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-466">The index of the logical network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-467"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-467"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <span data-ttu-id="f6e95-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-469">Indice dell'interfaccia di rete di origine per i pacchetti inoltrati, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-469">The index of the source network interface for forwarded packets, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="f6e95-470"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-470"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <span data-ttu-id="f6e95-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-472">Indice dell'interfaccia di rete logica di origine per i pacchetti inoltrati, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-472">The index of the source logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-473"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-473"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <span data-ttu-id="f6e95-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-475">Indice dell'interfaccia di rete di destinazione per i pacchetti inoltrati, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-475">The index of the destination network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-476"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-476"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <span data-ttu-id="f6e95-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-478">Indice dell'interfaccia di rete logica di destinazione per i pacchetti inoltrati, come enumerato dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-478">The index of the destination logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="f6e95-479"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-479"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <span data-ttu-id="f6e95-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-481">Percorso completo del dispositivo dell'applicazione, restituito dalla funzione <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f6e95-481">The fully qualified device path of the application, as returned by the <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> function.</span></span> <br/> <span data-ttu-id="f6e95-482">Ad esempio, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="f6e95-482">(For example, &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.)</span></span><br/> <span data-ttu-id="f6e95-483"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-483"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <span data-ttu-id="f6e95-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-485">Identificazione dell'utente locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-485">The identification of the local user.</span></span> <br/> <span data-ttu-id="f6e95-486"><strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-486"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <span data-ttu-id="f6e95-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-488">Identificazione dell'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-488">The identification of the remote user.</span></span> <br/> <span data-ttu-id="f6e95-489"><strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-489"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <span data-ttu-id="f6e95-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-491">Identificazione del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-491">The identification of the remote machine.</span></span> <br/> <span data-ttu-id="f6e95-492"><strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-492"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <span data-ttu-id="f6e95-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-494">Modalità socket non elaborata consentita o negata.</span><span class="sxs-lookup"><span data-stu-id="f6e95-494">The raw socket mode that is allowed or denied.</span></span><br/> <span data-ttu-id="f6e95-495"><strong>Valori possibili:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-495"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-496">SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="f6e95-496">SIO_RCVALL</span></span></li>
<li><span data-ttu-id="f6e95-497">SIO_RCVALL_IGMPMCAST</span><span class="sxs-lookup"><span data-stu-id="f6e95-497">SIO_RCVALL_IGMPMCAST</span></span></li>
<li><span data-ttu-id="f6e95-498">SIO_RCVALL_MCAST</span><span class="sxs-lookup"><span data-stu-id="f6e95-498">SIO_RCVALL_MCAST</span></span></li>
</ul>
<span data-ttu-id="f6e95-499">Per una descrizione di queste modalità socket non elaborate, vedere la funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f6e95-499">For a description of these raw socket modes, see the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> function.</span></span><br/> <span data-ttu-id="f6e95-500"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-500"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <span data-ttu-id="f6e95-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-502">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-502">Reserved for internal use.</span></span> <br/> <span data-ttu-id="f6e95-503"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-503"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <span data-ttu-id="f6e95-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-505">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-505">Reserved for internal use.</span></span> <br/> <span data-ttu-id="f6e95-506"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-506"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f6e95-507">Le costanti seguenti sono disponibili solo per la modalità utente.</span><span class="sxs-lookup"><span data-stu-id="f6e95-507">The following constants are available for user mode only.</span></span>



| <span data-ttu-id="f6e95-508">Condizioni della modalità utente disponibili per Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6e95-508">User-mode conditions available for Windows 8 and Windows Server 2012</span></span>                                                                                                                       | <span data-ttu-id="f6e95-509">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-509">Description</span></span>                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <span data-ttu-id="f6e95-510"><dt>**\_modalità FWPM Condition \_ mq \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-510"><dt>**FWPM\_CONDITION\_QM\_MODE**</dt></span></span> </dl> | <span data-ttu-id="f6e95-511">Modalità del filtro della modalità rapida (QM).</span><span class="sxs-lookup"><span data-stu-id="f6e95-511">The mode of the quick mode (QM) filter.</span></span> <span data-ttu-id="f6e95-512">Per i valori possibili, vedere [**\_ \_ tipo di traffico IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) .</span><span class="sxs-lookup"><span data-stu-id="f6e95-512">See [**IPSEC\_TRAFFIC\_TYPE**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) for possible values.</span></span><br/> <span data-ttu-id="f6e95-513">**Tipo di dati:** \_UInt32 FWP</span><span class="sxs-lookup"><span data-stu-id="f6e95-513">**Data type:** FWP\_UINT32</span></span><br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f6e95-514">Condizioni della modalità utente disponibili per Windows 7, Windows Server 2008 R2 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f6e95-514">User-mode conditions available for Windows 7, Windows Server 2008 R2, and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f6e95-515">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-515">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <span data-ttu-id="f6e95-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-517">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-517">Reserved for internal use.</span></span><br/> <span data-ttu-id="f6e95-518"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-518"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <span data-ttu-id="f6e95-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-520">Nome del peer.</span><span class="sxs-lookup"><span data-stu-id="f6e95-520">The name of the peer.</span></span> <span data-ttu-id="f6e95-521">Ad esempio, il nome DNS del peer.</span><span class="sxs-lookup"><span data-stu-id="f6e95-521">For example, the peer's DNS name.</span></span><br/> <span data-ttu-id="f6e95-522"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-522"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <span data-ttu-id="f6e95-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-524">Identità dell'entità di autenticazione remota.</span><span class="sxs-lookup"><span data-stu-id="f6e95-524">The identity of the remote authentication principal.</span></span> <br/> <span data-ttu-id="f6e95-525"><strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-525"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="f6e95-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-527">Tipo di metodo di autenticazione IKE, IKEv2 o AuthIP.</span><span class="sxs-lookup"><span data-stu-id="f6e95-527">The type of IKE, IKEv2, or AuthIP authentication method.</span></span> <br/> <span data-ttu-id="f6e95-528"><strong>Tipo di dati:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-528"><strong>Data type:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <span data-ttu-id="f6e95-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-530">Tipo di modulo di chiavi.</span><span class="sxs-lookup"><span data-stu-id="f6e95-530">The type of keying module.</span></span><br/> <span data-ttu-id="f6e95-531"><strong>Tipo di dati:</strong> IKEEXT_KEY_MODULE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-531"><strong>Data type:</strong> IKEEXT_KEY_MODULE_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <span data-ttu-id="f6e95-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-533">Modalità IPsec in cui è possibile ottenere un token.</span><span class="sxs-lookup"><span data-stu-id="f6e95-533">The IPsec mode in which a token can be obtained.</span></span><br/> <span data-ttu-id="f6e95-534"><strong>Tipo di dati:</strong> IPSEC_TOKEN_MODE</span><span class="sxs-lookup"><span data-stu-id="f6e95-534"><strong>Data type:</strong> IPSEC_TOKEN_MODE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <span data-ttu-id="f6e95-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-536">Chiave di contesto del provider di criteri in modalità principale (MM) o in modalità rapida (QM) dell'autorizzazione SA.</span><span class="sxs-lookup"><span data-stu-id="f6e95-536">The main mode (MM) or quick mode (QM) policy provider context key of the SA being authorized.</span></span> <span data-ttu-id="f6e95-537">Utile per limitare l'ambito della regola di autorizzazione alla firma di accesso condiviso usando una chiave del criterio IPsec MM o QM specificata.</span><span class="sxs-lookup"><span data-stu-id="f6e95-537">Useful for restricting the scope of the authorization rule to SAs formed using a specified IPsec MM or QM policy key.</span></span><br/> <span data-ttu-id="f6e95-538"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-538"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="f6e95-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-540">Metodo utilizzato per autenticare l'associazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f6e95-540">The method used to authenticate the security association.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f6e95-541">Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f6e95-541">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="f6e95-542"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-542"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
</tbody>
</table>





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f6e95-543">Costanti disponibili per Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="f6e95-543">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f6e95-544">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6e95-544">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <span data-ttu-id="f6e95-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-546">Identificazione dell'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-546">The identification of the remote user.</span></span><br/> <span data-ttu-id="f6e95-547"><strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-547"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <span data-ttu-id="f6e95-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-549">UUID dell'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="f6e95-549">The UUID of the RPC interface.</span></span> <br/> <span data-ttu-id="f6e95-550"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-550"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <span data-ttu-id="f6e95-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-552">Versione dell'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="f6e95-552">The version of the RPC interface.</span></span> <br/> <span data-ttu-id="f6e95-553"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-553"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <span data-ttu-id="f6e95-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-555">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-555">Reserved for internal use.</span></span> <br/> <span data-ttu-id="f6e95-556"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-556"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <span data-ttu-id="f6e95-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-558">Identificazione dell'applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="f6e95-558">The identification of the COM application.</span></span><br/> <span data-ttu-id="f6e95-559"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-559"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <span data-ttu-id="f6e95-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-561">Nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6e95-561">The name of the application.</span></span><br/> <span data-ttu-id="f6e95-562"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-562"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <span data-ttu-id="f6e95-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-564">Protocollo RPC.</span><span class="sxs-lookup"><span data-stu-id="f6e95-564">The RPC protocol.</span></span> <br/> <span data-ttu-id="f6e95-565"><strong>Valori possibili:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-565"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-566">RPC_PROTSEQ_TCP</span><span class="sxs-lookup"><span data-stu-id="f6e95-566">RPC_PROTSEQ_TCP</span></span></li>
<li><span data-ttu-id="f6e95-567">RPC_PROTSEQ_NMP</span><span class="sxs-lookup"><span data-stu-id="f6e95-567">RPC_PROTSEQ_NMP</span></span></li>
<li><span data-ttu-id="f6e95-568">RPC_PROTSEQ_LRPC</span><span class="sxs-lookup"><span data-stu-id="f6e95-568">RPC_PROTSEQ_LRPC</span></span></li>
<li><span data-ttu-id="f6e95-569">RPC_PROTSEQ_HTTP</span><span class="sxs-lookup"><span data-stu-id="f6e95-569">RPC_PROTSEQ_HTTP</span></span></li>
</ul>
<br/> <span data-ttu-id="f6e95-570"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-570"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <span data-ttu-id="f6e95-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-572">Tipo di servizio di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f6e95-572">The authentication service type.</span></span> <span data-ttu-id="f6e95-573">Per ulteriori informazioni sui tipi di servizio di autenticazione, vedere <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>costanti del servizio di autenticazione</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f6e95-573">For more information about authentication service types, see <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>.</span></span> <br/> <span data-ttu-id="f6e95-574"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-574"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <span data-ttu-id="f6e95-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-576">Livello del servizio di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f6e95-576">The authentication service level.</span></span> <span data-ttu-id="f6e95-577">Per altre informazioni sui livelli di servizio di autenticazione, vedere <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>costanti a livello di autenticazione</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f6e95-577">For more information about authentication service levels, see <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Authentication-Level Constants</strong></a>.</span></span> <br/> <span data-ttu-id="f6e95-578"><strong>Tipo di dati:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="f6e95-578"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <span data-ttu-id="f6e95-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-580">Algoritmo di crittografia SSPI (Security Service Provider Interface) basato su certificati.</span><span class="sxs-lookup"><span data-stu-id="f6e95-580">The certificate based Security Service Provider Interface (SSPI) encryption algorithm.</span></span><br/> <span data-ttu-id="f6e95-581"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-581"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <span data-ttu-id="f6e95-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-583">Dimensione della chiave di crittografia SSPI basata sul certificato.</span><span class="sxs-lookup"><span data-stu-id="f6e95-583">The certificate based SSPI encryption key size.</span></span><br/> <span data-ttu-id="f6e95-584"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-584"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <span data-ttu-id="f6e95-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-586">Indirizzo IPv4 locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-586">The local IPv4 address.</span></span> <br/> <span data-ttu-id="f6e95-587"><strong>Tipo di dati:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-587"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-588">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-588">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-589">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-589">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <span data-ttu-id="f6e95-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-591">Indirizzo IPv6 locale.</span><span class="sxs-lookup"><span data-stu-id="f6e95-591">The local IPv6 address.</span></span> <br/> <span data-ttu-id="f6e95-592"><strong>Tipo di dati:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-592"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-593">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-593">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-594">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-594">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <span data-ttu-id="f6e95-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-596">Indirizzo IPv4 remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-596">The remote IPv4 address.</span></span> <br/> <span data-ttu-id="f6e95-597"><strong>Tipo di dati:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-597"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-598">FWP_V4_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-598">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-599">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-599">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <span data-ttu-id="f6e95-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-601">Indirizzo IPv6 remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-601">The remote IPv6 address.</span></span> <br/> <span data-ttu-id="f6e95-602"><strong>Tipo di dati:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="f6e95-602"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="f6e95-603">FWP_V6_ADDR_MASK o</span><span class="sxs-lookup"><span data-stu-id="f6e95-603">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="f6e95-604">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-604">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <span data-ttu-id="f6e95-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-606">Nome del named pipe remoto.</span><span class="sxs-lookup"><span data-stu-id="f6e95-606">The name of the remote named pipe.</span></span><br/> <span data-ttu-id="f6e95-607"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-607"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <span data-ttu-id="f6e95-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-609">UUID del processo con l'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="f6e95-609">The UUID of the process with the RPC interface.</span></span><br/> <span data-ttu-id="f6e95-610"><strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-610"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <span data-ttu-id="f6e95-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-612">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-612">Reserved for internal use.</span></span><br/> <span data-ttu-id="f6e95-613"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-613"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <span data-ttu-id="f6e95-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-615">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="f6e95-615">Reserved for internal use.</span></span><br/> <span data-ttu-id="f6e95-616"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-616"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <span data-ttu-id="f6e95-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-618">Identificazione del client quando si utilizza RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="f6e95-618">The identification of the client when using RpcProxy.</span></span><br/> <span data-ttu-id="f6e95-619"><strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-619"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <span data-ttu-id="f6e95-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-621">Nome del server RPC quando si utilizza RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="f6e95-621">The name of the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="f6e95-622"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-622"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <span data-ttu-id="f6e95-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-624">La porta sul server RPC quando si utilizza RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="f6e95-624">The port on the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="f6e95-625"><strong>Tipo di dati:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="f6e95-625"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <span data-ttu-id="f6e95-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-627">Tipo di servizio di autenticazione proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="f6e95-627">The RPC proxy authentication service type.</span></span><br/> <span data-ttu-id="f6e95-628"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-628"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <span data-ttu-id="f6e95-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-630">Lunghezza della chiave SSL (Secure Socket Layer) nel certificato client.</span><span class="sxs-lookup"><span data-stu-id="f6e95-630">The Secure Socket Layer (SSL) key length in the client certificate.</span></span><br/> <span data-ttu-id="f6e95-631"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-631"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <span data-ttu-id="f6e95-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-633">Identificatore di oggetto nel certificato client.</span><span class="sxs-lookup"><span data-stu-id="f6e95-633">The object identifier in the client certificate.</span></span><br/> <span data-ttu-id="f6e95-634"><strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6e95-634"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <span data-ttu-id="f6e95-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f6e95-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f6e95-636">Tipo di evento NET.</span><span class="sxs-lookup"><span data-stu-id="f6e95-636">The type of net event.</span></span><br/> <span data-ttu-id="f6e95-637"><strong>Tipo di dati:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="f6e95-637"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="f6e95-638">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6e95-638">Remarks</span></span>

<span data-ttu-id="f6e95-639">Quando gli indirizzi IP vengono archiviati nel \_ formato FWP UInt32 o quando una porta IP viene archiviata nel \_ formato FWP UInt16, vengono archiviati in ordine host, non in base all'ordine di rete.</span><span class="sxs-lookup"><span data-stu-id="f6e95-639">When IP addresses are stored in FWP\_UINT32 format or when an IP port is stored in FWP\_UINT16 format, they are stored in host-order, not network-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e95-640">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6e95-640">Requirements</span></span>



| <span data-ttu-id="f6e95-641">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6e95-641">Requirement</span></span> | <span data-ttu-id="f6e95-642">Valore</span><span class="sxs-lookup"><span data-stu-id="f6e95-642">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e95-643">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6e95-643">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e95-644">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6e95-644">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f6e95-645">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6e95-645">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e95-646">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6e95-646">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f6e95-647">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6e95-647">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6e95-648"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e95-648"><dt>Fwpmu.h</dt></span></span> </dl> |
