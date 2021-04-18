---
title: Attributo cluster MS-SQL
description: True se il server è di tipo cluster.
ms.assetid: 066609a4-fdf1-422b-9b26-445f617c99d4
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo cluster MS-SQL-cluster
- Schema AD dell'attributo cluster mS-SQL-cluster
topic_type:
- apiref
api_name:
- MS-SQL-Clustered
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ba701168f3dff5b3809818a6df987855a08e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302980"
---
# <a name="ms-sql-clustered-attribute"></a><span data-ttu-id="71b77-105">Attributo cluster MS-SQL</span><span class="sxs-lookup"><span data-stu-id="71b77-105">MS-SQL-Clustered attribute</span></span>

<span data-ttu-id="71b77-106">True se il server è di tipo cluster.</span><span class="sxs-lookup"><span data-stu-id="71b77-106">True if the server is clustered.</span></span>



| <span data-ttu-id="71b77-107">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-107">Entry</span></span> | <span data-ttu-id="71b77-108">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="71b77-109">CN</span><span class="sxs-lookup"><span data-stu-id="71b77-109">CN</span></span>                | <span data-ttu-id="71b77-110">MS-SQL-cluster</span><span class="sxs-lookup"><span data-stu-id="71b77-110">MS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="71b77-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="71b77-111">Ldap-Display-Name</span></span> | <span data-ttu-id="71b77-112">mS-SQL-cluster</span><span class="sxs-lookup"><span data-stu-id="71b77-112">mS-SQL-Clustered</span></span>                     |
| <span data-ttu-id="71b77-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="71b77-113">Size</span></span>              | <span data-ttu-id="71b77-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="71b77-114">4 bytes</span></span>                              |
| <span data-ttu-id="71b77-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="71b77-115">Update Privilege</span></span>  | <span data-ttu-id="71b77-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="71b77-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="71b77-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="71b77-117">Update Frequency</span></span>  | <span data-ttu-id="71b77-118">All'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="71b77-118">At system startup.</span></span>                   |
| <span data-ttu-id="71b77-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-119">Attribute-Id</span></span>      | <span data-ttu-id="71b77-120">1.2.840.113556.1.4.1373</span><span class="sxs-lookup"><span data-stu-id="71b77-120">1.2.840.113556.1.4.1373</span></span>              |
| <span data-ttu-id="71b77-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="71b77-121">System-Id-Guid</span></span>    | <span data-ttu-id="71b77-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="71b77-122">7778bd90-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="71b77-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71b77-123">Syntax</span></span>            | [<span data-ttu-id="71b77-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="71b77-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="71b77-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="71b77-125">Implementations</span></span>

-   [<span data-ttu-id="71b77-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="71b77-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="71b77-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="71b77-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="71b77-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="71b77-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="71b77-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="71b77-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="71b77-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="71b77-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="71b77-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="71b77-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="71b77-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71b77-132">Windows 2000 Server</span></span>



| <span data-ttu-id="71b77-133">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-133">Entry</span></span> | <span data-ttu-id="71b77-134">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-134">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="71b77-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71b77-135">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="71b77-137">System-Only</span></span>            | <span data-ttu-id="71b77-138">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-138">False</span></span>                                                     |
| <span data-ttu-id="71b77-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71b77-139">Is-Single-Valued</span></span>       | <span data-ttu-id="71b77-140">Vero</span><span class="sxs-lookup"><span data-stu-id="71b77-140">True</span></span>                                                      |
| <span data-ttu-id="71b77-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71b77-141">Is Indexed</span></span>             | <span data-ttu-id="71b77-142">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-142">False</span></span>                                                     |
| <span data-ttu-id="71b77-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71b77-143">In Global Catalog</span></span>      | <span data-ttu-id="71b77-144">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-144">False</span></span>                                                     |
| <span data-ttu-id="71b77-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71b77-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="71b77-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71b77-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="71b77-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71b77-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71b77-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-149">Search-Flags</span></span>           | <span data-ttu-id="71b77-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71b77-150">0x00000000</span></span>                                                |
| <span data-ttu-id="71b77-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-151">System-Flags</span></span>           | <span data-ttu-id="71b77-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71b77-152">0x00000010</span></span>                                                |
| <span data-ttu-id="71b77-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71b77-153">Classes used in</span></span>        | [<span data-ttu-id="71b77-154">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="71b77-154">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="71b77-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71b77-155">Windows Server 2003</span></span>



| <span data-ttu-id="71b77-156">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-156">Entry</span></span> | <span data-ttu-id="71b77-157">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="71b77-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71b77-158">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-159">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="71b77-160">System-Only</span></span>            | <span data-ttu-id="71b77-161">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-161">False</span></span>                                                     |
| <span data-ttu-id="71b77-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71b77-162">Is-Single-Valued</span></span>       | <span data-ttu-id="71b77-163">Vero</span><span class="sxs-lookup"><span data-stu-id="71b77-163">True</span></span>                                                      |
| <span data-ttu-id="71b77-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71b77-164">Is Indexed</span></span>             | <span data-ttu-id="71b77-165">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-165">False</span></span>                                                     |
| <span data-ttu-id="71b77-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71b77-166">In Global Catalog</span></span>      | <span data-ttu-id="71b77-167">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-167">False</span></span>                                                     |
| <span data-ttu-id="71b77-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71b77-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="71b77-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71b77-169">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="71b77-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71b77-170">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71b77-171">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-172">Search-Flags</span></span>           | <span data-ttu-id="71b77-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71b77-173">0x00000000</span></span>                                                |
| <span data-ttu-id="71b77-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-174">System-Flags</span></span>           | <span data-ttu-id="71b77-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71b77-175">0x00000010</span></span>                                                |
| <span data-ttu-id="71b77-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71b77-176">Classes used in</span></span>        | [<span data-ttu-id="71b77-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="71b77-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="71b77-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="71b77-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="71b77-179">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-179">Entry</span></span> | <span data-ttu-id="71b77-180">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-180">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="71b77-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71b77-181">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-182">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="71b77-183">System-Only</span></span>            | <span data-ttu-id="71b77-184">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-184">False</span></span>                                                     |
| <span data-ttu-id="71b77-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71b77-185">Is-Single-Valued</span></span>       | <span data-ttu-id="71b77-186">Vero</span><span class="sxs-lookup"><span data-stu-id="71b77-186">True</span></span>                                                      |
| <span data-ttu-id="71b77-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71b77-187">Is Indexed</span></span>             | <span data-ttu-id="71b77-188">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-188">False</span></span>                                                     |
| <span data-ttu-id="71b77-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71b77-189">In Global Catalog</span></span>      | <span data-ttu-id="71b77-190">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-190">False</span></span>                                                     |
| <span data-ttu-id="71b77-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71b77-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="71b77-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71b77-192">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="71b77-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71b77-193">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71b77-194">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-195">Search-Flags</span></span>           | <span data-ttu-id="71b77-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71b77-196">0x00000000</span></span>                                                |
| <span data-ttu-id="71b77-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-197">System-Flags</span></span>           | <span data-ttu-id="71b77-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71b77-198">0x00000010</span></span>                                                |
| <span data-ttu-id="71b77-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71b77-199">Classes used in</span></span>        | [<span data-ttu-id="71b77-200">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="71b77-200">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="71b77-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71b77-201">Windows Server 2008</span></span>



| <span data-ttu-id="71b77-202">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-202">Entry</span></span> | <span data-ttu-id="71b77-203">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-203">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="71b77-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71b77-204">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-205">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="71b77-206">System-Only</span></span>            | <span data-ttu-id="71b77-207">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-207">False</span></span>                                                     |
| <span data-ttu-id="71b77-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71b77-208">Is-Single-Valued</span></span>       | <span data-ttu-id="71b77-209">Vero</span><span class="sxs-lookup"><span data-stu-id="71b77-209">True</span></span>                                                      |
| <span data-ttu-id="71b77-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71b77-210">Is Indexed</span></span>             | <span data-ttu-id="71b77-211">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-211">False</span></span>                                                     |
| <span data-ttu-id="71b77-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71b77-212">In Global Catalog</span></span>      | <span data-ttu-id="71b77-213">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-213">False</span></span>                                                     |
| <span data-ttu-id="71b77-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71b77-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="71b77-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71b77-215">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="71b77-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71b77-216">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71b77-217">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-218">Search-Flags</span></span>           | <span data-ttu-id="71b77-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71b77-219">0x00000000</span></span>                                                |
| <span data-ttu-id="71b77-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-220">System-Flags</span></span>           | <span data-ttu-id="71b77-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71b77-221">0x00000010</span></span>                                                |
| <span data-ttu-id="71b77-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71b77-222">Classes used in</span></span>        | [<span data-ttu-id="71b77-223">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="71b77-223">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="71b77-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71b77-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="71b77-225">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-225">Entry</span></span> | <span data-ttu-id="71b77-226">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-226">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="71b77-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71b77-227">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-228">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="71b77-229">System-Only</span></span>            | <span data-ttu-id="71b77-230">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-230">False</span></span>                                                     |
| <span data-ttu-id="71b77-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71b77-231">Is-Single-Valued</span></span>       | <span data-ttu-id="71b77-232">Vero</span><span class="sxs-lookup"><span data-stu-id="71b77-232">True</span></span>                                                      |
| <span data-ttu-id="71b77-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71b77-233">Is Indexed</span></span>             | <span data-ttu-id="71b77-234">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-234">False</span></span>                                                     |
| <span data-ttu-id="71b77-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71b77-235">In Global Catalog</span></span>      | <span data-ttu-id="71b77-236">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-236">False</span></span>                                                     |
| <span data-ttu-id="71b77-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71b77-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="71b77-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71b77-238">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="71b77-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71b77-239">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71b77-240">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-241">Search-Flags</span></span>           | <span data-ttu-id="71b77-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71b77-242">0x00000000</span></span>                                                |
| <span data-ttu-id="71b77-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-243">System-Flags</span></span>           | <span data-ttu-id="71b77-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71b77-244">0x00000010</span></span>                                                |
| <span data-ttu-id="71b77-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71b77-245">Classes used in</span></span>        | [<span data-ttu-id="71b77-246">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="71b77-246">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="71b77-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71b77-247">Windows Server 2012</span></span>



| <span data-ttu-id="71b77-248">Voce</span><span class="sxs-lookup"><span data-stu-id="71b77-248">Entry</span></span> | <span data-ttu-id="71b77-249">Valore</span><span class="sxs-lookup"><span data-stu-id="71b77-249">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="71b77-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="71b77-250">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71b77-251">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="71b77-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="71b77-252">System-Only</span></span>            | <span data-ttu-id="71b77-253">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-253">False</span></span>                                                     |
| <span data-ttu-id="71b77-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="71b77-254">Is-Single-Valued</span></span>       | <span data-ttu-id="71b77-255">Vero</span><span class="sxs-lookup"><span data-stu-id="71b77-255">True</span></span>                                                      |
| <span data-ttu-id="71b77-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="71b77-256">Is Indexed</span></span>             | <span data-ttu-id="71b77-257">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-257">False</span></span>                                                     |
| <span data-ttu-id="71b77-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="71b77-258">In Global Catalog</span></span>      | <span data-ttu-id="71b77-259">Falso</span><span class="sxs-lookup"><span data-stu-id="71b77-259">False</span></span>                                                     |
| <span data-ttu-id="71b77-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="71b77-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="71b77-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="71b77-261">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="71b77-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71b77-262">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71b77-263">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="71b77-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-264">Search-Flags</span></span>           | <span data-ttu-id="71b77-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71b77-265">0x00000000</span></span>                                                |
| <span data-ttu-id="71b77-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71b77-266">System-Flags</span></span>           | <span data-ttu-id="71b77-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71b77-267">0x00000010</span></span>                                                |
| <span data-ttu-id="71b77-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="71b77-268">Classes used in</span></span>        | [<span data-ttu-id="71b77-269">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="71b77-269">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





