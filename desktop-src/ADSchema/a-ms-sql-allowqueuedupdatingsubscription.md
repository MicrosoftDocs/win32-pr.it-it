---
title: Attributo MS-SQL-AllowQueuedUpdatingSubscription
description: True per consentire le transazioni in coda durante l'aggiornamento delle sottoscrizioni.
ms.assetid: 132c107f-8586-48db-b70c-027c619aadf7
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-AllowQueuedUpdatingSubscription
- Schema AD dell'attributo mS-SQL-AllowQueuedUpdatingSubscription
topic_type:
- apiref
api_name:
- MS-SQL-AllowQueuedUpdatingSubscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2056a04b6e0f155c156cde06975e96eb13f61eb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874937"
---
# <a name="ms-sql-allowqueuedupdatingsubscription-attribute"></a><span data-ttu-id="ea7b3-105">Attributo MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="ea7b3-105">MS-SQL-AllowQueuedUpdatingSubscription attribute</span></span>

<span data-ttu-id="ea7b3-106">True per consentire le transazioni in coda durante l'aggiornamento delle sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-106">True to allow queued transactions when updating subscriptions.</span></span>



| <span data-ttu-id="ea7b3-107">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-107">Entry</span></span> | <span data-ttu-id="ea7b3-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="ea7b3-109">CN</span><span class="sxs-lookup"><span data-stu-id="ea7b3-109">CN</span></span>                | <span data-ttu-id="ea7b3-110">MS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="ea7b3-110">MS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="ea7b3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ea7b3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ea7b3-112">mS-SQL-AllowQueuedUpdatingSubscription</span><span class="sxs-lookup"><span data-stu-id="ea7b3-112">mS-SQL-AllowQueuedUpdatingSubscription</span></span> |
| <span data-ttu-id="ea7b3-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ea7b3-113">Size</span></span>              | <span data-ttu-id="ea7b3-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="ea7b3-114">4 bytes</span></span>                                |
| <span data-ttu-id="ea7b3-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-115">Update Privilege</span></span>  | <span data-ttu-id="ea7b3-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-116">This value is set by the system.</span></span>       |
| <span data-ttu-id="ea7b3-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-117">Update Frequency</span></span>  | <span data-ttu-id="ea7b3-118">Quando la replica è impostata.</span><span class="sxs-lookup"><span data-stu-id="ea7b3-118">When replication is setup.</span></span>             |
| <span data-ttu-id="ea7b3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-119">Attribute-Id</span></span>      | <span data-ttu-id="ea7b3-120">1.2.840.113556.1.4.1405</span><span class="sxs-lookup"><span data-stu-id="ea7b3-120">1.2.840.113556.1.4.1405</span></span>                |
| <span data-ttu-id="ea7b3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ea7b3-121">System-Id-Guid</span></span>    | <span data-ttu-id="ea7b3-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ea7b3-122">c458ca80-d34b-11d2-999a-0000f87a57d4</span></span>   |
| <span data-ttu-id="ea7b3-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea7b3-123">Syntax</span></span>            | [<span data-ttu-id="ea7b3-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-124">**Boolean**</span></span>](s-boolean.md)           |



## <a name="implementations"></a><span data-ttu-id="ea7b3-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ea7b3-125">Implementations</span></span>

