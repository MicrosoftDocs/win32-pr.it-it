---
title: Attributo Repl-Interval
description: Attributo di Site-Link oggetti che definiscono l'intervallo, in minuti, tra i cicli di replica tra i siti nell'elenco di siti.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Schema AD Repl-Interval attribute
- Schema AD dell'attributo replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122378"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="4bec3-105">Attributo Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="4bec3-105">Repl-Interval attribute</span></span>

<span data-ttu-id="4bec3-106">Attributo di Site-Link oggetti che definiscono l'intervallo, in minuti, tra i cicli di replica tra i siti nell'elenco di siti.</span><span class="sxs-lookup"><span data-stu-id="4bec3-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="4bec3-107">Deve essere un multiplo di 15 minuti (la granularità della replica DS tra siti), un minimo di 15 minuti e un massimo di 10.080 minuti (una settimana).</span><span class="sxs-lookup"><span data-stu-id="4bec3-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="4bec3-108">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-108">Entry</span></span> | <span data-ttu-id="4bec3-109">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="4bec3-110">CN</span><span class="sxs-lookup"><span data-stu-id="4bec3-110">CN</span></span>                | <span data-ttu-id="4bec3-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="4bec3-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="4bec3-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4bec3-112">Ldap-Display-Name</span></span> | <span data-ttu-id="4bec3-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="4bec3-113">replInterval</span></span>                                   |
| <span data-ttu-id="4bec3-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4bec3-114">Size</span></span>              | <span data-ttu-id="4bec3-115">4 byte</span><span class="sxs-lookup"><span data-stu-id="4bec3-115">4 bytes</span></span>                                        |
| <span data-ttu-id="4bec3-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-116">Update Privilege</span></span>  | <span data-ttu-id="4bec3-117">Amministratore dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="4bec3-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="4bec3-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-118">Update Frequency</span></span>  | <span data-ttu-id="4bec3-119">Quando l'intervallo di replica deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="4bec3-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="4bec3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-120">Attribute-Id</span></span>      | <span data-ttu-id="4bec3-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="4bec3-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="4bec3-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4bec3-122">System-Id-Guid</span></span>    | <span data-ttu-id="4bec3-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="4bec3-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="4bec3-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bec3-124">Syntax</span></span>            | [<span data-ttu-id="4bec3-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="4bec3-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="4bec3-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4bec3-126">Implementations</span></span>

-   [<span data-ttu-id="4bec3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4bec3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4bec3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4bec3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4bec3-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4bec3-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4bec3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4bec3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4bec3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4bec3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4bec3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4bec3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4bec3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4bec3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4bec3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4bec3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4bec3-135">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-135">Entry</span></span> | <span data-ttu-id="4bec3-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-139">System-Only</span></span>            | <span data-ttu-id="4bec3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-140">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-142">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-142">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-143">Is Indexed</span></span>             | <span data-ttu-id="4bec3-144">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-144">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-145">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-146">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-146">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-151">Search-Flags</span></span>           | <span data-ttu-id="4bec3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-153">System-Flags</span></span>           | <span data-ttu-id="4bec3-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-155">Classes used in</span></span>        | [<span data-ttu-id="4bec3-156">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-157">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4bec3-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4bec3-158">Windows Server 2003</span></span>



| <span data-ttu-id="4bec3-159">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-159">Entry</span></span> | <span data-ttu-id="4bec3-160">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-163">System-Only</span></span>            | <span data-ttu-id="4bec3-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-164">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-166">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-166">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-167">Is Indexed</span></span>             | <span data-ttu-id="4bec3-168">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-168">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-169">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-170">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-170">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-175">Search-Flags</span></span>           | <span data-ttu-id="4bec3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-177">System-Flags</span></span>           | <span data-ttu-id="4bec3-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-179">Classes used in</span></span>        | [<span data-ttu-id="4bec3-180">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-181">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4bec3-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="4bec3-182">ADAM</span></span>



| <span data-ttu-id="4bec3-183">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-183">Entry</span></span> | <span data-ttu-id="4bec3-184">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-187">System-Only</span></span>            | <span data-ttu-id="4bec3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-188">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-190">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-190">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-191">Is Indexed</span></span>             | <span data-ttu-id="4bec3-192">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-192">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-193">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-194">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-194">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-199">Search-Flags</span></span>           | <span data-ttu-id="4bec3-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-201">System-Flags</span></span>           | <span data-ttu-id="4bec3-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-203">Classes used in</span></span>        | [<span data-ttu-id="4bec3-204">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-205">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4bec3-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4bec3-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4bec3-207">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-207">Entry</span></span> | <span data-ttu-id="4bec3-208">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-211">System-Only</span></span>            | <span data-ttu-id="4bec3-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-212">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-213">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-214">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-214">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-215">Is Indexed</span></span>             | <span data-ttu-id="4bec3-216">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-216">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-217">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-218">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-218">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-223">Search-Flags</span></span>           | <span data-ttu-id="4bec3-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-225">System-Flags</span></span>           | <span data-ttu-id="4bec3-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-227">Classes used in</span></span>        | [<span data-ttu-id="4bec3-228">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-229">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4bec3-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bec3-230">Windows Server 2008</span></span>



| <span data-ttu-id="4bec3-231">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-231">Entry</span></span> | <span data-ttu-id="4bec3-232">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-235">System-Only</span></span>            | <span data-ttu-id="4bec3-236">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-236">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-237">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-238">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-238">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-239">Is Indexed</span></span>             | <span data-ttu-id="4bec3-240">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-240">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-241">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-242">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-242">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-247">Search-Flags</span></span>           | <span data-ttu-id="4bec3-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-249">System-Flags</span></span>           | <span data-ttu-id="4bec3-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-251">Classes used in</span></span>        | [<span data-ttu-id="4bec3-252">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-253">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4bec3-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4bec3-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4bec3-255">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-255">Entry</span></span> | <span data-ttu-id="4bec3-256">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-257">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-259">System-Only</span></span>            | <span data-ttu-id="4bec3-260">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-260">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-261">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-262">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-262">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-263">Is Indexed</span></span>             | <span data-ttu-id="4bec3-264">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-264">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-265">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-266">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-266">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-271">Search-Flags</span></span>           | <span data-ttu-id="4bec3-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-273">System-Flags</span></span>           | <span data-ttu-id="4bec3-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-275">Classes used in</span></span>        | [<span data-ttu-id="4bec3-276">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-277">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4bec3-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bec3-278">Windows Server 2012</span></span>



| <span data-ttu-id="4bec3-279">Voce</span><span class="sxs-lookup"><span data-stu-id="4bec3-279">Entry</span></span> | <span data-ttu-id="4bec3-280">Valore</span><span class="sxs-lookup"><span data-stu-id="4bec3-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bec3-281">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4bec3-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4bec3-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="4bec3-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="4bec3-283">System-Only</span></span>            | <span data-ttu-id="4bec3-284">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-284">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4bec3-285">Is-Single-Valued</span></span>       | <span data-ttu-id="4bec3-286">Vero</span><span class="sxs-lookup"><span data-stu-id="4bec3-286">True</span></span>                                                                                                       |
| <span data-ttu-id="4bec3-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4bec3-287">Is Indexed</span></span>             | <span data-ttu-id="4bec3-288">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-288">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4bec3-289">In Global Catalog</span></span>      | <span data-ttu-id="4bec3-290">Falso</span><span class="sxs-lookup"><span data-stu-id="4bec3-290">False</span></span>                                                                                                      |
| <span data-ttu-id="4bec3-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4bec3-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="4bec3-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4bec3-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="4bec3-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4bec3-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4bec3-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="4bec3-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-295">Search-Flags</span></span>           | <span data-ttu-id="4bec3-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4bec3-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4bec3-297">System-Flags</span></span>           | <span data-ttu-id="4bec3-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4bec3-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="4bec3-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4bec3-299">Classes used in</span></span>        | [<span data-ttu-id="4bec3-300">**Trasporto tra siti**</span><span class="sxs-lookup"><span data-stu-id="4bec3-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="4bec3-301">**Sito-collegamento**</span><span class="sxs-lookup"><span data-stu-id="4bec3-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





