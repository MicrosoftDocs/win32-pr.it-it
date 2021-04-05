---
title: Attributo MS-SQL-database
description: Nome del database SQL Server necessario per la replica.
ms.assetid: 624705d9-df3f-458e-98f4-fb8da073efd6
ms.tgt_platform: multiple
keywords:
- MS-SQL-schema di AD dell'attributo del database
- mS-SQL-schema di AD dell'attributo del database
topic_type:
- apiref
api_name:
- MS-SQL-Database
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6c448213bee18fede3cc8a77cabf607c3b2ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874930"
---
# <a name="ms-sql-database-attribute"></a><span data-ttu-id="6e6cd-105">Attributo MS-SQL-database</span><span class="sxs-lookup"><span data-stu-id="6e6cd-105">MS-SQL-Database attribute</span></span>

<span data-ttu-id="6e6cd-106">Nome del database SQL Server necessario per la replica.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-106">The name of the SQL Server database involved in replication.</span></span>



| <span data-ttu-id="6e6cd-107">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-107">Entry</span></span> | <span data-ttu-id="6e6cd-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6e6cd-109">CN</span><span class="sxs-lookup"><span data-stu-id="6e6cd-109">CN</span></span>                | <span data-ttu-id="6e6cd-110">MS-SQL-database</span><span class="sxs-lookup"><span data-stu-id="6e6cd-110">MS-SQL-Database</span></span>                             |
| <span data-ttu-id="6e6cd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6e6cd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6e6cd-112">mS-SQL-database</span><span class="sxs-lookup"><span data-stu-id="6e6cd-112">mS-SQL-Database</span></span>                             |
| <span data-ttu-id="6e6cd-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6e6cd-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6e6cd-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-114">Update Privilege</span></span>  | <span data-ttu-id="6e6cd-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="6e6cd-115">Domain administrator</span></span>                        |
| <span data-ttu-id="6e6cd-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-116">Update Frequency</span></span>  | <span data-ttu-id="6e6cd-117">Quando la replica è impostata.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="6e6cd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-118">Attribute-Id</span></span>      | <span data-ttu-id="6e6cd-119">1.2.840.113556.1.4.1393</span><span class="sxs-lookup"><span data-stu-id="6e6cd-119">1.2.840.113556.1.4.1393</span></span>                     |
| <span data-ttu-id="6e6cd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6e6cd-120">System-Id-Guid</span></span>    | <span data-ttu-id="6e6cd-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="6e6cd-121">d5a0dbdc-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="6e6cd-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e6cd-122">Syntax</span></span>            | [<span data-ttu-id="6e6cd-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6e6cd-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6e6cd-124">Implementations</span></span>

