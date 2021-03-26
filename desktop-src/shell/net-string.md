---
description: Rappresentano i tipi di indirizzi di rete. Usare uno o più (come combinazione bit per bit) delle costanti seguenti per creare una maschera di indirizzo di rete da usare con la macro NetAddr \_ SetAllowType.
title: NET_STRING (Iphlpapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993773"
---
# <a name="net_string"></a>\_stringa net

Rappresentano i tipi di indirizzi di rete. Usare uno o più (come combinazione bit per bit) delle costanti seguenti per creare una maschera di indirizzo di rete da usare con la macro [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Costante                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**\_ \_ Indirizzo IPv4 stringa \_ net**</dt> </dl>                              | La stringa identifica un host/router IPv4 usando un indirizzo letterale (la porta o il prefisso non è consentito).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**\_Servizio NET String \_ IPv4 \_**</dt> </dl>                              | La stringa identifica un servizio IPv4 usando un indirizzo letterale (porta richiesta; prefisso non consentito).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**\_Rete stringa \_ IPv4 \_ net**</dt> </dl>                              | La stringa identifica una rete IPv4 (prefisso obbligatorio; la porta non è consentita).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**\_ \_ Indirizzo IPv6 stringa \_ net**</dt> </dl>                              | La stringa identifica un host/router IPv6 usando un indirizzo letterale (porta o prefisso non consentito; ID ambito consentito).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**\_ \_ Indirizzo IPv6 NET \_ String \_ senza \_ ambito**</dt> </dl> | La stringa identifica un host/router IPv6 usando un indirizzo letterale in cui il contesto dell'interfaccia è già noto (la porta o il prefisso non è consentito; ID ambito non consentito).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**\_ \_ Servizio IPv6 NET \_ String**</dt> </dl>                              | La stringa identifica un servizio IPv6 usando un indirizzo letterale (porta necessaria; prefisso non consentito; ID ambito consentito).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**\_ \_ Servizio IPv6 NET \_ String \_ senza \_ ambito**</dt> </dl> | La stringa identifica un servizio IPv6 usando un indirizzo letterale in cui il contesto dell'interfaccia è già noto (porta richiesta; prefisso non consentito; ID ambito non consentito).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**\_Rete stringa net \_ IPv6 \_**</dt> </dl>                              | La stringa identifica una rete IPv6 (prefisso obbligatorio, porta o ID ambito non consentito).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**\_indirizzo stringa net \_ denominato \_**</dt> </dl>                           | La stringa identifica un host Internet che usa il DNS (porta o prefisso o ID ambito non consentito).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ stringa \_ denominata \_ Service**</dt> </dl>                           | La stringa identifica un servizio Internet che usa DNS (porta richiesta; prefisso o ID ambito non consentito).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**\_ \_ indirizzo IP stringa \_ net**</dt> </dl>                                    | Indirizzo IPv4 della stringa di rete NET \_ \_ \_ Address \| \_ \_ IPv6 \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**\_ \_ indirizzo IP stringa \_ net \_ senza \_ ambito**</dt> </dl>       | Indirizzo \_ IPv4 NET String \_ net Address \_ \| \_ \_ IPv6 \_ \_ senza \_ ambito. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**NET \_ String \_ IP \_ Service**</dt> </dl>                                    | \_ \_ \_ \| \_ \_ \_ Servizio IPv6 NET String NET String.<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**\_ \_ servizio IP stringa \_ net \_ senza \_ ambito**</dt> </dl>       | stringa di rete \_ \_ denominata \_ indirizzo \| IP stringa net indirizzo \_ \_ \_ \_ nessun \_ ambito.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**\_ \_ rete IP stringa \_ net**</dt> </dl>                                    | Rete stringa net \_ \_ IPv4 \_ rete \| IPv6 rete \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**\_stringa net \_ Any \_ Address**</dt> </dl>                                 | stringa di rete \_ \_ denominata \_ indirizzo \| IP della \_ stringa \_ \_ di rete.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**\_stringa net \_ Any \_ Address \_ senza \_ ambito**</dt> </dl>    | stringa di rete \_ \_ denominata \_ indirizzo \| IP stringa net indirizzo \_ \_ \_ \_ nessun \_ ambito.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ String \_ Any \_ Service**</dt> </dl>                                 | \_stringa net \_ denominata \_ servizio \| net \_ String \_ IP \_ Service.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ String \_ Any \_ Service \_ senza \_ ambito**</dt> </dl>    | stringa di rete \_ \_ denominata \_ indirizzo \| IP stringa net indirizzo \_ \_ \_ \_ nessun \_ ambito.<br/>                                                                                                 |



## <a name="remarks"></a>Commenti

Questi valori sono definiti in iphlpapi. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Iphlpapi. h</dt> </dl> |



 

 




