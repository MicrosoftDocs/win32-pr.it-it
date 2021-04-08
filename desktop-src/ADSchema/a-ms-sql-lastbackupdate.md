---
title: Attributo MS-SQL-LastBackupDate
description: Data dell'ultima volta in cui è stato eseguito il backup del database.
ms.assetid: 09bd6c2a-85fe-46af-8569-5bc3cbc8411d
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-LastBackupDate
- Schema AD dell'attributo mS-SQL-LastBackupDate
topic_type:
- apiref
api_name:
- MS-SQL-LastBackupDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d91cadf953ab51185882c73d4d999a5ccb3fed9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965412"
---
# <a name="ms-sql-lastbackupdate-attribute"></a><span data-ttu-id="7da50-105">Attributo MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="7da50-105">MS-SQL-LastBackupDate attribute</span></span>

<span data-ttu-id="7da50-106">Data dell'ultima volta in cui è stato eseguito il backup del database.</span><span class="sxs-lookup"><span data-stu-id="7da50-106">The last date that the database was backed up.</span></span>



| <span data-ttu-id="7da50-107">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-107">Entry</span></span> | <span data-ttu-id="7da50-108">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7da50-109">CN</span><span class="sxs-lookup"><span data-stu-id="7da50-109">CN</span></span>                | <span data-ttu-id="7da50-110">MS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="7da50-110">MS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="7da50-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7da50-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7da50-112">mS-SQL-LastBackupDate</span><span class="sxs-lookup"><span data-stu-id="7da50-112">mS-SQL-LastBackupDate</span></span>                       |
| <span data-ttu-id="7da50-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7da50-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7da50-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7da50-114">Update Privilege</span></span>  | <span data-ttu-id="7da50-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7da50-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="7da50-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7da50-116">Update Frequency</span></span>  | <span data-ttu-id="7da50-117">Quando viene eseguito il backup del database.</span><span class="sxs-lookup"><span data-stu-id="7da50-117">When the database is backed up.</span></span>             |
| <span data-ttu-id="7da50-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-118">Attribute-Id</span></span>      | <span data-ttu-id="7da50-119">1.2.840.113556.1.4.1398</span><span class="sxs-lookup"><span data-stu-id="7da50-119">1.2.840.113556.1.4.1398</span></span>                     |
| <span data-ttu-id="7da50-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7da50-120">System-Id-Guid</span></span>    | <span data-ttu-id="7da50-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="7da50-121">f2b6abca-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="7da50-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7da50-122">Syntax</span></span>            | [<span data-ttu-id="7da50-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7da50-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7da50-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7da50-124">Implementations</span></span>

