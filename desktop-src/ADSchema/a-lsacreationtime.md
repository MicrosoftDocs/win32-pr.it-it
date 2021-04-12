---
title: LSA-fase di creazione-attributo
description: L'attributo LSA-Creation-Time viene usato per supportare la replica nei domini di Windows NT 4,0.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo in fase di creazione LSA
- Schema AD dell'attributo lSACreationTime
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400966"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="05e57-105">LSA-fase di creazione-attributo</span><span class="sxs-lookup"><span data-stu-id="05e57-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="05e57-106">L'attributo **LSA-Creation-Time** viene usato per supportare la replica nei domini di Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="05e57-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="05e57-107">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-107">Entry</span></span> | <span data-ttu-id="05e57-108">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="05e57-109">CN</span><span class="sxs-lookup"><span data-stu-id="05e57-109">CN</span></span>                | <span data-ttu-id="05e57-110">LSA-fase di creazione</span><span class="sxs-lookup"><span data-stu-id="05e57-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="05e57-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="05e57-111">Ldap-Display-Name</span></span> | <span data-ttu-id="05e57-112">lSACreationTime</span><span class="sxs-lookup"><span data-stu-id="05e57-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="05e57-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="05e57-113">Size</span></span>              | <span data-ttu-id="05e57-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="05e57-114">8 bytes</span></span>                              |
| <span data-ttu-id="05e57-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="05e57-115">Update Privilege</span></span>  | <span data-ttu-id="05e57-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="05e57-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="05e57-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="05e57-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="05e57-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-118">Attribute-Id</span></span>      | <span data-ttu-id="05e57-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="05e57-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="05e57-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="05e57-120">System-Id-Guid</span></span>    | <span data-ttu-id="05e57-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="05e57-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="05e57-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05e57-122">Syntax</span></span>            | [<span data-ttu-id="05e57-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="05e57-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="05e57-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="05e57-124">Implementations</span></span>

-   [<span data-ttu-id="05e57-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="05e57-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="05e57-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="05e57-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="05e57-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="05e57-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="05e57-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="05e57-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="05e57-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="05e57-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="05e57-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="05e57-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="05e57-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05e57-131">Windows 2000 Server</span></span>



| <span data-ttu-id="05e57-132">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-132">Entry</span></span> | <span data-ttu-id="05e57-133">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="05e57-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05e57-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="05e57-136">System-Only</span></span>            | <span data-ttu-id="05e57-137">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-137">False</span></span>                                        |
| <span data-ttu-id="05e57-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05e57-138">Is-Single-Valued</span></span>       | <span data-ttu-id="05e57-139">Vero</span><span class="sxs-lookup"><span data-stu-id="05e57-139">True</span></span>                                         |
| <span data-ttu-id="05e57-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05e57-140">Is Indexed</span></span>             | <span data-ttu-id="05e57-141">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-141">False</span></span>                                        |
| <span data-ttu-id="05e57-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05e57-142">In Global Catalog</span></span>      | <span data-ttu-id="05e57-143">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-143">False</span></span>                                        |
| <span data-ttu-id="05e57-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05e57-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="05e57-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05e57-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="05e57-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05e57-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="05e57-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05e57-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="05e57-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-148">Search-Flags</span></span>           | <span data-ttu-id="05e57-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e57-149">0x00000000</span></span>                                   |
| <span data-ttu-id="05e57-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-150">System-Flags</span></span>           | <span data-ttu-id="05e57-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05e57-151">0x00000010</span></span>                                   |
| <span data-ttu-id="05e57-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05e57-152">Classes used in</span></span>        | [<span data-ttu-id="05e57-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="05e57-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="05e57-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05e57-154">Windows Server 2003</span></span>



| <span data-ttu-id="05e57-155">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-155">Entry</span></span> | <span data-ttu-id="05e57-156">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="05e57-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05e57-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="05e57-159">System-Only</span></span>            | <span data-ttu-id="05e57-160">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-160">False</span></span>                                        |
| <span data-ttu-id="05e57-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05e57-161">Is-Single-Valued</span></span>       | <span data-ttu-id="05e57-162">Vero</span><span class="sxs-lookup"><span data-stu-id="05e57-162">True</span></span>                                         |
| <span data-ttu-id="05e57-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05e57-163">Is Indexed</span></span>             | <span data-ttu-id="05e57-164">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-164">False</span></span>                                        |
| <span data-ttu-id="05e57-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05e57-165">In Global Catalog</span></span>      | <span data-ttu-id="05e57-166">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-166">False</span></span>                                        |
| <span data-ttu-id="05e57-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05e57-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="05e57-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05e57-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="05e57-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05e57-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="05e57-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05e57-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="05e57-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-171">Search-Flags</span></span>           | <span data-ttu-id="05e57-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e57-172">0x00000000</span></span>                                   |
| <span data-ttu-id="05e57-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-173">System-Flags</span></span>           | <span data-ttu-id="05e57-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05e57-174">0x00000010</span></span>                                   |
| <span data-ttu-id="05e57-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05e57-175">Classes used in</span></span>        | [<span data-ttu-id="05e57-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="05e57-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="05e57-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="05e57-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="05e57-178">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-178">Entry</span></span> | <span data-ttu-id="05e57-179">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="05e57-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05e57-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="05e57-182">System-Only</span></span>            | <span data-ttu-id="05e57-183">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-183">False</span></span>                                        |
| <span data-ttu-id="05e57-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05e57-184">Is-Single-Valued</span></span>       | <span data-ttu-id="05e57-185">Vero</span><span class="sxs-lookup"><span data-stu-id="05e57-185">True</span></span>                                         |
| <span data-ttu-id="05e57-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05e57-186">Is Indexed</span></span>             | <span data-ttu-id="05e57-187">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-187">False</span></span>                                        |
| <span data-ttu-id="05e57-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05e57-188">In Global Catalog</span></span>      | <span data-ttu-id="05e57-189">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-189">False</span></span>                                        |
| <span data-ttu-id="05e57-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05e57-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="05e57-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05e57-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="05e57-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05e57-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="05e57-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05e57-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="05e57-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-194">Search-Flags</span></span>           | <span data-ttu-id="05e57-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e57-195">0x00000000</span></span>                                   |
| <span data-ttu-id="05e57-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-196">System-Flags</span></span>           | <span data-ttu-id="05e57-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05e57-197">0x00000010</span></span>                                   |
| <span data-ttu-id="05e57-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05e57-198">Classes used in</span></span>        | [<span data-ttu-id="05e57-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="05e57-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="05e57-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05e57-200">Windows Server 2008</span></span>



| <span data-ttu-id="05e57-201">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-201">Entry</span></span> | <span data-ttu-id="05e57-202">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="05e57-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05e57-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="05e57-205">System-Only</span></span>            | <span data-ttu-id="05e57-206">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-206">False</span></span>                                        |
| <span data-ttu-id="05e57-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05e57-207">Is-Single-Valued</span></span>       | <span data-ttu-id="05e57-208">Vero</span><span class="sxs-lookup"><span data-stu-id="05e57-208">True</span></span>                                         |
| <span data-ttu-id="05e57-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05e57-209">Is Indexed</span></span>             | <span data-ttu-id="05e57-210">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-210">False</span></span>                                        |
| <span data-ttu-id="05e57-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05e57-211">In Global Catalog</span></span>      | <span data-ttu-id="05e57-212">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-212">False</span></span>                                        |
| <span data-ttu-id="05e57-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05e57-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="05e57-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05e57-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="05e57-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05e57-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="05e57-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05e57-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="05e57-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-217">Search-Flags</span></span>           | <span data-ttu-id="05e57-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e57-218">0x00000000</span></span>                                   |
| <span data-ttu-id="05e57-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-219">System-Flags</span></span>           | <span data-ttu-id="05e57-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05e57-220">0x00000010</span></span>                                   |
| <span data-ttu-id="05e57-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05e57-221">Classes used in</span></span>        | [<span data-ttu-id="05e57-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="05e57-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="05e57-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05e57-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="05e57-224">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-224">Entry</span></span> | <span data-ttu-id="05e57-225">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="05e57-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05e57-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="05e57-228">System-Only</span></span>            | <span data-ttu-id="05e57-229">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-229">False</span></span>                                        |
| <span data-ttu-id="05e57-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05e57-230">Is-Single-Valued</span></span>       | <span data-ttu-id="05e57-231">Vero</span><span class="sxs-lookup"><span data-stu-id="05e57-231">True</span></span>                                         |
| <span data-ttu-id="05e57-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05e57-232">Is Indexed</span></span>             | <span data-ttu-id="05e57-233">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-233">False</span></span>                                        |
| <span data-ttu-id="05e57-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05e57-234">In Global Catalog</span></span>      | <span data-ttu-id="05e57-235">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-235">False</span></span>                                        |
| <span data-ttu-id="05e57-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05e57-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="05e57-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05e57-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="05e57-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05e57-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="05e57-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05e57-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="05e57-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-240">Search-Flags</span></span>           | <span data-ttu-id="05e57-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e57-241">0x00000000</span></span>                                   |
| <span data-ttu-id="05e57-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-242">System-Flags</span></span>           | <span data-ttu-id="05e57-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05e57-243">0x00000010</span></span>                                   |
| <span data-ttu-id="05e57-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05e57-244">Classes used in</span></span>        | [<span data-ttu-id="05e57-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="05e57-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="05e57-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05e57-246">Windows Server 2012</span></span>



| <span data-ttu-id="05e57-247">Voce</span><span class="sxs-lookup"><span data-stu-id="05e57-247">Entry</span></span> | <span data-ttu-id="05e57-248">Valore</span><span class="sxs-lookup"><span data-stu-id="05e57-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="05e57-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="05e57-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05e57-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="05e57-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="05e57-251">System-Only</span></span>            | <span data-ttu-id="05e57-252">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-252">False</span></span>                                        |
| <span data-ttu-id="05e57-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="05e57-253">Is-Single-Valued</span></span>       | <span data-ttu-id="05e57-254">Vero</span><span class="sxs-lookup"><span data-stu-id="05e57-254">True</span></span>                                         |
| <span data-ttu-id="05e57-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="05e57-255">Is Indexed</span></span>             | <span data-ttu-id="05e57-256">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-256">False</span></span>                                        |
| <span data-ttu-id="05e57-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="05e57-257">In Global Catalog</span></span>      | <span data-ttu-id="05e57-258">Falso</span><span class="sxs-lookup"><span data-stu-id="05e57-258">False</span></span>                                        |
| <span data-ttu-id="05e57-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="05e57-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="05e57-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="05e57-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="05e57-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05e57-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="05e57-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05e57-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="05e57-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-263">Search-Flags</span></span>           | <span data-ttu-id="05e57-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e57-264">0x00000000</span></span>                                   |
| <span data-ttu-id="05e57-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05e57-265">System-Flags</span></span>           | <span data-ttu-id="05e57-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="05e57-266">0x00000010</span></span>                                   |
| <span data-ttu-id="05e57-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="05e57-267">Classes used in</span></span>        | [<span data-ttu-id="05e57-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="05e57-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





