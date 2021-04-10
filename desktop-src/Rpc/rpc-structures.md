---
title: Strutture RPC
description: In questa sezione vengono illustrate le strutture definite e utilizzate da Microsoft RPC.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- RPC, informazioni di riferimento e strutture Remote Procedure Call
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729402"
---
# <a name="rpc-structures"></a><span data-ttu-id="098d9-104">Strutture RPC</span><span class="sxs-lookup"><span data-stu-id="098d9-104">RPC Structures</span></span>

<span data-ttu-id="098d9-105">In questa sezione vengono illustrate le strutture definite e utilizzate da Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="098d9-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="098d9-106">[**\_SCONTEXT NDR**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="098d9-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="098d9-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="098d9-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="098d9-108">**\_informazioni sul \_ marshalling dell'utente NDR \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="098d9-109">**\_Informazioni sul marshalling utente del rapporto di recapito \_ \_ \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="098d9-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="098d9-110">**\_informazioni di \_ notifica \_ asincrona RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="098d9-111">**\_stato asincrono \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="098d9-112">**\_Opzioni dell'handle di binding RPC \_ \_ \_ V1**</span><span class="sxs-lookup"><span data-stu-id="098d9-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="098d9-113">**\_ \_ \_ Sicurezza \_ V1 handle di binding RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="098d9-114">**\_Modello di handle di binding RPC \_ \_ \_ V1**</span><span class="sxs-lookup"><span data-stu-id="098d9-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="098d9-115">**\_vettore di binding RPC \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="098d9-116">**\_descrittore di \_ autenticazione del cookie C opt \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="098d9-117">**\_Attributi di chiamata RPC \_ \_ V1**</span><span class="sxs-lookup"><span data-stu-id="098d9-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="098d9-118">**\_Attributi di chiamata RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="098d9-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="098d9-119">**\_Indirizzo locale della chiamata RPC \_ \_ \_ V1**</span><span class="sxs-lookup"><span data-stu-id="098d9-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="098d9-120">**\_interfaccia client \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="098d9-121">**\_tabella dispatch \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="098d9-122">**\_ \_ param info EE \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="098d9-123">**\_modello di endpoint RPC \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="098d9-124">**\_ \_ handle enum errore \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="098d9-125">**\_informazioni sugli \_ errori EStesi RPC \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="098d9-126">**\_credenziali di \_ trasporto \_ http RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="098d9-127">**\_Credenziali di \_ trasporto http RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="098d9-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="098d9-128">**\_Credenziali di \_ trasporto http RPC \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="098d9-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="098d9-129">**\_ID RPC if \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="098d9-130">**\_ \_ vettore ID RPC \_ if**</span><span class="sxs-lookup"><span data-stu-id="098d9-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="098d9-131">**\_modello di interfaccia RPC \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="098d9-132">**\_criterio RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="098d9-133">**\_vettore PROTSEQ \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="098d9-134">**\_QoS di sicurezza RPC \_**</span><span class="sxs-lookup"><span data-stu-id="098d9-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="098d9-135">**\_QoS di sicurezza RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="098d9-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="098d9-136">**\_QoS di sicurezza RPC \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="098d9-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="098d9-137">**\_QoS di sicurezza RPC \_ \_ V4**</span><span class="sxs-lookup"><span data-stu-id="098d9-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="098d9-138">**\_QoS di sicurezza RPC \_ \_ V5**</span><span class="sxs-lookup"><span data-stu-id="098d9-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="098d9-139">**\_vettore statistiche \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="098d9-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="098d9-140">**\_ \_ identità autenticazione WINNT \_ sec**</span><span class="sxs-lookup"><span data-stu-id="098d9-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="098d9-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="098d9-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="098d9-142">**\_vettore UUID**</span><span class="sxs-lookup"><span data-stu-id="098d9-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 