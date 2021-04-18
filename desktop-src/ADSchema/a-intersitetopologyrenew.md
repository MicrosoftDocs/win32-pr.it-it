---
title: Attributo tra siti-topologia-rinnovo
description: Questa classe indica la frequenza con cui il generatore di topologia tra siti aggiorna il messaggio keep-alive inviato ai controller di dominio contenuti nello stesso sito.
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- Schema AD per l'attributo tra siti-topologia-rinnovo
- Schema AD dell'attributo interSiteTopologyRenew
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303337"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="2f05e-105">Attributo tra siti-topologia-rinnovo</span><span class="sxs-lookup"><span data-stu-id="2f05e-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="2f05e-106">Questa classe indica la frequenza con cui il generatore di topologia tra siti aggiorna il messaggio keep-alive inviato ai controller di dominio contenuti nello stesso sito.</span><span class="sxs-lookup"><span data-stu-id="2f05e-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="2f05e-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-107">Entry</span></span> | <span data-ttu-id="2f05e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2f05e-109">CN</span><span class="sxs-lookup"><span data-stu-id="2f05e-109">CN</span></span>                | <span data-ttu-id="2f05e-110">Topologia tra siti-rinnovo</span><span class="sxs-lookup"><span data-stu-id="2f05e-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="2f05e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2f05e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2f05e-112">interSiteTopologyRenew</span><span class="sxs-lookup"><span data-stu-id="2f05e-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="2f05e-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2f05e-113">Size</span></span>              | <span data-ttu-id="2f05e-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="2f05e-114">4 bytes</span></span>                              |
| <span data-ttu-id="2f05e-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2f05e-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2f05e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-117">Attribute-Id</span></span>      | <span data-ttu-id="2f05e-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="2f05e-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="2f05e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2f05e-119">System-Id-Guid</span></span>    | <span data-ttu-id="2f05e-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="2f05e-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="2f05e-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f05e-121">Syntax</span></span>            | [<span data-ttu-id="2f05e-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="2f05e-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2f05e-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2f05e-123">Implementations</span></span>

-   [<span data-ttu-id="2f05e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2f05e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2f05e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2f05e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2f05e-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2f05e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2f05e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2f05e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2f05e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2f05e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2f05e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2f05e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2f05e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2f05e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2f05e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f05e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2f05e-132">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-132">Entry</span></span> | <span data-ttu-id="2f05e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-136">System-Only</span></span>            | <span data-ttu-id="2f05e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-137">False</span></span>                                                       |
| <span data-ttu-id="2f05e-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-139">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-139">True</span></span>                                                        |
| <span data-ttu-id="2f05e-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-140">Is Indexed</span></span>             | <span data-ttu-id="2f05e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-141">False</span></span>                                                       |
| <span data-ttu-id="2f05e-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-142">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-143">False</span></span>                                                       |
| <span data-ttu-id="2f05e-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-148">Search-Flags</span></span>           | <span data-ttu-id="2f05e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-150">System-Flags</span></span>           | <span data-ttu-id="2f05e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-152">Classes used in</span></span>        | [<span data-ttu-id="2f05e-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2f05e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2f05e-154">Windows Server 2003</span></span>



| <span data-ttu-id="2f05e-155">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-155">Entry</span></span> | <span data-ttu-id="2f05e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-159">System-Only</span></span>            | <span data-ttu-id="2f05e-160">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-160">False</span></span>                                                       |
| <span data-ttu-id="2f05e-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-162">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-162">True</span></span>                                                        |
| <span data-ttu-id="2f05e-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-163">Is Indexed</span></span>             | <span data-ttu-id="2f05e-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-164">False</span></span>                                                       |
| <span data-ttu-id="2f05e-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-165">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-166">False</span></span>                                                       |
| <span data-ttu-id="2f05e-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-171">Search-Flags</span></span>           | <span data-ttu-id="2f05e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-173">System-Flags</span></span>           | <span data-ttu-id="2f05e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-175">Classes used in</span></span>        | [<span data-ttu-id="2f05e-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2f05e-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="2f05e-177">ADAM</span></span>



| <span data-ttu-id="2f05e-178">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-178">Entry</span></span> | <span data-ttu-id="2f05e-179">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-182">System-Only</span></span>            | <span data-ttu-id="2f05e-183">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-183">False</span></span>                                                       |
| <span data-ttu-id="2f05e-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-185">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-185">True</span></span>                                                        |
| <span data-ttu-id="2f05e-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-186">Is Indexed</span></span>             | <span data-ttu-id="2f05e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-187">False</span></span>                                                       |
| <span data-ttu-id="2f05e-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-188">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-189">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-189">False</span></span>                                                       |
| <span data-ttu-id="2f05e-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-194">Search-Flags</span></span>           | <span data-ttu-id="2f05e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-196">System-Flags</span></span>           | <span data-ttu-id="2f05e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-198">Classes used in</span></span>        | [<span data-ttu-id="2f05e-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2f05e-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2f05e-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2f05e-201">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-201">Entry</span></span> | <span data-ttu-id="2f05e-202">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-205">System-Only</span></span>            | <span data-ttu-id="2f05e-206">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-206">False</span></span>                                                       |
| <span data-ttu-id="2f05e-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-208">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-208">True</span></span>                                                        |
| <span data-ttu-id="2f05e-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-209">Is Indexed</span></span>             | <span data-ttu-id="2f05e-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-210">False</span></span>                                                       |
| <span data-ttu-id="2f05e-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-211">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-212">False</span></span>                                                       |
| <span data-ttu-id="2f05e-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-217">Search-Flags</span></span>           | <span data-ttu-id="2f05e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-219">System-Flags</span></span>           | <span data-ttu-id="2f05e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-221">Classes used in</span></span>        | [<span data-ttu-id="2f05e-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2f05e-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f05e-223">Windows Server 2008</span></span>



| <span data-ttu-id="2f05e-224">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-224">Entry</span></span> | <span data-ttu-id="2f05e-225">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-228">System-Only</span></span>            | <span data-ttu-id="2f05e-229">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-229">False</span></span>                                                       |
| <span data-ttu-id="2f05e-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-231">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-231">True</span></span>                                                        |
| <span data-ttu-id="2f05e-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-232">Is Indexed</span></span>             | <span data-ttu-id="2f05e-233">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-233">False</span></span>                                                       |
| <span data-ttu-id="2f05e-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-234">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-235">False</span></span>                                                       |
| <span data-ttu-id="2f05e-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-240">Search-Flags</span></span>           | <span data-ttu-id="2f05e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-242">System-Flags</span></span>           | <span data-ttu-id="2f05e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-244">Classes used in</span></span>        | [<span data-ttu-id="2f05e-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2f05e-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2f05e-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2f05e-247">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-247">Entry</span></span> | <span data-ttu-id="2f05e-248">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-251">System-Only</span></span>            | <span data-ttu-id="2f05e-252">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-252">False</span></span>                                                       |
| <span data-ttu-id="2f05e-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-254">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-254">True</span></span>                                                        |
| <span data-ttu-id="2f05e-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-255">Is Indexed</span></span>             | <span data-ttu-id="2f05e-256">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-256">False</span></span>                                                       |
| <span data-ttu-id="2f05e-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-257">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-258">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-258">False</span></span>                                                       |
| <span data-ttu-id="2f05e-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-263">Search-Flags</span></span>           | <span data-ttu-id="2f05e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-265">System-Flags</span></span>           | <span data-ttu-id="2f05e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-267">Classes used in</span></span>        | [<span data-ttu-id="2f05e-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2f05e-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f05e-269">Windows Server 2012</span></span>



| <span data-ttu-id="2f05e-270">Voce</span><span class="sxs-lookup"><span data-stu-id="2f05e-270">Entry</span></span> | <span data-ttu-id="2f05e-271">Valore</span><span class="sxs-lookup"><span data-stu-id="2f05e-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f05e-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2f05e-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2f05e-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="2f05e-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="2f05e-274">System-Only</span></span>            | <span data-ttu-id="2f05e-275">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-275">False</span></span>                                                       |
| <span data-ttu-id="2f05e-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2f05e-276">Is-Single-Valued</span></span>       | <span data-ttu-id="2f05e-277">Vero</span><span class="sxs-lookup"><span data-stu-id="2f05e-277">True</span></span>                                                        |
| <span data-ttu-id="2f05e-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2f05e-278">Is Indexed</span></span>             | <span data-ttu-id="2f05e-279">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-279">False</span></span>                                                       |
| <span data-ttu-id="2f05e-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2f05e-280">In Global Catalog</span></span>      | <span data-ttu-id="2f05e-281">Falso</span><span class="sxs-lookup"><span data-stu-id="2f05e-281">False</span></span>                                                       |
| <span data-ttu-id="2f05e-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2f05e-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="2f05e-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2f05e-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="2f05e-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2f05e-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2f05e-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="2f05e-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-286">Search-Flags</span></span>           | <span data-ttu-id="2f05e-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2f05e-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="2f05e-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2f05e-288">System-Flags</span></span>           | <span data-ttu-id="2f05e-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f05e-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="2f05e-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2f05e-290">Classes used in</span></span>        | [<span data-ttu-id="2f05e-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="2f05e-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





