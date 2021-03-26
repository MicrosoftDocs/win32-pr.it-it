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
# <a name="net_string"></a><span data-ttu-id="59b0a-104">\_stringa net</span><span class="sxs-lookup"><span data-stu-id="59b0a-104">NET\_STRING</span></span>

<span data-ttu-id="59b0a-105">Rappresentano i tipi di indirizzi di rete.</span><span class="sxs-lookup"><span data-stu-id="59b0a-105">Represent network address types.</span></span> <span data-ttu-id="59b0a-106">Usare uno o più (come combinazione bit per bit) delle costanti seguenti per creare una maschera di indirizzo di rete da usare con la macro [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).</span><span class="sxs-lookup"><span data-stu-id="59b0a-106">Use one or more (as a bitwise combination) of the following constants to create a network address mask to use with the macro [**NetAddr\_SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).</span></span>



| <span data-ttu-id="59b0a-107">Costante</span><span class="sxs-lookup"><span data-stu-id="59b0a-107">Constant</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="59b0a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59b0a-108">Description</span></span>                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <span data-ttu-id="59b0a-109"><dt>**\_ \_ Indirizzo IPv4 stringa \_ net**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-109"><dt>**NET\_STRING\_IPV4\_ADDRESS**</dt></span></span> </dl>                              | <span data-ttu-id="59b0a-110">La stringa identifica un host/router IPv4 usando un indirizzo letterale (la porta o il prefisso non è consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-110">The string identifies an IPv4 host/router using literal address (port or prefix not allowed).</span></span><br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <span data-ttu-id="59b0a-111"><dt>**\_Servizio NET String \_ IPv4 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-111"><dt>**NET\_STRING\_IPV4\_SERVICE**</dt></span></span> </dl>                              | <span data-ttu-id="59b0a-112">La stringa identifica un servizio IPv4 usando un indirizzo letterale (porta richiesta; prefisso non consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-112">The string identifies an IPv4 service using literal address (port required; prefix not allowed).</span></span><br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <span data-ttu-id="59b0a-113"><dt>**\_Rete stringa \_ IPv4 \_ net**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-113"><dt>**NET\_STRING\_IPV4\_NETWORK**</dt></span></span> </dl>                              | <span data-ttu-id="59b0a-114">La stringa identifica una rete IPv4 (prefisso obbligatorio; la porta non è consentita).</span><span class="sxs-lookup"><span data-stu-id="59b0a-114">The string identifies an IPv4 network (prefix required; port not allowed).</span></span><br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <span data-ttu-id="59b0a-115"><dt>**\_ \_ Indirizzo IPv6 stringa \_ net**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-115"><dt>**NET\_STRING\_IPV6\_ADDRESS**</dt></span></span> </dl>                              | <span data-ttu-id="59b0a-116">La stringa identifica un host/router IPv6 usando un indirizzo letterale (porta o prefisso non consentito; ID ambito consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-116">The string identifies an IPv6 Host/router using literal address (port or prefix not allowed; scope-id allowed.)</span></span><br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <span data-ttu-id="59b0a-117"><dt>**\_ \_ Indirizzo IPv6 NET \_ String \_ senza \_ ambito**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-117"><dt>**NET\_STRING\_IPV6\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl> | <span data-ttu-id="59b0a-118">La stringa identifica un host/router IPv6 usando un indirizzo letterale in cui il contesto dell'interfaccia è già noto (la porta o il prefisso non è consentito; ID ambito non consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-118">The string identifies an IPv6 Host/router using literal address where the interface context is already known (port or prefix not allowed; scope-id not allowed).</span></span><br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <span data-ttu-id="59b0a-119"><dt>**\_ \_ Servizio IPv6 NET \_ String**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-119"><dt>**NET\_STRING\_IPV6\_SERVICE**</dt></span></span> </dl>                              | <span data-ttu-id="59b0a-120">La stringa identifica un servizio IPv6 usando un indirizzo letterale (porta necessaria; prefisso non consentito; ID ambito consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-120">The string identifies an IPv6 service using literal address (port required; prefix not allowed; scope-id allowed).</span></span><br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <span data-ttu-id="59b0a-121"><dt>**\_ \_ Servizio IPv6 NET \_ String \_ senza \_ ambito**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-121"><dt>**NET\_STRING\_IPV6\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl> | <span data-ttu-id="59b0a-122">La stringa identifica un servizio IPv6 usando un indirizzo letterale in cui il contesto dell'interfaccia è già noto (porta richiesta; prefisso non consentito; ID ambito non consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-122">The string identifies an IPv6 service using literal address where the interface context is already known (port required; prefix not allowed; scope-id not allowed).</span></span><br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <span data-ttu-id="59b0a-123"><dt>**\_Rete stringa net \_ IPv6 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-123"><dt>**NET\_STRING\_IPV6\_NETWORK**</dt></span></span> </dl>                              | <span data-ttu-id="59b0a-124">La stringa identifica una rete IPv6 (prefisso obbligatorio, porta o ID ambito non consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-124">The string identifies an IPv6 network (prefix required; port or scope-id not allowed).</span></span><br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <span data-ttu-id="59b0a-125"><dt>**\_indirizzo stringa net \_ denominato \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-125"><dt>**NET\_STRING\_NAMED\_ADDRESS**</dt></span></span> </dl>                           | <span data-ttu-id="59b0a-126">La stringa identifica un host Internet che usa il DNS (porta o prefisso o ID ambito non consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-126">The string identifies an Internet Host using the DNS(port or prefix or scope-id not allowed).</span></span><br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <span data-ttu-id="59b0a-127"><dt>**NET \_ stringa \_ denominata \_ Service**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-127"><dt>**NET\_STRING\_NAMED\_SERVICE**</dt></span></span> </dl>                           | <span data-ttu-id="59b0a-128">La stringa identifica un servizio Internet che usa DNS (porta richiesta; prefisso o ID ambito non consentito).</span><span class="sxs-lookup"><span data-stu-id="59b0a-128">The string identifies an Internet service using DNS (port required; prefix or scope-id not allowed).</span></span><br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <span data-ttu-id="59b0a-129"><dt>**\_ \_ indirizzo IP stringa \_ net**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-129"><dt>**NET\_STRING\_IP\_ADDRESS**</dt></span></span> </dl>                                    | <span data-ttu-id="59b0a-130">Indirizzo IPv4 della stringa di rete NET \_ \_ \_ Address \| \_ \_ IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="59b0a-130">NET\_STRING\_IPV4\_ADDRESS \| NET\_STRING\_IPV6\_ADDRESS.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <span data-ttu-id="59b0a-131"><dt>**\_ \_ indirizzo IP stringa \_ net \_ senza \_ ambito**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-131"><dt>**NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl>       | <span data-ttu-id="59b0a-132">Indirizzo \_ IPv4 NET String \_ net Address \_ \| \_ \_ IPv6 \_ \_ senza \_ ambito.</span><span class="sxs-lookup"><span data-stu-id="59b0a-132">NET\_STRING\_IPV4\_ADDRESS \| NET\_STRING\_IPV6\_ADDRESS\_NO\_SCOPE.</span></span> <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <span data-ttu-id="59b0a-133"><dt>**NET \_ String \_ IP \_ Service**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-133"><dt>**NET\_STRING\_IP\_SERVICE**</dt></span></span> </dl>                                    | <span data-ttu-id="59b0a-134">\_ \_ \_ \| \_ \_ \_ Servizio IPv6 NET String NET String.</span><span class="sxs-lookup"><span data-stu-id="59b0a-134">NET\_STRING\_IPV4\_SERVICE \| NET\_STRING\_IPV6\_SERVICE.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <span data-ttu-id="59b0a-135"><dt>**\_ \_ servizio IP stringa \_ net \_ senza \_ ambito**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-135"><dt>**NET\_STRING\_IP\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl>       | <span data-ttu-id="59b0a-136">stringa di rete \_ \_ denominata \_ indirizzo \| IP stringa net indirizzo \_ \_ \_ \_ nessun \_ ambito.</span><span class="sxs-lookup"><span data-stu-id="59b0a-136">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <span data-ttu-id="59b0a-137"><dt>**\_ \_ rete IP stringa \_ net**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-137"><dt>**NET\_STRING\_IP\_NETWORK**</dt></span></span> </dl>                                    | <span data-ttu-id="59b0a-138">Rete stringa net \_ \_ IPv4 \_ rete \| IPv6 rete \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="59b0a-138">NET\_STRING\_IPV4\_NETWORK \| NET\_STRING\_IPV6\_NETWORK.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <span data-ttu-id="59b0a-139"><dt>**\_stringa net \_ Any \_ Address**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-139"><dt>**NET\_STRING\_ANY\_ADDRESS**</dt></span></span> </dl>                                 | <span data-ttu-id="59b0a-140">stringa di rete \_ \_ denominata \_ indirizzo \| IP della \_ stringa \_ \_ di rete.</span><span class="sxs-lookup"><span data-stu-id="59b0a-140">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS.</span></span><br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <span data-ttu-id="59b0a-141"><dt>**\_stringa net \_ Any \_ Address \_ senza \_ ambito**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-141"><dt>**NET\_STRING\_ANY\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl>    | <span data-ttu-id="59b0a-142">stringa di rete \_ \_ denominata \_ indirizzo \| IP stringa net indirizzo \_ \_ \_ \_ nessun \_ ambito.</span><span class="sxs-lookup"><span data-stu-id="59b0a-142">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <span data-ttu-id="59b0a-143"><dt>**NET \_ String \_ Any \_ Service**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-143"><dt>**NET\_STRING\_ANY\_SERVICE**</dt></span></span> </dl>                                 | <span data-ttu-id="59b0a-144">\_stringa net \_ denominata \_ servizio \| net \_ String \_ IP \_ Service.</span><span class="sxs-lookup"><span data-stu-id="59b0a-144">NET\_STRING\_NAMED\_SERVICE \| NET\_STRING\_IP\_SERVICE.</span></span><br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <span data-ttu-id="59b0a-145"><dt>**NET \_ String \_ Any \_ Service \_ senza \_ ambito**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-145"><dt>**NET\_STRING\_ANY\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl>    | <span data-ttu-id="59b0a-146">stringa di rete \_ \_ denominata \_ indirizzo \| IP stringa net indirizzo \_ \_ \_ \_ nessun \_ ambito.</span><span class="sxs-lookup"><span data-stu-id="59b0a-146">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="59b0a-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="59b0a-147">Remarks</span></span>

<span data-ttu-id="59b0a-148">Questi valori sono definiti in iphlpapi. h.</span><span class="sxs-lookup"><span data-stu-id="59b0a-148">These values are defined in Iphlpapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b0a-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59b0a-149">Requirements</span></span>



| <span data-ttu-id="59b0a-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b0a-150">Requirement</span></span> | <span data-ttu-id="59b0a-151">Valore</span><span class="sxs-lookup"><span data-stu-id="59b0a-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59b0a-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59b0a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="59b0a-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59b0a-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59b0a-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59b0a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="59b0a-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59b0a-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59b0a-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59b0a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b0a-157"><dt>Iphlpapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b0a-157"><dt>Iphlpapi.h</dt></span></span> </dl> |



 

 




