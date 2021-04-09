---
title: Attributo MS-SQL-LastDiagnosticDate
description: Data dell'ultima esecuzione di DBCC CHECKDB.
ms.assetid: 7060e111-e4cb-4c5a-bce1-32712cbea00e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-LastDiagnosticDate
- Schema AD dell'attributo mS-SQL-LastDiagnosticDate
topic_type:
- apiref
api_name:
- MS-SQL-LastDiagnosticDate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f25b8322a9f83b96c0ab4883478e6c0ffa2f3b49
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744319"
---
# <a name="ms-sql-lastdiagnosticdate-attribute"></a><span data-ttu-id="23775-105">Attributo MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="23775-105">MS-SQL-LastDiagnosticDate attribute</span></span>

<span data-ttu-id="23775-106">Data dell'ultima esecuzione di DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="23775-106">The last date that DBCC checkdb was run.</span></span>



| <span data-ttu-id="23775-107">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-107">Entry</span></span> | <span data-ttu-id="23775-108">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="23775-109">CN</span><span class="sxs-lookup"><span data-stu-id="23775-109">CN</span></span>                | <span data-ttu-id="23775-110">MS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="23775-110">MS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="23775-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="23775-111">Ldap-Display-Name</span></span> | <span data-ttu-id="23775-112">mS-SQL-LastDiagnosticDate</span><span class="sxs-lookup"><span data-stu-id="23775-112">mS-SQL-LastDiagnosticDate</span></span>                   |
| <span data-ttu-id="23775-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="23775-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="23775-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="23775-114">Update Privilege</span></span>  | <span data-ttu-id="23775-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="23775-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="23775-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="23775-116">Update Frequency</span></span>  | <span data-ttu-id="23775-117">Quando viene eseguito DBCC CHECKDB.</span><span class="sxs-lookup"><span data-stu-id="23775-117">When DBCC checkdb is run.</span></span>                   |
| <span data-ttu-id="23775-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="23775-118">Attribute-Id</span></span>      | <span data-ttu-id="23775-119">1.2.840.113556.1.4.1399</span><span class="sxs-lookup"><span data-stu-id="23775-119">1.2.840.113556.1.4.1399</span></span>                     |
| <span data-ttu-id="23775-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="23775-120">System-Id-Guid</span></span>    | <span data-ttu-id="23775-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="23775-121">f6d6dd88-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="23775-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23775-122">Syntax</span></span>            | [<span data-ttu-id="23775-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="23775-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="23775-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="23775-124">Implementations</span></span>

-   [<span data-ttu-id="23775-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="23775-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="23775-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="23775-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="23775-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="23775-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="23775-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="23775-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="23775-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="23775-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="23775-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="23775-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="23775-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23775-131">Windows 2000 Server</span></span>



| <span data-ttu-id="23775-132">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-132">Entry</span></span> | <span data-ttu-id="23775-133">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-133">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23775-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="23775-134">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23775-135">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="23775-136">System-Only</span></span>            | <span data-ttu-id="23775-137">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-137">False</span></span>                                                         |
| <span data-ttu-id="23775-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="23775-138">Is-Single-Valued</span></span>       | <span data-ttu-id="23775-139">Vero</span><span class="sxs-lookup"><span data-stu-id="23775-139">True</span></span>                                                          |
| <span data-ttu-id="23775-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="23775-140">Is Indexed</span></span>             | <span data-ttu-id="23775-141">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-141">False</span></span>                                                         |
| <span data-ttu-id="23775-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="23775-142">In Global Catalog</span></span>      | <span data-ttu-id="23775-143">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-143">False</span></span>                                                         |
| <span data-ttu-id="23775-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="23775-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="23775-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="23775-145">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="23775-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23775-146">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="23775-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23775-147">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="23775-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-148">Search-Flags</span></span>           | <span data-ttu-id="23775-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23775-149">0x00000000</span></span>                                                    |
| <span data-ttu-id="23775-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-150">System-Flags</span></span>           | <span data-ttu-id="23775-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23775-151">0x00000010</span></span>                                                    |
| <span data-ttu-id="23775-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="23775-152">Classes used in</span></span>        | [<span data-ttu-id="23775-153">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="23775-153">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="23775-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="23775-154">Windows Server 2003</span></span>



| <span data-ttu-id="23775-155">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-155">Entry</span></span> | <span data-ttu-id="23775-156">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-156">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23775-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="23775-157">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23775-158">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="23775-159">System-Only</span></span>            | <span data-ttu-id="23775-160">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-160">False</span></span>                                                         |
| <span data-ttu-id="23775-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="23775-161">Is-Single-Valued</span></span>       | <span data-ttu-id="23775-162">Vero</span><span class="sxs-lookup"><span data-stu-id="23775-162">True</span></span>                                                          |
| <span data-ttu-id="23775-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="23775-163">Is Indexed</span></span>             | <span data-ttu-id="23775-164">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-164">False</span></span>                                                         |
| <span data-ttu-id="23775-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="23775-165">In Global Catalog</span></span>      | <span data-ttu-id="23775-166">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-166">False</span></span>                                                         |
| <span data-ttu-id="23775-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="23775-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="23775-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="23775-168">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="23775-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23775-169">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="23775-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23775-170">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="23775-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-171">Search-Flags</span></span>           | <span data-ttu-id="23775-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23775-172">0x00000000</span></span>                                                    |
| <span data-ttu-id="23775-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-173">System-Flags</span></span>           | <span data-ttu-id="23775-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23775-174">0x00000010</span></span>                                                    |
| <span data-ttu-id="23775-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="23775-175">Classes used in</span></span>        | [<span data-ttu-id="23775-176">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="23775-176">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="23775-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="23775-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="23775-178">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-178">Entry</span></span> | <span data-ttu-id="23775-179">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-179">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23775-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="23775-180">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23775-181">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="23775-182">System-Only</span></span>            | <span data-ttu-id="23775-183">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-183">False</span></span>                                                         |
| <span data-ttu-id="23775-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="23775-184">Is-Single-Valued</span></span>       | <span data-ttu-id="23775-185">Vero</span><span class="sxs-lookup"><span data-stu-id="23775-185">True</span></span>                                                          |
| <span data-ttu-id="23775-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="23775-186">Is Indexed</span></span>             | <span data-ttu-id="23775-187">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-187">False</span></span>                                                         |
| <span data-ttu-id="23775-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="23775-188">In Global Catalog</span></span>      | <span data-ttu-id="23775-189">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-189">False</span></span>                                                         |
| <span data-ttu-id="23775-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="23775-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="23775-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="23775-191">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="23775-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23775-192">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="23775-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23775-193">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="23775-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-194">Search-Flags</span></span>           | <span data-ttu-id="23775-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23775-195">0x00000000</span></span>                                                    |
| <span data-ttu-id="23775-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-196">System-Flags</span></span>           | <span data-ttu-id="23775-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23775-197">0x00000010</span></span>                                                    |
| <span data-ttu-id="23775-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="23775-198">Classes used in</span></span>        | [<span data-ttu-id="23775-199">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="23775-199">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="23775-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23775-200">Windows Server 2008</span></span>



| <span data-ttu-id="23775-201">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-201">Entry</span></span> | <span data-ttu-id="23775-202">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-202">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23775-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="23775-203">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23775-204">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="23775-205">System-Only</span></span>            | <span data-ttu-id="23775-206">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-206">False</span></span>                                                         |
| <span data-ttu-id="23775-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="23775-207">Is-Single-Valued</span></span>       | <span data-ttu-id="23775-208">Vero</span><span class="sxs-lookup"><span data-stu-id="23775-208">True</span></span>                                                          |
| <span data-ttu-id="23775-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="23775-209">Is Indexed</span></span>             | <span data-ttu-id="23775-210">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-210">False</span></span>                                                         |
| <span data-ttu-id="23775-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="23775-211">In Global Catalog</span></span>      | <span data-ttu-id="23775-212">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-212">False</span></span>                                                         |
| <span data-ttu-id="23775-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="23775-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="23775-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="23775-214">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="23775-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23775-215">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="23775-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23775-216">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="23775-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-217">Search-Flags</span></span>           | <span data-ttu-id="23775-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23775-218">0x00000000</span></span>                                                    |
| <span data-ttu-id="23775-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-219">System-Flags</span></span>           | <span data-ttu-id="23775-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23775-220">0x00000010</span></span>                                                    |
| <span data-ttu-id="23775-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="23775-221">Classes used in</span></span>        | [<span data-ttu-id="23775-222">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="23775-222">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="23775-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="23775-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="23775-224">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-224">Entry</span></span> | <span data-ttu-id="23775-225">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-225">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23775-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="23775-226">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23775-227">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="23775-228">System-Only</span></span>            | <span data-ttu-id="23775-229">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-229">False</span></span>                                                         |
| <span data-ttu-id="23775-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="23775-230">Is-Single-Valued</span></span>       | <span data-ttu-id="23775-231">Vero</span><span class="sxs-lookup"><span data-stu-id="23775-231">True</span></span>                                                          |
| <span data-ttu-id="23775-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="23775-232">Is Indexed</span></span>             | <span data-ttu-id="23775-233">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-233">False</span></span>                                                         |
| <span data-ttu-id="23775-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="23775-234">In Global Catalog</span></span>      | <span data-ttu-id="23775-235">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-235">False</span></span>                                                         |
| <span data-ttu-id="23775-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="23775-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="23775-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="23775-237">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="23775-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23775-238">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="23775-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23775-239">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="23775-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-240">Search-Flags</span></span>           | <span data-ttu-id="23775-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23775-241">0x00000000</span></span>                                                    |
| <span data-ttu-id="23775-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-242">System-Flags</span></span>           | <span data-ttu-id="23775-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23775-243">0x00000010</span></span>                                                    |
| <span data-ttu-id="23775-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="23775-244">Classes used in</span></span>        | [<span data-ttu-id="23775-245">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="23775-245">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="23775-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23775-246">Windows Server 2012</span></span>



| <span data-ttu-id="23775-247">Voce</span><span class="sxs-lookup"><span data-stu-id="23775-247">Entry</span></span> | <span data-ttu-id="23775-248">Valore</span><span class="sxs-lookup"><span data-stu-id="23775-248">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="23775-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="23775-249">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="23775-250">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="23775-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="23775-251">System-Only</span></span>            | <span data-ttu-id="23775-252">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-252">False</span></span>                                                         |
| <span data-ttu-id="23775-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="23775-253">Is-Single-Valued</span></span>       | <span data-ttu-id="23775-254">Vero</span><span class="sxs-lookup"><span data-stu-id="23775-254">True</span></span>                                                          |
| <span data-ttu-id="23775-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="23775-255">Is Indexed</span></span>             | <span data-ttu-id="23775-256">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-256">False</span></span>                                                         |
| <span data-ttu-id="23775-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="23775-257">In Global Catalog</span></span>      | <span data-ttu-id="23775-258">Falso</span><span class="sxs-lookup"><span data-stu-id="23775-258">False</span></span>                                                         |
| <span data-ttu-id="23775-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="23775-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="23775-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="23775-260">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="23775-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="23775-261">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="23775-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="23775-262">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="23775-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-263">Search-Flags</span></span>           | <span data-ttu-id="23775-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23775-264">0x00000000</span></span>                                                    |
| <span data-ttu-id="23775-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="23775-265">System-Flags</span></span>           | <span data-ttu-id="23775-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23775-266">0x00000010</span></span>                                                    |
| <span data-ttu-id="23775-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="23775-267">Classes used in</span></span>        | [<span data-ttu-id="23775-268">**MS-SQL-SQLDatabase**</span><span class="sxs-lookup"><span data-stu-id="23775-268">**MS-SQL-SQLDatabase**</span></span>](c-ms-sql-sqldatabase.md)<br/> |



 

 





