---
title: Attributo MS-SQL-SortOrder
description: Ordinamento per l'istanza corrente di SQL Server.
ms.assetid: cd58cb56-19aa-4ee6-b241-1198b3e9e097
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-SortOrder
- Schema AD dell'attributo mS-SQL-SortOrder
topic_type:
- apiref
api_name:
- MS-SQL-SortOrder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940dafa4cc9bfce15ae1a5df472720e6e779f19e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302967"
---
# <a name="ms-sql-sortorder-attribute"></a><span data-ttu-id="4cec7-105">Attributo MS-SQL-SortOrder</span><span class="sxs-lookup"><span data-stu-id="4cec7-105">MS-SQL-SortOrder attribute</span></span>

<span data-ttu-id="4cec7-106">Ordinamento per l'istanza corrente di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4cec7-106">The sort order for the current instance of SQL Server.</span></span>



| <span data-ttu-id="4cec7-107">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-107">Entry</span></span> | <span data-ttu-id="4cec7-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4cec7-109">CN</span><span class="sxs-lookup"><span data-stu-id="4cec7-109">CN</span></span>                | <span data-ttu-id="4cec7-110">MS-SQL-SortOrder</span><span class="sxs-lookup"><span data-stu-id="4cec7-110">MS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="4cec7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4cec7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4cec7-112">mS-SQL-SortOrder</span><span class="sxs-lookup"><span data-stu-id="4cec7-112">mS-SQL-SortOrder</span></span>                            |
| <span data-ttu-id="4cec7-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4cec7-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="4cec7-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-114">Update Privilege</span></span>  | <span data-ttu-id="4cec7-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="4cec7-115">Domain administrator</span></span>                        |
| <span data-ttu-id="4cec7-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-116">Update Frequency</span></span>  | <span data-ttu-id="4cec7-117">Durante l'installazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="4cec7-117">At system setup.</span></span>                            |
| <span data-ttu-id="4cec7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-118">Attribute-Id</span></span>      | <span data-ttu-id="4cec7-119">1.2.840.113556.1.4.1371</span><span class="sxs-lookup"><span data-stu-id="4cec7-119">1.2.840.113556.1.4.1371</span></span>                     |
| <span data-ttu-id="4cec7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4cec7-120">System-Id-Guid</span></span>    | <span data-ttu-id="4cec7-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="4cec7-121">6ddc42c0-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="4cec7-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cec7-122">Syntax</span></span>            | [<span data-ttu-id="4cec7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4cec7-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4cec7-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4cec7-124">Implementations</span></span>

