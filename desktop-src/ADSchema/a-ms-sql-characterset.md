---
title: Attributo MS-SQL-characters
description: Set di caratteri per l'istanza corrente di SQL Server.
ms.assetid: 5c45058f-e883-455c-8e18-415ddae149f8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-characters
- Schema AD dell'attributo mS-SQL-characters
topic_type:
- apiref
api_name:
- MS-SQL-CharacterSet
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2f3718c9e47393498e42c4091283ea768d5072
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875786"
---
# <a name="ms-sql-characterset-attribute"></a><span data-ttu-id="da3b0-105">Attributo MS-SQL-characters</span><span class="sxs-lookup"><span data-stu-id="da3b0-105">MS-SQL-CharacterSet attribute</span></span>

<span data-ttu-id="da3b0-106">Set di caratteri per l'istanza corrente di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da3b0-106">The character set for the current instance of SQL Server.</span></span>



| <span data-ttu-id="da3b0-107">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-107">Entry</span></span> | <span data-ttu-id="da3b0-108">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="da3b0-109">CN</span><span class="sxs-lookup"><span data-stu-id="da3b0-109">CN</span></span>                | <span data-ttu-id="da3b0-110">Il carattere MS-SQL</span><span class="sxs-lookup"><span data-stu-id="da3b0-110">MS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="da3b0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da3b0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="da3b0-112">il carattere mS-SQL</span><span class="sxs-lookup"><span data-stu-id="da3b0-112">mS-SQL-CharacterSet</span></span>                  |
| <span data-ttu-id="da3b0-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="da3b0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="da3b0-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-114">Update Privilege</span></span>  | <span data-ttu-id="da3b0-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="da3b0-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="da3b0-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-116">Update Frequency</span></span>  | <span data-ttu-id="da3b0-117">All'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="da3b0-117">At system startup.</span></span>                   |
| <span data-ttu-id="da3b0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-118">Attribute-Id</span></span>      | <span data-ttu-id="da3b0-119">1.2.840.113556.1.4.1370</span><span class="sxs-lookup"><span data-stu-id="da3b0-119">1.2.840.113556.1.4.1370</span></span>              |
| <span data-ttu-id="da3b0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da3b0-120">System-Id-Guid</span></span>    | <span data-ttu-id="da3b0-121">696177a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="da3b0-121">696177a6-ccee-11d2-9993-0000f87a57d4</span></span> |
| <span data-ttu-id="da3b0-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da3b0-122">Syntax</span></span>            | [<span data-ttu-id="da3b0-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="da3b0-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="da3b0-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="da3b0-124">Implementations</span></span>

-   [<span data-ttu-id="da3b0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da3b0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da3b0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da3b0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da3b0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da3b0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da3b0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da3b0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da3b0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da3b0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da3b0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da3b0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da3b0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da3b0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="da3b0-132">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-132">Entry</span></span> | <span data-ttu-id="da3b0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da3b0-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3b0-136">System-Only</span></span>            | <span data-ttu-id="da3b0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-137">False</span></span>                                                     |
| <span data-ttu-id="da3b0-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da3b0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="da3b0-139">Vero</span><span class="sxs-lookup"><span data-stu-id="da3b0-139">True</span></span>                                                      |
| <span data-ttu-id="da3b0-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da3b0-140">Is Indexed</span></span>             | <span data-ttu-id="da3b0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-141">False</span></span>                                                     |
| <span data-ttu-id="da3b0-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da3b0-142">In Global Catalog</span></span>      | <span data-ttu-id="da3b0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-143">False</span></span>                                                     |
| <span data-ttu-id="da3b0-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da3b0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3b0-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da3b0-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="da3b0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3b0-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3b0-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-148">Search-Flags</span></span>           | <span data-ttu-id="da3b0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3b0-149">0x00000000</span></span>                                                |
| <span data-ttu-id="da3b0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-150">System-Flags</span></span>           | <span data-ttu-id="da3b0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3b0-151">0x00000010</span></span>                                                |
| <span data-ttu-id="da3b0-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da3b0-152">Classes used in</span></span>        | [<span data-ttu-id="da3b0-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="da3b0-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da3b0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da3b0-154">Windows Server 2003</span></span>



| <span data-ttu-id="da3b0-155">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-155">Entry</span></span> | <span data-ttu-id="da3b0-156">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da3b0-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3b0-159">System-Only</span></span>            | <span data-ttu-id="da3b0-160">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-160">False</span></span>                                                     |
| <span data-ttu-id="da3b0-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da3b0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="da3b0-162">Vero</span><span class="sxs-lookup"><span data-stu-id="da3b0-162">True</span></span>                                                      |
| <span data-ttu-id="da3b0-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da3b0-163">Is Indexed</span></span>             | <span data-ttu-id="da3b0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-164">False</span></span>                                                     |
| <span data-ttu-id="da3b0-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da3b0-165">In Global Catalog</span></span>      | <span data-ttu-id="da3b0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-166">False</span></span>                                                     |
| <span data-ttu-id="da3b0-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da3b0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3b0-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da3b0-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="da3b0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3b0-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3b0-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-171">Search-Flags</span></span>           | <span data-ttu-id="da3b0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3b0-172">0x00000000</span></span>                                                |
| <span data-ttu-id="da3b0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-173">System-Flags</span></span>           | <span data-ttu-id="da3b0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3b0-174">0x00000010</span></span>                                                |
| <span data-ttu-id="da3b0-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da3b0-175">Classes used in</span></span>        | [<span data-ttu-id="da3b0-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="da3b0-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da3b0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da3b0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da3b0-178">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-178">Entry</span></span> | <span data-ttu-id="da3b0-179">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da3b0-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3b0-182">System-Only</span></span>            | <span data-ttu-id="da3b0-183">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-183">False</span></span>                                                     |
| <span data-ttu-id="da3b0-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da3b0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="da3b0-185">Vero</span><span class="sxs-lookup"><span data-stu-id="da3b0-185">True</span></span>                                                      |
| <span data-ttu-id="da3b0-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da3b0-186">Is Indexed</span></span>             | <span data-ttu-id="da3b0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-187">False</span></span>                                                     |
| <span data-ttu-id="da3b0-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da3b0-188">In Global Catalog</span></span>      | <span data-ttu-id="da3b0-189">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-189">False</span></span>                                                     |
| <span data-ttu-id="da3b0-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da3b0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3b0-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da3b0-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="da3b0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3b0-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3b0-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-194">Search-Flags</span></span>           | <span data-ttu-id="da3b0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3b0-195">0x00000000</span></span>                                                |
| <span data-ttu-id="da3b0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-196">System-Flags</span></span>           | <span data-ttu-id="da3b0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3b0-197">0x00000010</span></span>                                                |
| <span data-ttu-id="da3b0-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da3b0-198">Classes used in</span></span>        | [<span data-ttu-id="da3b0-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="da3b0-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da3b0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da3b0-200">Windows Server 2008</span></span>



| <span data-ttu-id="da3b0-201">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-201">Entry</span></span> | <span data-ttu-id="da3b0-202">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da3b0-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3b0-205">System-Only</span></span>            | <span data-ttu-id="da3b0-206">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-206">False</span></span>                                                     |
| <span data-ttu-id="da3b0-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da3b0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="da3b0-208">Vero</span><span class="sxs-lookup"><span data-stu-id="da3b0-208">True</span></span>                                                      |
| <span data-ttu-id="da3b0-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da3b0-209">Is Indexed</span></span>             | <span data-ttu-id="da3b0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-210">False</span></span>                                                     |
| <span data-ttu-id="da3b0-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da3b0-211">In Global Catalog</span></span>      | <span data-ttu-id="da3b0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-212">False</span></span>                                                     |
| <span data-ttu-id="da3b0-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da3b0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3b0-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da3b0-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="da3b0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3b0-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3b0-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-217">Search-Flags</span></span>           | <span data-ttu-id="da3b0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3b0-218">0x00000000</span></span>                                                |
| <span data-ttu-id="da3b0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-219">System-Flags</span></span>           | <span data-ttu-id="da3b0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3b0-220">0x00000010</span></span>                                                |
| <span data-ttu-id="da3b0-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da3b0-221">Classes used in</span></span>        | [<span data-ttu-id="da3b0-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="da3b0-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da3b0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da3b0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da3b0-224">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-224">Entry</span></span> | <span data-ttu-id="da3b0-225">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da3b0-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3b0-228">System-Only</span></span>            | <span data-ttu-id="da3b0-229">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-229">False</span></span>                                                     |
| <span data-ttu-id="da3b0-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da3b0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="da3b0-231">Vero</span><span class="sxs-lookup"><span data-stu-id="da3b0-231">True</span></span>                                                      |
| <span data-ttu-id="da3b0-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da3b0-232">Is Indexed</span></span>             | <span data-ttu-id="da3b0-233">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-233">False</span></span>                                                     |
| <span data-ttu-id="da3b0-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da3b0-234">In Global Catalog</span></span>      | <span data-ttu-id="da3b0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-235">False</span></span>                                                     |
| <span data-ttu-id="da3b0-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da3b0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3b0-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da3b0-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="da3b0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3b0-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3b0-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-240">Search-Flags</span></span>           | <span data-ttu-id="da3b0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3b0-241">0x00000000</span></span>                                                |
| <span data-ttu-id="da3b0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-242">System-Flags</span></span>           | <span data-ttu-id="da3b0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3b0-243">0x00000010</span></span>                                                |
| <span data-ttu-id="da3b0-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da3b0-244">Classes used in</span></span>        | [<span data-ttu-id="da3b0-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="da3b0-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da3b0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da3b0-246">Windows Server 2012</span></span>



| <span data-ttu-id="da3b0-247">Voce</span><span class="sxs-lookup"><span data-stu-id="da3b0-247">Entry</span></span> | <span data-ttu-id="da3b0-248">Valore</span><span class="sxs-lookup"><span data-stu-id="da3b0-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="da3b0-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da3b0-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da3b0-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="da3b0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="da3b0-251">System-Only</span></span>            | <span data-ttu-id="da3b0-252">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-252">False</span></span>                                                     |
| <span data-ttu-id="da3b0-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da3b0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="da3b0-254">Vero</span><span class="sxs-lookup"><span data-stu-id="da3b0-254">True</span></span>                                                      |
| <span data-ttu-id="da3b0-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da3b0-255">Is Indexed</span></span>             | <span data-ttu-id="da3b0-256">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-256">False</span></span>                                                     |
| <span data-ttu-id="da3b0-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da3b0-257">In Global Catalog</span></span>      | <span data-ttu-id="da3b0-258">Falso</span><span class="sxs-lookup"><span data-stu-id="da3b0-258">False</span></span>                                                     |
| <span data-ttu-id="da3b0-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da3b0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="da3b0-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da3b0-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="da3b0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da3b0-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da3b0-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="da3b0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-263">Search-Flags</span></span>           | <span data-ttu-id="da3b0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da3b0-264">0x00000000</span></span>                                                |
| <span data-ttu-id="da3b0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da3b0-265">System-Flags</span></span>           | <span data-ttu-id="da3b0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da3b0-266">0x00000010</span></span>                                                |
| <span data-ttu-id="da3b0-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da3b0-267">Classes used in</span></span>        | [<span data-ttu-id="da3b0-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="da3b0-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





