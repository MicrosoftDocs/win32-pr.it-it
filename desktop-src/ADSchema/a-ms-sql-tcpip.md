---
title: Attributo MS-SQL-TCPIP
description: Punto di connessione TCP.
ms.assetid: f61f7d54-958e-4f34-852e-222338c26de0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo MS-SQL-TCPIP
- Schema AD dell'attributo mS-SQL-TCPIP
topic_type:
- apiref
api_name:
- MS-SQL-TCPIP
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 098d5e7818789774b425ad9e238f8f3b3a4d5378
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303566"
---
# <a name="ms-sql-tcpip-attribute"></a><span data-ttu-id="a0c47-105">Attributo MS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="a0c47-105">MS-SQL-TCPIP attribute</span></span>

<span data-ttu-id="a0c47-106">Punto di connessione TCP.</span><span class="sxs-lookup"><span data-stu-id="a0c47-106">The TCP connection point.</span></span>



| <span data-ttu-id="a0c47-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-107">Entry</span></span> | <span data-ttu-id="a0c47-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a0c47-109">CN</span><span class="sxs-lookup"><span data-stu-id="a0c47-109">CN</span></span>                | <span data-ttu-id="a0c47-110">MS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="a0c47-110">MS-SQL-TCPIP</span></span>                                |
| <span data-ttu-id="a0c47-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a0c47-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a0c47-112">mS-SQL-TCPIP</span><span class="sxs-lookup"><span data-stu-id="a0c47-112">mS-SQL-TCPIP</span></span>                                |
| <span data-ttu-id="a0c47-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a0c47-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a0c47-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-114">Update Privilege</span></span>  | <span data-ttu-id="a0c47-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a0c47-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="a0c47-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-116">Update Frequency</span></span>  | <span data-ttu-id="a0c47-117">All'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a0c47-117">At system startup.</span></span>                          |
| <span data-ttu-id="a0c47-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-118">Attribute-Id</span></span>      | <span data-ttu-id="a0c47-119">1.2.840.113556.1.4.1377</span><span class="sxs-lookup"><span data-stu-id="a0c47-119">1.2.840.113556.1.4.1377</span></span>                     |
| <span data-ttu-id="a0c47-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a0c47-120">System-Id-Guid</span></span>    | <span data-ttu-id="a0c47-121">8ac263a6-ccee-11d2-9993-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a0c47-121">8ac263a6-ccee-11d2-9993-0000f87a57d4</span></span>        |
| <span data-ttu-id="a0c47-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0c47-122">Syntax</span></span>            | [<span data-ttu-id="a0c47-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a0c47-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a0c47-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a0c47-124">Implementations</span></span>

-   [<span data-ttu-id="a0c47-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a0c47-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a0c47-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0c47-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0c47-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0c47-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0c47-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0c47-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0c47-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0c47-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0c47-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0c47-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a0c47-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0c47-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a0c47-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-132">Entry</span></span> | <span data-ttu-id="a0c47-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0c47-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0c47-136">System-Only</span></span>            | <span data-ttu-id="a0c47-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-137">False</span></span>                                                     |
| <span data-ttu-id="a0c47-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a0c47-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a0c47-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a0c47-139">True</span></span>                                                      |
| <span data-ttu-id="a0c47-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a0c47-140">Is Indexed</span></span>             | <span data-ttu-id="a0c47-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-141">False</span></span>                                                     |
| <span data-ttu-id="a0c47-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a0c47-142">In Global Catalog</span></span>      | <span data-ttu-id="a0c47-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-143">False</span></span>                                                     |
| <span data-ttu-id="a0c47-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a0c47-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0c47-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a0c47-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a0c47-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0c47-146">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0c47-147">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-148">Search-Flags</span></span>           | <span data-ttu-id="a0c47-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0c47-149">0x00000000</span></span>                                                |
| <span data-ttu-id="a0c47-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-150">System-Flags</span></span>           | <span data-ttu-id="a0c47-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0c47-151">0x00000010</span></span>                                                |
| <span data-ttu-id="a0c47-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a0c47-152">Classes used in</span></span>        | [<span data-ttu-id="a0c47-153">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a0c47-153">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a0c47-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0c47-154">Windows Server 2003</span></span>



| <span data-ttu-id="a0c47-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-155">Entry</span></span> | <span data-ttu-id="a0c47-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0c47-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0c47-159">System-Only</span></span>            | <span data-ttu-id="a0c47-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-160">False</span></span>                                                     |
| <span data-ttu-id="a0c47-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a0c47-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a0c47-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a0c47-162">True</span></span>                                                      |
| <span data-ttu-id="a0c47-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a0c47-163">Is Indexed</span></span>             | <span data-ttu-id="a0c47-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-164">False</span></span>                                                     |
| <span data-ttu-id="a0c47-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a0c47-165">In Global Catalog</span></span>      | <span data-ttu-id="a0c47-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-166">False</span></span>                                                     |
| <span data-ttu-id="a0c47-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a0c47-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0c47-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a0c47-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a0c47-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0c47-169">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0c47-170">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-171">Search-Flags</span></span>           | <span data-ttu-id="a0c47-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0c47-172">0x00000000</span></span>                                                |
| <span data-ttu-id="a0c47-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-173">System-Flags</span></span>           | <span data-ttu-id="a0c47-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0c47-174">0x00000010</span></span>                                                |
| <span data-ttu-id="a0c47-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a0c47-175">Classes used in</span></span>        | [<span data-ttu-id="a0c47-176">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a0c47-176">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0c47-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0c47-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0c47-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-178">Entry</span></span> | <span data-ttu-id="a0c47-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-179">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0c47-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-180">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-181">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0c47-182">System-Only</span></span>            | <span data-ttu-id="a0c47-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-183">False</span></span>                                                     |
| <span data-ttu-id="a0c47-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a0c47-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a0c47-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a0c47-185">True</span></span>                                                      |
| <span data-ttu-id="a0c47-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a0c47-186">Is Indexed</span></span>             | <span data-ttu-id="a0c47-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-187">False</span></span>                                                     |
| <span data-ttu-id="a0c47-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a0c47-188">In Global Catalog</span></span>      | <span data-ttu-id="a0c47-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-189">False</span></span>                                                     |
| <span data-ttu-id="a0c47-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a0c47-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0c47-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a0c47-191">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a0c47-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0c47-192">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0c47-193">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-194">Search-Flags</span></span>           | <span data-ttu-id="a0c47-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0c47-195">0x00000000</span></span>                                                |
| <span data-ttu-id="a0c47-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-196">System-Flags</span></span>           | <span data-ttu-id="a0c47-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0c47-197">0x00000010</span></span>                                                |
| <span data-ttu-id="a0c47-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a0c47-198">Classes used in</span></span>        | [<span data-ttu-id="a0c47-199">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a0c47-199">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0c47-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0c47-200">Windows Server 2008</span></span>



| <span data-ttu-id="a0c47-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-201">Entry</span></span> | <span data-ttu-id="a0c47-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-202">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0c47-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-203">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-204">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0c47-205">System-Only</span></span>            | <span data-ttu-id="a0c47-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-206">False</span></span>                                                     |
| <span data-ttu-id="a0c47-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a0c47-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a0c47-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a0c47-208">True</span></span>                                                      |
| <span data-ttu-id="a0c47-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a0c47-209">Is Indexed</span></span>             | <span data-ttu-id="a0c47-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-210">False</span></span>                                                     |
| <span data-ttu-id="a0c47-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a0c47-211">In Global Catalog</span></span>      | <span data-ttu-id="a0c47-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-212">False</span></span>                                                     |
| <span data-ttu-id="a0c47-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a0c47-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0c47-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a0c47-214">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a0c47-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0c47-215">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0c47-216">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-217">Search-Flags</span></span>           | <span data-ttu-id="a0c47-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0c47-218">0x00000000</span></span>                                                |
| <span data-ttu-id="a0c47-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-219">System-Flags</span></span>           | <span data-ttu-id="a0c47-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0c47-220">0x00000010</span></span>                                                |
| <span data-ttu-id="a0c47-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a0c47-221">Classes used in</span></span>        | [<span data-ttu-id="a0c47-222">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a0c47-222">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0c47-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0c47-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0c47-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-224">Entry</span></span> | <span data-ttu-id="a0c47-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-225">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0c47-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-226">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-227">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0c47-228">System-Only</span></span>            | <span data-ttu-id="a0c47-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-229">False</span></span>                                                     |
| <span data-ttu-id="a0c47-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a0c47-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a0c47-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a0c47-231">True</span></span>                                                      |
| <span data-ttu-id="a0c47-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a0c47-232">Is Indexed</span></span>             | <span data-ttu-id="a0c47-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-233">False</span></span>                                                     |
| <span data-ttu-id="a0c47-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a0c47-234">In Global Catalog</span></span>      | <span data-ttu-id="a0c47-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-235">False</span></span>                                                     |
| <span data-ttu-id="a0c47-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a0c47-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0c47-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a0c47-237">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a0c47-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0c47-238">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0c47-239">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-240">Search-Flags</span></span>           | <span data-ttu-id="a0c47-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0c47-241">0x00000000</span></span>                                                |
| <span data-ttu-id="a0c47-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-242">System-Flags</span></span>           | <span data-ttu-id="a0c47-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0c47-243">0x00000010</span></span>                                                |
| <span data-ttu-id="a0c47-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a0c47-244">Classes used in</span></span>        | [<span data-ttu-id="a0c47-245">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a0c47-245">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0c47-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0c47-246">Windows Server 2012</span></span>



| <span data-ttu-id="a0c47-247">Voce</span><span class="sxs-lookup"><span data-stu-id="a0c47-247">Entry</span></span> | <span data-ttu-id="a0c47-248">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c47-248">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0c47-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a0c47-249">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0c47-250">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a0c47-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0c47-251">System-Only</span></span>            | <span data-ttu-id="a0c47-252">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-252">False</span></span>                                                     |
| <span data-ttu-id="a0c47-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a0c47-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a0c47-254">Vero</span><span class="sxs-lookup"><span data-stu-id="a0c47-254">True</span></span>                                                      |
| <span data-ttu-id="a0c47-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a0c47-255">Is Indexed</span></span>             | <span data-ttu-id="a0c47-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-256">False</span></span>                                                     |
| <span data-ttu-id="a0c47-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a0c47-257">In Global Catalog</span></span>      | <span data-ttu-id="a0c47-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a0c47-258">False</span></span>                                                     |
| <span data-ttu-id="a0c47-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a0c47-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0c47-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a0c47-260">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a0c47-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0c47-261">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0c47-262">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a0c47-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-263">Search-Flags</span></span>           | <span data-ttu-id="a0c47-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0c47-264">0x00000000</span></span>                                                |
| <span data-ttu-id="a0c47-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0c47-265">System-Flags</span></span>           | <span data-ttu-id="a0c47-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0c47-266">0x00000010</span></span>                                                |
| <span data-ttu-id="a0c47-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a0c47-267">Classes used in</span></span>        | [<span data-ttu-id="a0c47-268">**MS-SQL-SQLServer**</span><span class="sxs-lookup"><span data-stu-id="a0c47-268">**MS-SQL-SQLServer**</span></span>](c-ms-sql-sqlserver.md)<br/> |



 

 





