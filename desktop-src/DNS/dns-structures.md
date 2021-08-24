---
title: Strutture DNS
description: Domain Name System di navigazione delle strutture (DNS).
ms.assetid: 636399be-43a5-4ddf-b652-f8efb81fbf42
keywords:
- Domain Name System strutture
- Strutture DNS
- Domain Name System, riferimento, strutture
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 223e5985b7282efd3349cd412279510f476315fb078ea459e524e80d703474ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825321"
---
# <a name="dns-structures"></a>Strutture DNS

Le strutture seguenti sono definite per l'uso con DNS:

- [**DNS_ADDR**](/windows/win32/api/windns/ns-windns-dns_addr)
- [**DNS_ADDR_ARRAY**](/windows/win32/api/windns/ns-windns-dns_addr_array)
- [**DNS_CUSTOM_SERVER**](/windows/win32/api/windns/ns-windns-dns_custom_server)
- [**DNS_HEADER**](/windows/desktop/api/Windns/ns-windns-dns_header)
- [**DNS_MESSAGE_BUFFER**](/windows/desktop/api/Windns/ns-windns-dns_message_buffer)
- [**DNS_PROXY_INFORMATION**](/windows/desktop/api/Windns/ns-windns-dns_proxy_information)
- [**DNS_QUERY_REQUEST**](/windows/desktop/api/Windns/ns-windns-dns_query_request)
- [**DNS_QUERY_REQUEST3**](/windows/desktop/api/Windns/ns-windns-dns_query_request3)
- [**DNS_RECORD**](/windows/win32/api/windns/ns-windns-dns_recorda)
- [**DNS_RECORD_FLAGS**](/windows/win32/api/windns/ns-windns-dns_record_flags)
- [**DNS_SERVICE_BROWSE_REQUEST**](/windows/desktop/api/Windns/ns-windns-dns_service_browse_request)
- [**DNS_SERVICE_CANCEL**](/windows/desktop/api/Windns/ns-windns-dns_service_cancel)
- [**DNS_SERVICE_INSTANCE**](/windows/desktop/api/Windns/ns-windns-dns_service_instance)
- [**DNS_SERVICE_REGISTER_REQUEST**](/windows/desktop/api/Windns/ns-windns-dns_service_register_request)
- [**DNS_SERVICE_RESOLVE_REQUEST**](/windows/desktop/api/Windns/ns-windns-dns_service_resolve_request)
- [**IP4_ARRAY**](/windows/desktop/api/Windns/ns-windns-ip4_array)
- [**IP6_ADDRESS**](/windows/win32/api/windns/ns-windns-ip6_address)
- [**MDNS_QUERY_HANDLE**](/windows/desktop/api/Windns/ns-windns-mdns_query_handle)
- [**MDNS_QUERY_REQUEST**](/windows/desktop/api/Windns/ns-windns-mdns_query_request)

Nell'API DNS sono incluse anche le strutture RR (Resource Record) seguenti. Queste strutture vengono usate con la struttura DNS_RECORD **per** gestire i record di risorse DNS a livello di codice.

- [**DNS_A_DATA**](/windows/win32/api/windns/ns-windns-dns_a_data)
- [**DNS_AAAA_DATA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data)
- [**DNS_ATMA_DATA**](/windows/win32/api/windns/ns-windns-dns_atma_data)
- [**DNS_DHCID_DATA**](/windows/win32/api/windns/ns-windns-dns_dhcid_data)
- [**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))
- [**DNS_DS_DATA**](/windows/win32/api/windns/ns-windns-dns_ds_data)
- [**DNS_KEY_DATA**](/windows/win32/api/windns/ns-windns-dns_key_data)
- [**DNS_LOC_DATA**](/windows/win32/api/windns/ns-windns-dns_loc_data)
- [**DNS_MINFO_DATA**](/windows/win32/api/windns/ns-windns-dns_minfo_dataw)
- [**DNS_MX_DATA**](/windows/win32/api/windns/ns-windns-dns_mx_dataa)
- [**DNS_NAPTR_DATA**](/windows/win32/api/windns/ns-windns-dns_naptr_dataw)
- [**DNS_NSEC_DATA**](/windows/win32/api/windns/ns-windns-dns_nsec_dataw)
- [**DNS_NULL_DATA**](/windows/win32/api/windns/ns-windns-dns_null_data)
- [**DNS_NXT_DATA**](/windows/win32/api/windns/ns-windns-dns_nxt_dataw)
- [**DNS_OPT_DATA**](/windows/win32/api/windns/ns-windns-dns_opt_data)
- [**DNS_PTR_DATA**](/windows/win32/api/windns/ns-windns-dns_ptr_dataw)
- [**DNS_RRSET**](/windows/win32/api/windns/ns-windns-dns_rrset)
- [**DNS_RRSIG_DATA**](/windows/win32/api/windns/ns-windns-dns_sig_dataw)
- [**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))
- [**DNS_SOA_DATA**](/windows/win32/api/windns/ns-windns-dns_soa_dataw)
- [**DNS_SRV_DATA**](/windows/win32/api/windns/ns-windns-dns_srv_dataw)
- [**DNS_TKEY_DATA**](/windows/win32/api/windns/ns-windns-dns_tkey_dataw)
- [**DNS_TSIG_DATA**](/windows/win32/api/windns/ns-windns-dns_tsig_dataw)
- [**DNS_TXT_DATA**](/windows/win32/api/windns/ns-windns-dns_txt_dataw)
- [**DNS_WINS_DATA**](/windows/win32/api/windns/ns-windns-dns_wins_data)
- [**DNS_WINSR_DATA**](/windows/win32/api/windns/ns-windns-dns_winsr_dataw)
- [**DNS_WIRE_QUESTION**](/windows/desktop/api/Windns/ns-windns-dns_wire_question)
- [**DNS_WIRE_RECORD**](/windows/desktop/api/Windns/ns-windns-dns_wire_record)
- [**DNS_WKS_DATA**](/windows/win32/api/windns/ns-windns-dns_wks_data)
