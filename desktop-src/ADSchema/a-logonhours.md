---
title: Attributo Logon-Hours
description: Ore a cui l'utente può accedere al dominio.
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- Schema AD Logon-Hours attribute
- Schema AD dell'attributo logonHours
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479769"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="dec34-105">Attributo Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="dec34-105">Logon-Hours attribute</span></span>

<span data-ttu-id="dec34-106">Ore a cui l'utente può accedere al dominio.</span><span class="sxs-lookup"><span data-stu-id="dec34-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="dec34-107">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-107">Entry</span></span> | <span data-ttu-id="dec34-108">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="dec34-109">CN</span><span class="sxs-lookup"><span data-stu-id="dec34-109">CN</span></span>                | <span data-ttu-id="dec34-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="dec34-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="dec34-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dec34-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dec34-112">logonHours</span><span class="sxs-lookup"><span data-stu-id="dec34-112">logonHours</span></span>                                            |
| <span data-ttu-id="dec34-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dec34-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="dec34-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dec34-114">Update Privilege</span></span>  | <span data-ttu-id="dec34-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="dec34-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="dec34-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dec34-116">Update Frequency</span></span>  | <span data-ttu-id="dec34-117">Ogni volta che è necessario modificare l'orario di accesso dell'account.</span><span class="sxs-lookup"><span data-stu-id="dec34-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="dec34-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-118">Attribute-Id</span></span>      | <span data-ttu-id="dec34-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="dec34-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="dec34-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dec34-120">System-Id-Guid</span></span>    | <span data-ttu-id="dec34-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dec34-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="dec34-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dec34-122">Syntax</span></span>            | [<span data-ttu-id="dec34-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="dec34-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="dec34-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dec34-124">Implementations</span></span>

