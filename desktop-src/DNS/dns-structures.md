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
ms.openlocfilehash: da0e83639eaa92e84dd076e797431d5f7138245c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588032"
---
# <a name="dns-structures"></a><span data-ttu-id="0fb31-106">Strutture DNS</span><span class="sxs-lookup"><span data-stu-id="0fb31-106">DNS Structures</span></span>

<span data-ttu-id="0fb31-107">Le strutture seguenti sono definite per l'uso con DNS:</span><span class="sxs-lookup"><span data-stu-id="0fb31-107">The following structures are defined for use with DNS:</span></span>

- [<span data-ttu-id="0fb31-108">**DNS_ADDR**</span><span class="sxs-lookup"><span data-stu-id="0fb31-108">**DNS_ADDR**</span></span>](/windows/win32/api/windns/ns-windns-dns_addr)
- [<span data-ttu-id="0fb31-109">**DNS_ADDR_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="0fb31-109">**DNS_ADDR_ARRAY**</span></span>](/windows/win32/api/windns/ns-windns-dns_addr_array)
- [<span data-ttu-id="0fb31-110">**DNS_CUSTOM_SERVER**</span><span class="sxs-lookup"><span data-stu-id="0fb31-110">**DNS_CUSTOM_SERVER**</span></span>](/windows/win32/api/windns/ns-windns-dns_custom_server)
- [<span data-ttu-id="0fb31-111">**DNS_HEADER**</span><span class="sxs-lookup"><span data-stu-id="0fb31-111">**DNS_HEADER**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_header)
- [<span data-ttu-id="0fb31-112">**DNS_MESSAGE_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="0fb31-112">**DNS_MESSAGE_BUFFER**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_message_buffer)
- [<span data-ttu-id="0fb31-113">**DNS_PROXY_INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="0fb31-113">**DNS_PROXY_INFORMATION**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_proxy_information)
- [<span data-ttu-id="0fb31-114">**DNS_QUERY_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="0fb31-114">**DNS_QUERY_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_query_request)
- [<span data-ttu-id="0fb31-115">**DNS_QUERY_REQUEST3**</span><span class="sxs-lookup"><span data-stu-id="0fb31-115">**DNS_QUERY_REQUEST3**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_query_request3)
- [<span data-ttu-id="0fb31-116">**DNS_RECORD**</span><span class="sxs-lookup"><span data-stu-id="0fb31-116">**DNS_RECORD**</span></span>](/windows/win32/api/windns/ns-windns-dns_recorda)
- [<span data-ttu-id="0fb31-117">**DNS_RECORD_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="0fb31-117">**DNS_RECORD_FLAGS**</span></span>](/windows/win32/api/windns/ns-windns-dns_record_flags)
- [<span data-ttu-id="0fb31-118">**DNS_SERVICE_BROWSE_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="0fb31-118">**DNS_SERVICE_BROWSE_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_browse_request)
- [<span data-ttu-id="0fb31-119">**DNS_SERVICE_CANCEL**</span><span class="sxs-lookup"><span data-stu-id="0fb31-119">**DNS_SERVICE_CANCEL**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_cancel)
- [<span data-ttu-id="0fb31-120">**DNS_SERVICE_INSTANCE**</span><span class="sxs-lookup"><span data-stu-id="0fb31-120">**DNS_SERVICE_INSTANCE**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_instance)
- [<span data-ttu-id="0fb31-121">**DNS_SERVICE_REGISTER_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="0fb31-121">**DNS_SERVICE_REGISTER_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_register_request)
- [<span data-ttu-id="0fb31-122">**DNS_SERVICE_RESOLVE_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="0fb31-122">**DNS_SERVICE_RESOLVE_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_service_resolve_request)
- [<span data-ttu-id="0fb31-123">**IP4_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="0fb31-123">**IP4_ARRAY**</span></span>](/windows/desktop/api/Windns/ns-windns-ip4_array)
- [<span data-ttu-id="0fb31-124">**IP6_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="0fb31-124">**IP6_ADDRESS**</span></span>](/windows/win32/api/windns/ns-windns-ip6_address)
- [<span data-ttu-id="0fb31-125">**MDNS_QUERY_HANDLE**</span><span class="sxs-lookup"><span data-stu-id="0fb31-125">**MDNS_QUERY_HANDLE**</span></span>](/windows/desktop/api/Windns/ns-windns-mdns_query_handle)
- [<span data-ttu-id="0fb31-126">**MDNS_QUERY_REQUEST**</span><span class="sxs-lookup"><span data-stu-id="0fb31-126">**MDNS_QUERY_REQUEST**</span></span>](/windows/desktop/api/Windns/ns-windns-mdns_query_request)

