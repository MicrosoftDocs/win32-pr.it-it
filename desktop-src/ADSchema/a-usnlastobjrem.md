---
title: USN-Last-obj-REM (attributo)
description: Contiene il numero di sequenza di aggiornamento (USN) per l'ultimo oggetto non di sistema che è stato rimosso da un server.
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- USN-Last-obj-REM-schema AD dell'attributo
- Schema AD dell'attributo uSNLastObjRem
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519949"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="bc40f-105">USN-Last-obj-REM (attributo)</span><span class="sxs-lookup"><span data-stu-id="bc40f-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="bc40f-106">Contiene il numero di sequenza di aggiornamento (USN) per l'ultimo oggetto non di sistema che è stato rimosso da un server.</span><span class="sxs-lookup"><span data-stu-id="bc40f-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="bc40f-107">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-107">Entry</span></span> | <span data-ttu-id="bc40f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bc40f-109">CN</span><span class="sxs-lookup"><span data-stu-id="bc40f-109">CN</span></span>                | <span data-ttu-id="bc40f-110">USN-ultimo-obj-REM</span><span class="sxs-lookup"><span data-stu-id="bc40f-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="bc40f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bc40f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bc40f-112">uSNLastObjRem</span><span class="sxs-lookup"><span data-stu-id="bc40f-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="bc40f-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bc40f-113">Size</span></span>              | <span data-ttu-id="bc40f-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="bc40f-114">8 bytes</span></span>                              |
| <span data-ttu-id="bc40f-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-115">Update Privilege</span></span>  | <span data-ttu-id="bc40f-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bc40f-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="bc40f-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-117">Update Frequency</span></span>  | <span data-ttu-id="bc40f-118">Ogni volta che un oggetto directory viene modificato.</span><span class="sxs-lookup"><span data-stu-id="bc40f-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="bc40f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-119">Attribute-Id</span></span>      | <span data-ttu-id="bc40f-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="bc40f-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="bc40f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bc40f-121">System-Id-Guid</span></span>    | <span data-ttu-id="bc40f-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bc40f-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="bc40f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc40f-123">Syntax</span></span>            | [<span data-ttu-id="bc40f-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="bc40f-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="bc40f-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="bc40f-125">Implementations</span></span>

