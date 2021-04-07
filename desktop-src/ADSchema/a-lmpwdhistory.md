---
title: Attributo LM-pwd-History
description: La cronologia delle password dell'utente nel formato unidirezionale di LAN Manager (LM) (OWF). La OWF LM viene utilizzata per la compatibilità con i client LAN Manager 2. x, Windows 95 e Windows 98.
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- LM-pwd-schema AD dell'attributo della cronologia
- Schema AD dell'attributo lmPwdHistory
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875458"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="c7dc3-106">Attributo LM-pwd-History</span><span class="sxs-lookup"><span data-stu-id="c7dc3-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="c7dc3-107">La cronologia delle password dell'utente nel formato unidirezionale di LAN Manager (LM) (OWF).</span><span class="sxs-lookup"><span data-stu-id="c7dc3-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="c7dc3-108">La OWF LM viene utilizzata per la compatibilità con LAN Manager 2. client *x* , Windows 95 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="c7dc3-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="c7dc3-109">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-109">Entry</span></span> | <span data-ttu-id="c7dc3-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c7dc3-111">CN</span><span class="sxs-lookup"><span data-stu-id="c7dc3-111">CN</span></span>                | <span data-ttu-id="c7dc3-112">LM-pwd-cronologia</span><span class="sxs-lookup"><span data-stu-id="c7dc3-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="c7dc3-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c7dc3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c7dc3-114">lmPwdHistory</span><span class="sxs-lookup"><span data-stu-id="c7dc3-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="c7dc3-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c7dc3-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c7dc3-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-116">Update Privilege</span></span>  | <span data-ttu-id="c7dc3-117">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="c7dc3-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="c7dc3-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="c7dc3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-119">Attribute-Id</span></span>      | <span data-ttu-id="c7dc3-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="c7dc3-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="c7dc3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c7dc3-121">System-Id-Guid</span></span>    | <span data-ttu-id="c7dc3-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c7dc3-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="c7dc3-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7dc3-123">Syntax</span></span>            | [<span data-ttu-id="c7dc3-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c7dc3-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c7dc3-125">Implementations</span></span>

