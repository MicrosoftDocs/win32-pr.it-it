---
title: Attributo in fase di creazione incorporato
description: Per supportare la replica nei domini di Windows NT 4,0, viene usato l'attributo della fase di creazione incorporato.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo in fase di creazione incorporato
- Schema AD dell'attributo builtinCreationTime
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875849"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="3e5e0-105">Attributo in fase di creazione incorporato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="3e5e0-106">Per supportare la replica nei domini di Windows NT 4,0, viene usato l'attributo della **fase di creazione incorporato** .</span><span class="sxs-lookup"><span data-stu-id="3e5e0-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="3e5e0-107">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-107">Entry</span></span> | <span data-ttu-id="3e5e0-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3e5e0-109">CN</span><span class="sxs-lookup"><span data-stu-id="3e5e0-109">CN</span></span>                | <span data-ttu-id="3e5e0-110">Tempo di creazione predefinito</span><span class="sxs-lookup"><span data-stu-id="3e5e0-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="3e5e0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3e5e0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3e5e0-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="3e5e0-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="3e5e0-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3e5e0-113">Size</span></span>              | <span data-ttu-id="3e5e0-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="3e5e0-114">8 bytes</span></span>                              |
| <span data-ttu-id="3e5e0-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-115">Update Privilege</span></span>  | <span data-ttu-id="3e5e0-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e5e0-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="3e5e0-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3e5e0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-118">Attribute-Id</span></span>      | <span data-ttu-id="3e5e0-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="3e5e0-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="3e5e0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3e5e0-120">System-Id-Guid</span></span>    | <span data-ttu-id="3e5e0-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3e5e0-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3e5e0-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e5e0-122">Syntax</span></span>            | [<span data-ttu-id="3e5e0-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="3e5e0-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3e5e0-124">Implementations</span></span>