-   [<span data-ttu-id="dec34-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dec34-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dec34-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dec34-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dec34-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dec34-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dec34-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dec34-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dec34-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dec34-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dec34-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dec34-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dec34-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dec34-131">Windows 2000 Server</span></span>



| <span data-ttu-id="dec34-132">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-132">Entry</span></span> | <span data-ttu-id="dec34-133">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dec34-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dec34-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="dec34-136">System-Only</span></span>            | <span data-ttu-id="dec34-137">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-137">False</span></span>                             |
| <span data-ttu-id="dec34-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dec34-138">Is-Single-Valued</span></span>       | <span data-ttu-id="dec34-139">Vero</span><span class="sxs-lookup"><span data-stu-id="dec34-139">True</span></span>                              |
| <span data-ttu-id="dec34-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dec34-140">Is Indexed</span></span>             | <span data-ttu-id="dec34-141">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-141">False</span></span>                             |
| <span data-ttu-id="dec34-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dec34-142">In Global Catalog</span></span>      | <span data-ttu-id="dec34-143">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-143">False</span></span>                             |
| <span data-ttu-id="dec34-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dec34-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="dec34-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dec34-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dec34-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dec34-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dec34-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dec34-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dec34-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-148">Search-Flags</span></span>           | <span data-ttu-id="dec34-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-149">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-150">System-Flags</span></span>           | <span data-ttu-id="dec34-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-151">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dec34-152">Classes used in</span></span>        | [<span data-ttu-id="dec34-153">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dec34-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dec34-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dec34-154">Windows Server 2003</span></span>



| <span data-ttu-id="dec34-155">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-155">Entry</span></span> | <span data-ttu-id="dec34-156">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dec34-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dec34-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dec34-159">System-Only</span></span>            | <span data-ttu-id="dec34-160">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-160">False</span></span>                             |
| <span data-ttu-id="dec34-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dec34-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dec34-162">Vero</span><span class="sxs-lookup"><span data-stu-id="dec34-162">True</span></span>                              |
| <span data-ttu-id="dec34-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dec34-163">Is Indexed</span></span>             | <span data-ttu-id="dec34-164">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-164">False</span></span>                             |
| <span data-ttu-id="dec34-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dec34-165">In Global Catalog</span></span>      | <span data-ttu-id="dec34-166">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-166">False</span></span>                             |
| <span data-ttu-id="dec34-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dec34-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dec34-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dec34-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dec34-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dec34-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dec34-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dec34-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dec34-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-171">Search-Flags</span></span>           | <span data-ttu-id="dec34-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-172">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-173">System-Flags</span></span>           | <span data-ttu-id="dec34-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-174">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dec34-175">Classes used in</span></span>        | [<span data-ttu-id="dec34-176">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dec34-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dec34-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dec34-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dec34-178">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-178">Entry</span></span> | <span data-ttu-id="dec34-179">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dec34-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dec34-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="dec34-182">System-Only</span></span>            | <span data-ttu-id="dec34-183">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-183">False</span></span>                             |
| <span data-ttu-id="dec34-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dec34-184">Is-Single-Valued</span></span>       | <span data-ttu-id="dec34-185">Vero</span><span class="sxs-lookup"><span data-stu-id="dec34-185">True</span></span>                              |
| <span data-ttu-id="dec34-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dec34-186">Is Indexed</span></span>             | <span data-ttu-id="dec34-187">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-187">False</span></span>                             |
| <span data-ttu-id="dec34-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dec34-188">In Global Catalog</span></span>      | <span data-ttu-id="dec34-189">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-189">False</span></span>                             |
| <span data-ttu-id="dec34-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dec34-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="dec34-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dec34-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dec34-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dec34-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dec34-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dec34-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dec34-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-194">Search-Flags</span></span>           | <span data-ttu-id="dec34-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-195">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-196">System-Flags</span></span>           | <span data-ttu-id="dec34-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-197">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dec34-198">Classes used in</span></span>        | [<span data-ttu-id="dec34-199">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dec34-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dec34-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dec34-200">Windows Server 2008</span></span>



| <span data-ttu-id="dec34-201">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-201">Entry</span></span> | <span data-ttu-id="dec34-202">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dec34-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dec34-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="dec34-205">System-Only</span></span>            | <span data-ttu-id="dec34-206">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-206">False</span></span>                             |
| <span data-ttu-id="dec34-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dec34-207">Is-Single-Valued</span></span>       | <span data-ttu-id="dec34-208">Vero</span><span class="sxs-lookup"><span data-stu-id="dec34-208">True</span></span>                              |
| <span data-ttu-id="dec34-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dec34-209">Is Indexed</span></span>             | <span data-ttu-id="dec34-210">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-210">False</span></span>                             |
| <span data-ttu-id="dec34-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dec34-211">In Global Catalog</span></span>      | <span data-ttu-id="dec34-212">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-212">False</span></span>                             |
| <span data-ttu-id="dec34-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dec34-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="dec34-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dec34-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dec34-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dec34-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dec34-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dec34-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dec34-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-217">Search-Flags</span></span>           | <span data-ttu-id="dec34-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-218">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-219">System-Flags</span></span>           | <span data-ttu-id="dec34-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-220">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dec34-221">Classes used in</span></span>        | [<span data-ttu-id="dec34-222">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dec34-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dec34-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dec34-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dec34-224">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-224">Entry</span></span> | <span data-ttu-id="dec34-225">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dec34-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dec34-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="dec34-228">System-Only</span></span>            | <span data-ttu-id="dec34-229">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-229">False</span></span>                             |
| <span data-ttu-id="dec34-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dec34-230">Is-Single-Valued</span></span>       | <span data-ttu-id="dec34-231">Vero</span><span class="sxs-lookup"><span data-stu-id="dec34-231">True</span></span>                              |
| <span data-ttu-id="dec34-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dec34-232">Is Indexed</span></span>             | <span data-ttu-id="dec34-233">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-233">False</span></span>                             |
| <span data-ttu-id="dec34-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dec34-234">In Global Catalog</span></span>      | <span data-ttu-id="dec34-235">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-235">False</span></span>                             |
| <span data-ttu-id="dec34-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dec34-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="dec34-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dec34-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dec34-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dec34-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dec34-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dec34-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dec34-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-240">Search-Flags</span></span>           | <span data-ttu-id="dec34-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-241">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-242">System-Flags</span></span>           | <span data-ttu-id="dec34-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-243">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dec34-244">Classes used in</span></span>        | [<span data-ttu-id="dec34-245">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dec34-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dec34-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dec34-246">Windows Server 2012</span></span>



| <span data-ttu-id="dec34-247">Voce</span><span class="sxs-lookup"><span data-stu-id="dec34-247">Entry</span></span> | <span data-ttu-id="dec34-248">Valore</span><span class="sxs-lookup"><span data-stu-id="dec34-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dec34-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dec34-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dec34-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dec34-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="dec34-251">System-Only</span></span>            | <span data-ttu-id="dec34-252">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-252">False</span></span>                             |
| <span data-ttu-id="dec34-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dec34-253">Is-Single-Valued</span></span>       | <span data-ttu-id="dec34-254">Vero</span><span class="sxs-lookup"><span data-stu-id="dec34-254">True</span></span>                              |
| <span data-ttu-id="dec34-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dec34-255">Is Indexed</span></span>             | <span data-ttu-id="dec34-256">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-256">False</span></span>                             |
| <span data-ttu-id="dec34-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dec34-257">In Global Catalog</span></span>      | <span data-ttu-id="dec34-258">Falso</span><span class="sxs-lookup"><span data-stu-id="dec34-258">False</span></span>                             |
| <span data-ttu-id="dec34-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dec34-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="dec34-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dec34-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dec34-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dec34-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dec34-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dec34-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dec34-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-263">Search-Flags</span></span>           | <span data-ttu-id="dec34-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-264">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dec34-265">System-Flags</span></span>           | <span data-ttu-id="dec34-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dec34-266">0x00000010</span></span>                        |
| <span data-ttu-id="dec34-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dec34-267">Classes used in</span></span>        | [<span data-ttu-id="dec34-268">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dec34-268">**User**</span></span>](c-user.md)<br/> |



 

 





