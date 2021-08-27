---
description: Rappresentano i tipi di indirizzi di rete. Usare una o più costanti seguenti (come combinazione bit per bit) per creare una maschera di indirizzi di rete da usare con la macro NetAddr \_ SetAllowType.
title: NET_STRING (Iphlpapi.h)
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
ms.openlocfilehash: a7d1a09e6165e77ee5419da47419a65e3995ce0ffedb8a6fb71f01fb9c63dde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111221"
---
# <a name="net_string"></a>STRINGA \_ DI RETE

Rappresentano i tipi di indirizzi di rete. Usare una o più costanti seguenti (come combinazione bit per bit) per creare una maschera di indirizzi di rete da usare con la macro [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Costante                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**INDIRIZZO \_ \_ IPV4 DELLA STRINGA \_ DI RETE**</dt> </dl>                              | La stringa identifica un host/router IPv4 usando un indirizzo letterale (porta o prefisso non consentito).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**SERVIZIO \_ NET STRING \_ IPV4 \_**</dt> </dl>                              | La stringa identifica un servizio IPv4 usando un indirizzo letterale (porta obbligatoria; prefisso non consentito).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ NETWORK**</dt> </dl>                              | La stringa identifica una rete IPv4 (prefisso obbligatorio; porta non consentita).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**INDIRIZZO \_ \_ IPV6 DELLA STRINGA \_ DI RETE**</dt> </dl>                              | La stringa identifica un host/router IPv6 usando un indirizzo letterale (porta o prefisso non consentito; scope-id consentito).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl> | La stringa identifica un host/router IPv6 usando un indirizzo letterale in cui il contesto dell'interfaccia è già noto (porta o prefisso non consentito; scope-id non consentito).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**SERVIZIO \_ NET STRING \_ IPV6 \_**</dt> </dl>                              | La stringa identifica un servizio IPv6 usando un indirizzo letterale (porta obbligatoria; prefisso non consentito; scope-id consentito).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ SERVICE \_ NO \_ SCOPE**</dt> </dl> | La stringa identifica un servizio IPv6 usando un indirizzo letterale in cui il contesto dell'interfaccia è già noto (porta obbligatoria; prefisso non consentito; scope-id non consentito).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ NETWORK**</dt> </dl>                              | La stringa identifica una rete IPv6 (prefisso obbligatorio; porta o id ambito non consentito).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**INDIRIZZO \_ DENOMINATO DELLA STRINGA DI \_ \_ RETE**</dt> </dl>                           | La stringa identifica un host Internet usando DNS(porta o prefisso o id ambito non consentito).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ STRING \_ NAMED \_ SERVICE**</dt> </dl>                           | La stringa identifica un servizio Internet tramite DNS (porta obbligatoria; prefisso o id ambito non consentito).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**INDIRIZZO \_ \_ IP DELLA STRINGA DI \_ RETE**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ ADDRESS NET STRING \| \_ \_ IPV6 ADDRESS (INDIRIZZO NET STRING IPV6). \_<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**INDIRIZZO \_ \_ IP DELLA STRINGA DI RETE \_ SENZA \_ \_ AMBITO**</dt> </dl>       | NET \_ STRING \_ IPV4 \_ ADDRESS NET STRING \| \_ \_ IPV6 ADDRESS NO SCOPE .NET STRING IPV6 ADDRESS NO SCOPE ( INDIRIZZO IPV6 NET STRING IPV4 ADDRESS NET STRING IPV6 \_ ADDRESS NO \_ \_ SCOPE). <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**SERVIZIO \_ \_ IP DELLA STRINGA DI \_ RETE**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ SERVICE NET STRING \| \_ \_ IPV6 \_ SERVICE .<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>       | NET STRING NAMED ADDRESS NET STRING IP ADDRESS NO SCOPE (INDIRIZZO IP DELLA STRINGA DI RETE \_ \_ SENZA \_ \| \_ \_ \_ \_ \_ AMBITO).<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**RETE \_ \_ IP DELLA STRINGA DI \_ RETE**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ NETWORK NET STRING \| \_ \_ IPV6 NETWORK .NET STRING IPV6 \_ NETWORK<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS**</dt> </dl>                                 | NET \_ STRING NAMED ADDRESS NET STRING IP ADDRESS \_ \_ \| \_ \_ \_ .<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl>    | NET STRING NAMED ADDRESS NET STRING IP ADDRESS NO SCOPE (INDIRIZZO IP DELLA STRINGA DI RETE \_ \_ SENZA \_ \| \_ \_ \_ \_ \_ AMBITO).<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE**</dt> </dl>                                 | STRINGA \_ DI RETE DENOMINATA SERVIZIO NET STRING IP \_ \_ \| \_ \_ \_ SERVICE.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>    | NET STRING NAMED ADDRESS NET STRING IP ADDRESS NO SCOPE (INDIRIZZO IP DELLA STRINGA DI RETE \_ \_ SENZA \_ \| \_ \_ \_ \_ \_ AMBITO).<br/>                                                                                                 |



## <a name="remarks"></a>Commenti

Questi valori sono definiti in Iphlpapi.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Iphlpapi.h</dt> </dl> |



 

 




