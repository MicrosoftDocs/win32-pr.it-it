---
title: USN-DSA-ultimo-obj-attributo rimosso
description: Contiene il numero di sequenza di aggiornamento (USN) dell'ultimo oggetto di sistema che è stato rimosso da un server.
ms.assetid: af0afd80-fe4a-4bc6-84e3-14c2900bec93
ms.tgt_platform: multiple
keywords:
- USN-DSA-Last-obj-schema AD dell'attributo rimosso
- Schema AD dell'attributo uSNDSALastObjRemoved
topic_type:
- apiref
api_name:
- USN-DSA-Last-Obj-Removed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbc246aa1a0f7c794b9dc0a9d2a725273a918e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965314"
---
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="b1e26-105">USN-DSA-ultimo-obj-attributo rimosso</span><span class="sxs-lookup"><span data-stu-id="b1e26-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="b1e26-106">Contiene il numero di sequenza di aggiornamento (USN) dell'ultimo oggetto di sistema che è stato rimosso da un server.</span><span class="sxs-lookup"><span data-stu-id="b1e26-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="b1e26-107">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-107">Entry</span></span> | <span data-ttu-id="b1e26-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b1e26-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1e26-109">CN</span></span>                | <span data-ttu-id="b1e26-110">USN-DSA-Last-obj-rimosso</span><span class="sxs-lookup"><span data-stu-id="b1e26-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="b1e26-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b1e26-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1e26-112">uSNDSALastObjRemoved</span><span class="sxs-lookup"><span data-stu-id="b1e26-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="b1e26-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b1e26-113">Size</span></span>              | <span data-ttu-id="b1e26-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="b1e26-114">8 bytes</span></span>                              |
| <span data-ttu-id="b1e26-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-115">Update Privilege</span></span>  | <span data-ttu-id="b1e26-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1e26-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="b1e26-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-117">Update Frequency</span></span>  | <span data-ttu-id="b1e26-118">Ogni volta che un oggetto directory viene modificato.</span><span class="sxs-lookup"><span data-stu-id="b1e26-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="b1e26-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-119">Attribute-Id</span></span>      | <span data-ttu-id="b1e26-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="b1e26-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="b1e26-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b1e26-121">System-Id-Guid</span></span>    | <span data-ttu-id="b1e26-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b1e26-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b1e26-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1e26-123">Syntax</span></span>            | [<span data-ttu-id="b1e26-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="b1e26-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b1e26-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b1e26-125">Implementations</span></span>

-   [<span data-ttu-id="b1e26-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b1e26-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b1e26-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1e26-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1e26-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b1e26-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b1e26-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1e26-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1e26-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1e26-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1e26-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1e26-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1e26-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1e26-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b1e26-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1e26-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b1e26-134">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-134">Entry</span></span> | <span data-ttu-id="b1e26-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-137">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-138">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-139">System-Only</span></span>            | <span data-ttu-id="b1e26-140">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-140">True</span></span>                            |
| <span data-ttu-id="b1e26-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-142">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-142">True</span></span>                            |
| <span data-ttu-id="b1e26-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-143">Is Indexed</span></span>             | <span data-ttu-id="b1e26-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-144">False</span></span>                           |
| <span data-ttu-id="b1e26-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-145">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-146">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-146">False</span></span>                           |
| <span data-ttu-id="b1e26-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-151">Search-Flags</span></span>           | <span data-ttu-id="b1e26-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-152">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-153">System-Flags</span></span>           | <span data-ttu-id="b1e26-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-154">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-155">Classes used in</span></span>        | [<span data-ttu-id="b1e26-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b1e26-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1e26-157">Windows Server 2003</span></span>



| <span data-ttu-id="b1e26-158">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-158">Entry</span></span> | <span data-ttu-id="b1e26-159">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-161">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-162">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-163">System-Only</span></span>            | <span data-ttu-id="b1e26-164">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-164">True</span></span>                            |
| <span data-ttu-id="b1e26-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-166">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-166">True</span></span>                            |
| <span data-ttu-id="b1e26-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-167">Is Indexed</span></span>             | <span data-ttu-id="b1e26-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-168">False</span></span>                           |
| <span data-ttu-id="b1e26-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-169">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-170">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-170">False</span></span>                           |
| <span data-ttu-id="b1e26-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-175">Search-Flags</span></span>           | <span data-ttu-id="b1e26-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-176">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-177">System-Flags</span></span>           | <span data-ttu-id="b1e26-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-178">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-179">Classes used in</span></span>        | [<span data-ttu-id="b1e26-180">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b1e26-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="b1e26-181">ADAM</span></span>



| <span data-ttu-id="b1e26-182">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-182">Entry</span></span> | <span data-ttu-id="b1e26-183">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-185">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-186">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-187">System-Only</span></span>            | <span data-ttu-id="b1e26-188">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-188">True</span></span>                            |
| <span data-ttu-id="b1e26-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-190">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-190">True</span></span>                            |
| <span data-ttu-id="b1e26-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-191">Is Indexed</span></span>             | <span data-ttu-id="b1e26-192">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-192">False</span></span>                           |
| <span data-ttu-id="b1e26-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-193">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-194">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-194">False</span></span>                           |
| <span data-ttu-id="b1e26-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-199">Search-Flags</span></span>           | <span data-ttu-id="b1e26-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-200">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-201">System-Flags</span></span>           | <span data-ttu-id="b1e26-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-202">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-203">Classes used in</span></span>        | [<span data-ttu-id="b1e26-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1e26-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1e26-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1e26-206">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-206">Entry</span></span> | <span data-ttu-id="b1e26-207">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-209">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-210">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-211">System-Only</span></span>            | <span data-ttu-id="b1e26-212">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-212">True</span></span>                            |
| <span data-ttu-id="b1e26-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-214">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-214">True</span></span>                            |
| <span data-ttu-id="b1e26-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-215">Is Indexed</span></span>             | <span data-ttu-id="b1e26-216">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-216">False</span></span>                           |
| <span data-ttu-id="b1e26-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-217">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-218">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-218">False</span></span>                           |
| <span data-ttu-id="b1e26-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-223">Search-Flags</span></span>           | <span data-ttu-id="b1e26-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-224">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-225">System-Flags</span></span>           | <span data-ttu-id="b1e26-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-226">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-227">Classes used in</span></span>        | [<span data-ttu-id="b1e26-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1e26-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1e26-229">Windows Server 2008</span></span>



| <span data-ttu-id="b1e26-230">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-230">Entry</span></span> | <span data-ttu-id="b1e26-231">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-233">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-234">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-235">System-Only</span></span>            | <span data-ttu-id="b1e26-236">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-236">True</span></span>                            |
| <span data-ttu-id="b1e26-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-238">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-238">True</span></span>                            |
| <span data-ttu-id="b1e26-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-239">Is Indexed</span></span>             | <span data-ttu-id="b1e26-240">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-240">False</span></span>                           |
| <span data-ttu-id="b1e26-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-241">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-242">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-242">False</span></span>                           |
| <span data-ttu-id="b1e26-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-247">Search-Flags</span></span>           | <span data-ttu-id="b1e26-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-248">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-249">System-Flags</span></span>           | <span data-ttu-id="b1e26-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-250">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-251">Classes used in</span></span>        | [<span data-ttu-id="b1e26-252">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1e26-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1e26-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1e26-254">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-254">Entry</span></span> | <span data-ttu-id="b1e26-255">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-257">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-258">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-259">System-Only</span></span>            | <span data-ttu-id="b1e26-260">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-260">True</span></span>                            |
| <span data-ttu-id="b1e26-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-262">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-262">True</span></span>                            |
| <span data-ttu-id="b1e26-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-263">Is Indexed</span></span>             | <span data-ttu-id="b1e26-264">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-264">False</span></span>                           |
| <span data-ttu-id="b1e26-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-265">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-266">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-266">False</span></span>                           |
| <span data-ttu-id="b1e26-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-271">Search-Flags</span></span>           | <span data-ttu-id="b1e26-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-272">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-273">System-Flags</span></span>           | <span data-ttu-id="b1e26-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-274">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-275">Classes used in</span></span>        | [<span data-ttu-id="b1e26-276">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1e26-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1e26-277">Windows Server 2012</span></span>



| <span data-ttu-id="b1e26-278">Voce</span><span class="sxs-lookup"><span data-stu-id="b1e26-278">Entry</span></span> | <span data-ttu-id="b1e26-279">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e26-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b1e26-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b1e26-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b1e26-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1e26-281">MAPI-Id</span></span>                | <span data-ttu-id="b1e26-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="b1e26-282">0x8155</span></span>                          |
| <span data-ttu-id="b1e26-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1e26-283">System-Only</span></span>            | <span data-ttu-id="b1e26-284">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-284">True</span></span>                            |
| <span data-ttu-id="b1e26-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b1e26-285">Is-Single-Valued</span></span>       | <span data-ttu-id="b1e26-286">Vero</span><span class="sxs-lookup"><span data-stu-id="b1e26-286">True</span></span>                            |
| <span data-ttu-id="b1e26-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b1e26-287">Is Indexed</span></span>             | <span data-ttu-id="b1e26-288">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-288">False</span></span>                           |
| <span data-ttu-id="b1e26-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b1e26-289">In Global Catalog</span></span>      | <span data-ttu-id="b1e26-290">Falso</span><span class="sxs-lookup"><span data-stu-id="b1e26-290">False</span></span>                           |
| <span data-ttu-id="b1e26-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b1e26-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1e26-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b1e26-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b1e26-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1e26-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b1e26-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1e26-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b1e26-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-295">Search-Flags</span></span>           | <span data-ttu-id="b1e26-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1e26-296">0x00000000</span></span>                      |
| <span data-ttu-id="b1e26-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1e26-297">System-Flags</span></span>           | <span data-ttu-id="b1e26-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1e26-298">0x00000010</span></span>                      |
| <span data-ttu-id="b1e26-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b1e26-299">Classes used in</span></span>        | [<span data-ttu-id="b1e26-300">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b1e26-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="b1e26-301">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1e26-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e26-302">**USN-ultimo-obj-REM**</span><span class="sxs-lookup"><span data-stu-id="b1e26-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 





