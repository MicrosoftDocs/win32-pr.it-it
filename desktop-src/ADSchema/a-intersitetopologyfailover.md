---
title: Attribute tra siti-topologia-failover
description: Indica la quantità di tempo che deve trascorrere dall'ultimo Keep-Alive affinché il generatore di topologia tra siti venga considerato inattivo.
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- "Topologia tra siti: schema di AD dell'attributo di failover"
- Schema AD dell'attributo interSiteTopologyFailover
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480192"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="caad4-105">Attribute tra siti-topologia-failover</span><span class="sxs-lookup"><span data-stu-id="caad4-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="caad4-106">Indica la quantità di tempo che deve trascorrere dall'ultimo Keep-Alive affinché il generatore di topologia tra siti venga considerato inattivo.</span><span class="sxs-lookup"><span data-stu-id="caad4-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="caad4-107">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-107">Entry</span></span> | <span data-ttu-id="caad4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="caad4-109">CN</span><span class="sxs-lookup"><span data-stu-id="caad4-109">CN</span></span>                | <span data-ttu-id="caad4-110">Topologia tra siti-failover</span><span class="sxs-lookup"><span data-stu-id="caad4-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="caad4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="caad4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="caad4-112">interSiteTopologyFailover</span><span class="sxs-lookup"><span data-stu-id="caad4-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="caad4-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="caad4-113">Size</span></span>              | <span data-ttu-id="caad4-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="caad4-114">4 bytes</span></span>                              |
| <span data-ttu-id="caad4-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="caad4-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="caad4-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="caad4-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="caad4-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-117">Attribute-Id</span></span>      | <span data-ttu-id="caad4-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="caad4-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="caad4-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="caad4-119">System-Id-Guid</span></span>    | <span data-ttu-id="caad4-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="caad4-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="caad4-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="caad4-121">Syntax</span></span>            | [<span data-ttu-id="caad4-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="caad4-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="caad4-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="caad4-123">Implementations</span></span>

-   [<span data-ttu-id="caad4-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="caad4-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="caad4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="caad4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="caad4-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="caad4-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="caad4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="caad4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="caad4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="caad4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="caad4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="caad4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="caad4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="caad4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="caad4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="caad4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="caad4-132">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-132">Entry</span></span> | <span data-ttu-id="caad4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-136">System-Only</span></span>            | <span data-ttu-id="caad4-137">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-137">False</span></span>                                                       |
| <span data-ttu-id="caad4-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-139">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-139">True</span></span>                                                        |
| <span data-ttu-id="caad4-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-140">Is Indexed</span></span>             | <span data-ttu-id="caad4-141">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-141">False</span></span>                                                       |
| <span data-ttu-id="caad4-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-142">In Global Catalog</span></span>      | <span data-ttu-id="caad4-143">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-143">False</span></span>                                                       |
| <span data-ttu-id="caad4-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-148">Search-Flags</span></span>           | <span data-ttu-id="caad4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-150">System-Flags</span></span>           | <span data-ttu-id="caad4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-152">Classes used in</span></span>        | [<span data-ttu-id="caad4-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="caad4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="caad4-154">Windows Server 2003</span></span>



| <span data-ttu-id="caad4-155">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-155">Entry</span></span> | <span data-ttu-id="caad4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-159">System-Only</span></span>            | <span data-ttu-id="caad4-160">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-160">False</span></span>                                                       |
| <span data-ttu-id="caad4-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-162">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-162">True</span></span>                                                        |
| <span data-ttu-id="caad4-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-163">Is Indexed</span></span>             | <span data-ttu-id="caad4-164">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-164">False</span></span>                                                       |
| <span data-ttu-id="caad4-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-165">In Global Catalog</span></span>      | <span data-ttu-id="caad4-166">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-166">False</span></span>                                                       |
| <span data-ttu-id="caad4-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-171">Search-Flags</span></span>           | <span data-ttu-id="caad4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-173">System-Flags</span></span>           | <span data-ttu-id="caad4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-175">Classes used in</span></span>        | [<span data-ttu-id="caad4-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="caad4-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="caad4-177">ADAM</span></span>



| <span data-ttu-id="caad4-178">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-178">Entry</span></span> | <span data-ttu-id="caad4-179">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-182">System-Only</span></span>            | <span data-ttu-id="caad4-183">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-183">False</span></span>                                                       |
| <span data-ttu-id="caad4-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-185">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-185">True</span></span>                                                        |
| <span data-ttu-id="caad4-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-186">Is Indexed</span></span>             | <span data-ttu-id="caad4-187">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-187">False</span></span>                                                       |
| <span data-ttu-id="caad4-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-188">In Global Catalog</span></span>      | <span data-ttu-id="caad4-189">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-189">False</span></span>                                                       |
| <span data-ttu-id="caad4-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-194">Search-Flags</span></span>           | <span data-ttu-id="caad4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-196">System-Flags</span></span>           | <span data-ttu-id="caad4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-198">Classes used in</span></span>        | [<span data-ttu-id="caad4-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="caad4-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="caad4-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="caad4-201">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-201">Entry</span></span> | <span data-ttu-id="caad4-202">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-205">System-Only</span></span>            | <span data-ttu-id="caad4-206">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-206">False</span></span>                                                       |
| <span data-ttu-id="caad4-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-208">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-208">True</span></span>                                                        |
| <span data-ttu-id="caad4-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-209">Is Indexed</span></span>             | <span data-ttu-id="caad4-210">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-210">False</span></span>                                                       |
| <span data-ttu-id="caad4-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-211">In Global Catalog</span></span>      | <span data-ttu-id="caad4-212">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-212">False</span></span>                                                       |
| <span data-ttu-id="caad4-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-217">Search-Flags</span></span>           | <span data-ttu-id="caad4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-219">System-Flags</span></span>           | <span data-ttu-id="caad4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-221">Classes used in</span></span>        | [<span data-ttu-id="caad4-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="caad4-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="caad4-223">Windows Server 2008</span></span>



| <span data-ttu-id="caad4-224">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-224">Entry</span></span> | <span data-ttu-id="caad4-225">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-228">System-Only</span></span>            | <span data-ttu-id="caad4-229">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-229">False</span></span>                                                       |
| <span data-ttu-id="caad4-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-231">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-231">True</span></span>                                                        |
| <span data-ttu-id="caad4-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-232">Is Indexed</span></span>             | <span data-ttu-id="caad4-233">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-233">False</span></span>                                                       |
| <span data-ttu-id="caad4-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-234">In Global Catalog</span></span>      | <span data-ttu-id="caad4-235">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-235">False</span></span>                                                       |
| <span data-ttu-id="caad4-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-240">Search-Flags</span></span>           | <span data-ttu-id="caad4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-242">System-Flags</span></span>           | <span data-ttu-id="caad4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-244">Classes used in</span></span>        | [<span data-ttu-id="caad4-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="caad4-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="caad4-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="caad4-247">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-247">Entry</span></span> | <span data-ttu-id="caad4-248">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-251">System-Only</span></span>            | <span data-ttu-id="caad4-252">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-252">False</span></span>                                                       |
| <span data-ttu-id="caad4-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-254">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-254">True</span></span>                                                        |
| <span data-ttu-id="caad4-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-255">Is Indexed</span></span>             | <span data-ttu-id="caad4-256">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-256">False</span></span>                                                       |
| <span data-ttu-id="caad4-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-257">In Global Catalog</span></span>      | <span data-ttu-id="caad4-258">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-258">False</span></span>                                                       |
| <span data-ttu-id="caad4-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-263">Search-Flags</span></span>           | <span data-ttu-id="caad4-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-265">System-Flags</span></span>           | <span data-ttu-id="caad4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-267">Classes used in</span></span>        | [<span data-ttu-id="caad4-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="caad4-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="caad4-269">Windows Server 2012</span></span>



| <span data-ttu-id="caad4-270">Voce</span><span class="sxs-lookup"><span data-stu-id="caad4-270">Entry</span></span> | <span data-ttu-id="caad4-271">Valore</span><span class="sxs-lookup"><span data-stu-id="caad4-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="caad4-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="caad4-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="caad4-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="caad4-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="caad4-274">System-Only</span></span>            | <span data-ttu-id="caad4-275">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-275">False</span></span>                                                       |
| <span data-ttu-id="caad4-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="caad4-276">Is-Single-Valued</span></span>       | <span data-ttu-id="caad4-277">Vero</span><span class="sxs-lookup"><span data-stu-id="caad4-277">True</span></span>                                                        |
| <span data-ttu-id="caad4-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="caad4-278">Is Indexed</span></span>             | <span data-ttu-id="caad4-279">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-279">False</span></span>                                                       |
| <span data-ttu-id="caad4-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="caad4-280">In Global Catalog</span></span>      | <span data-ttu-id="caad4-281">Falso</span><span class="sxs-lookup"><span data-stu-id="caad4-281">False</span></span>                                                       |
| <span data-ttu-id="caad4-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="caad4-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="caad4-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="caad4-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="caad4-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="caad4-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="caad4-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="caad4-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-286">Search-Flags</span></span>           | <span data-ttu-id="caad4-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="caad4-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="caad4-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="caad4-288">System-Flags</span></span>           | <span data-ttu-id="caad4-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="caad4-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="caad4-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="caad4-290">Classes used in</span></span>        | [<span data-ttu-id="caad4-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="caad4-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





