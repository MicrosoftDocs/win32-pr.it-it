---
title: ACS-attributo non riservato-frequenza di punta
description: L'attributo ACS-non riservato a picco è solo per uso interno.
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- AD schema AD di attributo AD alta frequenza (ACS) non riservato
- Schema AD dell'attributo aCSNonReservedPeakRate
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122202"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="f046e-105">ACS-attributo non riservato-frequenza di punta</span><span class="sxs-lookup"><span data-stu-id="f046e-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="f046e-106">L'attributo **ACS-non riservato a picco** è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="f046e-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="f046e-107">Basato su RFC2814.</span><span class="sxs-lookup"><span data-stu-id="f046e-107">Based on RFC2814.</span></span>



| <span data-ttu-id="f046e-108">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-108">Entry</span></span> | <span data-ttu-id="f046e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f046e-110">CN</span><span class="sxs-lookup"><span data-stu-id="f046e-110">CN</span></span>                | <span data-ttu-id="f046e-111">ACS-non riservato-frequenza massima</span><span class="sxs-lookup"><span data-stu-id="f046e-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="f046e-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f046e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f046e-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="f046e-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="f046e-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f046e-114">Size</span></span>              | <span data-ttu-id="f046e-115">8 byte</span><span class="sxs-lookup"><span data-stu-id="f046e-115">8 bytes</span></span>                              |
| <span data-ttu-id="f046e-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f046e-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f046e-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f046e-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f046e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-118">Attribute-Id</span></span>      | <span data-ttu-id="f046e-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="f046e-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="f046e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f046e-120">System-Id-Guid</span></span>    | <span data-ttu-id="f046e-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="f046e-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="f046e-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f046e-122">Syntax</span></span>            | [<span data-ttu-id="f046e-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="f046e-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f046e-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f046e-124">Implementations</span></span>

-   [<span data-ttu-id="f046e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f046e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f046e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f046e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f046e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f046e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f046e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f046e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f046e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f046e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f046e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f046e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f046e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f046e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f046e-132">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-132">Entry</span></span> | <span data-ttu-id="f046e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f046e-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f046e-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f046e-136">System-Only</span></span>            | <span data-ttu-id="f046e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-137">False</span></span>                                        |
| <span data-ttu-id="f046e-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f046e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f046e-139">Vero</span><span class="sxs-lookup"><span data-stu-id="f046e-139">True</span></span>                                         |
| <span data-ttu-id="f046e-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f046e-140">Is Indexed</span></span>             | <span data-ttu-id="f046e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-141">False</span></span>                                        |
| <span data-ttu-id="f046e-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f046e-142">In Global Catalog</span></span>      | <span data-ttu-id="f046e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-143">False</span></span>                                        |
| <span data-ttu-id="f046e-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f046e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f046e-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f046e-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f046e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f046e-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f046e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f046e-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f046e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-148">Search-Flags</span></span>           | <span data-ttu-id="f046e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f046e-149">0x00000000</span></span>                                   |
| <span data-ttu-id="f046e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-150">System-Flags</span></span>           | <span data-ttu-id="f046e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f046e-151">0x00000010</span></span>                                   |
| <span data-ttu-id="f046e-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f046e-152">Classes used in</span></span>        | [<span data-ttu-id="f046e-153">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="f046e-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f046e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f046e-154">Windows Server 2003</span></span>



| <span data-ttu-id="f046e-155">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-155">Entry</span></span> | <span data-ttu-id="f046e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f046e-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f046e-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f046e-159">System-Only</span></span>            | <span data-ttu-id="f046e-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-160">False</span></span>                                        |
| <span data-ttu-id="f046e-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f046e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f046e-162">Vero</span><span class="sxs-lookup"><span data-stu-id="f046e-162">True</span></span>                                         |
| <span data-ttu-id="f046e-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f046e-163">Is Indexed</span></span>             | <span data-ttu-id="f046e-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-164">False</span></span>                                        |
| <span data-ttu-id="f046e-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f046e-165">In Global Catalog</span></span>      | <span data-ttu-id="f046e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-166">False</span></span>                                        |
| <span data-ttu-id="f046e-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f046e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f046e-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f046e-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f046e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f046e-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f046e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f046e-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f046e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-171">Search-Flags</span></span>           | <span data-ttu-id="f046e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f046e-172">0x00000000</span></span>                                   |
| <span data-ttu-id="f046e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-173">System-Flags</span></span>           | <span data-ttu-id="f046e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f046e-174">0x00000010</span></span>                                   |
| <span data-ttu-id="f046e-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f046e-175">Classes used in</span></span>        | [<span data-ttu-id="f046e-176">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="f046e-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f046e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f046e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f046e-178">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-178">Entry</span></span> | <span data-ttu-id="f046e-179">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f046e-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f046e-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f046e-182">System-Only</span></span>            | <span data-ttu-id="f046e-183">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-183">False</span></span>                                        |
| <span data-ttu-id="f046e-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f046e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f046e-185">Vero</span><span class="sxs-lookup"><span data-stu-id="f046e-185">True</span></span>                                         |
| <span data-ttu-id="f046e-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f046e-186">Is Indexed</span></span>             | <span data-ttu-id="f046e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-187">False</span></span>                                        |
| <span data-ttu-id="f046e-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f046e-188">In Global Catalog</span></span>      | <span data-ttu-id="f046e-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-189">False</span></span>                                        |
| <span data-ttu-id="f046e-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f046e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f046e-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f046e-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f046e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f046e-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f046e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f046e-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f046e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-194">Search-Flags</span></span>           | <span data-ttu-id="f046e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f046e-195">0x00000000</span></span>                                   |
| <span data-ttu-id="f046e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-196">System-Flags</span></span>           | <span data-ttu-id="f046e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f046e-197">0x00000010</span></span>                                   |
| <span data-ttu-id="f046e-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f046e-198">Classes used in</span></span>        | [<span data-ttu-id="f046e-199">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="f046e-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f046e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f046e-200">Windows Server 2008</span></span>



| <span data-ttu-id="f046e-201">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-201">Entry</span></span> | <span data-ttu-id="f046e-202">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f046e-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f046e-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f046e-205">System-Only</span></span>            | <span data-ttu-id="f046e-206">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-206">False</span></span>                                        |
| <span data-ttu-id="f046e-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f046e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f046e-208">Vero</span><span class="sxs-lookup"><span data-stu-id="f046e-208">True</span></span>                                         |
| <span data-ttu-id="f046e-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f046e-209">Is Indexed</span></span>             | <span data-ttu-id="f046e-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-210">False</span></span>                                        |
| <span data-ttu-id="f046e-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f046e-211">In Global Catalog</span></span>      | <span data-ttu-id="f046e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-212">False</span></span>                                        |
| <span data-ttu-id="f046e-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f046e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f046e-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f046e-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f046e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f046e-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f046e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f046e-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f046e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-217">Search-Flags</span></span>           | <span data-ttu-id="f046e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f046e-218">0x00000000</span></span>                                   |
| <span data-ttu-id="f046e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-219">System-Flags</span></span>           | <span data-ttu-id="f046e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f046e-220">0x00000010</span></span>                                   |
| <span data-ttu-id="f046e-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f046e-221">Classes used in</span></span>        | [<span data-ttu-id="f046e-222">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="f046e-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f046e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f046e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f046e-224">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-224">Entry</span></span> | <span data-ttu-id="f046e-225">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f046e-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f046e-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f046e-228">System-Only</span></span>            | <span data-ttu-id="f046e-229">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-229">False</span></span>                                        |
| <span data-ttu-id="f046e-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f046e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f046e-231">Vero</span><span class="sxs-lookup"><span data-stu-id="f046e-231">True</span></span>                                         |
| <span data-ttu-id="f046e-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f046e-232">Is Indexed</span></span>             | <span data-ttu-id="f046e-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-233">False</span></span>                                        |
| <span data-ttu-id="f046e-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f046e-234">In Global Catalog</span></span>      | <span data-ttu-id="f046e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-235">False</span></span>                                        |
| <span data-ttu-id="f046e-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f046e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f046e-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f046e-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f046e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f046e-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f046e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f046e-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f046e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-240">Search-Flags</span></span>           | <span data-ttu-id="f046e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f046e-241">0x00000000</span></span>                                   |
| <span data-ttu-id="f046e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-242">System-Flags</span></span>           | <span data-ttu-id="f046e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f046e-243">0x00000010</span></span>                                   |
| <span data-ttu-id="f046e-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f046e-244">Classes used in</span></span>        | [<span data-ttu-id="f046e-245">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="f046e-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f046e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f046e-246">Windows Server 2012</span></span>



| <span data-ttu-id="f046e-247">Voce</span><span class="sxs-lookup"><span data-stu-id="f046e-247">Entry</span></span> | <span data-ttu-id="f046e-248">Valore</span><span class="sxs-lookup"><span data-stu-id="f046e-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f046e-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f046e-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f046e-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f046e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f046e-251">System-Only</span></span>            | <span data-ttu-id="f046e-252">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-252">False</span></span>                                        |
| <span data-ttu-id="f046e-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f046e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f046e-254">Vero</span><span class="sxs-lookup"><span data-stu-id="f046e-254">True</span></span>                                         |
| <span data-ttu-id="f046e-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f046e-255">Is Indexed</span></span>             | <span data-ttu-id="f046e-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-256">False</span></span>                                        |
| <span data-ttu-id="f046e-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f046e-257">In Global Catalog</span></span>      | <span data-ttu-id="f046e-258">Falso</span><span class="sxs-lookup"><span data-stu-id="f046e-258">False</span></span>                                        |
| <span data-ttu-id="f046e-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f046e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f046e-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f046e-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f046e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f046e-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f046e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f046e-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f046e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-263">Search-Flags</span></span>           | <span data-ttu-id="f046e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f046e-264">0x00000000</span></span>                                   |
| <span data-ttu-id="f046e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f046e-265">System-Flags</span></span>           | <span data-ttu-id="f046e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f046e-266">0x00000010</span></span>                                   |
| <span data-ttu-id="f046e-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f046e-267">Classes used in</span></span>        | [<span data-ttu-id="f046e-268">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="f046e-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





