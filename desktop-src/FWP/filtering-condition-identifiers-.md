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
# <a name="filtering-condition-identifiers"></a>Filtraggio degli identificatori di condizione

Gli identificatori della condizione di filtro Windows Filtering Platform (WFP) sono rappresentati da un **GUID**. Il tipo di dati per il valore della condizione per ogni condizione di filtro viene specificato come [**\_ \_ tipo di dati FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Questi identificatori e i relativi tipi di dati sono definiti qui.

Le condizioni standard sono elencate per prime, seguite dalle condizioni specifiche per la modalità utente. Le condizioni sono raggruppate in base al sistema operativo supportato, in modo che sia possibile stabilire facilmente quali condizioni sono supportate per un determinato sistema operativo.

> [!Note]  
> Ognuna delle seguenti condizioni di filtro è disponibile solo in un subset dei livelli di filtro WFP. Per altre informazioni sulla disponibilità di ogni condizione a un determinato livello, vedere [**condizioni di filtro disponibili a ogni livello di filtro**](filtering-conditions-available-at-each-filtering-layer.md).

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Condizioni disponibili per Windows 8 e Windows Server 2012</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo MAC di una particolare interfaccia locale.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo di destinazione di un frame in ingresso o indirizzo di origine di un frame in uscita.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo di origine di un frame in ingresso o indirizzo di destinazione di un frame in uscita.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di dati del payload di rete Ethernet V2. (Vedere ETHERNET_TYPE_IPV4 e così via in netiodef. h).<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </dl></td>
<td style="text-align: left;">L'intestazione della VLAN a 16 bit, inclusi i campi VID, CFI e Priority, in base allo standard 802.1 q (vedere VLAN_TAG in netiodef. h per le posizioni del campi).<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore univoco per la rete vSwitch. Non può essere usato in combinazione con VLAN_IDs.<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Numero di porta della porta NDIS.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di supporto della porta NDIS.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>NDIS_MEDIUM</strong> . (Vedere Ntddndis. h). <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di supporto fisico della porta NDIS.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>NDIS_PHYSICAL_MEDIUM</strong> . (Vedere Ntddndis. h). <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">OR bit per bit di una combinazione di flag di condizione di filtro. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/> <strong>Valori possibili:  </strong>
<ul>
<li>FWP_CONDITION_L2_IS_MOBILE_BROADBAND</li>
<li>FWP_CONDITION_L2_IS_NATIVE_ETHERNET</li>
<li>FWP_CONDITION_L2_IS_WIFI</li>
<li>FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo dell'indirizzo locale fisico.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo dell'indirizzo remoto fisico.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo di origine fisico di un frame.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo di destinazione fisico di un frame.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo dell'indirizzo di destinazione fisico.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo dell'indirizzo di destinazione fisico.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <strong>DL_ADDRESS_TYPE</strong> seguenti.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Porta di origine del trasporto del pacchetto.<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Il campo di tipo ICMP, come specificato nella RFC 792.<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Porta di destinazione del trasporto del pacchetto.<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">Il campo del codice ICMP, come specificato nella RFC 792. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore univoco di un'istanza di vSwitch.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Specifica se l'istanza di vSwitch fa parte di una rete virtuale esterna, interna o privata.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore univoco dell'origine del pacchetto corrente. (Il nome di una VM-NIC, P-NIC o V-NIC).<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore univoco della destinazione del pacchetto corrente. (Il nome di una VM-NIC, P-NIC o V-NIC).<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore univoco della macchina virtuale di origine vSwitch.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore univoco della macchina virtuale di destinazione vSwitch.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di interfaccia dell'origine del pacchetto corrente.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/> <strong>Valori possibili:  </strong>
<ul>
<li>SwitchNicSyntheticNic (quando il tipo di interfaccia è VM-NIC)</li>
<li>SwitchNicEmulatedNic (quando il tipo di interfaccia è VM-NIC)</li>
<li>SwitchNicPhysicalNic (quando il tipo di interfaccia è P-NIC)</li>
<li>SwitchNicVNic (quando il tipo di interfaccia è V-NIC, connesso alla partizione host)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di interfaccia della destinazione del pacchetto corrente.<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/> <strong>Valori possibili:  </strong>
<ul>
<li>SwitchNicSyntheticNic (quando il tipo di interfaccia è VM-NIC)</li>
<li>SwitchNicEmulatedNic (quando il tipo di interfaccia è VM-NIC)</li>
<li>SwitchNicPhysicalNic (quando il tipo di interfaccia è P-NIC)</li>
<li>SwitchNicVNic (quando il tipo di interfaccia è V-NIC, connesso alla partizione host)</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">LUID per l'interfaccia di rete associata all'indirizzo IP locale. <br/> <strong>Tipo di dati:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </dl></td>
<td style="text-align: left;">ID di sicurezza (SID) di un contenitore di app.<br/> <strong>Tipo di dati:</strong> FWP_SID<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Percorso completo del dispositivo dell'applicazione, ad esempio &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; . Quando una connessione è stata reindirizzata, questo sarà l'identificatore dell'app di origine. in caso contrario, sarà uguale a <strong>FWPM_CONDITION_ALE_APP_ID</strong>.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
</tbody>
</table>





| Condizioni disponibili per Windows 7, Windows Server 2008 R2 e versioni successive                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <dt>**\_ \_ \_ Indirizzo NEXTHOP IP della condizione FWPM \_**</dt> </dl>                                             | Indirizzo IP dell'interfaccia hop successiva.<br/> **Tipo di dati:** \_Maschera FWP V4 \_ addr \_<br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <dt>**interfaccia NEXTHOP di FWPM \_ Condition \_ IP \_ \_**</dt> </dl>                                       | Interfaccia hop successiva da cui il pacchetto verrà ripartito. <br/> **Tipo di dati:** FWP \_ UInt64<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <dt>**FWPM \_ Condition \_ NEXTHOP \_ - \_ tipo interfaccia**</dt> </dl>                                 | Tipo di interfaccia dell'interfaccia hop successiva.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <dt>**\_tipo di \_ \_ tunnel NEXTHOP della condizione \_ FWPM**</dt> </dl>                                          | Tipo di tunnel dell'interfaccia hop successiva.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <dt>**\_indice dell' \_ \_ interfaccia NEXTHOP della condizione \_ FWPM**</dt> </dl>                              | Indice di interfaccia dell'interfaccia hop successiva.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <dt>**FWPM \_ Condition \_ NEXTHOP \_ \_ indice secondario interfaccia \_**</dt> </dl>                 | Indice dell'interfaccia secondaria dell'interfaccia hop successiva.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <dt>**\_ \_ \_ ID profilo originale della condizione FWPM \_**</dt> </dl>                                          | Categoria di rete dell'interfaccia di arrivo o di hop successivo tramite la quale viene creato il flusso di ALE (in entrata o in uscita). <br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <dt>**\_ \_ \_ ID profilo corrente della condizione FWPM \_**</dt> </dl>                                             | Categoria di rete dell'interfaccia di arrivo o di hop successivo tramite la quale viene creato il pacchetto corrente (in entrata o in uscita). <br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <dt>**\_ \_ \_ \_ ID profilo interfaccia locale della condizione FWPM \_**</dt> </dl>                    | Categoria di rete dell'interfaccia di recapito.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <dt>**\_ \_ \_ \_ ID profilo interfaccia arrivo condizione \_ FWPM**</dt> </dl>              | Categoria di rete dell'interfaccia di arrivo.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <dt>**FWPM \_ Condition \_ NEXTHOP \_ \_ ID profilo \_ interfaccia**</dt> </dl>              | Categoria di rete dell'interfaccia hop successiva.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <dt>**\_motivo della \_ Riautorizzazione della condizione FWPM \_**</dt> </dl>                                              | Motivo della Riautorizzazione di una connessione precedentemente autorizzata.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <dt>**\_motivo della \_ \_ riautenticazione ale della condizione FWPM \_**</dt> </dl>                                                | Il motivo per cui è stata riautorizzata una connessione precedentemente autorizzata, ad esempio la **\_ \_ \_ \_ \_ modifica del criterio di Riautorizzazione della condizione FWP** (o uno degli altri valori elencati nei flag di condizione di [**filtro**](filtering-condition-flags-.md)).<br/> **Tipo di dati:** \_UInt32 FWP<br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <dt>**\_ \_ \_ tipo ICMP originale della condizione FWPM \_**</dt> </dl>                                             | Tipo ICMP con cui è stato creato il flusso.<br/> **Tipo di dati:** FWP \_ UInt16<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <dt>**\_interfaccia di \_ \_ arrivo fisica \_ IP \_ della condizione FWPM**</dt> </dl>           | LUID dell'interfaccia fisica associata all'indirizzo IP di arrivo.<br/> **Tipo di dati:** FWP \_ UInt64<br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <dt>**FWPM \_ Condition \_ IP \_ - \_ interfaccia NEXTHOP fisica \_**</dt> </dl>           | LUID dell'interfaccia fisica dell'hop successivo.<br/> **Tipo di dati:** FWP \_ UInt64<br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <dt>**\_epoca di \_ quarantena dell'interfaccia della condizione FWPM \_ \_**</dt> </dl>                     | Numero di Epoch associato a un'interfaccia. Riservato.<br/> **Tipo di dati:** FWP \_ UInt64<br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <dt>**\_proprietà del socket del firewall della condizione FWPM \_ ale \_ sio \_ \_ \_**</dt> </dl> | Riservato per utilizzo interno. <br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                                              |





| Costanti disponibili per Windows Vista con SP1, Windows Server 2008 e versioni successive                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <dt>**\_interfaccia di \_ \_ arrivo IP della condizione \_ FWPM**</dt> </dl>                       | LUID per l'interfaccia di rete associata all'indirizzo IP di arrivo. <br/> **Tipo di dati:** FWP \_ UInt64<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <dt>**\_tipo di \_ interfaccia di arrivo della condizione FWPM \_ \_**</dt> </dl>                 | Tipo di interfaccia di rete di arrivo come definito da IANA (Internet Assigned Names Authority). Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valori possibili:** Valori del tipo di interfaccia elencati nel file di intestazione Ipifcons. h.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <dt>**FWPM \_ \_tipo di \_ tunnel \_ di arrivo della condizione**</dt> </dl>                       | Metodo di incapsulamento usato da un tunnel associato all'interfaccia di rete di arrivo se il membro del tipo è se il \_ tunnel del tipo \_ . Il tipo di tunnel è definito da IANA (Internet Assigned Names Authority). Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valori possibili:** Valori del \_ tipo di enumerazione del tipo di tunnel elencati nel file di intestazione ifdef. h.<br/> **Tipo di dati:** \_UInt32 FWP<br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <dt>**\_ \_ indice dell'interfaccia di arrivo della condizione FWPM \_ \_**</dt> </dl>              | Indice dell'interfaccia di rete di arrivo, come enumerato dallo stack di rete.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <dt>**\_ \_ \_ indice dell'interfaccia secondaria \_ di arrivo della condizione \_ FWPM**</dt> </dl> | Indice dell'interfaccia di rete di arrivo, come enumerato dallo stack di rete. <br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <dt>**\_indice dell' \_ \_ interfaccia locale della condizione \_ FWPM**</dt> </dl>                    | Indice dell'interfaccia di rete, come enumerato dallo stack di rete. <br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <dt>**\_tipo di \_ \_ interfaccia locale della condizione \_ FWPM**</dt> </dl>                       | Il tipo di interfaccia definito da IANA (Internet Assigned Names Authority). Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valori possibili:** Valori del tipo di interfaccia elencati nel file di intestazione Ipifcons. h.<br/> **Tipo di dati:** \_UInt32 FWP<br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <dt>**\_tipo di \_ \_ tunnel locale della condizione \_ FWPM**</dt> </dl>                                | Metodo di incapsulamento usato da un tunnel se il membro del tipo è se il \_ tunnel del tipo \_ . Il tipo di tunnel è definito da IANA (Internet Assigned Names Authority). Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valori possibili:** Valori del \_ tipo di enumerazione del tipo di tunnel elencati nel file di intestazione ifdef. h.<br/> **Tipo di dati:** \_UInt32 FWP <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costanti disponibili per Windows Vista e versioni successive</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IP locale. <br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv4
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv6
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IP remoto. <br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv4
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv6
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IP di origine per i pacchetti inoltrati. <br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv4
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv6
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IP di destinazione per i pacchetti inoltrati. <br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv4
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv6
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo IP locale. <br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> seguenti.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo IP di destinazione per i pacchetti inoltrati. <br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> seguenti.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">LUID per l'interfaccia di rete associata all'indirizzo IP locale. <br/> <strong>Tipo di dati:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Il tipo di interfaccia definito da IANA (Internet Assigned Names Authority). Per altre informazioni, vedere [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> <strong>Valori possibili:</strong> Valori del tipo di interfaccia elencati nel file di intestazione Ipifcons. h.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Metodo di incapsulamento utilizzato da un tunnel se il membro del tipo è IF_TYPE_TUNNEL. Il tipo di tunnel è definito da IANA (Internet Assigned Names Authority). Per altre informazioni, vedere <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>. <br/> <strong>Valori possibili:</strong> I valori del tipo di enumerazione TUNNEL_TYPE elencati nel file di intestazione ifdef. h.<br/> <strong>Tipo di dati:</strong> FWP_UINT32 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">LUID per l'interfaccia di rete in cui deve essere inviato il pacchetto inoltrato. <br/> <strong>Tipo di dati:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Il numero di protocollo IP, come specificato nella RFC 1700. <br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Numero di porta del protocollo di trasporto locale.<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Il campo di tipo ICMP, come specificato nella RFC 792. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Numero di porta del protocollo di trasporto remoto. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">Il campo del codice ICMP, come specificato nella RFC 792. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di indirizzo IP locale incorporato nel pacchetto ICMP.<br/> <strong>Valori possibili:</strong> Uno dei valori di enumerazione <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> seguenti.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IP remoto incorporato nel pacchetto ICMP. <br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv4
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo di dati:</strong> Per un indirizzo IPv6
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Il numero di protocollo IP incorporato nel pacchetto ICMP, come specificato nella RFC 1700. <br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Numero di porta del protocollo di trasporto locale incorporato nel pacchetto ICMP. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Numero di porta del protocollo di trasporto remoto incorporato nel pacchetto ICMP. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">OR bit per bit di una combinazione di flag di condizione di filtro. <br/> <strong>Valori possibili:</strong> Vedere <a href="filtering-condition-flags-.md"> <strong>flag della condizione di filtro</strong></a><br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </dl></td>
<td style="text-align: left;">Direzione del traffico o del flusso di dati. <br/> <strong>Valori possibili:  </strong>
<ul>
<li>FWP_DIRECTION_INBOUND</li>
<li>FWP_DIRECTION_OUTBOUND</li>
</ul>
<br/> Per i livelli di datagramma (FWPM_LAYER_DATAGRAM_DATA_ *) e i livelli di pacchetti di flusso (FWPM_LAYER_STREAM_PACKET_*), il valore sarà uguale a quello della direzione del pacchetto. <br/> Per i livelli di flusso (FWPM_LAYER_STREAM_ *) e i livelli stabiliti dal flusso (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), il valore sarà uguale alla direzione della connessione. Ad esempio, quando un'applicazione locale avvia la connessione, un pacchetto in ingresso ha <strong>FWPM_CONDITION_DIRECTION</strong> impostato su <strong>FWP_DIRECTION_OUTBOUND</strong>. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Indice dell'interfaccia di rete, come enumerato dallo stack di rete. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Indice dell'interfaccia di rete logica, come enumerato dallo stack di rete. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Indice dell'interfaccia di rete di origine per i pacchetti inoltrati, come enumerato dallo stack di rete.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Indice dell'interfaccia di rete logica di origine per i pacchetti inoltrati, come enumerato dallo stack di rete. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Indice dell'interfaccia di rete di destinazione per i pacchetti inoltrati, come enumerato dallo stack di rete. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">Indice dell'interfaccia di rete logica di destinazione per i pacchetti inoltrati, come enumerato dallo stack di rete. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Percorso completo del dispositivo dell'applicazione, restituito dalla funzione <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> . <br/> Ad esempio, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificazione dell'utente locale. <br/> <strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificazione dell'utente remoto. <br/> <strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificazione del computer remoto. <br/> <strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </dl></td>
<td style="text-align: left;">Modalità socket non elaborata consentita o negata.<br/> <strong>Valori possibili:  </strong>
<ul>
<li>SIO_RCVALL</li>
<li>SIO_RCVALL_IGMPMCAST</li>
<li>SIO_RCVALL_MCAST</li>
</ul>
Per una descrizione di queste modalità socket non elaborate, vedere la funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per utilizzo interno. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per utilizzo interno. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



Le costanti seguenti sono disponibili solo per la modalità utente.



| Condizioni della modalità utente disponibili per Windows 8 e Windows Server 2012                                                                                                                       | Descrizione                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <dt>**\_modalità FWPM Condition \_ mq \_**</dt> </dl> | Modalità del filtro della modalità rapida (QM). Per i valori possibili, vedere [**\_ \_ tipo di traffico IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) .<br/> **Tipo di dati:** \_UInt32 FWP<br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Condizioni della modalità utente disponibili per Windows 7, Windows Server 2008 R2 e versioni successive</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per utilizzo interno.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Nome del peer. Ad esempio, il nome DNS del peer.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identità dell'entità di autenticazione remota. <br/> <strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di metodo di autenticazione IKE, IKEv2 o AuthIP. <br/> <strong>Tipo di dati:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di modulo di chiavi.<br/> <strong>Tipo di dati:</strong> IKEEXT_KEY_MODULE_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </dl></td>
<td style="text-align: left;">Modalità IPsec in cui è possibile ottenere un token.<br/> <strong>Tipo di dati:</strong> IPSEC_TOKEN_MODE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </dl></td>
<td style="text-align: left;">Chiave di contesto del provider di criteri in modalità principale (MM) o in modalità rapida (QM) dell'autorizzazione SA. Utile per limitare l'ambito della regola di autorizzazione alla firma di accesso condiviso usando una chiave del criterio IPsec MM o QM specificata.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Metodo utilizzato per autenticare l'associazione di sicurezza.<br/>
<blockquote>
[!Note]<br />
Disponibile solo in Windows Server 2008 R2, Windows 7 e versioni successive.
</blockquote>
<br/> <strong>Tipo di dati:</strong> FWP_UINT32 <br/></td>
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
<th style="text-align: left;">Costanti disponibili per Windows Vista e versioni successive</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">Identificazione dell'utente remoto.<br/> <strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </dl></td>
<td style="text-align: left;">UUID dell'interfaccia RPC. <br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </dl></td>
<td style="text-align: left;">Versione dell'interfaccia RPC. <br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per utilizzo interno. <br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificazione dell'applicazione COM.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Nome dell'applicazione.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">Protocollo RPC. <br/> <strong>Valori possibili:  </strong>
<ul>
<li>RPC_PROTSEQ_TCP</li>
<li>RPC_PROTSEQ_NMP</li>
<li>RPC_PROTSEQ_LRPC</li>
<li>RPC_PROTSEQ_HTTP</li>
</ul>
<br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di servizio di autenticazione. Per ulteriori informazioni sui tipi di servizio di autenticazione, vedere <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>costanti del servizio di autenticazione</strong></a>. <br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </dl></td>
<td style="text-align: left;">Livello del servizio di autenticazione. Per altre informazioni sui livelli di servizio di autenticazione, vedere <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>costanti a livello di autenticazione</strong></a>. <br/> <strong>Tipo di dati:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia SSPI (Security Service Provider Interface) basato su certificati.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </dl></td>
<td style="text-align: left;">Dimensione della chiave di crittografia SSPI basata sul certificato.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IPv4 locale. <br/> <strong>Tipo di dati:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IPv6 locale. <br/> <strong>Tipo di dati:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IPv4 remoto. <br/> <strong>Tipo di dati:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK o</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">Indirizzo IPv6 remoto. <br/> <strong>Tipo di dati:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK o</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <dt><strong>FWPM_CONDITION_PIPE</strong></dt> </dl></td>
<td style="text-align: left;">Nome del named pipe remoto.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </dl></td>
<td style="text-align: left;">UUID del processo con l'interfaccia RPC.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per utilizzo interno.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per utilizzo interno.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">Identificazione del client quando si utilizza RpcProxy.<br/> <strong>Tipo di dati:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">Nome del server RPC quando si utilizza RpcProxy.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </dl></td>
<td style="text-align: left;">La porta sul server RPC quando si utilizza RpcProxy.<br/> <strong>Tipo di dati:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di servizio di autenticazione proxy RPC.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </dl></td>
<td style="text-align: left;">Lunghezza della chiave SSL (Secure Socket Layer) nel certificato client.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </dl></td>
<td style="text-align: left;">Identificatore di oggetto nel certificato client.<br/> <strong>Tipo di dati:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo di evento NET.<br/> <strong>Tipo di dati:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Quando gli indirizzi IP vengono archiviati nel \_ formato FWP UInt32 o quando una porta IP viene archiviata nel \_ formato FWP UInt16, vengono archiviati in ordine host, non in base all'ordine di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |
