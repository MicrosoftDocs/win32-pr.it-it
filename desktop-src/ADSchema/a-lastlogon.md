---
title: Attributo Last-Logon
description: Ultima volta in cui l'utente ha effettuato l'accesso.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Schema AD Last-Logon attribute
- Schema AD dell'attributo lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875462"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="6305d-105">Attributo Last-Logon</span><span class="sxs-lookup"><span data-stu-id="6305d-105">Last-Logon attribute</span></span>

<span data-ttu-id="6305d-106">Ultima volta in cui l'utente ha effettuato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6305d-106">The last time the user logged on.</span></span> <span data-ttu-id="6305d-107">Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="6305d-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="6305d-108">Un valore pari a zero indica che l'ora dell'ultimo accesso è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="6305d-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="6305d-109">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-109">Entry</span></span> | <span data-ttu-id="6305d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6305d-111">CN</span><span class="sxs-lookup"><span data-stu-id="6305d-111">CN</span></span>                | <span data-ttu-id="6305d-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="6305d-112">Last-Logon</span></span>                           |
| <span data-ttu-id="6305d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6305d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6305d-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="6305d-114">lastLogon</span></span>                            |
| <span data-ttu-id="6305d-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6305d-115">Size</span></span>              | <span data-ttu-id="6305d-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="6305d-116">8 bytes</span></span>                              |
| <span data-ttu-id="6305d-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6305d-117">Update Privilege</span></span>  | <span data-ttu-id="6305d-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="6305d-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="6305d-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6305d-119">Update Frequency</span></span>  | <span data-ttu-id="6305d-120">Ogni volta che l'utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6305d-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="6305d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-121">Attribute-Id</span></span>      | <span data-ttu-id="6305d-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="6305d-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="6305d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6305d-123">System-Id-Guid</span></span>    | <span data-ttu-id="6305d-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6305d-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6305d-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6305d-125">Syntax</span></span>            | [<span data-ttu-id="6305d-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6305d-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6305d-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6305d-127">Implementations</span></span>

-   [<span data-ttu-id="6305d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6305d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6305d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6305d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6305d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6305d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6305d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6305d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6305d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6305d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6305d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6305d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6305d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6305d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6305d-135">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-135">Entry</span></span> | <span data-ttu-id="6305d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6305d-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6305d-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6305d-139">System-Only</span></span>            | <span data-ttu-id="6305d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-140">False</span></span>                             |
| <span data-ttu-id="6305d-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6305d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6305d-142">Vero</span><span class="sxs-lookup"><span data-stu-id="6305d-142">True</span></span>                              |
| <span data-ttu-id="6305d-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6305d-143">Is Indexed</span></span>             | <span data-ttu-id="6305d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-144">False</span></span>                             |
| <span data-ttu-id="6305d-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6305d-145">In Global Catalog</span></span>      | <span data-ttu-id="6305d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-146">False</span></span>                             |
| <span data-ttu-id="6305d-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6305d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6305d-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6305d-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6305d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6305d-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6305d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6305d-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6305d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-151">Search-Flags</span></span>           | <span data-ttu-id="6305d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6305d-152">0x00000000</span></span>                        |
| <span data-ttu-id="6305d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-153">System-Flags</span></span>           | <span data-ttu-id="6305d-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6305d-154">0x00000011</span></span>                        |
| <span data-ttu-id="6305d-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6305d-155">Classes used in</span></span>        | [<span data-ttu-id="6305d-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6305d-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6305d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6305d-157">Windows Server 2003</span></span>



| <span data-ttu-id="6305d-158">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-158">Entry</span></span> | <span data-ttu-id="6305d-159">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6305d-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6305d-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6305d-162">System-Only</span></span>            | <span data-ttu-id="6305d-163">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-163">False</span></span>                             |
| <span data-ttu-id="6305d-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6305d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6305d-165">Vero</span><span class="sxs-lookup"><span data-stu-id="6305d-165">True</span></span>                              |
| <span data-ttu-id="6305d-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6305d-166">Is Indexed</span></span>             | <span data-ttu-id="6305d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-167">False</span></span>                             |
| <span data-ttu-id="6305d-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6305d-168">In Global Catalog</span></span>      | <span data-ttu-id="6305d-169">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-169">False</span></span>                             |
| <span data-ttu-id="6305d-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6305d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6305d-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6305d-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6305d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6305d-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6305d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6305d-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6305d-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-174">Search-Flags</span></span>           | <span data-ttu-id="6305d-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6305d-175">0x00000000</span></span>                        |
| <span data-ttu-id="6305d-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-176">System-Flags</span></span>           | <span data-ttu-id="6305d-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6305d-177">0x00000011</span></span>                        |
| <span data-ttu-id="6305d-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6305d-178">Classes used in</span></span>        | [<span data-ttu-id="6305d-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6305d-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6305d-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6305d-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6305d-181">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-181">Entry</span></span> | <span data-ttu-id="6305d-182">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6305d-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6305d-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6305d-185">System-Only</span></span>            | <span data-ttu-id="6305d-186">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-186">False</span></span>                             |
| <span data-ttu-id="6305d-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6305d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6305d-188">Vero</span><span class="sxs-lookup"><span data-stu-id="6305d-188">True</span></span>                              |
| <span data-ttu-id="6305d-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6305d-189">Is Indexed</span></span>             | <span data-ttu-id="6305d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-190">False</span></span>                             |
| <span data-ttu-id="6305d-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6305d-191">In Global Catalog</span></span>      | <span data-ttu-id="6305d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-192">False</span></span>                             |
| <span data-ttu-id="6305d-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6305d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6305d-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6305d-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6305d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6305d-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6305d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6305d-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6305d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-197">Search-Flags</span></span>           | <span data-ttu-id="6305d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6305d-198">0x00000000</span></span>                        |
| <span data-ttu-id="6305d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-199">System-Flags</span></span>           | <span data-ttu-id="6305d-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6305d-200">0x00000011</span></span>                        |
| <span data-ttu-id="6305d-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6305d-201">Classes used in</span></span>        | [<span data-ttu-id="6305d-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6305d-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6305d-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6305d-203">Windows Server 2008</span></span>



| <span data-ttu-id="6305d-204">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-204">Entry</span></span> | <span data-ttu-id="6305d-205">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6305d-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6305d-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6305d-208">System-Only</span></span>            | <span data-ttu-id="6305d-209">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-209">False</span></span>                             |
| <span data-ttu-id="6305d-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6305d-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6305d-211">Vero</span><span class="sxs-lookup"><span data-stu-id="6305d-211">True</span></span>                              |
| <span data-ttu-id="6305d-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6305d-212">Is Indexed</span></span>             | <span data-ttu-id="6305d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-213">False</span></span>                             |
| <span data-ttu-id="6305d-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6305d-214">In Global Catalog</span></span>      | <span data-ttu-id="6305d-215">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-215">False</span></span>                             |
| <span data-ttu-id="6305d-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6305d-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6305d-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6305d-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6305d-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6305d-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6305d-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6305d-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6305d-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-220">Search-Flags</span></span>           | <span data-ttu-id="6305d-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6305d-221">0x00000000</span></span>                        |
| <span data-ttu-id="6305d-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-222">System-Flags</span></span>           | <span data-ttu-id="6305d-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6305d-223">0x00000011</span></span>                        |
| <span data-ttu-id="6305d-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6305d-224">Classes used in</span></span>        | [<span data-ttu-id="6305d-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6305d-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6305d-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6305d-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6305d-227">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-227">Entry</span></span> | <span data-ttu-id="6305d-228">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6305d-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6305d-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6305d-231">System-Only</span></span>            | <span data-ttu-id="6305d-232">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-232">False</span></span>                             |
| <span data-ttu-id="6305d-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6305d-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6305d-234">Vero</span><span class="sxs-lookup"><span data-stu-id="6305d-234">True</span></span>                              |
| <span data-ttu-id="6305d-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6305d-235">Is Indexed</span></span>             | <span data-ttu-id="6305d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-236">False</span></span>                             |
| <span data-ttu-id="6305d-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6305d-237">In Global Catalog</span></span>      | <span data-ttu-id="6305d-238">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-238">False</span></span>                             |
| <span data-ttu-id="6305d-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6305d-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6305d-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6305d-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6305d-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6305d-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6305d-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6305d-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6305d-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-243">Search-Flags</span></span>           | <span data-ttu-id="6305d-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6305d-244">0x00000000</span></span>                        |
| <span data-ttu-id="6305d-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-245">System-Flags</span></span>           | <span data-ttu-id="6305d-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6305d-246">0x00000011</span></span>                        |
| <span data-ttu-id="6305d-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6305d-247">Classes used in</span></span>        | [<span data-ttu-id="6305d-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6305d-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6305d-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6305d-249">Windows Server 2012</span></span>



| <span data-ttu-id="6305d-250">Voce</span><span class="sxs-lookup"><span data-stu-id="6305d-250">Entry</span></span> | <span data-ttu-id="6305d-251">Valore</span><span class="sxs-lookup"><span data-stu-id="6305d-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6305d-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6305d-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6305d-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6305d-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6305d-254">System-Only</span></span>            | <span data-ttu-id="6305d-255">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-255">False</span></span>                             |
| <span data-ttu-id="6305d-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6305d-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6305d-257">Vero</span><span class="sxs-lookup"><span data-stu-id="6305d-257">True</span></span>                              |
| <span data-ttu-id="6305d-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6305d-258">Is Indexed</span></span>             | <span data-ttu-id="6305d-259">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-259">False</span></span>                             |
| <span data-ttu-id="6305d-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6305d-260">In Global Catalog</span></span>      | <span data-ttu-id="6305d-261">Falso</span><span class="sxs-lookup"><span data-stu-id="6305d-261">False</span></span>                             |
| <span data-ttu-id="6305d-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6305d-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6305d-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6305d-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6305d-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6305d-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6305d-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6305d-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6305d-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-266">Search-Flags</span></span>           | <span data-ttu-id="6305d-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6305d-267">0x00000000</span></span>                        |
| <span data-ttu-id="6305d-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6305d-268">System-Flags</span></span>           | <span data-ttu-id="6305d-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6305d-269">0x00000011</span></span>                        |
| <span data-ttu-id="6305d-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6305d-270">Classes used in</span></span>        | [<span data-ttu-id="6305d-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6305d-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6305d-272">Commenti</span><span class="sxs-lookup"><span data-stu-id="6305d-272">Remarks</span></span>

<span data-ttu-id="6305d-273">La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="6305d-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="6305d-274">Questo attributo non viene replicato e viene mantenuto separatamente in ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="6305d-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="6305d-275">Per ottenere un valore accurato per l'ultimo accesso dell'utente nel dominio, è necessario recuperare l'attributo **Last-Logon** per l'utente da ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="6305d-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="6305d-276">Il valore più grande recuperato è l'ora dell'ultimo accesso true per tale utente.</span><span class="sxs-lookup"><span data-stu-id="6305d-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="6305d-277">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6305d-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6305d-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="6305d-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

