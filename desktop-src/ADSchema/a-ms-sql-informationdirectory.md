---
title: Attributo MS-SQL-InformationDirectory
description: Directory Informativa per l'istanza corrente di SQL Server.
ms.assetid: fec29b94-b136-4862-8615-7190b3b45ec3
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-InformationDirectory
- Schema AD dell'attributo mS-SQL-InformationDirectory
topic_type:
- apiref
api_name:
- MS-SQL-InformationDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a5ca19d6c746e6e5874e82010fcbca367c1157
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303568"
---
# <a name="ms-sql-informationdirectory-attribute"></a><span data-ttu-id="2e093-105">Attributo MS-SQL-InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="2e093-105">MS-SQL-InformationDirectory attribute</span></span>

<span data-ttu-id="2e093-106">Directory Informativa per l'istanza corrente di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2e093-106">The informational directory for the current instance of SQL Server.</span></span>



| <span data-ttu-id="2e093-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-107">Entry</span></span> | <span data-ttu-id="2e093-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="2e093-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e093-109">CN</span></span>                | <span data-ttu-id="2e093-110">MS-SQL-InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="2e093-110">MS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="2e093-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e093-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e093-112">mS-SQL-InformationDirectory</span><span class="sxs-lookup"><span data-stu-id="2e093-112">mS-SQL-InformationDirectory</span></span>              |
| <span data-ttu-id="2e093-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2e093-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="2e093-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e093-114">Update Privilege</span></span>  | <span data-ttu-id="2e093-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="2e093-115">Domain administrator</span></span>                     |
| <span data-ttu-id="2e093-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e093-116">Update Frequency</span></span>  | <span data-ttu-id="2e093-117">All'avvio del sistema o quando Active Directory viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2e093-117">At system startup or when AD is updated.</span></span> |
| <span data-ttu-id="2e093-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-118">Attribute-Id</span></span>      | <span data-ttu-id="2e093-119">1.2.840.113556.1.4.1392</span><span class="sxs-lookup"><span data-stu-id="2e093-119">1.2.840.113556.1.4.1392</span></span>                  |
| <span data-ttu-id="2e093-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e093-120">System-Id-Guid</span></span>    | <span data-ttu-id="2e093-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2e093-121">d0aedb2e-ccee-11d2-9993-0000f87a57d4</span></span>     |
| <span data-ttu-id="2e093-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e093-122">Syntax</span></span>            | [<span data-ttu-id="2e093-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2e093-123">**Boolean**</span></span>](s-boolean.md)             |



## <a name="implementations"></a><span data-ttu-id="2e093-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2e093-124">Implementations</span></span>