-   [<span data-ttu-id="c7dc3-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c7dc3-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c7dc3-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c7dc3-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c7dc3-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c7dc3-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c7dc3-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7dc3-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c7dc3-133">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-133">Entry</span></span> | <span data-ttu-id="c7dc3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c7dc3-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7dc3-137">System-Only</span></span>            | <span data-ttu-id="c7dc3-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-138">False</span></span>                             |
| <span data-ttu-id="c7dc3-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c7dc3-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c7dc3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-140">False</span></span>                             |
| <span data-ttu-id="c7dc3-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c7dc3-141">Is Indexed</span></span>             | <span data-ttu-id="c7dc3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-142">False</span></span>                             |
| <span data-ttu-id="c7dc3-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c7dc3-143">In Global Catalog</span></span>      | <span data-ttu-id="c7dc3-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-144">False</span></span>                             |
| <span data-ttu-id="c7dc3-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7dc3-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c7dc3-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c7dc3-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7dc3-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7dc3-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-149">Search-Flags</span></span>           | <span data-ttu-id="c7dc3-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7dc3-150">0x00000000</span></span>                        |
| <span data-ttu-id="c7dc3-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-151">System-Flags</span></span>           | <span data-ttu-id="c7dc3-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7dc3-152">0x00000010</span></span>                        |
| <span data-ttu-id="c7dc3-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c7dc3-153">Classes used in</span></span>        | [<span data-ttu-id="c7dc3-154">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c7dc3-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7dc3-155">Windows Server 2003</span></span>



| <span data-ttu-id="c7dc3-156">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-156">Entry</span></span> | <span data-ttu-id="c7dc3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c7dc3-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7dc3-160">System-Only</span></span>            | <span data-ttu-id="c7dc3-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-161">False</span></span>                             |
| <span data-ttu-id="c7dc3-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c7dc3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c7dc3-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-163">False</span></span>                             |
| <span data-ttu-id="c7dc3-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c7dc3-164">Is Indexed</span></span>             | <span data-ttu-id="c7dc3-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-165">False</span></span>                             |
| <span data-ttu-id="c7dc3-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c7dc3-166">In Global Catalog</span></span>      | <span data-ttu-id="c7dc3-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-167">False</span></span>                             |
| <span data-ttu-id="c7dc3-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7dc3-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c7dc3-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c7dc3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7dc3-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7dc3-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-172">Search-Flags</span></span>           | <span data-ttu-id="c7dc3-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7dc3-173">0x00000000</span></span>                        |
| <span data-ttu-id="c7dc3-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-174">System-Flags</span></span>           | <span data-ttu-id="c7dc3-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7dc3-175">0x00000010</span></span>                        |
| <span data-ttu-id="c7dc3-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c7dc3-176">Classes used in</span></span>        | [<span data-ttu-id="c7dc3-177">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c7dc3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7dc3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c7dc3-179">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-179">Entry</span></span> | <span data-ttu-id="c7dc3-180">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c7dc3-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7dc3-183">System-Only</span></span>            | <span data-ttu-id="c7dc3-184">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-184">False</span></span>                             |
| <span data-ttu-id="c7dc3-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c7dc3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c7dc3-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-186">False</span></span>                             |
| <span data-ttu-id="c7dc3-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c7dc3-187">Is Indexed</span></span>             | <span data-ttu-id="c7dc3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-188">False</span></span>                             |
| <span data-ttu-id="c7dc3-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c7dc3-189">In Global Catalog</span></span>      | <span data-ttu-id="c7dc3-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-190">False</span></span>                             |
| <span data-ttu-id="c7dc3-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7dc3-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c7dc3-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c7dc3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7dc3-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7dc3-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-195">Search-Flags</span></span>           | <span data-ttu-id="c7dc3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7dc3-196">0x00000000</span></span>                        |
| <span data-ttu-id="c7dc3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-197">System-Flags</span></span>           | <span data-ttu-id="c7dc3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7dc3-198">0x00000010</span></span>                        |
| <span data-ttu-id="c7dc3-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c7dc3-199">Classes used in</span></span>        | [<span data-ttu-id="c7dc3-200">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c7dc3-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7dc3-201">Windows Server 2008</span></span>



| <span data-ttu-id="c7dc3-202">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-202">Entry</span></span> | <span data-ttu-id="c7dc3-203">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c7dc3-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7dc3-206">System-Only</span></span>            | <span data-ttu-id="c7dc3-207">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-207">False</span></span>                             |
| <span data-ttu-id="c7dc3-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c7dc3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c7dc3-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-209">False</span></span>                             |
| <span data-ttu-id="c7dc3-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c7dc3-210">Is Indexed</span></span>             | <span data-ttu-id="c7dc3-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-211">False</span></span>                             |
| <span data-ttu-id="c7dc3-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c7dc3-212">In Global Catalog</span></span>      | <span data-ttu-id="c7dc3-213">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-213">False</span></span>                             |
| <span data-ttu-id="c7dc3-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7dc3-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c7dc3-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c7dc3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7dc3-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7dc3-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-218">Search-Flags</span></span>           | <span data-ttu-id="c7dc3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7dc3-219">0x00000000</span></span>                        |
| <span data-ttu-id="c7dc3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-220">System-Flags</span></span>           | <span data-ttu-id="c7dc3-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7dc3-221">0x00000010</span></span>                        |
| <span data-ttu-id="c7dc3-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c7dc3-222">Classes used in</span></span>        | [<span data-ttu-id="c7dc3-223">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c7dc3-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7dc3-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c7dc3-225">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-225">Entry</span></span> | <span data-ttu-id="c7dc3-226">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c7dc3-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7dc3-229">System-Only</span></span>            | <span data-ttu-id="c7dc3-230">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-230">False</span></span>                             |
| <span data-ttu-id="c7dc3-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c7dc3-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c7dc3-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-232">False</span></span>                             |
| <span data-ttu-id="c7dc3-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c7dc3-233">Is Indexed</span></span>             | <span data-ttu-id="c7dc3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-234">False</span></span>                             |
| <span data-ttu-id="c7dc3-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c7dc3-235">In Global Catalog</span></span>      | <span data-ttu-id="c7dc3-236">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-236">False</span></span>                             |
| <span data-ttu-id="c7dc3-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7dc3-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c7dc3-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c7dc3-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7dc3-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7dc3-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-241">Search-Flags</span></span>           | <span data-ttu-id="c7dc3-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7dc3-242">0x00000000</span></span>                        |
| <span data-ttu-id="c7dc3-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-243">System-Flags</span></span>           | <span data-ttu-id="c7dc3-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7dc3-244">0x00000010</span></span>                        |
| <span data-ttu-id="c7dc3-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c7dc3-245">Classes used in</span></span>        | [<span data-ttu-id="c7dc3-246">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c7dc3-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7dc3-247">Windows Server 2012</span></span>



| <span data-ttu-id="c7dc3-248">Voce</span><span class="sxs-lookup"><span data-stu-id="c7dc3-248">Entry</span></span> | <span data-ttu-id="c7dc3-249">Valore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c7dc3-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c7dc3-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7dc3-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c7dc3-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7dc3-252">System-Only</span></span>            | <span data-ttu-id="c7dc3-253">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-253">False</span></span>                             |
| <span data-ttu-id="c7dc3-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c7dc3-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c7dc3-255">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-255">False</span></span>                             |
| <span data-ttu-id="c7dc3-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c7dc3-256">Is Indexed</span></span>             | <span data-ttu-id="c7dc3-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-257">False</span></span>                             |
| <span data-ttu-id="c7dc3-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c7dc3-258">In Global Catalog</span></span>      | <span data-ttu-id="c7dc3-259">Falso</span><span class="sxs-lookup"><span data-stu-id="c7dc3-259">False</span></span>                             |
| <span data-ttu-id="c7dc3-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c7dc3-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7dc3-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c7dc3-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c7dc3-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7dc3-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7dc3-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c7dc3-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-264">Search-Flags</span></span>           | <span data-ttu-id="c7dc3-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7dc3-265">0x00000000</span></span>                        |
| <span data-ttu-id="c7dc3-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7dc3-266">System-Flags</span></span>           | <span data-ttu-id="c7dc3-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7dc3-267">0x00000010</span></span>                        |
| <span data-ttu-id="c7dc3-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c7dc3-268">Classes used in</span></span>        | [<span data-ttu-id="c7dc3-269">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c7dc3-269">**User**</span></span>](c-user.md)<br/> |



 

 





