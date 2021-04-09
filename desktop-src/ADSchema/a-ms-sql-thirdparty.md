---
title: Attributo MS-SQL-ThirdParty
description: Questo attributo indica se i dati della pubblicazione provengano da un'origine dati diversa da SQL Server. Se si tratta di un'altra origine, viene impostata su TRUE.
ms.assetid: 84d93b9f-0acc-47da-9f1b-44d8468ad53e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-ThirdParty
- Schema AD dell'attributo mS-SQL-ThirdParty
topic_type:
- apiref
api_name:
- MS-SQL-ThirdParty
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc2b60f9589990f6357ee3c4cd24215e8af21df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744298"
---
# <a name="ms-sql-thirdparty-attribute"></a><span data-ttu-id="04371-106">Attributo MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="04371-106">MS-SQL-ThirdParty attribute</span></span>

<span data-ttu-id="04371-107">Questo attributo indica se i dati della pubblicazione provengano da un'origine dati diversa da SQL Server.</span><span class="sxs-lookup"><span data-stu-id="04371-107">This attribute indicates whether the publication data is from a data source other than SQL Server.</span></span> <span data-ttu-id="04371-108">Se si tratta di un'altra origine, viene impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="04371-108">If it is from another source, then it is set to **TRUE**.</span></span>