-   [<span data-ttu-id="4cec7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4cec7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4cec7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4cec7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4cec7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4cec7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4cec7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4cec7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4cec7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4cec7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4cec7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4cec7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4cec7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4cec7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4cec7-132">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-132">Entry</span></span> | <span data-ttu-id="4cec7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4cec7-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cec7-136">System-Only</span></span>            | <span data-ttu-id="4cec7-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-137">False</span></span>                                                     |
| <span data-ttu-id="4cec7-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4cec7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4cec7-139">Vero</span><span class="sxs-lookup"><span data-stu-id="4cec7-139">True</span></span>                                                      |
| <span data-ttu-id="4cec7-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4cec7-140">Is Indexed</span></span>             | <span data-ttu-id="4cec7-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-141">False</span></span>                                                     |
| <span data-ttu-id="4cec7-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4cec7-142">In Global Catalog</span></span>      | <span data-ttu-id="4cec7-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-143">False</span></span>                                                     |
| <span data-ttu-id="4cec7-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4cec7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cec7-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4cec7-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="4cec7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cec7-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cec7-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-148">Search-Flags</span></span>           | <span data-ttu-id="4cec7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cec7-149">0x00000000</span></span>                                                |
| <span data-ttu-id="4cec7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-150">System-Flags</span></span>           | <span data-ttu-id="4cec7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cec7-151">0x00000010</span></span>                                                |
| <span data-ttu-id="4cec7-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4cec7-152">Classes used in</span></span>        | [<span data-ttu-id="4cec7-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4cec7-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4cec7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cec7-154">Windows Server 2003</span></span>



| <span data-ttu-id="4cec7-155">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-155">Entry</span></span> | <span data-ttu-id="4cec7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4cec7-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cec7-159">System-Only</span></span>            | <span data-ttu-id="4cec7-160">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-160">False</span></span>                                                     |
| <span data-ttu-id="4cec7-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4cec7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4cec7-162">Vero</span><span class="sxs-lookup"><span data-stu-id="4cec7-162">True</span></span>                                                      |
| <span data-ttu-id="4cec7-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4cec7-163">Is Indexed</span></span>             | <span data-ttu-id="4cec7-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-164">False</span></span>                                                     |
| <span data-ttu-id="4cec7-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4cec7-165">In Global Catalog</span></span>      | <span data-ttu-id="4cec7-166">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-166">False</span></span>                                                     |
| <span data-ttu-id="4cec7-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4cec7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cec7-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4cec7-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="4cec7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cec7-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cec7-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-171">Search-Flags</span></span>           | <span data-ttu-id="4cec7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cec7-172">0x00000000</span></span>                                                |
| <span data-ttu-id="4cec7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-173">System-Flags</span></span>           | <span data-ttu-id="4cec7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cec7-174">0x00000010</span></span>                                                |
| <span data-ttu-id="4cec7-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4cec7-175">Classes used in</span></span>        | [<span data-ttu-id="4cec7-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4cec7-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4cec7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4cec7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4cec7-178">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-178">Entry</span></span> | <span data-ttu-id="4cec7-179">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4cec7-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cec7-182">System-Only</span></span>            | <span data-ttu-id="4cec7-183">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-183">False</span></span>                                                     |
| <span data-ttu-id="4cec7-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4cec7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4cec7-185">Vero</span><span class="sxs-lookup"><span data-stu-id="4cec7-185">True</span></span>                                                      |
| <span data-ttu-id="4cec7-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4cec7-186">Is Indexed</span></span>             | <span data-ttu-id="4cec7-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-187">False</span></span>                                                     |
| <span data-ttu-id="4cec7-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4cec7-188">In Global Catalog</span></span>      | <span data-ttu-id="4cec7-189">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-189">False</span></span>                                                     |
| <span data-ttu-id="4cec7-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4cec7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cec7-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4cec7-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="4cec7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cec7-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cec7-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-194">Search-Flags</span></span>           | <span data-ttu-id="4cec7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cec7-195">0x00000000</span></span>                                                |
| <span data-ttu-id="4cec7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-196">System-Flags</span></span>           | <span data-ttu-id="4cec7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cec7-197">0x00000010</span></span>                                                |
| <span data-ttu-id="4cec7-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4cec7-198">Classes used in</span></span>        | [<span data-ttu-id="4cec7-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4cec7-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4cec7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cec7-200">Windows Server 2008</span></span>



| <span data-ttu-id="4cec7-201">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-201">Entry</span></span> | <span data-ttu-id="4cec7-202">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4cec7-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cec7-205">System-Only</span></span>            | <span data-ttu-id="4cec7-206">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-206">False</span></span>                                                     |
| <span data-ttu-id="4cec7-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4cec7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4cec7-208">Vero</span><span class="sxs-lookup"><span data-stu-id="4cec7-208">True</span></span>                                                      |
| <span data-ttu-id="4cec7-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4cec7-209">Is Indexed</span></span>             | <span data-ttu-id="4cec7-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-210">False</span></span>                                                     |
| <span data-ttu-id="4cec7-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4cec7-211">In Global Catalog</span></span>      | <span data-ttu-id="4cec7-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-212">False</span></span>                                                     |
| <span data-ttu-id="4cec7-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4cec7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cec7-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4cec7-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="4cec7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cec7-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cec7-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-217">Search-Flags</span></span>           | <span data-ttu-id="4cec7-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cec7-218">0x00000000</span></span>                                                |
| <span data-ttu-id="4cec7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-219">System-Flags</span></span>           | <span data-ttu-id="4cec7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cec7-220">0x00000010</span></span>                                                |
| <span data-ttu-id="4cec7-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4cec7-221">Classes used in</span></span>        | [<span data-ttu-id="4cec7-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4cec7-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4cec7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4cec7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4cec7-224">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-224">Entry</span></span> | <span data-ttu-id="4cec7-225">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4cec7-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cec7-228">System-Only</span></span>            | <span data-ttu-id="4cec7-229">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-229">False</span></span>                                                     |
| <span data-ttu-id="4cec7-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4cec7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4cec7-231">Vero</span><span class="sxs-lookup"><span data-stu-id="4cec7-231">True</span></span>                                                      |
| <span data-ttu-id="4cec7-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4cec7-232">Is Indexed</span></span>             | <span data-ttu-id="4cec7-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-233">False</span></span>                                                     |
| <span data-ttu-id="4cec7-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4cec7-234">In Global Catalog</span></span>      | <span data-ttu-id="4cec7-235">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-235">False</span></span>                                                     |
| <span data-ttu-id="4cec7-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4cec7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cec7-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4cec7-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="4cec7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cec7-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cec7-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-240">Search-Flags</span></span>           | <span data-ttu-id="4cec7-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cec7-241">0x00000000</span></span>                                                |
| <span data-ttu-id="4cec7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-242">System-Flags</span></span>           | <span data-ttu-id="4cec7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cec7-243">0x00000010</span></span>                                                |
| <span data-ttu-id="4cec7-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4cec7-244">Classes used in</span></span>        | [<span data-ttu-id="4cec7-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4cec7-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4cec7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cec7-246">Windows Server 2012</span></span>



| <span data-ttu-id="4cec7-247">Voce</span><span class="sxs-lookup"><span data-stu-id="4cec7-247">Entry</span></span> | <span data-ttu-id="4cec7-248">Valore</span><span class="sxs-lookup"><span data-stu-id="4cec7-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4cec7-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4cec7-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cec7-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="4cec7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cec7-251">System-Only</span></span>            | <span data-ttu-id="4cec7-252">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-252">False</span></span>                                                     |
| <span data-ttu-id="4cec7-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4cec7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4cec7-254">Vero</span><span class="sxs-lookup"><span data-stu-id="4cec7-254">True</span></span>                                                      |
| <span data-ttu-id="4cec7-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4cec7-255">Is Indexed</span></span>             | <span data-ttu-id="4cec7-256">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-256">False</span></span>                                                     |
| <span data-ttu-id="4cec7-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4cec7-257">In Global Catalog</span></span>      | <span data-ttu-id="4cec7-258">Falso</span><span class="sxs-lookup"><span data-stu-id="4cec7-258">False</span></span>                                                     |
| <span data-ttu-id="4cec7-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4cec7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cec7-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4cec7-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="4cec7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cec7-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cec7-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="4cec7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-263">Search-Flags</span></span>           | <span data-ttu-id="4cec7-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cec7-264">0x00000000</span></span>                                                |
| <span data-ttu-id="4cec7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cec7-265">System-Flags</span></span>           | <span data-ttu-id="4cec7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cec7-266">0x00000010</span></span>                                                |
| <span data-ttu-id="4cec7-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4cec7-267">Classes used in</span></span>        | [<span data-ttu-id="4cec7-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="4cec7-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





