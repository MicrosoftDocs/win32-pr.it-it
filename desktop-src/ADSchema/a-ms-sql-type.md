---
title: Attributo di tipo MS-SQL
description: Tipo di replica utilizzato da SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di tipo MS-SQL
- Schema AD dell'attributo di tipo mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875773"
---
# <a name="ms-sql-type-attribute"></a><span data-ttu-id="ba766-105">Attributo di tipo MS-SQL</span><span class="sxs-lookup"><span data-stu-id="ba766-105">MS-SQL-Type attribute</span></span>

<span data-ttu-id="ba766-106">Tipo di replica utilizzato da SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ba766-106">The replication type used by this SQL server.</span></span> <span data-ttu-id="ba766-107">Di seguito sono riportati i valori possibili per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="ba766-107">The following values are the possible values for this attribute.</span></span>



| <span data-ttu-id="ba766-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-108">Value</span></span>        | <span data-ttu-id="ba766-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba766-109">Description</span></span>                           |
|--------------|---------------------------------------|
| <span data-ttu-id="ba766-110">0</span><span class="sxs-lookup"><span data-stu-id="ba766-110">0</span></span><br/> | <span data-ttu-id="ba766-111">Replica transazionale.</span><span class="sxs-lookup"><span data-stu-id="ba766-111">Transactional replication.</span></span><br/> |
| <span data-ttu-id="ba766-112">1</span><span class="sxs-lookup"><span data-stu-id="ba766-112">1</span></span><br/> | <span data-ttu-id="ba766-113">Replica snapshot.</span><span class="sxs-lookup"><span data-stu-id="ba766-113">Snapshot replication.</span></span><br/>      |
| <span data-ttu-id="ba766-114">2</span><span class="sxs-lookup"><span data-stu-id="ba766-114">2</span></span><br/> | <span data-ttu-id="ba766-115">Replica di tipo merge.</span><span class="sxs-lookup"><span data-stu-id="ba766-115">Merge replication.</span></span><br/>         |



 



