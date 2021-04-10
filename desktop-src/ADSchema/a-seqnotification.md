---
title: Attributo Seq-Notification
description: Questo attributo contiene un contatore che viene incrementato quotidianamente. Questo valore del contatore viene assegnato al servizio di rilevamento dei collegamenti che aggiunge il valore ai volumi e i file di origine del collegamento quando vengono aggiornati. Il controller di dominio mantiene questo valore.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Schema AD Seq-Notification attribute
- Schema AD dell'attributo seqNotification
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122342"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="9ea6d-107">Attributo Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="9ea6d-107">Seq-Notification attribute</span></span>

<span data-ttu-id="9ea6d-108">Questo attributo contiene un contatore che viene incrementato quotidianamente.</span><span class="sxs-lookup"><span data-stu-id="9ea6d-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="9ea6d-109">Questo valore del contatore viene assegnato al servizio di rilevamento dei collegamenti che aggiunge il valore ai volumi e i file di origine del collegamento quando vengono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="9ea6d-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="9ea6d-110">Il controller di dominio mantiene questo valore.</span><span class="sxs-lookup"><span data-stu-id="9ea6d-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="9ea6d-111">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-111">Entry</span></span> | <span data-ttu-id="9ea6d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9ea6d-113">CN</span><span class="sxs-lookup"><span data-stu-id="9ea6d-113">CN</span></span>                | <span data-ttu-id="9ea6d-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="9ea6d-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="9ea6d-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9ea6d-115">Ldap-Display-Name</span></span> | <span data-ttu-id="9ea6d-116">seqNotification</span><span class="sxs-lookup"><span data-stu-id="9ea6d-116">seqNotification</span></span>                      |
| <span data-ttu-id="9ea6d-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9ea6d-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="9ea6d-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9ea6d-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9ea6d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-120">Attribute-Id</span></span>      | <span data-ttu-id="9ea6d-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="9ea6d-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="9ea6d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9ea6d-122">System-Id-Guid</span></span>    | <span data-ttu-id="9ea6d-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9ea6d-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="9ea6d-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ea6d-124">Syntax</span></span>            | [<span data-ttu-id="9ea6d-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9ea6d-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9ea6d-126">Implementations</span></span>

-   [<span data-ttu-id="9ea6d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9ea6d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ea6d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ea6d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ea6d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ea6d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9ea6d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ea6d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9ea6d-134">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-134">Entry</span></span> | <span data-ttu-id="9ea6d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ea6d-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ea6d-138">System-Only</span></span>            | <span data-ttu-id="9ea6d-139">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-139">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9ea6d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9ea6d-141">Vero</span><span class="sxs-lookup"><span data-stu-id="9ea6d-141">True</span></span>                                                           |
| <span data-ttu-id="9ea6d-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9ea6d-142">Is Indexed</span></span>             | <span data-ttu-id="9ea6d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-143">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9ea6d-144">In Global Catalog</span></span>      | <span data-ttu-id="9ea6d-145">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-145">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ea6d-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9ea6d-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9ea6d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ea6d-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ea6d-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-150">Search-Flags</span></span>           | <span data-ttu-id="9ea6d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ea6d-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="9ea6d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-152">System-Flags</span></span>           | <span data-ttu-id="9ea6d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ea6d-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="9ea6d-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9ea6d-154">Classes used in</span></span>        | [<span data-ttu-id="9ea6d-155">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9ea6d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ea6d-156">Windows Server 2003</span></span>



| <span data-ttu-id="9ea6d-157">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-157">Entry</span></span> | <span data-ttu-id="9ea6d-158">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ea6d-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ea6d-161">System-Only</span></span>            | <span data-ttu-id="9ea6d-162">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-162">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9ea6d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9ea6d-164">Vero</span><span class="sxs-lookup"><span data-stu-id="9ea6d-164">True</span></span>                                                           |
| <span data-ttu-id="9ea6d-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9ea6d-165">Is Indexed</span></span>             | <span data-ttu-id="9ea6d-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-166">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9ea6d-167">In Global Catalog</span></span>      | <span data-ttu-id="9ea6d-168">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-168">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ea6d-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9ea6d-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9ea6d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ea6d-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ea6d-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-173">Search-Flags</span></span>           | <span data-ttu-id="9ea6d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ea6d-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="9ea6d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-175">System-Flags</span></span>           | <span data-ttu-id="9ea6d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ea6d-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="9ea6d-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9ea6d-177">Classes used in</span></span>        | [<span data-ttu-id="9ea6d-178">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ea6d-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ea6d-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ea6d-180">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-180">Entry</span></span> | <span data-ttu-id="9ea6d-181">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ea6d-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ea6d-184">System-Only</span></span>            | <span data-ttu-id="9ea6d-185">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-185">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9ea6d-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9ea6d-187">Vero</span><span class="sxs-lookup"><span data-stu-id="9ea6d-187">True</span></span>                                                           |
| <span data-ttu-id="9ea6d-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9ea6d-188">Is Indexed</span></span>             | <span data-ttu-id="9ea6d-189">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-189">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9ea6d-190">In Global Catalog</span></span>      | <span data-ttu-id="9ea6d-191">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-191">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ea6d-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9ea6d-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9ea6d-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ea6d-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ea6d-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-196">Search-Flags</span></span>           | <span data-ttu-id="9ea6d-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ea6d-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="9ea6d-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-198">System-Flags</span></span>           | <span data-ttu-id="9ea6d-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ea6d-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="9ea6d-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9ea6d-200">Classes used in</span></span>        | [<span data-ttu-id="9ea6d-201">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ea6d-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ea6d-202">Windows Server 2008</span></span>



| <span data-ttu-id="9ea6d-203">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-203">Entry</span></span> | <span data-ttu-id="9ea6d-204">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ea6d-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ea6d-207">System-Only</span></span>            | <span data-ttu-id="9ea6d-208">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-208">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9ea6d-209">Is-Single-Valued</span></span>       | <span data-ttu-id="9ea6d-210">Vero</span><span class="sxs-lookup"><span data-stu-id="9ea6d-210">True</span></span>                                                           |
| <span data-ttu-id="9ea6d-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9ea6d-211">Is Indexed</span></span>             | <span data-ttu-id="9ea6d-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-212">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9ea6d-213">In Global Catalog</span></span>      | <span data-ttu-id="9ea6d-214">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-214">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ea6d-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9ea6d-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9ea6d-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ea6d-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ea6d-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-219">Search-Flags</span></span>           | <span data-ttu-id="9ea6d-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ea6d-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="9ea6d-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-221">System-Flags</span></span>           | <span data-ttu-id="9ea6d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ea6d-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="9ea6d-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9ea6d-223">Classes used in</span></span>        | [<span data-ttu-id="9ea6d-224">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ea6d-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ea6d-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ea6d-226">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-226">Entry</span></span> | <span data-ttu-id="9ea6d-227">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ea6d-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ea6d-230">System-Only</span></span>            | <span data-ttu-id="9ea6d-231">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-231">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9ea6d-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9ea6d-233">Vero</span><span class="sxs-lookup"><span data-stu-id="9ea6d-233">True</span></span>                                                           |
| <span data-ttu-id="9ea6d-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9ea6d-234">Is Indexed</span></span>             | <span data-ttu-id="9ea6d-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-235">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9ea6d-236">In Global Catalog</span></span>      | <span data-ttu-id="9ea6d-237">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-237">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ea6d-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9ea6d-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9ea6d-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ea6d-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ea6d-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-242">Search-Flags</span></span>           | <span data-ttu-id="9ea6d-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ea6d-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="9ea6d-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-244">System-Flags</span></span>           | <span data-ttu-id="9ea6d-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ea6d-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="9ea6d-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9ea6d-246">Classes used in</span></span>        | [<span data-ttu-id="9ea6d-247">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ea6d-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ea6d-248">Windows Server 2012</span></span>



| <span data-ttu-id="9ea6d-249">Voce</span><span class="sxs-lookup"><span data-stu-id="9ea6d-249">Entry</span></span> | <span data-ttu-id="9ea6d-250">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ea6d-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9ea6d-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ea6d-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9ea6d-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ea6d-253">System-Only</span></span>            | <span data-ttu-id="9ea6d-254">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-254">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9ea6d-255">Is-Single-Valued</span></span>       | <span data-ttu-id="9ea6d-256">Vero</span><span class="sxs-lookup"><span data-stu-id="9ea6d-256">True</span></span>                                                           |
| <span data-ttu-id="9ea6d-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9ea6d-257">Is Indexed</span></span>             | <span data-ttu-id="9ea6d-258">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-258">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9ea6d-259">In Global Catalog</span></span>      | <span data-ttu-id="9ea6d-260">Falso</span><span class="sxs-lookup"><span data-stu-id="9ea6d-260">False</span></span>                                                          |
| <span data-ttu-id="9ea6d-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9ea6d-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ea6d-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9ea6d-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9ea6d-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ea6d-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ea6d-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9ea6d-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-265">Search-Flags</span></span>           | <span data-ttu-id="9ea6d-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ea6d-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="9ea6d-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ea6d-267">System-Flags</span></span>           | <span data-ttu-id="9ea6d-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ea6d-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="9ea6d-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9ea6d-269">Classes used in</span></span>        | [<span data-ttu-id="9ea6d-270">**Link-Track-vol-entry**</span><span class="sxs-lookup"><span data-stu-id="9ea6d-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





