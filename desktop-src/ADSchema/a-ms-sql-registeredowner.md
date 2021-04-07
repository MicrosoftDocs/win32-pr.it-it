---
title: Attributo MS-SQL-RegisteredOwner
description: Proprietario registrato per l'istanza corrente di SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-RegisteredOwner
- Schema AD dell'attributo mS-SQL-RegisteredOwner
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e201494afffdfea59b75bc1901a474469871351
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745202"
---
# <a name="ms-sql-registeredowner-attribute"></a><span data-ttu-id="1ccad-105">Attributo MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="1ccad-105">MS-SQL-RegisteredOwner attribute</span></span>

<span data-ttu-id="1ccad-106">Proprietario registrato per l'istanza corrente di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ccad-106">The registered owner for the current instance of SQL Server.</span></span>



| <span data-ttu-id="1ccad-107">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-107">Entry</span></span> | <span data-ttu-id="1ccad-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1ccad-109">CN</span><span class="sxs-lookup"><span data-stu-id="1ccad-109">CN</span></span>                | <span data-ttu-id="1ccad-110">MS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="1ccad-110">MS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="1ccad-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1ccad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1ccad-112">mS-SQL-RegisteredOwner</span><span class="sxs-lookup"><span data-stu-id="1ccad-112">mS-SQL-RegisteredOwner</span></span>                      |
| <span data-ttu-id="1ccad-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1ccad-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1ccad-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-114">Update Privilege</span></span>  | <span data-ttu-id="1ccad-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="1ccad-115">Domain administrator</span></span>                        |
| <span data-ttu-id="1ccad-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-116">Update Frequency</span></span>  | <span data-ttu-id="1ccad-117">Durante l'installazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="1ccad-117">At system setup.</span></span>                            |
| <span data-ttu-id="1ccad-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-118">Attribute-Id</span></span>      | <span data-ttu-id="1ccad-119">1.2.840.113556.1.4.1364</span><span class="sxs-lookup"><span data-stu-id="1ccad-119">1.2.840.113556.1.4.1364</span></span>                     |
| <span data-ttu-id="1ccad-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1ccad-120">System-Id-Guid</span></span>    | <span data-ttu-id="1ccad-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="1ccad-121">48fd44ea-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="1ccad-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ccad-122">Syntax</span></span>            | [<span data-ttu-id="1ccad-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1ccad-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1ccad-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1ccad-124">Implementations</span></span>

