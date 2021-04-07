---
title: Attributo Last-Backup-restorment-Time
description: Quando si è verificato l'ultimo ripristino del sistema.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Last-Backup-restorment-Time
- Schema AD dell'attributo lastBackupRestorationTime
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104048792"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="c882d-105">Attributo Last-Backup-restorment-Time</span><span class="sxs-lookup"><span data-stu-id="c882d-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="c882d-106">Quando si è verificato l'ultimo ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="c882d-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="c882d-107">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-107">Entry</span></span> | <span data-ttu-id="c882d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c882d-109">CN</span><span class="sxs-lookup"><span data-stu-id="c882d-109">CN</span></span>                | <span data-ttu-id="c882d-110">Ultimo backup-tempo di ripristino</span><span class="sxs-lookup"><span data-stu-id="c882d-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="c882d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c882d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c882d-112">lastBackupRestorationTime</span><span class="sxs-lookup"><span data-stu-id="c882d-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="c882d-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c882d-113">Size</span></span>              | <span data-ttu-id="c882d-114">8 byte</span><span class="sxs-lookup"><span data-stu-id="c882d-114">8 bytes</span></span>                              |
| <span data-ttu-id="c882d-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c882d-115">Update Privilege</span></span>  | <span data-ttu-id="c882d-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c882d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="c882d-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c882d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c882d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-118">Attribute-Id</span></span>      | <span data-ttu-id="c882d-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="c882d-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="c882d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c882d-120">System-Id-Guid</span></span>    | <span data-ttu-id="c882d-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c882d-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="c882d-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c882d-122">Syntax</span></span>            | [<span data-ttu-id="c882d-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c882d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c882d-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c882d-124">Implementations</span></span>

-   [<span data-ttu-id="c882d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c882d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c882d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c882d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c882d-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c882d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c882d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c882d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c882d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c882d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c882d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c882d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c882d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c882d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c882d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c882d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c882d-133">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-133">Entry</span></span> | <span data-ttu-id="c882d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-137">System-Only</span></span>            | <span data-ttu-id="c882d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-138">False</span></span>                                    |
| <span data-ttu-id="c882d-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-140">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-140">True</span></span>                                     |
| <span data-ttu-id="c882d-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-141">Is Indexed</span></span>             | <span data-ttu-id="c882d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-142">False</span></span>                                    |
| <span data-ttu-id="c882d-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-143">In Global Catalog</span></span>      | <span data-ttu-id="c882d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-144">False</span></span>                                    |
| <span data-ttu-id="c882d-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-149">Search-Flags</span></span>           | <span data-ttu-id="c882d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-150">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-151">System-Flags</span></span>           | <span data-ttu-id="c882d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-152">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-153">Classes used in</span></span>        | [<span data-ttu-id="c882d-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c882d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c882d-155">Windows Server 2003</span></span>



| <span data-ttu-id="c882d-156">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-156">Entry</span></span> | <span data-ttu-id="c882d-157">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-160">System-Only</span></span>            | <span data-ttu-id="c882d-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-161">False</span></span>                                    |
| <span data-ttu-id="c882d-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-163">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-163">True</span></span>                                     |
| <span data-ttu-id="c882d-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-164">Is Indexed</span></span>             | <span data-ttu-id="c882d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-165">False</span></span>                                    |
| <span data-ttu-id="c882d-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-166">In Global Catalog</span></span>      | <span data-ttu-id="c882d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-167">False</span></span>                                    |
| <span data-ttu-id="c882d-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-172">Search-Flags</span></span>           | <span data-ttu-id="c882d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-173">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-174">System-Flags</span></span>           | <span data-ttu-id="c882d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-175">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-176">Classes used in</span></span>        | [<span data-ttu-id="c882d-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c882d-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="c882d-178">ADAM</span></span>



| <span data-ttu-id="c882d-179">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-179">Entry</span></span> | <span data-ttu-id="c882d-180">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-183">System-Only</span></span>            | <span data-ttu-id="c882d-184">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-184">False</span></span>                                    |
| <span data-ttu-id="c882d-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-186">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-186">True</span></span>                                     |
| <span data-ttu-id="c882d-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-187">Is Indexed</span></span>             | <span data-ttu-id="c882d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-188">False</span></span>                                    |
| <span data-ttu-id="c882d-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-189">In Global Catalog</span></span>      | <span data-ttu-id="c882d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-190">False</span></span>                                    |
| <span data-ttu-id="c882d-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-195">Search-Flags</span></span>           | <span data-ttu-id="c882d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-196">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-197">System-Flags</span></span>           | <span data-ttu-id="c882d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-198">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-199">Classes used in</span></span>        | [<span data-ttu-id="c882d-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c882d-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c882d-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c882d-202">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-202">Entry</span></span> | <span data-ttu-id="c882d-203">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-206">System-Only</span></span>            | <span data-ttu-id="c882d-207">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-207">False</span></span>                                    |
| <span data-ttu-id="c882d-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-209">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-209">True</span></span>                                     |
| <span data-ttu-id="c882d-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-210">Is Indexed</span></span>             | <span data-ttu-id="c882d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-211">False</span></span>                                    |
| <span data-ttu-id="c882d-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-212">In Global Catalog</span></span>      | <span data-ttu-id="c882d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-213">False</span></span>                                    |
| <span data-ttu-id="c882d-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-218">Search-Flags</span></span>           | <span data-ttu-id="c882d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-219">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-220">System-Flags</span></span>           | <span data-ttu-id="c882d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-221">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-222">Classes used in</span></span>        | [<span data-ttu-id="c882d-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c882d-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c882d-224">Windows Server 2008</span></span>



| <span data-ttu-id="c882d-225">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-225">Entry</span></span> | <span data-ttu-id="c882d-226">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-229">System-Only</span></span>            | <span data-ttu-id="c882d-230">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-230">False</span></span>                                    |
| <span data-ttu-id="c882d-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-232">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-232">True</span></span>                                     |
| <span data-ttu-id="c882d-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-233">Is Indexed</span></span>             | <span data-ttu-id="c882d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-234">False</span></span>                                    |
| <span data-ttu-id="c882d-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-235">In Global Catalog</span></span>      | <span data-ttu-id="c882d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-236">False</span></span>                                    |
| <span data-ttu-id="c882d-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-241">Search-Flags</span></span>           | <span data-ttu-id="c882d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-242">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-243">System-Flags</span></span>           | <span data-ttu-id="c882d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-244">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-245">Classes used in</span></span>        | [<span data-ttu-id="c882d-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c882d-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c882d-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c882d-248">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-248">Entry</span></span> | <span data-ttu-id="c882d-249">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-252">System-Only</span></span>            | <span data-ttu-id="c882d-253">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-253">False</span></span>                                    |
| <span data-ttu-id="c882d-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-255">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-255">True</span></span>                                     |
| <span data-ttu-id="c882d-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-256">Is Indexed</span></span>             | <span data-ttu-id="c882d-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-257">False</span></span>                                    |
| <span data-ttu-id="c882d-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-258">In Global Catalog</span></span>      | <span data-ttu-id="c882d-259">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-259">False</span></span>                                    |
| <span data-ttu-id="c882d-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-264">Search-Flags</span></span>           | <span data-ttu-id="c882d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-265">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-266">System-Flags</span></span>           | <span data-ttu-id="c882d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-267">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-268">Classes used in</span></span>        | [<span data-ttu-id="c882d-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c882d-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c882d-270">Windows Server 2012</span></span>



| <span data-ttu-id="c882d-271">Voce</span><span class="sxs-lookup"><span data-stu-id="c882d-271">Entry</span></span> | <span data-ttu-id="c882d-272">Valore</span><span class="sxs-lookup"><span data-stu-id="c882d-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c882d-273">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c882d-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c882d-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c882d-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="c882d-275">System-Only</span></span>            | <span data-ttu-id="c882d-276">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-276">False</span></span>                                    |
| <span data-ttu-id="c882d-277">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c882d-277">Is-Single-Valued</span></span>       | <span data-ttu-id="c882d-278">Vero</span><span class="sxs-lookup"><span data-stu-id="c882d-278">True</span></span>                                     |
| <span data-ttu-id="c882d-279">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c882d-279">Is Indexed</span></span>             | <span data-ttu-id="c882d-280">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-280">False</span></span>                                    |
| <span data-ttu-id="c882d-281">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c882d-281">In Global Catalog</span></span>      | <span data-ttu-id="c882d-282">Falso</span><span class="sxs-lookup"><span data-stu-id="c882d-282">False</span></span>                                    |
| <span data-ttu-id="c882d-283">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c882d-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="c882d-284">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c882d-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c882d-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c882d-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c882d-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c882d-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c882d-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-287">Search-Flags</span></span>           | <span data-ttu-id="c882d-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c882d-288">0x00000000</span></span>                               |
| <span data-ttu-id="c882d-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c882d-289">System-Flags</span></span>           | <span data-ttu-id="c882d-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c882d-290">0x00000010</span></span>                               |
| <span data-ttu-id="c882d-291">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c882d-291">Classes used in</span></span>        | [<span data-ttu-id="c882d-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c882d-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