-   [<span data-ttu-id="3e5e0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3e5e0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e5e0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e5e0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e5e0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e5e0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3e5e0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e5e0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3e5e0-132">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-132">Entry</span></span> | <span data-ttu-id="3e5e0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e5e0-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5e0-136">System-Only</span></span>            | <span data-ttu-id="3e5e0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-137">False</span></span>                                        |
| <span data-ttu-id="3e5e0-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3e5e0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5e0-139">Vero</span><span class="sxs-lookup"><span data-stu-id="3e5e0-139">True</span></span>                                         |
| <span data-ttu-id="3e5e0-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-140">Is Indexed</span></span>             | <span data-ttu-id="3e5e0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-141">False</span></span>                                        |
| <span data-ttu-id="3e5e0-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3e5e0-142">In Global Catalog</span></span>      | <span data-ttu-id="3e5e0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-143">False</span></span>                                        |
| <span data-ttu-id="3e5e0-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5e0-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3e5e0-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e5e0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5e0-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5e0-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-148">Search-Flags</span></span>           | <span data-ttu-id="3e5e0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5e0-149">0x00000000</span></span>                                   |
| <span data-ttu-id="3e5e0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-150">System-Flags</span></span>           | <span data-ttu-id="3e5e0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5e0-151">0x00000010</span></span>                                   |
| <span data-ttu-id="3e5e0-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3e5e0-152">Classes used in</span></span>        | [<span data-ttu-id="3e5e0-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3e5e0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e5e0-154">Windows Server 2003</span></span>



| <span data-ttu-id="3e5e0-155">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-155">Entry</span></span> | <span data-ttu-id="3e5e0-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e5e0-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5e0-159">System-Only</span></span>            | <span data-ttu-id="3e5e0-160">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-160">False</span></span>                                        |
| <span data-ttu-id="3e5e0-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3e5e0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5e0-162">Vero</span><span class="sxs-lookup"><span data-stu-id="3e5e0-162">True</span></span>                                         |
| <span data-ttu-id="3e5e0-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-163">Is Indexed</span></span>             | <span data-ttu-id="3e5e0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-164">False</span></span>                                        |
| <span data-ttu-id="3e5e0-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3e5e0-165">In Global Catalog</span></span>      | <span data-ttu-id="3e5e0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-166">False</span></span>                                        |
| <span data-ttu-id="3e5e0-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5e0-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3e5e0-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e5e0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5e0-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5e0-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-171">Search-Flags</span></span>           | <span data-ttu-id="3e5e0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5e0-172">0x00000000</span></span>                                   |
| <span data-ttu-id="3e5e0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-173">System-Flags</span></span>           | <span data-ttu-id="3e5e0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5e0-174">0x00000010</span></span>                                   |
| <span data-ttu-id="3e5e0-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3e5e0-175">Classes used in</span></span>        | [<span data-ttu-id="3e5e0-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e5e0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e5e0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e5e0-178">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-178">Entry</span></span> | <span data-ttu-id="3e5e0-179">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e5e0-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5e0-182">System-Only</span></span>            | <span data-ttu-id="3e5e0-183">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-183">False</span></span>                                        |
| <span data-ttu-id="3e5e0-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3e5e0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5e0-185">Vero</span><span class="sxs-lookup"><span data-stu-id="3e5e0-185">True</span></span>                                         |
| <span data-ttu-id="3e5e0-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-186">Is Indexed</span></span>             | <span data-ttu-id="3e5e0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-187">False</span></span>                                        |
| <span data-ttu-id="3e5e0-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3e5e0-188">In Global Catalog</span></span>      | <span data-ttu-id="3e5e0-189">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-189">False</span></span>                                        |
| <span data-ttu-id="3e5e0-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5e0-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3e5e0-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e5e0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5e0-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5e0-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-194">Search-Flags</span></span>           | <span data-ttu-id="3e5e0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5e0-195">0x00000000</span></span>                                   |
| <span data-ttu-id="3e5e0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-196">System-Flags</span></span>           | <span data-ttu-id="3e5e0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5e0-197">0x00000010</span></span>                                   |
| <span data-ttu-id="3e5e0-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3e5e0-198">Classes used in</span></span>        | [<span data-ttu-id="3e5e0-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e5e0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e5e0-200">Windows Server 2008</span></span>



| <span data-ttu-id="3e5e0-201">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-201">Entry</span></span> | <span data-ttu-id="3e5e0-202">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e5e0-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5e0-205">System-Only</span></span>            | <span data-ttu-id="3e5e0-206">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-206">False</span></span>                                        |
| <span data-ttu-id="3e5e0-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3e5e0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5e0-208">Vero</span><span class="sxs-lookup"><span data-stu-id="3e5e0-208">True</span></span>                                         |
| <span data-ttu-id="3e5e0-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-209">Is Indexed</span></span>             | <span data-ttu-id="3e5e0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-210">False</span></span>                                        |
| <span data-ttu-id="3e5e0-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3e5e0-211">In Global Catalog</span></span>      | <span data-ttu-id="3e5e0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-212">False</span></span>                                        |
| <span data-ttu-id="3e5e0-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5e0-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3e5e0-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e5e0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5e0-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5e0-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-217">Search-Flags</span></span>           | <span data-ttu-id="3e5e0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5e0-218">0x00000000</span></span>                                   |
| <span data-ttu-id="3e5e0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-219">System-Flags</span></span>           | <span data-ttu-id="3e5e0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5e0-220">0x00000010</span></span>                                   |
| <span data-ttu-id="3e5e0-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3e5e0-221">Classes used in</span></span>        | [<span data-ttu-id="3e5e0-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e5e0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e5e0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e5e0-224">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-224">Entry</span></span> | <span data-ttu-id="3e5e0-225">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e5e0-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5e0-228">System-Only</span></span>            | <span data-ttu-id="3e5e0-229">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-229">False</span></span>                                        |
| <span data-ttu-id="3e5e0-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3e5e0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5e0-231">Vero</span><span class="sxs-lookup"><span data-stu-id="3e5e0-231">True</span></span>                                         |
| <span data-ttu-id="3e5e0-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-232">Is Indexed</span></span>             | <span data-ttu-id="3e5e0-233">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-233">False</span></span>                                        |
| <span data-ttu-id="3e5e0-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3e5e0-234">In Global Catalog</span></span>      | <span data-ttu-id="3e5e0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-235">False</span></span>                                        |
| <span data-ttu-id="3e5e0-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5e0-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3e5e0-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e5e0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5e0-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5e0-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-240">Search-Flags</span></span>           | <span data-ttu-id="3e5e0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5e0-241">0x00000000</span></span>                                   |
| <span data-ttu-id="3e5e0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-242">System-Flags</span></span>           | <span data-ttu-id="3e5e0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5e0-243">0x00000010</span></span>                                   |
| <span data-ttu-id="3e5e0-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3e5e0-244">Classes used in</span></span>        | [<span data-ttu-id="3e5e0-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e5e0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e5e0-246">Windows Server 2012</span></span>



| <span data-ttu-id="3e5e0-247">Voce</span><span class="sxs-lookup"><span data-stu-id="3e5e0-247">Entry</span></span> | <span data-ttu-id="3e5e0-248">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="3e5e0-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3e5e0-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5e0-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="3e5e0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5e0-251">System-Only</span></span>            | <span data-ttu-id="3e5e0-252">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-252">False</span></span>                                        |
| <span data-ttu-id="3e5e0-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3e5e0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5e0-254">Vero</span><span class="sxs-lookup"><span data-stu-id="3e5e0-254">True</span></span>                                         |
| <span data-ttu-id="3e5e0-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3e5e0-255">Is Indexed</span></span>             | <span data-ttu-id="3e5e0-256">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-256">False</span></span>                                        |
| <span data-ttu-id="3e5e0-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3e5e0-257">In Global Catalog</span></span>      | <span data-ttu-id="3e5e0-258">Falso</span><span class="sxs-lookup"><span data-stu-id="3e5e0-258">False</span></span>                                        |
| <span data-ttu-id="3e5e0-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3e5e0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5e0-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3e5e0-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="3e5e0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5e0-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5e0-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="3e5e0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-263">Search-Flags</span></span>           | <span data-ttu-id="3e5e0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5e0-264">0x00000000</span></span>                                   |
| <span data-ttu-id="3e5e0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5e0-265">System-Flags</span></span>           | <span data-ttu-id="3e5e0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5e0-266">0x00000010</span></span>                                   |
| <span data-ttu-id="3e5e0-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3e5e0-267">Classes used in</span></span>        | [<span data-ttu-id="3e5e0-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="3e5e0-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