-   [<span data-ttu-id="6e6cd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6e6cd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6e6cd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6e6cd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e6cd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e6cd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6e6cd-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e6cd-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6e6cd-132">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-132">Entry</span></span> | <span data-ttu-id="6e6cd-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e6cd-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6cd-136">System-Only</span></span>            | <span data-ttu-id="6e6cd-137">Falso</span><span class="sxs-lookup"><span data-stu-id="6e6cd-137">False</span></span>                                                               |
| <span data-ttu-id="6e6cd-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e6cd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6cd-139">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-139">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e6cd-140">Is Indexed</span></span>             | <span data-ttu-id="6e6cd-141">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-141">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e6cd-142">In Global Catalog</span></span>      | <span data-ttu-id="6e6cd-143">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-143">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6cd-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6e6cd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6cd-146">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6cd-147">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-148">Search-Flags</span></span>           | <span data-ttu-id="6e6cd-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e6cd-149">0x00000001</span></span>                                                          |
| <span data-ttu-id="6e6cd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-150">System-Flags</span></span>           | <span data-ttu-id="6e6cd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6cd-151">0x00000010</span></span>                                                          |
| <span data-ttu-id="6e6cd-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e6cd-152">Classes used in</span></span>        | [<span data-ttu-id="6e6cd-153">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-153">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6e6cd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e6cd-154">Windows Server 2003</span></span>



| <span data-ttu-id="6e6cd-155">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-155">Entry</span></span> | <span data-ttu-id="6e6cd-156">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e6cd-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-157">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-158">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6cd-159">System-Only</span></span>            | <span data-ttu-id="6e6cd-160">Falso</span><span class="sxs-lookup"><span data-stu-id="6e6cd-160">False</span></span>                                                               |
| <span data-ttu-id="6e6cd-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e6cd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6cd-162">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-162">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e6cd-163">Is Indexed</span></span>             | <span data-ttu-id="6e6cd-164">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-164">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e6cd-165">In Global Catalog</span></span>      | <span data-ttu-id="6e6cd-166">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-166">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6cd-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-168">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6e6cd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6cd-169">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6cd-170">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-171">Search-Flags</span></span>           | <span data-ttu-id="6e6cd-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e6cd-172">0x00000001</span></span>                                                          |
| <span data-ttu-id="6e6cd-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-173">System-Flags</span></span>           | <span data-ttu-id="6e6cd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6cd-174">0x00000010</span></span>                                                          |
| <span data-ttu-id="6e6cd-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e6cd-175">Classes used in</span></span>        | [<span data-ttu-id="6e6cd-176">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-176">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6e6cd-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6e6cd-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6e6cd-178">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-178">Entry</span></span> | <span data-ttu-id="6e6cd-179">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e6cd-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-180">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-181">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6cd-182">System-Only</span></span>            | <span data-ttu-id="6e6cd-183">Falso</span><span class="sxs-lookup"><span data-stu-id="6e6cd-183">False</span></span>                                                               |
| <span data-ttu-id="6e6cd-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e6cd-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6cd-185">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-185">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e6cd-186">Is Indexed</span></span>             | <span data-ttu-id="6e6cd-187">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-187">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e6cd-188">In Global Catalog</span></span>      | <span data-ttu-id="6e6cd-189">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-189">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6cd-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-191">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6e6cd-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6cd-192">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6cd-193">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-194">Search-Flags</span></span>           | <span data-ttu-id="6e6cd-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e6cd-195">0x00000001</span></span>                                                          |
| <span data-ttu-id="6e6cd-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-196">System-Flags</span></span>           | <span data-ttu-id="6e6cd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6cd-197">0x00000010</span></span>                                                          |
| <span data-ttu-id="6e6cd-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e6cd-198">Classes used in</span></span>        | [<span data-ttu-id="6e6cd-199">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-199">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6e6cd-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e6cd-200">Windows Server 2008</span></span>



| <span data-ttu-id="6e6cd-201">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-201">Entry</span></span> | <span data-ttu-id="6e6cd-202">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-202">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e6cd-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-203">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-204">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6cd-205">System-Only</span></span>            | <span data-ttu-id="6e6cd-206">Falso</span><span class="sxs-lookup"><span data-stu-id="6e6cd-206">False</span></span>                                                               |
| <span data-ttu-id="6e6cd-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e6cd-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6cd-208">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-208">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e6cd-209">Is Indexed</span></span>             | <span data-ttu-id="6e6cd-210">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-210">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e6cd-211">In Global Catalog</span></span>      | <span data-ttu-id="6e6cd-212">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-212">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6cd-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-214">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6e6cd-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6cd-215">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6cd-216">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-217">Search-Flags</span></span>           | <span data-ttu-id="6e6cd-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e6cd-218">0x00000001</span></span>                                                          |
| <span data-ttu-id="6e6cd-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-219">System-Flags</span></span>           | <span data-ttu-id="6e6cd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6cd-220">0x00000010</span></span>                                                          |
| <span data-ttu-id="6e6cd-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e6cd-221">Classes used in</span></span>        | [<span data-ttu-id="6e6cd-222">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-222">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e6cd-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e6cd-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e6cd-224">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-224">Entry</span></span> | <span data-ttu-id="6e6cd-225">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e6cd-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-226">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-227">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6cd-228">System-Only</span></span>            | <span data-ttu-id="6e6cd-229">Falso</span><span class="sxs-lookup"><span data-stu-id="6e6cd-229">False</span></span>                                                               |
| <span data-ttu-id="6e6cd-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e6cd-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6cd-231">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-231">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e6cd-232">Is Indexed</span></span>             | <span data-ttu-id="6e6cd-233">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-233">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e6cd-234">In Global Catalog</span></span>      | <span data-ttu-id="6e6cd-235">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-235">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6cd-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-237">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6e6cd-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6cd-238">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6cd-239">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-240">Search-Flags</span></span>           | <span data-ttu-id="6e6cd-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e6cd-241">0x00000001</span></span>                                                          |
| <span data-ttu-id="6e6cd-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-242">System-Flags</span></span>           | <span data-ttu-id="6e6cd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6cd-243">0x00000010</span></span>                                                          |
| <span data-ttu-id="6e6cd-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e6cd-244">Classes used in</span></span>        | [<span data-ttu-id="6e6cd-245">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-245">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e6cd-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e6cd-246">Windows Server 2012</span></span>



| <span data-ttu-id="6e6cd-247">Voce</span><span class="sxs-lookup"><span data-stu-id="6e6cd-247">Entry</span></span> | <span data-ttu-id="6e6cd-248">Valore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-248">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e6cd-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6e6cd-249">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e6cd-250">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="6e6cd-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e6cd-251">System-Only</span></span>            | <span data-ttu-id="6e6cd-252">Falso</span><span class="sxs-lookup"><span data-stu-id="6e6cd-252">False</span></span>                                                               |
| <span data-ttu-id="6e6cd-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6e6cd-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6e6cd-254">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-254">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6e6cd-255">Is Indexed</span></span>             | <span data-ttu-id="6e6cd-256">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-256">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6e6cd-257">In Global Catalog</span></span>      | <span data-ttu-id="6e6cd-258">Vero</span><span class="sxs-lookup"><span data-stu-id="6e6cd-258">True</span></span>                                                                |
| <span data-ttu-id="6e6cd-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e6cd-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-260">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="6e6cd-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e6cd-261">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e6cd-262">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="6e6cd-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-263">Search-Flags</span></span>           | <span data-ttu-id="6e6cd-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6e6cd-264">0x00000001</span></span>                                                          |
| <span data-ttu-id="6e6cd-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e6cd-265">System-Flags</span></span>           | <span data-ttu-id="6e6cd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e6cd-266">0x00000010</span></span>                                                          |
| <span data-ttu-id="6e6cd-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6e6cd-267">Classes used in</span></span>        | [<span data-ttu-id="6e6cd-268">**MS-SQL-SQLPublication**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-268">**MS-SQL-SQLPublication**</span></span>](c-ms-sql-sqlpublication.md)<br/> |



 

 





