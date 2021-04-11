---
title: Attributo builtin-count modificato
description: Per supportare la replica nei domini di Windows NT 4,0, viene usato l'attributo builtin-modified-Count.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo builtin-modified-count
- Schema AD dell'attributo builtinModifiedCount
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123096"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="4a97a-105">Attributo builtin-count modificato</span><span class="sxs-lookup"><span data-stu-id="4a97a-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="4a97a-106">Per supportare la replica nei domini di Windows NT 4,0, viene usato l'attributo **Builtin-modified-count** .</span><span class="sxs-lookup"><span data-stu-id="4a97a-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="4a97a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-107">Entry</span></span> | <span data-ttu-id="4a97a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4a97a-109">CN</span><span class="sxs-lookup"><span data-stu-id="4a97a-109">CN</span></span>                | <span data-ttu-id="4a97a-110">Builtin-modificato-conteggio</span><span class="sxs-lookup"><span data-stu-id="4a97a-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="4a97a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a97a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4a97a-112">builtinModifiedCount</span><span class="sxs-lookup"><span data-stu-id="4a97a-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="4a97a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4a97a-113">Size</span></span>              | <span data-ttu-id="4a97a-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="4a97a-114">8 bytes</span></span>                              |
| <span data-ttu-id="4a97a-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-115">Update Privilege</span></span>  | <span data-ttu-id="4a97a-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4a97a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="4a97a-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4a97a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-118">Attribute-Id</span></span>      | <span data-ttu-id="4a97a-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="4a97a-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="4a97a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a97a-120">System-Id-Guid</span></span>    | <span data-ttu-id="4a97a-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4a97a-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="4a97a-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a97a-122">Syntax</span></span>            | [<span data-ttu-id="4a97a-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="4a97a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4a97a-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4a97a-124">Implementations</span></span>

-   [<span data-ttu-id="4a97a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a97a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a97a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a97a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a97a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a97a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a97a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a97a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a97a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a97a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a97a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a97a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a97a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a97a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4a97a-132">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-132">Entry</span></span> | <span data-ttu-id="4a97a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a97a-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a97a-136">System-Only</span></span>            | <span data-ttu-id="4a97a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-137">False</span></span>                                        |
| <span data-ttu-id="4a97a-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a97a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4a97a-139">Vero</span><span class="sxs-lookup"><span data-stu-id="4a97a-139">True</span></span>                                         |
| <span data-ttu-id="4a97a-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a97a-140">Is Indexed</span></span>             | <span data-ttu-id="4a97a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-141">False</span></span>                                        |
| <span data-ttu-id="4a97a-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a97a-142">In Global Catalog</span></span>      | <span data-ttu-id="4a97a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-143">False</span></span>                                        |
| <span data-ttu-id="4a97a-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a97a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a97a-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a97a-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a97a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a97a-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a97a-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-148">Search-Flags</span></span>           | <span data-ttu-id="4a97a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a97a-149">0x00000000</span></span>                                   |
| <span data-ttu-id="4a97a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-150">System-Flags</span></span>           | <span data-ttu-id="4a97a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a97a-151">0x00000010</span></span>                                   |
| <span data-ttu-id="4a97a-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a97a-152">Classes used in</span></span>        | [<span data-ttu-id="4a97a-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="4a97a-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a97a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a97a-154">Windows Server 2003</span></span>



| <span data-ttu-id="4a97a-155">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-155">Entry</span></span> | <span data-ttu-id="4a97a-156">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a97a-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a97a-159">System-Only</span></span>            | <span data-ttu-id="4a97a-160">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-160">False</span></span>                                        |
| <span data-ttu-id="4a97a-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a97a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4a97a-162">Vero</span><span class="sxs-lookup"><span data-stu-id="4a97a-162">True</span></span>                                         |
| <span data-ttu-id="4a97a-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a97a-163">Is Indexed</span></span>             | <span data-ttu-id="4a97a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-164">False</span></span>                                        |
| <span data-ttu-id="4a97a-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a97a-165">In Global Catalog</span></span>      | <span data-ttu-id="4a97a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-166">False</span></span>                                        |
| <span data-ttu-id="4a97a-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a97a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a97a-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a97a-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a97a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a97a-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a97a-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-171">Search-Flags</span></span>           | <span data-ttu-id="4a97a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a97a-172">0x00000000</span></span>                                   |
| <span data-ttu-id="4a97a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-173">System-Flags</span></span>           | <span data-ttu-id="4a97a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a97a-174">0x00000010</span></span>                                   |
| <span data-ttu-id="4a97a-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a97a-175">Classes used in</span></span>        | [<span data-ttu-id="4a97a-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="4a97a-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a97a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a97a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a97a-178">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-178">Entry</span></span> | <span data-ttu-id="4a97a-179">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a97a-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a97a-182">System-Only</span></span>            | <span data-ttu-id="4a97a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-183">False</span></span>                                        |
| <span data-ttu-id="4a97a-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a97a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4a97a-185">Vero</span><span class="sxs-lookup"><span data-stu-id="4a97a-185">True</span></span>                                         |
| <span data-ttu-id="4a97a-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a97a-186">Is Indexed</span></span>             | <span data-ttu-id="4a97a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-187">False</span></span>                                        |
| <span data-ttu-id="4a97a-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a97a-188">In Global Catalog</span></span>      | <span data-ttu-id="4a97a-189">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-189">False</span></span>                                        |
| <span data-ttu-id="4a97a-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a97a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a97a-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a97a-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a97a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a97a-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a97a-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-194">Search-Flags</span></span>           | <span data-ttu-id="4a97a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a97a-195">0x00000000</span></span>                                   |
| <span data-ttu-id="4a97a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-196">System-Flags</span></span>           | <span data-ttu-id="4a97a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a97a-197">0x00000010</span></span>                                   |
| <span data-ttu-id="4a97a-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a97a-198">Classes used in</span></span>        | [<span data-ttu-id="4a97a-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="4a97a-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a97a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a97a-200">Windows Server 2008</span></span>



| <span data-ttu-id="4a97a-201">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-201">Entry</span></span> | <span data-ttu-id="4a97a-202">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a97a-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a97a-205">System-Only</span></span>            | <span data-ttu-id="4a97a-206">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-206">False</span></span>                                        |
| <span data-ttu-id="4a97a-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a97a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4a97a-208">Vero</span><span class="sxs-lookup"><span data-stu-id="4a97a-208">True</span></span>                                         |
| <span data-ttu-id="4a97a-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a97a-209">Is Indexed</span></span>             | <span data-ttu-id="4a97a-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-210">False</span></span>                                        |
| <span data-ttu-id="4a97a-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a97a-211">In Global Catalog</span></span>      | <span data-ttu-id="4a97a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-212">False</span></span>                                        |
| <span data-ttu-id="4a97a-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a97a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a97a-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a97a-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a97a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a97a-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a97a-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-217">Search-Flags</span></span>           | <span data-ttu-id="4a97a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a97a-218">0x00000000</span></span>                                   |
| <span data-ttu-id="4a97a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-219">System-Flags</span></span>           | <span data-ttu-id="4a97a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a97a-220">0x00000010</span></span>                                   |
| <span data-ttu-id="4a97a-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a97a-221">Classes used in</span></span>        | [<span data-ttu-id="4a97a-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="4a97a-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a97a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a97a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a97a-224">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-224">Entry</span></span> | <span data-ttu-id="4a97a-225">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a97a-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a97a-228">System-Only</span></span>            | <span data-ttu-id="4a97a-229">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-229">False</span></span>                                        |
| <span data-ttu-id="4a97a-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a97a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4a97a-231">Vero</span><span class="sxs-lookup"><span data-stu-id="4a97a-231">True</span></span>                                         |
| <span data-ttu-id="4a97a-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a97a-232">Is Indexed</span></span>             | <span data-ttu-id="4a97a-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-233">False</span></span>                                        |
| <span data-ttu-id="4a97a-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a97a-234">In Global Catalog</span></span>      | <span data-ttu-id="4a97a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-235">False</span></span>                                        |
| <span data-ttu-id="4a97a-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a97a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a97a-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a97a-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a97a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a97a-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a97a-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-240">Search-Flags</span></span>           | <span data-ttu-id="4a97a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a97a-241">0x00000000</span></span>                                   |
| <span data-ttu-id="4a97a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-242">System-Flags</span></span>           | <span data-ttu-id="4a97a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a97a-243">0x00000010</span></span>                                   |
| <span data-ttu-id="4a97a-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a97a-244">Classes used in</span></span>        | [<span data-ttu-id="4a97a-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="4a97a-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a97a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a97a-246">Windows Server 2012</span></span>



| <span data-ttu-id="4a97a-247">Voce</span><span class="sxs-lookup"><span data-stu-id="4a97a-247">Entry</span></span> | <span data-ttu-id="4a97a-248">Valore</span><span class="sxs-lookup"><span data-stu-id="4a97a-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4a97a-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4a97a-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a97a-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4a97a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a97a-251">System-Only</span></span>            | <span data-ttu-id="4a97a-252">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-252">False</span></span>                                        |
| <span data-ttu-id="4a97a-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4a97a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4a97a-254">Vero</span><span class="sxs-lookup"><span data-stu-id="4a97a-254">True</span></span>                                         |
| <span data-ttu-id="4a97a-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4a97a-255">Is Indexed</span></span>             | <span data-ttu-id="4a97a-256">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-256">False</span></span>                                        |
| <span data-ttu-id="4a97a-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4a97a-257">In Global Catalog</span></span>      | <span data-ttu-id="4a97a-258">Falso</span><span class="sxs-lookup"><span data-stu-id="4a97a-258">False</span></span>                                        |
| <span data-ttu-id="4a97a-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4a97a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a97a-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4a97a-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4a97a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a97a-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a97a-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4a97a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-263">Search-Flags</span></span>           | <span data-ttu-id="4a97a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a97a-264">0x00000000</span></span>                                   |
| <span data-ttu-id="4a97a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a97a-265">System-Flags</span></span>           | <span data-ttu-id="4a97a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a97a-266">0x00000010</span></span>                                   |
| <span data-ttu-id="4a97a-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4a97a-267">Classes used in</span></span>        | [<span data-ttu-id="4a97a-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="4a97a-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





