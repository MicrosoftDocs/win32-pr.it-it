---
title: ACS-attributo dimensioni minime-criteri
description: L'attributo ACS-Minimum-Size è solo per uso interno.
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di dimensioni minime del servizio ACS
- Schema AD dell'attributo aCSMinimumPolicedSize
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303630"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="c8037-105">ACS-attributo dimensioni minime-criteri</span><span class="sxs-lookup"><span data-stu-id="c8037-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="c8037-106">L'attributo **ACS-Minimum-Size** è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="c8037-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="c8037-107">Basato su RFC2210.</span><span class="sxs-lookup"><span data-stu-id="c8037-107">Based on RFC2210.</span></span>



| <span data-ttu-id="c8037-108">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-108">Entry</span></span> | <span data-ttu-id="c8037-109">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c8037-110">CN</span><span class="sxs-lookup"><span data-stu-id="c8037-110">CN</span></span>                | <span data-ttu-id="c8037-111">ACS-dimensioni minime di polizia</span><span class="sxs-lookup"><span data-stu-id="c8037-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="c8037-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c8037-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c8037-113">aCSMinimumPolicedSize</span><span class="sxs-lookup"><span data-stu-id="c8037-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="c8037-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c8037-114">Size</span></span>              | <span data-ttu-id="c8037-115">8 byte</span><span class="sxs-lookup"><span data-stu-id="c8037-115">8 bytes</span></span>                              |
| <span data-ttu-id="c8037-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c8037-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c8037-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c8037-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c8037-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-118">Attribute-Id</span></span>      | <span data-ttu-id="c8037-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="c8037-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="c8037-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c8037-120">System-Id-Guid</span></span>    | <span data-ttu-id="c8037-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="c8037-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="c8037-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8037-122">Syntax</span></span>            | [<span data-ttu-id="c8037-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c8037-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c8037-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c8037-124">Implementations</span></span>

-   [<span data-ttu-id="c8037-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c8037-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c8037-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c8037-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c8037-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c8037-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c8037-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c8037-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c8037-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c8037-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c8037-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c8037-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c8037-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8037-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c8037-132">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-132">Entry</span></span> | <span data-ttu-id="c8037-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8037-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c8037-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8037-136">System-Only</span></span>            | <span data-ttu-id="c8037-137">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-137">False</span></span>                                        |
| <span data-ttu-id="c8037-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c8037-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c8037-139">Vero</span><span class="sxs-lookup"><span data-stu-id="c8037-139">True</span></span>                                         |
| <span data-ttu-id="c8037-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c8037-140">Is Indexed</span></span>             | <span data-ttu-id="c8037-141">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-141">False</span></span>                                        |
| <span data-ttu-id="c8037-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c8037-142">In Global Catalog</span></span>      | <span data-ttu-id="c8037-143">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-143">False</span></span>                                        |
| <span data-ttu-id="c8037-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c8037-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8037-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c8037-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8037-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8037-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8037-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8037-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8037-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-148">Search-Flags</span></span>           | <span data-ttu-id="c8037-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8037-149">0x00000000</span></span>                                   |
| <span data-ttu-id="c8037-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-150">System-Flags</span></span>           | <span data-ttu-id="c8037-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8037-151">0x00000010</span></span>                                   |
| <span data-ttu-id="c8037-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c8037-152">Classes used in</span></span>        | [<span data-ttu-id="c8037-153">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c8037-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c8037-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8037-154">Windows Server 2003</span></span>



| <span data-ttu-id="c8037-155">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-155">Entry</span></span> | <span data-ttu-id="c8037-156">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8037-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c8037-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8037-159">System-Only</span></span>            | <span data-ttu-id="c8037-160">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-160">False</span></span>                                        |
| <span data-ttu-id="c8037-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c8037-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c8037-162">Vero</span><span class="sxs-lookup"><span data-stu-id="c8037-162">True</span></span>                                         |
| <span data-ttu-id="c8037-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c8037-163">Is Indexed</span></span>             | <span data-ttu-id="c8037-164">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-164">False</span></span>                                        |
| <span data-ttu-id="c8037-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c8037-165">In Global Catalog</span></span>      | <span data-ttu-id="c8037-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-166">False</span></span>                                        |
| <span data-ttu-id="c8037-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c8037-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8037-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c8037-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8037-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8037-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8037-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8037-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8037-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-171">Search-Flags</span></span>           | <span data-ttu-id="c8037-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8037-172">0x00000000</span></span>                                   |
| <span data-ttu-id="c8037-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-173">System-Flags</span></span>           | <span data-ttu-id="c8037-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8037-174">0x00000010</span></span>                                   |
| <span data-ttu-id="c8037-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c8037-175">Classes used in</span></span>        | [<span data-ttu-id="c8037-176">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c8037-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c8037-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c8037-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c8037-178">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-178">Entry</span></span> | <span data-ttu-id="c8037-179">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8037-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c8037-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8037-182">System-Only</span></span>            | <span data-ttu-id="c8037-183">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-183">False</span></span>                                        |
| <span data-ttu-id="c8037-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c8037-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c8037-185">Vero</span><span class="sxs-lookup"><span data-stu-id="c8037-185">True</span></span>                                         |
| <span data-ttu-id="c8037-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c8037-186">Is Indexed</span></span>             | <span data-ttu-id="c8037-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-187">False</span></span>                                        |
| <span data-ttu-id="c8037-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c8037-188">In Global Catalog</span></span>      | <span data-ttu-id="c8037-189">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-189">False</span></span>                                        |
| <span data-ttu-id="c8037-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c8037-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8037-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c8037-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8037-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8037-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8037-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8037-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8037-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-194">Search-Flags</span></span>           | <span data-ttu-id="c8037-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8037-195">0x00000000</span></span>                                   |
| <span data-ttu-id="c8037-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-196">System-Flags</span></span>           | <span data-ttu-id="c8037-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8037-197">0x00000010</span></span>                                   |
| <span data-ttu-id="c8037-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c8037-198">Classes used in</span></span>        | [<span data-ttu-id="c8037-199">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c8037-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c8037-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8037-200">Windows Server 2008</span></span>



| <span data-ttu-id="c8037-201">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-201">Entry</span></span> | <span data-ttu-id="c8037-202">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8037-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c8037-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8037-205">System-Only</span></span>            | <span data-ttu-id="c8037-206">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-206">False</span></span>                                        |
| <span data-ttu-id="c8037-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c8037-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c8037-208">Vero</span><span class="sxs-lookup"><span data-stu-id="c8037-208">True</span></span>                                         |
| <span data-ttu-id="c8037-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c8037-209">Is Indexed</span></span>             | <span data-ttu-id="c8037-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-210">False</span></span>                                        |
| <span data-ttu-id="c8037-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c8037-211">In Global Catalog</span></span>      | <span data-ttu-id="c8037-212">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-212">False</span></span>                                        |
| <span data-ttu-id="c8037-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c8037-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8037-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c8037-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8037-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8037-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8037-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8037-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8037-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-217">Search-Flags</span></span>           | <span data-ttu-id="c8037-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8037-218">0x00000000</span></span>                                   |
| <span data-ttu-id="c8037-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-219">System-Flags</span></span>           | <span data-ttu-id="c8037-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8037-220">0x00000010</span></span>                                   |
| <span data-ttu-id="c8037-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c8037-221">Classes used in</span></span>        | [<span data-ttu-id="c8037-222">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c8037-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c8037-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8037-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c8037-224">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-224">Entry</span></span> | <span data-ttu-id="c8037-225">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8037-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c8037-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8037-228">System-Only</span></span>            | <span data-ttu-id="c8037-229">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-229">False</span></span>                                        |
| <span data-ttu-id="c8037-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c8037-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c8037-231">Vero</span><span class="sxs-lookup"><span data-stu-id="c8037-231">True</span></span>                                         |
| <span data-ttu-id="c8037-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c8037-232">Is Indexed</span></span>             | <span data-ttu-id="c8037-233">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-233">False</span></span>                                        |
| <span data-ttu-id="c8037-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c8037-234">In Global Catalog</span></span>      | <span data-ttu-id="c8037-235">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-235">False</span></span>                                        |
| <span data-ttu-id="c8037-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c8037-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8037-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c8037-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8037-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8037-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8037-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8037-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8037-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-240">Search-Flags</span></span>           | <span data-ttu-id="c8037-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8037-241">0x00000000</span></span>                                   |
| <span data-ttu-id="c8037-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-242">System-Flags</span></span>           | <span data-ttu-id="c8037-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8037-243">0x00000010</span></span>                                   |
| <span data-ttu-id="c8037-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c8037-244">Classes used in</span></span>        | [<span data-ttu-id="c8037-245">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c8037-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c8037-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8037-246">Windows Server 2012</span></span>



| <span data-ttu-id="c8037-247">Voce</span><span class="sxs-lookup"><span data-stu-id="c8037-247">Entry</span></span> | <span data-ttu-id="c8037-248">Valore</span><span class="sxs-lookup"><span data-stu-id="c8037-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8037-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c8037-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8037-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8037-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8037-251">System-Only</span></span>            | <span data-ttu-id="c8037-252">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-252">False</span></span>                                        |
| <span data-ttu-id="c8037-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c8037-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c8037-254">Vero</span><span class="sxs-lookup"><span data-stu-id="c8037-254">True</span></span>                                         |
| <span data-ttu-id="c8037-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c8037-255">Is Indexed</span></span>             | <span data-ttu-id="c8037-256">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-256">False</span></span>                                        |
| <span data-ttu-id="c8037-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c8037-257">In Global Catalog</span></span>      | <span data-ttu-id="c8037-258">Falso</span><span class="sxs-lookup"><span data-stu-id="c8037-258">False</span></span>                                        |
| <span data-ttu-id="c8037-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c8037-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8037-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c8037-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8037-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8037-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8037-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8037-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8037-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-263">Search-Flags</span></span>           | <span data-ttu-id="c8037-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8037-264">0x00000000</span></span>                                   |
| <span data-ttu-id="c8037-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8037-265">System-Flags</span></span>           | <span data-ttu-id="c8037-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8037-266">0x00000010</span></span>                                   |
| <span data-ttu-id="c8037-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c8037-267">Classes used in</span></span>        | [<span data-ttu-id="c8037-268">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="c8037-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





