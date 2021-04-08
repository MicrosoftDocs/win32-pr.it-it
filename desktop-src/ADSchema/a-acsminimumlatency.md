---
title: ACS-attributo latenza minima
description: L'attributo ACS-latenza minima è solo per uso interno.
ms.assetid: ec2cca55-9e31-49da-98aa-aa2f6664ea90
ms.tgt_platform: multiple
keywords:
- ACS-schema AD dell'attributo con latenza minima
- Schema AD dell'attributo aCSMinimumLatency
topic_type:
- apiref
api_name:
- ACS-Minimum-Latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab7e9e6d5a9ccf626cdf8849ffe0e29504b4a0b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104048806"
---
# <a name="acs-minimum-latency-attribute"></a><span data-ttu-id="ea235-105">ACS-attributo latenza minima</span><span class="sxs-lookup"><span data-stu-id="ea235-105">ACS-Minimum-Latency attribute</span></span>

<span data-ttu-id="ea235-106">L'attributo **ACS-latenza minima** è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="ea235-106">The **ACS-Minimum-Latency** attribute is for internal use only.</span></span> <span data-ttu-id="ea235-107">Basato su RFC2210.</span><span class="sxs-lookup"><span data-stu-id="ea235-107">Based on RFC2210.</span></span>



| <span data-ttu-id="ea235-108">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-108">Entry</span></span> | <span data-ttu-id="ea235-109">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ea235-110">CN</span><span class="sxs-lookup"><span data-stu-id="ea235-110">CN</span></span>                | <span data-ttu-id="ea235-111">ACS-latenza minima</span><span class="sxs-lookup"><span data-stu-id="ea235-111">ACS-Minimum-Latency</span></span>                  |
| <span data-ttu-id="ea235-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ea235-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ea235-113">aCSMinimumLatency</span><span class="sxs-lookup"><span data-stu-id="ea235-113">aCSMinimumLatency</span></span>                    |
| <span data-ttu-id="ea235-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ea235-114">Size</span></span>              | <span data-ttu-id="ea235-115">8 byte</span><span class="sxs-lookup"><span data-stu-id="ea235-115">8 bytes</span></span>                              |
| <span data-ttu-id="ea235-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ea235-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ea235-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ea235-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ea235-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-118">Attribute-Id</span></span>      | <span data-ttu-id="ea235-119">1.2.840.113556.1.4.1316</span><span class="sxs-lookup"><span data-stu-id="ea235-119">1.2.840.113556.1.4.1316</span></span>              |
| <span data-ttu-id="ea235-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ea235-120">System-Id-Guid</span></span>    | <span data-ttu-id="ea235-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ea235-121">9517fefb-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="ea235-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea235-122">Syntax</span></span>            | [<span data-ttu-id="ea235-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="ea235-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ea235-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ea235-124">Implementations</span></span>

-   [<span data-ttu-id="ea235-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ea235-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ea235-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ea235-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ea235-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ea235-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ea235-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ea235-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ea235-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ea235-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ea235-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ea235-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ea235-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea235-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ea235-132">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-132">Entry</span></span> | <span data-ttu-id="ea235-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ea235-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea235-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea235-136">System-Only</span></span>            | <span data-ttu-id="ea235-137">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-137">False</span></span>                                        |
| <span data-ttu-id="ea235-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea235-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ea235-139">Vero</span><span class="sxs-lookup"><span data-stu-id="ea235-139">True</span></span>                                         |
| <span data-ttu-id="ea235-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea235-140">Is Indexed</span></span>             | <span data-ttu-id="ea235-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-141">False</span></span>                                        |
| <span data-ttu-id="ea235-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea235-142">In Global Catalog</span></span>      | <span data-ttu-id="ea235-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-143">False</span></span>                                        |
| <span data-ttu-id="ea235-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea235-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea235-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea235-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ea235-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea235-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ea235-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea235-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ea235-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-148">Search-Flags</span></span>           | <span data-ttu-id="ea235-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea235-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ea235-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-150">System-Flags</span></span>           | <span data-ttu-id="ea235-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea235-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ea235-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea235-152">Classes used in</span></span>        | [<span data-ttu-id="ea235-153">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="ea235-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ea235-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea235-154">Windows Server 2003</span></span>



| <span data-ttu-id="ea235-155">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-155">Entry</span></span> | <span data-ttu-id="ea235-156">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ea235-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea235-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea235-159">System-Only</span></span>            | <span data-ttu-id="ea235-160">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-160">False</span></span>                                        |
| <span data-ttu-id="ea235-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea235-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ea235-162">Vero</span><span class="sxs-lookup"><span data-stu-id="ea235-162">True</span></span>                                         |
| <span data-ttu-id="ea235-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea235-163">Is Indexed</span></span>             | <span data-ttu-id="ea235-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-164">False</span></span>                                        |
| <span data-ttu-id="ea235-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea235-165">In Global Catalog</span></span>      | <span data-ttu-id="ea235-166">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-166">False</span></span>                                        |
| <span data-ttu-id="ea235-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea235-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea235-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea235-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ea235-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea235-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ea235-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea235-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ea235-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-171">Search-Flags</span></span>           | <span data-ttu-id="ea235-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea235-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ea235-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-173">System-Flags</span></span>           | <span data-ttu-id="ea235-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea235-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ea235-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea235-175">Classes used in</span></span>        | [<span data-ttu-id="ea235-176">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="ea235-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ea235-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ea235-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ea235-178">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-178">Entry</span></span> | <span data-ttu-id="ea235-179">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ea235-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea235-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea235-182">System-Only</span></span>            | <span data-ttu-id="ea235-183">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-183">False</span></span>                                        |
| <span data-ttu-id="ea235-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea235-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ea235-185">Vero</span><span class="sxs-lookup"><span data-stu-id="ea235-185">True</span></span>                                         |
| <span data-ttu-id="ea235-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea235-186">Is Indexed</span></span>             | <span data-ttu-id="ea235-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-187">False</span></span>                                        |
| <span data-ttu-id="ea235-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea235-188">In Global Catalog</span></span>      | <span data-ttu-id="ea235-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-189">False</span></span>                                        |
| <span data-ttu-id="ea235-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea235-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea235-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea235-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ea235-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea235-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ea235-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea235-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ea235-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-194">Search-Flags</span></span>           | <span data-ttu-id="ea235-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea235-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ea235-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-196">System-Flags</span></span>           | <span data-ttu-id="ea235-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea235-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ea235-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea235-198">Classes used in</span></span>        | [<span data-ttu-id="ea235-199">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="ea235-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ea235-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea235-200">Windows Server 2008</span></span>



| <span data-ttu-id="ea235-201">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-201">Entry</span></span> | <span data-ttu-id="ea235-202">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ea235-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea235-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea235-205">System-Only</span></span>            | <span data-ttu-id="ea235-206">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-206">False</span></span>                                        |
| <span data-ttu-id="ea235-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea235-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ea235-208">Vero</span><span class="sxs-lookup"><span data-stu-id="ea235-208">True</span></span>                                         |
| <span data-ttu-id="ea235-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea235-209">Is Indexed</span></span>             | <span data-ttu-id="ea235-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-210">False</span></span>                                        |
| <span data-ttu-id="ea235-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea235-211">In Global Catalog</span></span>      | <span data-ttu-id="ea235-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-212">False</span></span>                                        |
| <span data-ttu-id="ea235-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea235-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea235-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea235-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ea235-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea235-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ea235-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea235-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ea235-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-217">Search-Flags</span></span>           | <span data-ttu-id="ea235-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea235-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ea235-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-219">System-Flags</span></span>           | <span data-ttu-id="ea235-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea235-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ea235-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea235-221">Classes used in</span></span>        | [<span data-ttu-id="ea235-222">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="ea235-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ea235-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea235-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ea235-224">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-224">Entry</span></span> | <span data-ttu-id="ea235-225">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ea235-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea235-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea235-228">System-Only</span></span>            | <span data-ttu-id="ea235-229">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-229">False</span></span>                                        |
| <span data-ttu-id="ea235-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea235-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ea235-231">Vero</span><span class="sxs-lookup"><span data-stu-id="ea235-231">True</span></span>                                         |
| <span data-ttu-id="ea235-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea235-232">Is Indexed</span></span>             | <span data-ttu-id="ea235-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-233">False</span></span>                                        |
| <span data-ttu-id="ea235-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea235-234">In Global Catalog</span></span>      | <span data-ttu-id="ea235-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-235">False</span></span>                                        |
| <span data-ttu-id="ea235-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea235-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea235-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea235-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ea235-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea235-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ea235-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea235-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ea235-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-240">Search-Flags</span></span>           | <span data-ttu-id="ea235-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea235-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ea235-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-242">System-Flags</span></span>           | <span data-ttu-id="ea235-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea235-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ea235-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea235-244">Classes used in</span></span>        | [<span data-ttu-id="ea235-245">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="ea235-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ea235-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea235-246">Windows Server 2012</span></span>



| <span data-ttu-id="ea235-247">Voce</span><span class="sxs-lookup"><span data-stu-id="ea235-247">Entry</span></span> | <span data-ttu-id="ea235-248">Valore</span><span class="sxs-lookup"><span data-stu-id="ea235-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ea235-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea235-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea235-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ea235-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea235-251">System-Only</span></span>            | <span data-ttu-id="ea235-252">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-252">False</span></span>                                        |
| <span data-ttu-id="ea235-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea235-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ea235-254">Vero</span><span class="sxs-lookup"><span data-stu-id="ea235-254">True</span></span>                                         |
| <span data-ttu-id="ea235-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea235-255">Is Indexed</span></span>             | <span data-ttu-id="ea235-256">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-256">False</span></span>                                        |
| <span data-ttu-id="ea235-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea235-257">In Global Catalog</span></span>      | <span data-ttu-id="ea235-258">Falso</span><span class="sxs-lookup"><span data-stu-id="ea235-258">False</span></span>                                        |
| <span data-ttu-id="ea235-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea235-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea235-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea235-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ea235-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea235-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ea235-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea235-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ea235-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-263">Search-Flags</span></span>           | <span data-ttu-id="ea235-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea235-264">0x00000000</span></span>                                   |
| <span data-ttu-id="ea235-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea235-265">System-Flags</span></span>           | <span data-ttu-id="ea235-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea235-266">0x00000010</span></span>                                   |
| <span data-ttu-id="ea235-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea235-267">Classes used in</span></span>        | [<span data-ttu-id="ea235-268">**ACS-criteri**</span><span class="sxs-lookup"><span data-stu-id="ea235-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