| <span data-ttu-id="ba766-116">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-116">Entry</span></span> | <span data-ttu-id="ba766-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-117">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ba766-118">CN</span><span class="sxs-lookup"><span data-stu-id="ba766-118">CN</span></span>                | <span data-ttu-id="ba766-119">Tipo MS-SQL</span><span class="sxs-lookup"><span data-stu-id="ba766-119">MS-SQL-Type</span></span>                                 |
| <span data-ttu-id="ba766-120">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ba766-120">Ldap-Display-Name</span></span> | <span data-ttu-id="ba766-121">Tipo mS-SQL</span><span class="sxs-lookup"><span data-stu-id="ba766-121">mS-SQL-Type</span></span>                                 |
| <span data-ttu-id="ba766-122">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ba766-122">Size</span></span>              | \-                                          |
| <span data-ttu-id="ba766-123">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ba766-123">Update Privilege</span></span>  | <span data-ttu-id="ba766-124">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="ba766-124">Domain administrator</span></span>                        |
| <span data-ttu-id="ba766-125">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ba766-125">Update Frequency</span></span>  | <span data-ttu-id="ba766-126">Quando la replica è configurata.</span><span class="sxs-lookup"><span data-stu-id="ba766-126">When replication is set up.</span></span>                 |
| <span data-ttu-id="ba766-127">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-127">Attribute-Id</span></span>      | <span data-ttu-id="ba766-128">1.2.840.113556.1.4.1391</span><span class="sxs-lookup"><span data-stu-id="ba766-128">1.2.840.113556.1.4.1391</span></span>                     |
| <span data-ttu-id="ba766-129">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ba766-129">System-Id-Guid</span></span>    | <span data-ttu-id="ba766-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ba766-130">ca48eba8-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="ba766-131">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba766-131">Syntax</span></span>            | [<span data-ttu-id="ba766-132">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ba766-132">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ba766-133">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ba766-133">Implementations</span></span>

-   [<span data-ttu-id="ba766-134">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba766-134">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba766-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba766-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba766-136">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba766-136">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba766-137">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba766-137">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba766-138">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba766-138">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba766-139">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba766-139">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba766-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba766-140">Windows 2000 Server</span></span>



| <span data-ttu-id="ba766-141">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-141">Entry</span></span> | <span data-ttu-id="ba766-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-142">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba766-143">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba766-143">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-144">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-144">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-145">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba766-145">System-Only</span></span>            | <span data-ttu-id="ba766-146">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-146">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-147">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba766-147">Is-Single-Valued</span></span>       | <span data-ttu-id="ba766-148">Vero</span><span class="sxs-lookup"><span data-stu-id="ba766-148">True</span></span>                                                                                                                                |
| <span data-ttu-id="ba766-149">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba766-149">Is Indexed</span></span>             | <span data-ttu-id="ba766-150">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-150">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-151">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba766-151">In Global Catalog</span></span>      | <span data-ttu-id="ba766-152">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-152">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-153">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba766-153">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba766-154">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba766-154">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="ba766-155">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba766-155">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-156">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba766-156">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-157">Search-Flags</span></span>           | <span data-ttu-id="ba766-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba766-158">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-159">System-Flags</span></span>           | <span data-ttu-id="ba766-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba766-160">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-161">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba766-161">Classes used in</span></span>        | [<span data-ttu-id="ba766-162">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ba766-162">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="ba766-163">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="ba766-163">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba766-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba766-164">Windows Server 2003</span></span>



| <span data-ttu-id="ba766-165">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-165">Entry</span></span> | <span data-ttu-id="ba766-166">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba766-167">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba766-167">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-168">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba766-169">System-Only</span></span>            | <span data-ttu-id="ba766-170">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-170">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-171">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba766-171">Is-Single-Valued</span></span>       | <span data-ttu-id="ba766-172">Vero</span><span class="sxs-lookup"><span data-stu-id="ba766-172">True</span></span>                                                                                                                                |
| <span data-ttu-id="ba766-173">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba766-173">Is Indexed</span></span>             | <span data-ttu-id="ba766-174">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-174">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-175">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba766-175">In Global Catalog</span></span>      | <span data-ttu-id="ba766-176">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-176">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-177">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba766-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba766-178">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba766-178">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="ba766-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba766-179">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba766-180">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-181">Search-Flags</span></span>           | <span data-ttu-id="ba766-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba766-182">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-183">System-Flags</span></span>           | <span data-ttu-id="ba766-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba766-184">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-185">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba766-185">Classes used in</span></span>        | [<span data-ttu-id="ba766-186">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ba766-186">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="ba766-187">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="ba766-187">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba766-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba766-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba766-189">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-189">Entry</span></span> | <span data-ttu-id="ba766-190">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-190">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba766-191">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba766-191">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-192">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba766-193">System-Only</span></span>            | <span data-ttu-id="ba766-194">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-194">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-195">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba766-195">Is-Single-Valued</span></span>       | <span data-ttu-id="ba766-196">Vero</span><span class="sxs-lookup"><span data-stu-id="ba766-196">True</span></span>                                                                                                                                |
| <span data-ttu-id="ba766-197">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba766-197">Is Indexed</span></span>             | <span data-ttu-id="ba766-198">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-198">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-199">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba766-199">In Global Catalog</span></span>      | <span data-ttu-id="ba766-200">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-200">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-201">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba766-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba766-202">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba766-202">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="ba766-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba766-203">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba766-204">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-205">Search-Flags</span></span>           | <span data-ttu-id="ba766-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba766-206">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-207">System-Flags</span></span>           | <span data-ttu-id="ba766-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba766-208">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba766-209">Classes used in</span></span>        | [<span data-ttu-id="ba766-210">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ba766-210">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="ba766-211">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="ba766-211">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba766-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba766-212">Windows Server 2008</span></span>



| <span data-ttu-id="ba766-213">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-213">Entry</span></span> | <span data-ttu-id="ba766-214">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-214">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba766-215">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba766-215">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-216">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba766-217">System-Only</span></span>            | <span data-ttu-id="ba766-218">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-218">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba766-219">Is-Single-Valued</span></span>       | <span data-ttu-id="ba766-220">Vero</span><span class="sxs-lookup"><span data-stu-id="ba766-220">True</span></span>                                                                                                                                |
| <span data-ttu-id="ba766-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba766-221">Is Indexed</span></span>             | <span data-ttu-id="ba766-222">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-222">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba766-223">In Global Catalog</span></span>      | <span data-ttu-id="ba766-224">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-224">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba766-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba766-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba766-226">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="ba766-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba766-227">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba766-228">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-229">Search-Flags</span></span>           | <span data-ttu-id="ba766-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba766-230">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-231">System-Flags</span></span>           | <span data-ttu-id="ba766-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba766-232">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba766-233">Classes used in</span></span>        | [<span data-ttu-id="ba766-234">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ba766-234">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="ba766-235">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="ba766-235">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba766-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba766-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba766-237">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-237">Entry</span></span> | <span data-ttu-id="ba766-238">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-238">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba766-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba766-239">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-240">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba766-241">System-Only</span></span>            | <span data-ttu-id="ba766-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba766-243">Is-Single-Valued</span></span>       | <span data-ttu-id="ba766-244">Vero</span><span class="sxs-lookup"><span data-stu-id="ba766-244">True</span></span>                                                                                                                                |
| <span data-ttu-id="ba766-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba766-245">Is Indexed</span></span>             | <span data-ttu-id="ba766-246">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-246">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba766-247">In Global Catalog</span></span>      | <span data-ttu-id="ba766-248">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-248">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba766-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba766-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba766-250">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="ba766-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba766-251">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba766-252">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-253">Search-Flags</span></span>           | <span data-ttu-id="ba766-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba766-254">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-255">System-Flags</span></span>           | <span data-ttu-id="ba766-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba766-256">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-257">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba766-257">Classes used in</span></span>        | [<span data-ttu-id="ba766-258">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ba766-258">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="ba766-259">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="ba766-259">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba766-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba766-260">Windows Server 2012</span></span>



| <span data-ttu-id="ba766-261">Voce</span><span class="sxs-lookup"><span data-stu-id="ba766-261">Entry</span></span> | <span data-ttu-id="ba766-262">Valore</span><span class="sxs-lookup"><span data-stu-id="ba766-262">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba766-263">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba766-263">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba766-264">MAPI-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="ba766-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba766-265">System-Only</span></span>            | <span data-ttu-id="ba766-266">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-266">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-267">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba766-267">Is-Single-Valued</span></span>       | <span data-ttu-id="ba766-268">Vero</span><span class="sxs-lookup"><span data-stu-id="ba766-268">True</span></span>                                                                                                                                |
| <span data-ttu-id="ba766-269">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba766-269">Is Indexed</span></span>             | <span data-ttu-id="ba766-270">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-270">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-271">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba766-271">In Global Catalog</span></span>      | <span data-ttu-id="ba766-272">Falso</span><span class="sxs-lookup"><span data-stu-id="ba766-272">False</span></span>                                                                                                                               |
| <span data-ttu-id="ba766-273">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba766-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba766-274">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba766-274">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="ba766-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba766-275">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba766-276">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="ba766-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-277">Search-Flags</span></span>           | <span data-ttu-id="ba766-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba766-278">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba766-279">System-Flags</span></span>           | <span data-ttu-id="ba766-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba766-280">0x00000010</span></span>                                                                                                                          |
| <span data-ttu-id="ba766-281">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba766-281">Classes used in</span></span>        | [<span data-ttu-id="ba766-282">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="ba766-282">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> [<span data-ttu-id="ba766-283">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="ba766-283">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