| <span data-ttu-id="04371-109">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-109">Entry</span></span> | <span data-ttu-id="04371-110">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="04371-111">CN</span><span class="sxs-lookup"><span data-stu-id="04371-111">CN</span></span>                | <span data-ttu-id="04371-112">MS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="04371-112">MS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="04371-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04371-113">Ldap-Display-Name</span></span> | <span data-ttu-id="04371-114">mS-SQL-ThirdParty</span><span class="sxs-lookup"><span data-stu-id="04371-114">mS-SQL-ThirdParty</span></span>                    |
| <span data-ttu-id="04371-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="04371-115">Size</span></span>              | <span data-ttu-id="04371-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="04371-116">4 bytes</span></span>                              |
| <span data-ttu-id="04371-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="04371-117">Update Privilege</span></span>  | <span data-ttu-id="04371-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="04371-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="04371-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="04371-119">Update Frequency</span></span>  | <span data-ttu-id="04371-120">Quando la replica è impostata.</span><span class="sxs-lookup"><span data-stu-id="04371-120">When replication is setup.</span></span>           |
| <span data-ttu-id="04371-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04371-121">Attribute-Id</span></span>      | <span data-ttu-id="04371-122">1.2.840.113556.1.4.1407</span><span class="sxs-lookup"><span data-stu-id="04371-122">1.2.840.113556.1.4.1407</span></span>              |
| <span data-ttu-id="04371-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04371-123">System-Id-Guid</span></span>    | <span data-ttu-id="04371-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="04371-124">c4e311fc-d34b-11d2-999a-0000f87a57d4</span></span> |
| <span data-ttu-id="04371-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04371-125">Syntax</span></span>            | [<span data-ttu-id="04371-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="04371-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="04371-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="04371-127">Implementations</span></span>

-   [<span data-ttu-id="04371-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04371-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04371-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04371-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04371-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04371-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04371-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04371-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04371-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04371-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04371-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04371-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04371-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04371-134">Windows 2000 Server</span></span>



| <span data-ttu-id="04371-135">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-135">Entry</span></span> | <span data-ttu-id="04371-136">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="04371-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04371-137">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04371-138">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="04371-139">System-Only</span></span>            | <span data-ttu-id="04371-140">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-140">False</span></span>                                                               |
| <span data-ttu-id="04371-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04371-141">Is-Single-Valued</span></span>       | <span data-ttu-id="04371-142">Vero</span><span class="sxs-lookup"><span data-stu-id="04371-142">True</span></span>                                                                |
| <span data-ttu-id="04371-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04371-143">Is Indexed</span></span>             | <span data-ttu-id="04371-144">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-144">False</span></span>                                                               |
| <span data-ttu-id="04371-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04371-145">In Global Catalog</span></span>      | <span data-ttu-id="04371-146">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-146">False</span></span>                                                               |
| <span data-ttu-id="04371-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04371-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="04371-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04371-148">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="04371-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04371-149">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04371-150">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-151">Search-Flags</span></span>           | <span data-ttu-id="04371-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04371-152">0x00000000</span></span>                                                          |
| <span data-ttu-id="04371-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-153">System-Flags</span></span>           | <span data-ttu-id="04371-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04371-154">0x00000010</span></span>                                                          |
| <span data-ttu-id="04371-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04371-155">Classes used in</span></span>        | [<span data-ttu-id="04371-156">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="04371-156">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04371-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04371-157">Windows Server 2003</span></span>



| <span data-ttu-id="04371-158">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-158">Entry</span></span> | <span data-ttu-id="04371-159">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-159">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="04371-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04371-160">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04371-161">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="04371-162">System-Only</span></span>            | <span data-ttu-id="04371-163">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-163">False</span></span>                                                               |
| <span data-ttu-id="04371-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04371-164">Is-Single-Valued</span></span>       | <span data-ttu-id="04371-165">Vero</span><span class="sxs-lookup"><span data-stu-id="04371-165">True</span></span>                                                                |
| <span data-ttu-id="04371-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04371-166">Is Indexed</span></span>             | <span data-ttu-id="04371-167">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-167">False</span></span>                                                               |
| <span data-ttu-id="04371-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04371-168">In Global Catalog</span></span>      | <span data-ttu-id="04371-169">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-169">False</span></span>                                                               |
| <span data-ttu-id="04371-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04371-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="04371-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04371-171">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="04371-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04371-172">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04371-173">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-174">Search-Flags</span></span>           | <span data-ttu-id="04371-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04371-175">0x00000000</span></span>                                                          |
| <span data-ttu-id="04371-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-176">System-Flags</span></span>           | <span data-ttu-id="04371-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04371-177">0x00000010</span></span>                                                          |
| <span data-ttu-id="04371-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04371-178">Classes used in</span></span>        | [<span data-ttu-id="04371-179">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="04371-179">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04371-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04371-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04371-181">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-181">Entry</span></span> | <span data-ttu-id="04371-182">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="04371-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04371-183">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04371-184">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="04371-185">System-Only</span></span>            | <span data-ttu-id="04371-186">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-186">False</span></span>                                                               |
| <span data-ttu-id="04371-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04371-187">Is-Single-Valued</span></span>       | <span data-ttu-id="04371-188">Vero</span><span class="sxs-lookup"><span data-stu-id="04371-188">True</span></span>                                                                |
| <span data-ttu-id="04371-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04371-189">Is Indexed</span></span>             | <span data-ttu-id="04371-190">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-190">False</span></span>                                                               |
| <span data-ttu-id="04371-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04371-191">In Global Catalog</span></span>      | <span data-ttu-id="04371-192">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-192">False</span></span>                                                               |
| <span data-ttu-id="04371-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04371-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="04371-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04371-194">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="04371-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04371-195">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04371-196">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-197">Search-Flags</span></span>           | <span data-ttu-id="04371-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04371-198">0x00000000</span></span>                                                          |
| <span data-ttu-id="04371-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-199">System-Flags</span></span>           | <span data-ttu-id="04371-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04371-200">0x00000010</span></span>                                                          |
| <span data-ttu-id="04371-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04371-201">Classes used in</span></span>        | [<span data-ttu-id="04371-202">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="04371-202">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04371-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04371-203">Windows Server 2008</span></span>



| <span data-ttu-id="04371-204">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-204">Entry</span></span> | <span data-ttu-id="04371-205">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-205">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="04371-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04371-206">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04371-207">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="04371-208">System-Only</span></span>            | <span data-ttu-id="04371-209">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-209">False</span></span>                                                               |
| <span data-ttu-id="04371-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04371-210">Is-Single-Valued</span></span>       | <span data-ttu-id="04371-211">Vero</span><span class="sxs-lookup"><span data-stu-id="04371-211">True</span></span>                                                                |
| <span data-ttu-id="04371-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04371-212">Is Indexed</span></span>             | <span data-ttu-id="04371-213">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-213">False</span></span>                                                               |
| <span data-ttu-id="04371-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04371-214">In Global Catalog</span></span>      | <span data-ttu-id="04371-215">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-215">False</span></span>                                                               |
| <span data-ttu-id="04371-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04371-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="04371-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04371-217">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="04371-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04371-218">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04371-219">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-220">Search-Flags</span></span>           | <span data-ttu-id="04371-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04371-221">0x00000000</span></span>                                                          |
| <span data-ttu-id="04371-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-222">System-Flags</span></span>           | <span data-ttu-id="04371-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04371-223">0x00000010</span></span>                                                          |
| <span data-ttu-id="04371-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04371-224">Classes used in</span></span>        | [<span data-ttu-id="04371-225">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="04371-225">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04371-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04371-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04371-227">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-227">Entry</span></span> | <span data-ttu-id="04371-228">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-228">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="04371-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04371-229">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04371-230">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="04371-231">System-Only</span></span>            | <span data-ttu-id="04371-232">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-232">False</span></span>                                                               |
| <span data-ttu-id="04371-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04371-233">Is-Single-Valued</span></span>       | <span data-ttu-id="04371-234">Vero</span><span class="sxs-lookup"><span data-stu-id="04371-234">True</span></span>                                                                |
| <span data-ttu-id="04371-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04371-235">Is Indexed</span></span>             | <span data-ttu-id="04371-236">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-236">False</span></span>                                                               |
| <span data-ttu-id="04371-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04371-237">In Global Catalog</span></span>      | <span data-ttu-id="04371-238">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-238">False</span></span>                                                               |
| <span data-ttu-id="04371-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04371-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="04371-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04371-240">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="04371-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04371-241">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04371-242">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-243">Search-Flags</span></span>           | <span data-ttu-id="04371-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04371-244">0x00000000</span></span>                                                          |
| <span data-ttu-id="04371-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-245">System-Flags</span></span>           | <span data-ttu-id="04371-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04371-246">0x00000010</span></span>                                                          |
| <span data-ttu-id="04371-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04371-247">Classes used in</span></span>        | [<span data-ttu-id="04371-248">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="04371-248">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04371-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04371-249">Windows Server 2012</span></span>



| <span data-ttu-id="04371-250">Voce</span><span class="sxs-lookup"><span data-stu-id="04371-250">Entry</span></span> | <span data-ttu-id="04371-251">Valore</span><span class="sxs-lookup"><span data-stu-id="04371-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="04371-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="04371-252">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04371-253">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="04371-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="04371-254">System-Only</span></span>            | <span data-ttu-id="04371-255">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-255">False</span></span>                                                               |
| <span data-ttu-id="04371-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="04371-256">Is-Single-Valued</span></span>       | <span data-ttu-id="04371-257">Vero</span><span class="sxs-lookup"><span data-stu-id="04371-257">True</span></span>                                                                |
| <span data-ttu-id="04371-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="04371-258">Is Indexed</span></span>             | <span data-ttu-id="04371-259">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-259">False</span></span>                                                               |
| <span data-ttu-id="04371-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="04371-260">In Global Catalog</span></span>      | <span data-ttu-id="04371-261">Falso</span><span class="sxs-lookup"><span data-stu-id="04371-261">False</span></span>                                                               |
| <span data-ttu-id="04371-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="04371-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="04371-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="04371-263">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="04371-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04371-264">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04371-265">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="04371-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-266">Search-Flags</span></span>           | <span data-ttu-id="04371-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04371-267">0x00000000</span></span>                                                          |
| <span data-ttu-id="04371-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04371-268">System-Flags</span></span>           | <span data-ttu-id="04371-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04371-269">0x00000010</span></span>                                                          |
| <span data-ttu-id="04371-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="04371-270">Classes used in</span></span>        | [<span data-ttu-id="04371-271">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="04371-271">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





