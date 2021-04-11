---
title: Attributo ACS-max-token-bucket-per-Flow
description: L'attributo ACS-max-token-bucket-per-Flow è solo per uso interno.
ms.assetid: 2c269bda-7b0d-4ef4-8c67-9f5e7c52e3ae
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ACS-max-token-bucket per flusso
- Schema AD dell'attributo aCSMaxTokenBucketPerFlow
topic_type:
- apiref
api_name:
- ACS-Max-Token-Bucket-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb323af82b270c20478e8af4aafc3ee4142125ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123216"
---
# <a name="acs-max-token-bucket-per-flow-attribute"></a><span data-ttu-id="6307f-105">Attributo ACS-max-token-bucket-per-Flow</span><span class="sxs-lookup"><span data-stu-id="6307f-105">ACS-Max-Token-Bucket-Per-Flow attribute</span></span>

<span data-ttu-id="6307f-106">L'attributo **ACS-max-token-bucket-per-Flow** è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="6307f-106">The **ACS-Max-Token-Bucket-Per-Flow** attribute is for internal use only.</span></span> <span data-ttu-id="6307f-107">Basato su RFC2210.</span><span class="sxs-lookup"><span data-stu-id="6307f-107">Based on RFC2210.</span></span>



| <span data-ttu-id="6307f-108">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-108">Entry</span></span> | <span data-ttu-id="6307f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6307f-110">CN</span><span class="sxs-lookup"><span data-stu-id="6307f-110">CN</span></span>                | <span data-ttu-id="6307f-111">ACS-max-token-bucket per flusso</span><span class="sxs-lookup"><span data-stu-id="6307f-111">ACS-Max-Token-Bucket-Per-Flow</span></span>        |
| <span data-ttu-id="6307f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6307f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6307f-113">aCSMaxTokenBucketPerFlow</span><span class="sxs-lookup"><span data-stu-id="6307f-113">aCSMaxTokenBucketPerFlow</span></span>             |
| <span data-ttu-id="6307f-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6307f-114">Size</span></span>              | <span data-ttu-id="6307f-115">8 byte</span><span class="sxs-lookup"><span data-stu-id="6307f-115">8 bytes</span></span>                              |
| <span data-ttu-id="6307f-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6307f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6307f-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6307f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6307f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-118">Attribute-Id</span></span>      | <span data-ttu-id="6307f-119">1.2.840.113556.1.4.1313</span><span class="sxs-lookup"><span data-stu-id="6307f-119">1.2.840.113556.1.4.1313</span></span>              |
| <span data-ttu-id="6307f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6307f-120">System-Id-Guid</span></span>    | <span data-ttu-id="6307f-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="6307f-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="6307f-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6307f-122">Syntax</span></span>            | [<span data-ttu-id="6307f-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6307f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6307f-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6307f-124">Implementations</span></span>

-   [<span data-ttu-id="6307f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6307f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6307f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6307f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6307f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6307f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6307f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6307f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6307f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6307f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6307f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6307f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6307f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6307f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6307f-132">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-132">Entry</span></span> | <span data-ttu-id="6307f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6307f-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6307f-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6307f-136">System-Only</span></span>            | <span data-ttu-id="6307f-137">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-137">False</span></span>                                        |
| <span data-ttu-id="6307f-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6307f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6307f-139">Vero</span><span class="sxs-lookup"><span data-stu-id="6307f-139">True</span></span>                                         |
| <span data-ttu-id="6307f-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6307f-140">Is Indexed</span></span>             | <span data-ttu-id="6307f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-141">False</span></span>                                        |
| <span data-ttu-id="6307f-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6307f-142">In Global Catalog</span></span>      | <span data-ttu-id="6307f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-143">False</span></span>                                        |
| <span data-ttu-id="6307f-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6307f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6307f-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6307f-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6307f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6307f-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6307f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6307f-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6307f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-148">Search-Flags</span></span>           | <span data-ttu-id="6307f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6307f-149">0x00000000</span></span>                                   |
| <span data-ttu-id="6307f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-150">System-Flags</span></span>           | <span data-ttu-id="6307f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6307f-151">0x00000010</span></span>                                   |
| <span data-ttu-id="6307f-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6307f-152">Classes used in</span></span>        | [<span data-ttu-id="6307f-153">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="6307f-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6307f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6307f-154">Windows Server 2003</span></span>



| <span data-ttu-id="6307f-155">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-155">Entry</span></span> | <span data-ttu-id="6307f-156">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6307f-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6307f-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6307f-159">System-Only</span></span>            | <span data-ttu-id="6307f-160">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-160">False</span></span>                                        |
| <span data-ttu-id="6307f-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6307f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6307f-162">Vero</span><span class="sxs-lookup"><span data-stu-id="6307f-162">True</span></span>                                         |
| <span data-ttu-id="6307f-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6307f-163">Is Indexed</span></span>             | <span data-ttu-id="6307f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-164">False</span></span>                                        |
| <span data-ttu-id="6307f-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6307f-165">In Global Catalog</span></span>      | <span data-ttu-id="6307f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-166">False</span></span>                                        |
| <span data-ttu-id="6307f-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6307f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6307f-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6307f-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6307f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6307f-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6307f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6307f-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6307f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-171">Search-Flags</span></span>           | <span data-ttu-id="6307f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6307f-172">0x00000000</span></span>                                   |
| <span data-ttu-id="6307f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-173">System-Flags</span></span>           | <span data-ttu-id="6307f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6307f-174">0x00000010</span></span>                                   |
| <span data-ttu-id="6307f-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6307f-175">Classes used in</span></span>        | [<span data-ttu-id="6307f-176">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="6307f-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6307f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6307f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6307f-178">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-178">Entry</span></span> | <span data-ttu-id="6307f-179">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6307f-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6307f-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6307f-182">System-Only</span></span>            | <span data-ttu-id="6307f-183">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-183">False</span></span>                                        |
| <span data-ttu-id="6307f-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6307f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6307f-185">Vero</span><span class="sxs-lookup"><span data-stu-id="6307f-185">True</span></span>                                         |
| <span data-ttu-id="6307f-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6307f-186">Is Indexed</span></span>             | <span data-ttu-id="6307f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-187">False</span></span>                                        |
| <span data-ttu-id="6307f-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6307f-188">In Global Catalog</span></span>      | <span data-ttu-id="6307f-189">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-189">False</span></span>                                        |
| <span data-ttu-id="6307f-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6307f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6307f-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6307f-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6307f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6307f-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6307f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6307f-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6307f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-194">Search-Flags</span></span>           | <span data-ttu-id="6307f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6307f-195">0x00000000</span></span>                                   |
| <span data-ttu-id="6307f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-196">System-Flags</span></span>           | <span data-ttu-id="6307f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6307f-197">0x00000010</span></span>                                   |
| <span data-ttu-id="6307f-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6307f-198">Classes used in</span></span>        | [<span data-ttu-id="6307f-199">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="6307f-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6307f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6307f-200">Windows Server 2008</span></span>



| <span data-ttu-id="6307f-201">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-201">Entry</span></span> | <span data-ttu-id="6307f-202">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6307f-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6307f-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6307f-205">System-Only</span></span>            | <span data-ttu-id="6307f-206">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-206">False</span></span>                                        |
| <span data-ttu-id="6307f-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6307f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6307f-208">Vero</span><span class="sxs-lookup"><span data-stu-id="6307f-208">True</span></span>                                         |
| <span data-ttu-id="6307f-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6307f-209">Is Indexed</span></span>             | <span data-ttu-id="6307f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-210">False</span></span>                                        |
| <span data-ttu-id="6307f-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6307f-211">In Global Catalog</span></span>      | <span data-ttu-id="6307f-212">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-212">False</span></span>                                        |
| <span data-ttu-id="6307f-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6307f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6307f-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6307f-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6307f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6307f-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6307f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6307f-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6307f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-217">Search-Flags</span></span>           | <span data-ttu-id="6307f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6307f-218">0x00000000</span></span>                                   |
| <span data-ttu-id="6307f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-219">System-Flags</span></span>           | <span data-ttu-id="6307f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6307f-220">0x00000010</span></span>                                   |
| <span data-ttu-id="6307f-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6307f-221">Classes used in</span></span>        | [<span data-ttu-id="6307f-222">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="6307f-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6307f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6307f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6307f-224">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-224">Entry</span></span> | <span data-ttu-id="6307f-225">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6307f-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6307f-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6307f-228">System-Only</span></span>            | <span data-ttu-id="6307f-229">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-229">False</span></span>                                        |
| <span data-ttu-id="6307f-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6307f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6307f-231">Vero</span><span class="sxs-lookup"><span data-stu-id="6307f-231">True</span></span>                                         |
| <span data-ttu-id="6307f-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6307f-232">Is Indexed</span></span>             | <span data-ttu-id="6307f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-233">False</span></span>                                        |
| <span data-ttu-id="6307f-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6307f-234">In Global Catalog</span></span>      | <span data-ttu-id="6307f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-235">False</span></span>                                        |
| <span data-ttu-id="6307f-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6307f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6307f-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6307f-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6307f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6307f-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6307f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6307f-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6307f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-240">Search-Flags</span></span>           | <span data-ttu-id="6307f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6307f-241">0x00000000</span></span>                                   |
| <span data-ttu-id="6307f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-242">System-Flags</span></span>           | <span data-ttu-id="6307f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6307f-243">0x00000010</span></span>                                   |
| <span data-ttu-id="6307f-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6307f-244">Classes used in</span></span>        | [<span data-ttu-id="6307f-245">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="6307f-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6307f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6307f-246">Windows Server 2012</span></span>



| <span data-ttu-id="6307f-247">Voce</span><span class="sxs-lookup"><span data-stu-id="6307f-247">Entry</span></span> | <span data-ttu-id="6307f-248">Valore</span><span class="sxs-lookup"><span data-stu-id="6307f-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6307f-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6307f-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6307f-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6307f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6307f-251">System-Only</span></span>            | <span data-ttu-id="6307f-252">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-252">False</span></span>                                        |
| <span data-ttu-id="6307f-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6307f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6307f-254">Vero</span><span class="sxs-lookup"><span data-stu-id="6307f-254">True</span></span>                                         |
| <span data-ttu-id="6307f-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6307f-255">Is Indexed</span></span>             | <span data-ttu-id="6307f-256">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-256">False</span></span>                                        |
| <span data-ttu-id="6307f-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6307f-257">In Global Catalog</span></span>      | <span data-ttu-id="6307f-258">Falso</span><span class="sxs-lookup"><span data-stu-id="6307f-258">False</span></span>                                        |
| <span data-ttu-id="6307f-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6307f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6307f-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6307f-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6307f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6307f-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6307f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6307f-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6307f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-263">Search-Flags</span></span>           | <span data-ttu-id="6307f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6307f-264">0x00000000</span></span>                                   |
| <span data-ttu-id="6307f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6307f-265">System-Flags</span></span>           | <span data-ttu-id="6307f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6307f-266">0x00000010</span></span>                                   |
| <span data-ttu-id="6307f-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6307f-267">Classes used in</span></span>        | [<span data-ttu-id="6307f-268">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="6307f-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