<span data-ttu-id="0fb31-127">Nell'API DNS sono incluse anche le strutture RR (Resource Record) seguenti.</span><span class="sxs-lookup"><span data-stu-id="0fb31-127">The following Resource Record (RR) structures are also included in the DNS API.</span></span> <span data-ttu-id="0fb31-128">Queste strutture vengono usate con la struttura DNS_RECORD **per** gestire i record di risorse DNS a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="0fb31-128">These structures are used with the **DNS_RECORD** structure to programmatically manage DNS resource records.</span></span>

- [<span data-ttu-id="0fb31-129">**DNS_A_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-129">**DNS_A_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_a_data)
- [<span data-ttu-id="0fb31-130">**DNS_AAAA_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-130">**DNS_AAAA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_aaaa_data)
- [<span data-ttu-id="0fb31-131">**DNS_ATMA_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-131">**DNS_ATMA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_atma_data)
- [<span data-ttu-id="0fb31-132">**DNS_DHCID_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-132">**DNS_DHCID_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_dhcid_data)
- <span data-ttu-id="0fb31-133">[**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fb31-133">[**DNS_DNSKEY_DATA**](/previous-versions/windows/desktop/legacy/dd392295(v=vs.85))</span></span>
- [<span data-ttu-id="0fb31-134">**DNS_DS_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-134">**DNS_DS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_ds_data)
- [<span data-ttu-id="0fb31-135">**DNS_KEY_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-135">**DNS_KEY_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_key_data)
- [<span data-ttu-id="0fb31-136">**DNS_LOC_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-136">**DNS_LOC_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_loc_data)
- [<span data-ttu-id="0fb31-137">**DNS_MINFO_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-137">**DNS_MINFO_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_minfo_dataw)
- [<span data-ttu-id="0fb31-138">**DNS_MX_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-138">**DNS_MX_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_mx_dataa)
- [<span data-ttu-id="0fb31-139">**DNS_NAPTR_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-139">**DNS_NAPTR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_naptr_dataw)
- [<span data-ttu-id="0fb31-140">**DNS_NSEC_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-140">**DNS_NSEC_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_nsec_dataw)
- [<span data-ttu-id="0fb31-141">**DNS_NULL_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-141">**DNS_NULL_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_null_data)
- [<span data-ttu-id="0fb31-142">**DNS_NXT_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-142">**DNS_NXT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_nxt_dataw)
- [<span data-ttu-id="0fb31-143">**DNS_OPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-143">**DNS_OPT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_opt_data)
- [<span data-ttu-id="0fb31-144">**DNS_PTR_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-144">**DNS_PTR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_ptr_dataw)
- [<span data-ttu-id="0fb31-145">**DNS_RRSET**</span><span class="sxs-lookup"><span data-stu-id="0fb31-145">**DNS_RRSET**</span></span>](/windows/win32/api/windns/ns-windns-dns_rrset)
- [<span data-ttu-id="0fb31-146">**DNS_RRSIG_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-146">**DNS_RRSIG_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_sig_dataw)
- <span data-ttu-id="0fb31-147">[**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fb31-147">[**DNS_SIG_DATA**](/previous-versions/windows/desktop/legacy/ms682094(v=vs.85))</span></span>
- [<span data-ttu-id="0fb31-148">**DNS_SOA_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-148">**DNS_SOA_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_soa_dataw)
- [<span data-ttu-id="0fb31-149">**DNS_SRV_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-149">**DNS_SRV_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_srv_dataw)
- [<span data-ttu-id="0fb31-150">**DNS_TKEY_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-150">**DNS_TKEY_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_tkey_dataw)
- [<span data-ttu-id="0fb31-151">**DNS_TSIG_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-151">**DNS_TSIG_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_tsig_dataw)
- [<span data-ttu-id="0fb31-152">**DNS_TXT_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-152">**DNS_TXT_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_txt_dataw)
- [<span data-ttu-id="0fb31-153">**DNS_WINS_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-153">**DNS_WINS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_wins_data)
- [<span data-ttu-id="0fb31-154">**DNS_WINSR_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-154">**DNS_WINSR_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_winsr_dataw)
- [<span data-ttu-id="0fb31-155">**DNS_WIRE_QUESTION**</span><span class="sxs-lookup"><span data-stu-id="0fb31-155">**DNS_WIRE_QUESTION**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_wire_question)
- [<span data-ttu-id="0fb31-156">**DNS_WIRE_RECORD**</span><span class="sxs-lookup"><span data-stu-id="0fb31-156">**DNS_WIRE_RECORD**</span></span>](/windows/desktop/api/Windns/ns-windns-dns_wire_record)
- [<span data-ttu-id="0fb31-157">**DNS_WKS_DATA**</span><span class="sxs-lookup"><span data-stu-id="0fb31-157">**DNS_WKS_DATA**</span></span>](/windows/win32/api/windns/ns-windns-dns_wks_data)
