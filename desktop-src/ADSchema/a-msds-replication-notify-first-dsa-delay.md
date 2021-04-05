---
title: attributo ms-DS-Replication-Notify-First-DSA-Delay
description: Questo attributo controlla il ritardo nel tempo tra le modifiche al servizio DS e la notifica del primo partner di replica per un NC.
ms.assetid: 58474bf9-9069-402a-a94b-4d1b6df0810e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Replication-Notify-First-DSA-Delay
- Schema AD dell'attributo msDS-Replication-Notify-First-DSA-Delay
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-First-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a981ff257562e701b12e3855b279b7995721e39
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875361"
---
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="72dfb-105">attributo ms-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="72dfb-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="72dfb-106">Questo attributo controlla il ritardo nel tempo tra le modifiche al servizio DS e la notifica del primo partner di replica per un NC.</span><span class="sxs-lookup"><span data-stu-id="72dfb-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="72dfb-107">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-107">Entry</span></span> | <span data-ttu-id="72dfb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="72dfb-109">CN</span><span class="sxs-lookup"><span data-stu-id="72dfb-109">CN</span></span>                | <span data-ttu-id="72dfb-110">ms-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="72dfb-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="72dfb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72dfb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="72dfb-112">msDS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="72dfb-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="72dfb-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="72dfb-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="72dfb-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-114">Update Privilege</span></span>  | <span data-ttu-id="72dfb-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="72dfb-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="72dfb-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="72dfb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-117">Attribute-Id</span></span>      | <span data-ttu-id="72dfb-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="72dfb-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="72dfb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72dfb-119">System-Id-Guid</span></span>    | <span data-ttu-id="72dfb-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="72dfb-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="72dfb-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72dfb-121">Syntax</span></span>            | [<span data-ttu-id="72dfb-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="72dfb-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="72dfb-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="72dfb-123">Implementations</span></span>

-   [<span data-ttu-id="72dfb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72dfb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72dfb-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="72dfb-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="72dfb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72dfb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72dfb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72dfb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72dfb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72dfb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72dfb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72dfb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="72dfb-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72dfb-130">Windows Server 2003</span></span>



| <span data-ttu-id="72dfb-131">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-131">Entry</span></span> | <span data-ttu-id="72dfb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="72dfb-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="72dfb-135">System-Only</span></span>            | <span data-ttu-id="72dfb-136">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-136">False</span></span>                                      |
| <span data-ttu-id="72dfb-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72dfb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="72dfb-138">Vero</span><span class="sxs-lookup"><span data-stu-id="72dfb-138">True</span></span>                                       |
| <span data-ttu-id="72dfb-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72dfb-139">Is Indexed</span></span>             | <span data-ttu-id="72dfb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-140">False</span></span>                                      |
| <span data-ttu-id="72dfb-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72dfb-141">In Global Catalog</span></span>      | <span data-ttu-id="72dfb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-142">False</span></span>                                      |
| <span data-ttu-id="72dfb-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72dfb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="72dfb-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72dfb-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="72dfb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72dfb-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72dfb-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-147">Search-Flags</span></span>           | <span data-ttu-id="72dfb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72dfb-148">0x00000000</span></span>                                 |
| <span data-ttu-id="72dfb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-149">System-Flags</span></span>           | <span data-ttu-id="72dfb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72dfb-150">0x00000010</span></span>                                 |
| <span data-ttu-id="72dfb-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72dfb-151">Classes used in</span></span>        | [<span data-ttu-id="72dfb-152">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="72dfb-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="72dfb-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="72dfb-153">ADAM</span></span>



| <span data-ttu-id="72dfb-154">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-154">Entry</span></span> | <span data-ttu-id="72dfb-155">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="72dfb-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="72dfb-158">System-Only</span></span>            | <span data-ttu-id="72dfb-159">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-159">False</span></span>                                      |
| <span data-ttu-id="72dfb-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72dfb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="72dfb-161">Vero</span><span class="sxs-lookup"><span data-stu-id="72dfb-161">True</span></span>                                       |
| <span data-ttu-id="72dfb-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72dfb-162">Is Indexed</span></span>             | <span data-ttu-id="72dfb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-163">False</span></span>                                      |
| <span data-ttu-id="72dfb-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72dfb-164">In Global Catalog</span></span>      | <span data-ttu-id="72dfb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-165">False</span></span>                                      |
| <span data-ttu-id="72dfb-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72dfb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="72dfb-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72dfb-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="72dfb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72dfb-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72dfb-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-170">Search-Flags</span></span>           | <span data-ttu-id="72dfb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72dfb-171">0x00000000</span></span>                                 |
| <span data-ttu-id="72dfb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-172">System-Flags</span></span>           | <span data-ttu-id="72dfb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72dfb-173">0x00000010</span></span>                                 |
| <span data-ttu-id="72dfb-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72dfb-174">Classes used in</span></span>        | [<span data-ttu-id="72dfb-175">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="72dfb-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72dfb-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72dfb-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72dfb-177">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-177">Entry</span></span> | <span data-ttu-id="72dfb-178">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="72dfb-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="72dfb-181">System-Only</span></span>            | <span data-ttu-id="72dfb-182">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-182">False</span></span>                                      |
| <span data-ttu-id="72dfb-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72dfb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="72dfb-184">Vero</span><span class="sxs-lookup"><span data-stu-id="72dfb-184">True</span></span>                                       |
| <span data-ttu-id="72dfb-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72dfb-185">Is Indexed</span></span>             | <span data-ttu-id="72dfb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-186">False</span></span>                                      |
| <span data-ttu-id="72dfb-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72dfb-187">In Global Catalog</span></span>      | <span data-ttu-id="72dfb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-188">False</span></span>                                      |
| <span data-ttu-id="72dfb-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72dfb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="72dfb-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72dfb-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="72dfb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72dfb-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72dfb-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-193">Search-Flags</span></span>           | <span data-ttu-id="72dfb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72dfb-194">0x00000000</span></span>                                 |
| <span data-ttu-id="72dfb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-195">System-Flags</span></span>           | <span data-ttu-id="72dfb-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72dfb-196">0x00000010</span></span>                                 |
| <span data-ttu-id="72dfb-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72dfb-197">Classes used in</span></span>        | [<span data-ttu-id="72dfb-198">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="72dfb-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72dfb-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72dfb-199">Windows Server 2008</span></span>



| <span data-ttu-id="72dfb-200">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-200">Entry</span></span> | <span data-ttu-id="72dfb-201">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="72dfb-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="72dfb-204">System-Only</span></span>            | <span data-ttu-id="72dfb-205">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-205">False</span></span>                                      |
| <span data-ttu-id="72dfb-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72dfb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="72dfb-207">Vero</span><span class="sxs-lookup"><span data-stu-id="72dfb-207">True</span></span>                                       |
| <span data-ttu-id="72dfb-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72dfb-208">Is Indexed</span></span>             | <span data-ttu-id="72dfb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-209">False</span></span>                                      |
| <span data-ttu-id="72dfb-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72dfb-210">In Global Catalog</span></span>      | <span data-ttu-id="72dfb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-211">False</span></span>                                      |
| <span data-ttu-id="72dfb-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72dfb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="72dfb-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72dfb-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="72dfb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72dfb-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72dfb-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-216">Search-Flags</span></span>           | <span data-ttu-id="72dfb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72dfb-217">0x00000000</span></span>                                 |
| <span data-ttu-id="72dfb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-218">System-Flags</span></span>           | <span data-ttu-id="72dfb-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72dfb-219">0x00000010</span></span>                                 |
| <span data-ttu-id="72dfb-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72dfb-220">Classes used in</span></span>        | [<span data-ttu-id="72dfb-221">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="72dfb-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72dfb-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72dfb-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72dfb-223">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-223">Entry</span></span> | <span data-ttu-id="72dfb-224">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="72dfb-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="72dfb-227">System-Only</span></span>            | <span data-ttu-id="72dfb-228">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-228">False</span></span>                                      |
| <span data-ttu-id="72dfb-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72dfb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="72dfb-230">Vero</span><span class="sxs-lookup"><span data-stu-id="72dfb-230">True</span></span>                                       |
| <span data-ttu-id="72dfb-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72dfb-231">Is Indexed</span></span>             | <span data-ttu-id="72dfb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-232">False</span></span>                                      |
| <span data-ttu-id="72dfb-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72dfb-233">In Global Catalog</span></span>      | <span data-ttu-id="72dfb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-234">False</span></span>                                      |
| <span data-ttu-id="72dfb-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72dfb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="72dfb-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72dfb-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="72dfb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72dfb-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72dfb-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-239">Search-Flags</span></span>           | <span data-ttu-id="72dfb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72dfb-240">0x00000000</span></span>                                 |
| <span data-ttu-id="72dfb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-241">System-Flags</span></span>           | <span data-ttu-id="72dfb-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72dfb-242">0x00000010</span></span>                                 |
| <span data-ttu-id="72dfb-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72dfb-243">Classes used in</span></span>        | [<span data-ttu-id="72dfb-244">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="72dfb-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72dfb-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72dfb-245">Windows Server 2012</span></span>



| <span data-ttu-id="72dfb-246">Voce</span><span class="sxs-lookup"><span data-stu-id="72dfb-246">Entry</span></span> | <span data-ttu-id="72dfb-247">Valore</span><span class="sxs-lookup"><span data-stu-id="72dfb-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="72dfb-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="72dfb-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72dfb-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="72dfb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="72dfb-250">System-Only</span></span>            | <span data-ttu-id="72dfb-251">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-251">False</span></span>                                      |
| <span data-ttu-id="72dfb-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="72dfb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="72dfb-253">Vero</span><span class="sxs-lookup"><span data-stu-id="72dfb-253">True</span></span>                                       |
| <span data-ttu-id="72dfb-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="72dfb-254">Is Indexed</span></span>             | <span data-ttu-id="72dfb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-255">False</span></span>                                      |
| <span data-ttu-id="72dfb-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="72dfb-256">In Global Catalog</span></span>      | <span data-ttu-id="72dfb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="72dfb-257">False</span></span>                                      |
| <span data-ttu-id="72dfb-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="72dfb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="72dfb-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="72dfb-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="72dfb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72dfb-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72dfb-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="72dfb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-262">Search-Flags</span></span>           | <span data-ttu-id="72dfb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72dfb-263">0x00000000</span></span>                                 |
| <span data-ttu-id="72dfb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72dfb-264">System-Flags</span></span>           | <span data-ttu-id="72dfb-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72dfb-265">0x00000010</span></span>                                 |
| <span data-ttu-id="72dfb-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="72dfb-266">Classes used in</span></span>        | [<span data-ttu-id="72dfb-267">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="72dfb-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