-   [<span data-ttu-id="7da50-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7da50-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7da50-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7da50-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7da50-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7da50-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7da50-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7da50-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7da50-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7da50-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7da50-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7da50-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7da50-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7da50-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7da50-132">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-132">Entry</span></span> | <span data-ttu-id="7da50-133">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da50-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7da50-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da50-136">System-Only</span></span>            | <span data-ttu-id="7da50-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7da50-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7da50-139">Vero</span><span class="sxs-lookup"><span data-stu-id="7da50-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="7da50-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7da50-140">Is Indexed</span></span>             | <span data-ttu-id="7da50-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7da50-142">In Global Catalog</span></span>      | <span data-ttu-id="7da50-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7da50-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da50-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7da50-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7da50-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da50-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da50-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-148">Search-Flags</span></span>           | <span data-ttu-id="7da50-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da50-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-150">System-Flags</span></span>           | <span data-ttu-id="7da50-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7da50-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7da50-152">Classes used in</span></span>        | [<span data-ttu-id="7da50-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7da50-154">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-154">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7da50-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7da50-155">Windows Server 2003</span></span>



| <span data-ttu-id="7da50-156">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-156">Entry</span></span> | <span data-ttu-id="7da50-157">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da50-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7da50-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da50-160">System-Only</span></span>            | <span data-ttu-id="7da50-161">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7da50-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7da50-163">Vero</span><span class="sxs-lookup"><span data-stu-id="7da50-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="7da50-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7da50-164">Is Indexed</span></span>             | <span data-ttu-id="7da50-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7da50-166">In Global Catalog</span></span>      | <span data-ttu-id="7da50-167">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7da50-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da50-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7da50-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7da50-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da50-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da50-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-172">Search-Flags</span></span>           | <span data-ttu-id="7da50-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da50-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-174">System-Flags</span></span>           | <span data-ttu-id="7da50-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7da50-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7da50-176">Classes used in</span></span>        | [<span data-ttu-id="7da50-177">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-177">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7da50-178">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-178">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7da50-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7da50-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7da50-180">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-180">Entry</span></span> | <span data-ttu-id="7da50-181">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da50-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7da50-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da50-184">System-Only</span></span>            | <span data-ttu-id="7da50-185">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7da50-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7da50-187">Vero</span><span class="sxs-lookup"><span data-stu-id="7da50-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="7da50-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7da50-188">Is Indexed</span></span>             | <span data-ttu-id="7da50-189">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7da50-190">In Global Catalog</span></span>      | <span data-ttu-id="7da50-191">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7da50-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da50-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7da50-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7da50-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da50-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da50-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-196">Search-Flags</span></span>           | <span data-ttu-id="7da50-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da50-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-198">System-Flags</span></span>           | <span data-ttu-id="7da50-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7da50-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7da50-200">Classes used in</span></span>        | [<span data-ttu-id="7da50-201">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-201">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7da50-202">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-202">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7da50-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7da50-203">Windows Server 2008</span></span>



| <span data-ttu-id="7da50-204">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-204">Entry</span></span> | <span data-ttu-id="7da50-205">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da50-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7da50-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da50-208">System-Only</span></span>            | <span data-ttu-id="7da50-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7da50-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7da50-211">Vero</span><span class="sxs-lookup"><span data-stu-id="7da50-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="7da50-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7da50-212">Is Indexed</span></span>             | <span data-ttu-id="7da50-213">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7da50-214">In Global Catalog</span></span>      | <span data-ttu-id="7da50-215">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7da50-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da50-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7da50-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7da50-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da50-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da50-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-220">Search-Flags</span></span>           | <span data-ttu-id="7da50-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da50-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-222">System-Flags</span></span>           | <span data-ttu-id="7da50-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7da50-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7da50-224">Classes used in</span></span>        | [<span data-ttu-id="7da50-225">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-225">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7da50-226">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-226">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7da50-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7da50-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7da50-228">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-228">Entry</span></span> | <span data-ttu-id="7da50-229">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da50-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7da50-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da50-232">System-Only</span></span>            | <span data-ttu-id="7da50-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7da50-234">Is-Single-Valued</span></span>       | <span data-ttu-id="7da50-235">Vero</span><span class="sxs-lookup"><span data-stu-id="7da50-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="7da50-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7da50-236">Is Indexed</span></span>             | <span data-ttu-id="7da50-237">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7da50-238">In Global Catalog</span></span>      | <span data-ttu-id="7da50-239">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7da50-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da50-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7da50-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7da50-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da50-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da50-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-244">Search-Flags</span></span>           | <span data-ttu-id="7da50-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da50-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-246">System-Flags</span></span>           | <span data-ttu-id="7da50-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7da50-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7da50-248">Classes used in</span></span>        | [<span data-ttu-id="7da50-249">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-249">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7da50-250">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-250">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7da50-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7da50-251">Windows Server 2012</span></span>



| <span data-ttu-id="7da50-252">Voce</span><span class="sxs-lookup"><span data-stu-id="7da50-252">Entry</span></span> | <span data-ttu-id="7da50-253">Valore</span><span class="sxs-lookup"><span data-stu-id="7da50-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da50-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7da50-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7da50-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="7da50-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="7da50-256">System-Only</span></span>            | <span data-ttu-id="7da50-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7da50-258">Is-Single-Valued</span></span>       | <span data-ttu-id="7da50-259">Vero</span><span class="sxs-lookup"><span data-stu-id="7da50-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="7da50-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7da50-260">Is Indexed</span></span>             | <span data-ttu-id="7da50-261">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7da50-262">In Global Catalog</span></span>      | <span data-ttu-id="7da50-263">Falso</span><span class="sxs-lookup"><span data-stu-id="7da50-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="7da50-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7da50-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="7da50-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7da50-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="7da50-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7da50-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7da50-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="7da50-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-268">Search-Flags</span></span>           | <span data-ttu-id="7da50-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7da50-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7da50-270">System-Flags</span></span>           | <span data-ttu-id="7da50-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7da50-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="7da50-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7da50-272">Classes used in</span></span>        | [<span data-ttu-id="7da50-273">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-273">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> [<span data-ttu-id="7da50-274">**MS-SQL-OLAPDatabase**</span><span class="sxs-lookup"><span data-stu-id="7da50-274">**MS-SQL-OLAPDatabase**</span></span>](c-ms-sql-olapdatabase.md)<br/> |



 

 