-   [<span data-ttu-id="1ccad-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1ccad-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1ccad-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ccad-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ccad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ccad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ccad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ccad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ccad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ccad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ccad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ccad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1ccad-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ccad-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1ccad-132">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-132">Entry</span></span> | <span data-ttu-id="1ccad-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccad-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-134">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-135">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ccad-136">System-Only</span></span>            | <span data-ttu-id="1ccad-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-137">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1ccad-139">Vero</span><span class="sxs-lookup"><span data-stu-id="1ccad-139">True</span></span>                                                                                                                  |
| <span data-ttu-id="1ccad-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1ccad-140">Is Indexed</span></span>             | <span data-ttu-id="1ccad-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-141">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1ccad-142">In Global Catalog</span></span>      | <span data-ttu-id="1ccad-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-143">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1ccad-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ccad-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1ccad-145">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="1ccad-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ccad-146">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ccad-147">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-148">Search-Flags</span></span>           | <span data-ttu-id="1ccad-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ccad-149">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-150">System-Flags</span></span>           | <span data-ttu-id="1ccad-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ccad-151">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1ccad-152">Classes used in</span></span>        | [<span data-ttu-id="1ccad-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="1ccad-154">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-154">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1ccad-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ccad-155">Windows Server 2003</span></span>



| <span data-ttu-id="1ccad-156">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-156">Entry</span></span> | <span data-ttu-id="1ccad-157">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccad-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-158">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-159">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ccad-160">System-Only</span></span>            | <span data-ttu-id="1ccad-161">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-161">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1ccad-163">Vero</span><span class="sxs-lookup"><span data-stu-id="1ccad-163">True</span></span>                                                                                                                  |
| <span data-ttu-id="1ccad-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1ccad-164">Is Indexed</span></span>             | <span data-ttu-id="1ccad-165">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-165">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1ccad-166">In Global Catalog</span></span>      | <span data-ttu-id="1ccad-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-167">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1ccad-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ccad-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1ccad-169">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="1ccad-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ccad-170">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ccad-171">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-172">Search-Flags</span></span>           | <span data-ttu-id="1ccad-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ccad-173">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-174">System-Flags</span></span>           | <span data-ttu-id="1ccad-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ccad-175">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1ccad-176">Classes used in</span></span>        | [<span data-ttu-id="1ccad-177">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-177">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="1ccad-178">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-178">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ccad-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ccad-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ccad-180">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-180">Entry</span></span> | <span data-ttu-id="1ccad-181">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccad-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-182">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-183">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ccad-184">System-Only</span></span>            | <span data-ttu-id="1ccad-185">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-185">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-186">Is-Single-Valued</span></span>       | <span data-ttu-id="1ccad-187">Vero</span><span class="sxs-lookup"><span data-stu-id="1ccad-187">True</span></span>                                                                                                                  |
| <span data-ttu-id="1ccad-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1ccad-188">Is Indexed</span></span>             | <span data-ttu-id="1ccad-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-189">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1ccad-190">In Global Catalog</span></span>      | <span data-ttu-id="1ccad-191">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-191">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1ccad-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ccad-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1ccad-193">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="1ccad-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ccad-194">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ccad-195">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-196">Search-Flags</span></span>           | <span data-ttu-id="1ccad-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ccad-197">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-198">System-Flags</span></span>           | <span data-ttu-id="1ccad-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ccad-199">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1ccad-200">Classes used in</span></span>        | [<span data-ttu-id="1ccad-201">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-201">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="1ccad-202">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-202">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ccad-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ccad-203">Windows Server 2008</span></span>



| <span data-ttu-id="1ccad-204">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-204">Entry</span></span> | <span data-ttu-id="1ccad-205">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccad-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-206">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-207">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ccad-208">System-Only</span></span>            | <span data-ttu-id="1ccad-209">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-209">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-210">Is-Single-Valued</span></span>       | <span data-ttu-id="1ccad-211">Vero</span><span class="sxs-lookup"><span data-stu-id="1ccad-211">True</span></span>                                                                                                                  |
| <span data-ttu-id="1ccad-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1ccad-212">Is Indexed</span></span>             | <span data-ttu-id="1ccad-213">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-213">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1ccad-214">In Global Catalog</span></span>      | <span data-ttu-id="1ccad-215">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-215">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1ccad-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ccad-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1ccad-217">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="1ccad-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ccad-218">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ccad-219">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-220">Search-Flags</span></span>           | <span data-ttu-id="1ccad-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ccad-221">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-222">System-Flags</span></span>           | <span data-ttu-id="1ccad-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ccad-223">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1ccad-224">Classes used in</span></span>        | [<span data-ttu-id="1ccad-225">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-225">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="1ccad-226">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-226">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ccad-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ccad-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ccad-228">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-228">Entry</span></span> | <span data-ttu-id="1ccad-229">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccad-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-230">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-231">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ccad-232">System-Only</span></span>            | <span data-ttu-id="1ccad-233">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-233">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-234">Is-Single-Valued</span></span>       | <span data-ttu-id="1ccad-235">Vero</span><span class="sxs-lookup"><span data-stu-id="1ccad-235">True</span></span>                                                                                                                  |
| <span data-ttu-id="1ccad-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1ccad-236">Is Indexed</span></span>             | <span data-ttu-id="1ccad-237">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-237">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1ccad-238">In Global Catalog</span></span>      | <span data-ttu-id="1ccad-239">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-239">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1ccad-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ccad-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1ccad-241">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="1ccad-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ccad-242">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ccad-243">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-244">Search-Flags</span></span>           | <span data-ttu-id="1ccad-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ccad-245">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-246">System-Flags</span></span>           | <span data-ttu-id="1ccad-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ccad-247">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1ccad-248">Classes used in</span></span>        | [<span data-ttu-id="1ccad-249">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-249">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="1ccad-250">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-250">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ccad-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ccad-251">Windows Server 2012</span></span>



| <span data-ttu-id="1ccad-252">Voce</span><span class="sxs-lookup"><span data-stu-id="1ccad-252">Entry</span></span> | <span data-ttu-id="1ccad-253">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccad-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccad-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1ccad-254">Link-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ccad-255">MAPI-Id</span></span>                | \-                                                                                                                    |
| <span data-ttu-id="1ccad-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ccad-256">System-Only</span></span>            | <span data-ttu-id="1ccad-257">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-257">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-258">Is-Single-Valued</span></span>       | <span data-ttu-id="1ccad-259">Vero</span><span class="sxs-lookup"><span data-stu-id="1ccad-259">True</span></span>                                                                                                                  |
| <span data-ttu-id="1ccad-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1ccad-260">Is Indexed</span></span>             | <span data-ttu-id="1ccad-261">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1ccad-262">In Global Catalog</span></span>      | <span data-ttu-id="1ccad-263">Falso</span><span class="sxs-lookup"><span data-stu-id="1ccad-263">False</span></span>                                                                                                                 |
| <span data-ttu-id="1ccad-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1ccad-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ccad-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1ccad-265">O:BAG:BAD:S:</span></span>                                                                                                          |
| <span data-ttu-id="1ccad-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ccad-266">Range-Lower</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ccad-267">Range-Upper</span></span>            | \-                                                                                                                    |
| <span data-ttu-id="1ccad-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-268">Search-Flags</span></span>           | <span data-ttu-id="1ccad-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ccad-269">0x00000000</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ccad-270">System-Flags</span></span>           | <span data-ttu-id="1ccad-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ccad-271">0x00000010</span></span>                                                                                                            |
| <span data-ttu-id="1ccad-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1ccad-272">Classes used in</span></span>        | [<span data-ttu-id="1ccad-273">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-273">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> [<span data-ttu-id="1ccad-274">**MS-SQL-OLAPServer**</span><span class="sxs-lookup"><span data-stu-id="1ccad-274">**MS-SQL-OLAPServer**</span></span>](c-ms-sql-olapserver.md)<br/> |



 

 