-   [<span data-ttu-id="2e093-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e093-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e093-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e093-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e093-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e093-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e093-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e093-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e093-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e093-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e093-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e093-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e093-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e093-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2e093-132">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-132">Entry</span></span> | <span data-ttu-id="2e093-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e093-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e093-134">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-135">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e093-136">System-Only</span></span>            | <span data-ttu-id="2e093-137">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-137">False</span></span>                                                             |
| <span data-ttu-id="2e093-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e093-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2e093-139">Vero</span><span class="sxs-lookup"><span data-stu-id="2e093-139">True</span></span>                                                              |
| <span data-ttu-id="2e093-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e093-140">Is Indexed</span></span>             | <span data-ttu-id="2e093-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-141">False</span></span>                                                             |
| <span data-ttu-id="2e093-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e093-142">In Global Catalog</span></span>      | <span data-ttu-id="2e093-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-143">False</span></span>                                                             |
| <span data-ttu-id="2e093-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e093-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e093-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e093-145">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e093-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e093-146">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e093-147">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-148">Search-Flags</span></span>           | <span data-ttu-id="2e093-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e093-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e093-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-150">System-Flags</span></span>           | <span data-ttu-id="2e093-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e093-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e093-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e093-152">Classes used in</span></span>        | [<span data-ttu-id="2e093-153">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="2e093-153">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e093-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e093-154">Windows Server 2003</span></span>



| <span data-ttu-id="2e093-155">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-155">Entry</span></span> | <span data-ttu-id="2e093-156">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e093-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e093-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e093-159">System-Only</span></span>            | <span data-ttu-id="2e093-160">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-160">False</span></span>                                                             |
| <span data-ttu-id="2e093-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e093-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2e093-162">Vero</span><span class="sxs-lookup"><span data-stu-id="2e093-162">True</span></span>                                                              |
| <span data-ttu-id="2e093-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e093-163">Is Indexed</span></span>             | <span data-ttu-id="2e093-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-164">False</span></span>                                                             |
| <span data-ttu-id="2e093-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e093-165">In Global Catalog</span></span>      | <span data-ttu-id="2e093-166">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-166">False</span></span>                                                             |
| <span data-ttu-id="2e093-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e093-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e093-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e093-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e093-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e093-169">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e093-170">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-171">Search-Flags</span></span>           | <span data-ttu-id="2e093-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e093-172">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e093-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-173">System-Flags</span></span>           | <span data-ttu-id="2e093-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e093-174">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e093-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e093-175">Classes used in</span></span>        | [<span data-ttu-id="2e093-176">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="2e093-176">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e093-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e093-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e093-178">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-178">Entry</span></span> | <span data-ttu-id="2e093-179">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e093-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e093-180">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-181">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e093-182">System-Only</span></span>            | <span data-ttu-id="2e093-183">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-183">False</span></span>                                                             |
| <span data-ttu-id="2e093-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e093-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2e093-185">Vero</span><span class="sxs-lookup"><span data-stu-id="2e093-185">True</span></span>                                                              |
| <span data-ttu-id="2e093-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e093-186">Is Indexed</span></span>             | <span data-ttu-id="2e093-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-187">False</span></span>                                                             |
| <span data-ttu-id="2e093-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e093-188">In Global Catalog</span></span>      | <span data-ttu-id="2e093-189">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-189">False</span></span>                                                             |
| <span data-ttu-id="2e093-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e093-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e093-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e093-191">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e093-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e093-192">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e093-193">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-194">Search-Flags</span></span>           | <span data-ttu-id="2e093-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e093-195">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e093-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-196">System-Flags</span></span>           | <span data-ttu-id="2e093-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e093-197">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e093-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e093-198">Classes used in</span></span>        | [<span data-ttu-id="2e093-199">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="2e093-199">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e093-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e093-200">Windows Server 2008</span></span>



| <span data-ttu-id="2e093-201">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-201">Entry</span></span> | <span data-ttu-id="2e093-202">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e093-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e093-203">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-204">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e093-205">System-Only</span></span>            | <span data-ttu-id="2e093-206">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-206">False</span></span>                                                             |
| <span data-ttu-id="2e093-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e093-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2e093-208">Vero</span><span class="sxs-lookup"><span data-stu-id="2e093-208">True</span></span>                                                              |
| <span data-ttu-id="2e093-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e093-209">Is Indexed</span></span>             | <span data-ttu-id="2e093-210">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-210">False</span></span>                                                             |
| <span data-ttu-id="2e093-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e093-211">In Global Catalog</span></span>      | <span data-ttu-id="2e093-212">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-212">False</span></span>                                                             |
| <span data-ttu-id="2e093-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e093-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e093-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e093-214">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e093-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e093-215">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e093-216">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-217">Search-Flags</span></span>           | <span data-ttu-id="2e093-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e093-218">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e093-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-219">System-Flags</span></span>           | <span data-ttu-id="2e093-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e093-220">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e093-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e093-221">Classes used in</span></span>        | [<span data-ttu-id="2e093-222">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="2e093-222">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e093-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e093-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e093-224">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-224">Entry</span></span> | <span data-ttu-id="2e093-225">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e093-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e093-226">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-227">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e093-228">System-Only</span></span>            | <span data-ttu-id="2e093-229">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-229">False</span></span>                                                             |
| <span data-ttu-id="2e093-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e093-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2e093-231">Vero</span><span class="sxs-lookup"><span data-stu-id="2e093-231">True</span></span>                                                              |
| <span data-ttu-id="2e093-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e093-232">Is Indexed</span></span>             | <span data-ttu-id="2e093-233">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-233">False</span></span>                                                             |
| <span data-ttu-id="2e093-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e093-234">In Global Catalog</span></span>      | <span data-ttu-id="2e093-235">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-235">False</span></span>                                                             |
| <span data-ttu-id="2e093-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e093-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e093-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e093-237">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e093-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e093-238">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e093-239">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-240">Search-Flags</span></span>           | <span data-ttu-id="2e093-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e093-241">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e093-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-242">System-Flags</span></span>           | <span data-ttu-id="2e093-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e093-243">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e093-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e093-244">Classes used in</span></span>        | [<span data-ttu-id="2e093-245">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="2e093-245">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e093-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e093-246">Windows Server 2012</span></span>



| <span data-ttu-id="2e093-247">Voce</span><span class="sxs-lookup"><span data-stu-id="2e093-247">Entry</span></span> | <span data-ttu-id="2e093-248">Valore</span><span class="sxs-lookup"><span data-stu-id="2e093-248">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2e093-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2e093-249">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e093-250">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="2e093-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e093-251">System-Only</span></span>            | <span data-ttu-id="2e093-252">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-252">False</span></span>                                                             |
| <span data-ttu-id="2e093-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2e093-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2e093-254">Vero</span><span class="sxs-lookup"><span data-stu-id="2e093-254">True</span></span>                                                              |
| <span data-ttu-id="2e093-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2e093-255">Is Indexed</span></span>             | <span data-ttu-id="2e093-256">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-256">False</span></span>                                                             |
| <span data-ttu-id="2e093-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2e093-257">In Global Catalog</span></span>      | <span data-ttu-id="2e093-258">Falso</span><span class="sxs-lookup"><span data-stu-id="2e093-258">False</span></span>                                                             |
| <span data-ttu-id="2e093-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2e093-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e093-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2e093-260">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="2e093-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e093-261">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e093-262">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="2e093-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-263">Search-Flags</span></span>           | <span data-ttu-id="2e093-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e093-264">0x00000000</span></span>                                                        |
| <span data-ttu-id="2e093-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e093-265">System-Flags</span></span>           | <span data-ttu-id="2e093-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e093-266">0x00000010</span></span>                                                        |
| <span data-ttu-id="2e093-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2e093-267">Classes used in</span></span>        | [<span data-ttu-id="2e093-268">**MS-SQL-SQLRepository**</span><span class="sxs-lookup"><span data-stu-id="2e093-268">**MS-SQL-SQLRepository**</span></span>](c-ms-sql-sqlrepository.md)<br/> |



 

 