-   [<span data-ttu-id="bc40f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bc40f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bc40f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bc40f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bc40f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bc40f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bc40f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bc40f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bc40f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bc40f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bc40f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bc40f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bc40f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bc40f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bc40f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc40f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="bc40f-134">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-134">Entry</span></span> | <span data-ttu-id="bc40f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-137">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-138">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-139">System-Only</span></span>            | <span data-ttu-id="bc40f-140">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-140">True</span></span>                            |
| <span data-ttu-id="bc40f-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-142">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-142">True</span></span>                            |
| <span data-ttu-id="bc40f-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-143">Is Indexed</span></span>             | <span data-ttu-id="bc40f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-144">False</span></span>                           |
| <span data-ttu-id="bc40f-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-145">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-146">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-146">True</span></span>                            |
| <span data-ttu-id="bc40f-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-151">Search-Flags</span></span>           | <span data-ttu-id="bc40f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-152">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-153">System-Flags</span></span>           | <span data-ttu-id="bc40f-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-154">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-155">Classes used in</span></span>        | [<span data-ttu-id="bc40f-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bc40f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc40f-157">Windows Server 2003</span></span>



| <span data-ttu-id="bc40f-158">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-158">Entry</span></span> | <span data-ttu-id="bc40f-159">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-161">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-162">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-163">System-Only</span></span>            | <span data-ttu-id="bc40f-164">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-164">True</span></span>                            |
| <span data-ttu-id="bc40f-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-166">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-166">True</span></span>                            |
| <span data-ttu-id="bc40f-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-167">Is Indexed</span></span>             | <span data-ttu-id="bc40f-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-168">False</span></span>                           |
| <span data-ttu-id="bc40f-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-169">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-170">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-170">True</span></span>                            |
| <span data-ttu-id="bc40f-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-175">Search-Flags</span></span>           | <span data-ttu-id="bc40f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-176">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-177">System-Flags</span></span>           | <span data-ttu-id="bc40f-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-178">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-179">Classes used in</span></span>        | [<span data-ttu-id="bc40f-180">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bc40f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="bc40f-181">ADAM</span></span>



| <span data-ttu-id="bc40f-182">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-182">Entry</span></span> | <span data-ttu-id="bc40f-183">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-185">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-186">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-187">System-Only</span></span>            | <span data-ttu-id="bc40f-188">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-188">True</span></span>                            |
| <span data-ttu-id="bc40f-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-190">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-190">True</span></span>                            |
| <span data-ttu-id="bc40f-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-191">Is Indexed</span></span>             | <span data-ttu-id="bc40f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-192">False</span></span>                           |
| <span data-ttu-id="bc40f-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-193">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-194">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-194">True</span></span>                            |
| <span data-ttu-id="bc40f-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-199">Search-Flags</span></span>           | <span data-ttu-id="bc40f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-200">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-201">System-Flags</span></span>           | <span data-ttu-id="bc40f-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-202">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-203">Classes used in</span></span>        | [<span data-ttu-id="bc40f-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bc40f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bc40f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bc40f-206">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-206">Entry</span></span> | <span data-ttu-id="bc40f-207">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-209">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-210">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-211">System-Only</span></span>            | <span data-ttu-id="bc40f-212">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-212">True</span></span>                            |
| <span data-ttu-id="bc40f-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-214">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-214">True</span></span>                            |
| <span data-ttu-id="bc40f-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-215">Is Indexed</span></span>             | <span data-ttu-id="bc40f-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-216">False</span></span>                           |
| <span data-ttu-id="bc40f-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-217">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-218">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-218">True</span></span>                            |
| <span data-ttu-id="bc40f-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-223">Search-Flags</span></span>           | <span data-ttu-id="bc40f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-224">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-225">System-Flags</span></span>           | <span data-ttu-id="bc40f-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-226">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-227">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-227">Classes used in</span></span>        | [<span data-ttu-id="bc40f-228">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bc40f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc40f-229">Windows Server 2008</span></span>



| <span data-ttu-id="bc40f-230">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-230">Entry</span></span> | <span data-ttu-id="bc40f-231">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-233">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-234">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-235">System-Only</span></span>            | <span data-ttu-id="bc40f-236">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-236">True</span></span>                            |
| <span data-ttu-id="bc40f-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-238">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-238">True</span></span>                            |
| <span data-ttu-id="bc40f-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-239">Is Indexed</span></span>             | <span data-ttu-id="bc40f-240">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-240">False</span></span>                           |
| <span data-ttu-id="bc40f-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-241">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-242">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-242">True</span></span>                            |
| <span data-ttu-id="bc40f-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-247">Search-Flags</span></span>           | <span data-ttu-id="bc40f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-248">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-249">System-Flags</span></span>           | <span data-ttu-id="bc40f-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-250">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-251">Classes used in</span></span>        | [<span data-ttu-id="bc40f-252">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bc40f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc40f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bc40f-254">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-254">Entry</span></span> | <span data-ttu-id="bc40f-255">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-257">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-258">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-259">System-Only</span></span>            | <span data-ttu-id="bc40f-260">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-260">True</span></span>                            |
| <span data-ttu-id="bc40f-261">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-262">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-262">True</span></span>                            |
| <span data-ttu-id="bc40f-263">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-263">Is Indexed</span></span>             | <span data-ttu-id="bc40f-264">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-264">False</span></span>                           |
| <span data-ttu-id="bc40f-265">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-265">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-266">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-266">True</span></span>                            |
| <span data-ttu-id="bc40f-267">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-268">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-271">Search-Flags</span></span>           | <span data-ttu-id="bc40f-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-272">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-273">System-Flags</span></span>           | <span data-ttu-id="bc40f-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-274">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-275">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-275">Classes used in</span></span>        | [<span data-ttu-id="bc40f-276">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bc40f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc40f-277">Windows Server 2012</span></span>



| <span data-ttu-id="bc40f-278">Voce</span><span class="sxs-lookup"><span data-stu-id="bc40f-278">Entry</span></span> | <span data-ttu-id="bc40f-279">Valore</span><span class="sxs-lookup"><span data-stu-id="bc40f-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bc40f-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="bc40f-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bc40f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bc40f-281">MAPI-Id</span></span>                | <span data-ttu-id="bc40f-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="bc40f-282">0x8156</span></span>                          |
| <span data-ttu-id="bc40f-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="bc40f-283">System-Only</span></span>            | <span data-ttu-id="bc40f-284">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-284">True</span></span>                            |
| <span data-ttu-id="bc40f-285">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="bc40f-285">Is-Single-Valued</span></span>       | <span data-ttu-id="bc40f-286">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-286">True</span></span>                            |
| <span data-ttu-id="bc40f-287">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="bc40f-287">Is Indexed</span></span>             | <span data-ttu-id="bc40f-288">Falso</span><span class="sxs-lookup"><span data-stu-id="bc40f-288">False</span></span>                           |
| <span data-ttu-id="bc40f-289">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="bc40f-289">In Global Catalog</span></span>      | <span data-ttu-id="bc40f-290">Vero</span><span class="sxs-lookup"><span data-stu-id="bc40f-290">True</span></span>                            |
| <span data-ttu-id="bc40f-291">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="bc40f-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="bc40f-292">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="bc40f-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bc40f-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bc40f-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bc40f-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bc40f-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bc40f-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-295">Search-Flags</span></span>           | <span data-ttu-id="bc40f-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bc40f-296">0x00000000</span></span>                      |
| <span data-ttu-id="bc40f-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bc40f-297">System-Flags</span></span>           | <span data-ttu-id="bc40f-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="bc40f-298">0x00000013</span></span>                      |
| <span data-ttu-id="bc40f-299">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="bc40f-299">Classes used in</span></span>        | [<span data-ttu-id="bc40f-300">**In alto**</span><span class="sxs-lookup"><span data-stu-id="bc40f-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="bc40f-301">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc40f-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc40f-302">**USN-DSA-Last-obj-rimosso**</span><span class="sxs-lookup"><span data-stu-id="bc40f-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 