-   [<span data-ttu-id="ea7b3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ea7b3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ea7b3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ea7b3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ea7b3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ea7b3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ea7b3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea7b3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ea7b3-133">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-133">Entry</span></span> | <span data-ttu-id="ea7b3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea7b3-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea7b3-137">System-Only</span></span>            | <span data-ttu-id="ea7b3-138">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-138">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea7b3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ea7b3-140">Vero</span><span class="sxs-lookup"><span data-stu-id="ea7b3-140">True</span></span>                                                                |
| <span data-ttu-id="ea7b3-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea7b3-141">Is Indexed</span></span>             | <span data-ttu-id="ea7b3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-142">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea7b3-143">In Global Catalog</span></span>      | <span data-ttu-id="ea7b3-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-144">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea7b3-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea7b3-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ea7b3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea7b3-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea7b3-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-149">Search-Flags</span></span>           | <span data-ttu-id="ea7b3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea7b3-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="ea7b3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-151">System-Flags</span></span>           | <span data-ttu-id="ea7b3-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea7b3-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="ea7b3-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea7b3-153">Classes used in</span></span>        | [<span data-ttu-id="ea7b3-154">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-154">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ea7b3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea7b3-155">Windows Server 2003</span></span>



| <span data-ttu-id="ea7b3-156">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-156">Entry</span></span> | <span data-ttu-id="ea7b3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea7b3-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea7b3-160">System-Only</span></span>            | <span data-ttu-id="ea7b3-161">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-161">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea7b3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ea7b3-163">Vero</span><span class="sxs-lookup"><span data-stu-id="ea7b3-163">True</span></span>                                                                |
| <span data-ttu-id="ea7b3-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea7b3-164">Is Indexed</span></span>             | <span data-ttu-id="ea7b3-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-165">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea7b3-166">In Global Catalog</span></span>      | <span data-ttu-id="ea7b3-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-167">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea7b3-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea7b3-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ea7b3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea7b3-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea7b3-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-172">Search-Flags</span></span>           | <span data-ttu-id="ea7b3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea7b3-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="ea7b3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-174">System-Flags</span></span>           | <span data-ttu-id="ea7b3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea7b3-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="ea7b3-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea7b3-176">Classes used in</span></span>        | [<span data-ttu-id="ea7b3-177">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-177">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ea7b3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ea7b3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ea7b3-179">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-179">Entry</span></span> | <span data-ttu-id="ea7b3-180">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea7b3-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea7b3-183">System-Only</span></span>            | <span data-ttu-id="ea7b3-184">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-184">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea7b3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ea7b3-186">Vero</span><span class="sxs-lookup"><span data-stu-id="ea7b3-186">True</span></span>                                                                |
| <span data-ttu-id="ea7b3-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea7b3-187">Is Indexed</span></span>             | <span data-ttu-id="ea7b3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-188">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea7b3-189">In Global Catalog</span></span>      | <span data-ttu-id="ea7b3-190">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-190">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea7b3-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea7b3-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ea7b3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea7b3-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea7b3-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-195">Search-Flags</span></span>           | <span data-ttu-id="ea7b3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea7b3-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="ea7b3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-197">System-Flags</span></span>           | <span data-ttu-id="ea7b3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea7b3-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="ea7b3-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea7b3-199">Classes used in</span></span>        | [<span data-ttu-id="ea7b3-200">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-200">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ea7b3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea7b3-201">Windows Server 2008</span></span>



| <span data-ttu-id="ea7b3-202">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-202">Entry</span></span> | <span data-ttu-id="ea7b3-203">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea7b3-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea7b3-206">System-Only</span></span>            | <span data-ttu-id="ea7b3-207">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-207">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea7b3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ea7b3-209">Vero</span><span class="sxs-lookup"><span data-stu-id="ea7b3-209">True</span></span>                                                                |
| <span data-ttu-id="ea7b3-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea7b3-210">Is Indexed</span></span>             | <span data-ttu-id="ea7b3-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-211">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea7b3-212">In Global Catalog</span></span>      | <span data-ttu-id="ea7b3-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-213">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea7b3-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea7b3-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ea7b3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea7b3-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea7b3-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-218">Search-Flags</span></span>           | <span data-ttu-id="ea7b3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea7b3-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="ea7b3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-220">System-Flags</span></span>           | <span data-ttu-id="ea7b3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea7b3-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="ea7b3-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea7b3-222">Classes used in</span></span>        | [<span data-ttu-id="ea7b3-223">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-223">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ea7b3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea7b3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ea7b3-225">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-225">Entry</span></span> | <span data-ttu-id="ea7b3-226">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea7b3-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea7b3-229">System-Only</span></span>            | <span data-ttu-id="ea7b3-230">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-230">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea7b3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ea7b3-232">Vero</span><span class="sxs-lookup"><span data-stu-id="ea7b3-232">True</span></span>                                                                |
| <span data-ttu-id="ea7b3-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea7b3-233">Is Indexed</span></span>             | <span data-ttu-id="ea7b3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-234">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea7b3-235">In Global Catalog</span></span>      | <span data-ttu-id="ea7b3-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-236">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea7b3-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea7b3-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ea7b3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea7b3-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea7b3-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-241">Search-Flags</span></span>           | <span data-ttu-id="ea7b3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea7b3-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="ea7b3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-243">System-Flags</span></span>           | <span data-ttu-id="ea7b3-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea7b3-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="ea7b3-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea7b3-245">Classes used in</span></span>        | [<span data-ttu-id="ea7b3-246">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-246">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ea7b3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea7b3-247">Windows Server 2012</span></span>



| <span data-ttu-id="ea7b3-248">Voce</span><span class="sxs-lookup"><span data-stu-id="ea7b3-248">Entry</span></span> | <span data-ttu-id="ea7b3-249">Valore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea7b3-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ea7b3-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea7b3-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ea7b3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea7b3-252">System-Only</span></span>            | <span data-ttu-id="ea7b3-253">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-253">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ea7b3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ea7b3-255">Vero</span><span class="sxs-lookup"><span data-stu-id="ea7b3-255">True</span></span>                                                                |
| <span data-ttu-id="ea7b3-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ea7b3-256">Is Indexed</span></span>             | <span data-ttu-id="ea7b3-257">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-257">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ea7b3-258">In Global Catalog</span></span>      | <span data-ttu-id="ea7b3-259">Falso</span><span class="sxs-lookup"><span data-stu-id="ea7b3-259">False</span></span>                                                               |
| <span data-ttu-id="ea7b3-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ea7b3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea7b3-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ea7b3-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ea7b3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea7b3-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea7b3-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ea7b3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-264">Search-Flags</span></span>           | <span data-ttu-id="ea7b3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea7b3-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="ea7b3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea7b3-266">System-Flags</span></span>           | <span data-ttu-id="ea7b3-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea7b3-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="ea7b3-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ea7b3-268">Classes used in</span></span>        | [<span data-ttu-id="ea7b3-269">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ea7b3-269">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





