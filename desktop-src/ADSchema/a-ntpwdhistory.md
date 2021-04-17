---
title: NT-pwd-attributo della cronologia
description: La cronologia delle password dell'utente in formato unidirezionale Windows NT (OWF). Windows 2000 usa Windows NT OWF.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- NT-pwd-schema AD attributo della cronologia
- Schema AD dell'attributo ntPwdHistory
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520062"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="dee24-106">NT-pwd-attributo della cronologia</span><span class="sxs-lookup"><span data-stu-id="dee24-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="dee24-107">La cronologia delle password dell'utente in formato unidirezionale Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="dee24-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="dee24-108">Windows 2000 usa Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="dee24-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="dee24-109">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-109">Entry</span></span> | <span data-ttu-id="dee24-110">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="dee24-111">CN</span><span class="sxs-lookup"><span data-stu-id="dee24-111">CN</span></span>                | <span data-ttu-id="dee24-112">NT-pwd-cronologia</span><span class="sxs-lookup"><span data-stu-id="dee24-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="dee24-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dee24-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dee24-114">ntPwdHistory</span><span class="sxs-lookup"><span data-stu-id="dee24-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="dee24-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dee24-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="dee24-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dee24-116">Update Privilege</span></span>  | <span data-ttu-id="dee24-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dee24-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="dee24-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dee24-118">Update Frequency</span></span>  | <span data-ttu-id="dee24-119">Ogni volta che l'utente modifica le password.</span><span class="sxs-lookup"><span data-stu-id="dee24-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="dee24-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-120">Attribute-Id</span></span>      | <span data-ttu-id="dee24-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="dee24-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="dee24-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dee24-122">System-Id-Guid</span></span>    | <span data-ttu-id="dee24-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dee24-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="dee24-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dee24-124">Syntax</span></span>            | [<span data-ttu-id="dee24-125">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="dee24-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="dee24-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dee24-126">Implementations</span></span>

-   [<span data-ttu-id="dee24-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dee24-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dee24-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dee24-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dee24-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="dee24-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dee24-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dee24-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dee24-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dee24-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dee24-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dee24-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dee24-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dee24-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dee24-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dee24-134">Windows 2000 Server</span></span>



| <span data-ttu-id="dee24-135">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-135">Entry</span></span> | <span data-ttu-id="dee24-136">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dee24-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-139">System-Only</span></span>            | <span data-ttu-id="dee24-140">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-140">False</span></span>                             |
| <span data-ttu-id="dee24-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-141">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-142">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-142">False</span></span>                             |
| <span data-ttu-id="dee24-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-143">Is Indexed</span></span>             | <span data-ttu-id="dee24-144">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-144">False</span></span>                             |
| <span data-ttu-id="dee24-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-145">In Global Catalog</span></span>      | <span data-ttu-id="dee24-146">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-146">False</span></span>                             |
| <span data-ttu-id="dee24-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dee24-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dee24-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dee24-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-151">Search-Flags</span></span>           | <span data-ttu-id="dee24-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-152">0x00000000</span></span>                        |
| <span data-ttu-id="dee24-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-153">System-Flags</span></span>           | <span data-ttu-id="dee24-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-154">0x00000010</span></span>                        |
| <span data-ttu-id="dee24-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-155">Classes used in</span></span>        | [<span data-ttu-id="dee24-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dee24-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dee24-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dee24-157">Windows Server 2003</span></span>



| <span data-ttu-id="dee24-158">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-158">Entry</span></span> | <span data-ttu-id="dee24-159">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dee24-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-162">System-Only</span></span>            | <span data-ttu-id="dee24-163">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-163">False</span></span>                             |
| <span data-ttu-id="dee24-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-164">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-165">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-165">False</span></span>                             |
| <span data-ttu-id="dee24-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-166">Is Indexed</span></span>             | <span data-ttu-id="dee24-167">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-167">False</span></span>                             |
| <span data-ttu-id="dee24-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-168">In Global Catalog</span></span>      | <span data-ttu-id="dee24-169">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-169">False</span></span>                             |
| <span data-ttu-id="dee24-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dee24-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dee24-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dee24-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-174">Search-Flags</span></span>           | <span data-ttu-id="dee24-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-175">0x00000000</span></span>                        |
| <span data-ttu-id="dee24-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-176">System-Flags</span></span>           | <span data-ttu-id="dee24-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-177">0x00000010</span></span>                        |
| <span data-ttu-id="dee24-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-178">Classes used in</span></span>        | [<span data-ttu-id="dee24-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dee24-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dee24-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="dee24-180">ADAM</span></span>



| <span data-ttu-id="dee24-181">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-181">Entry</span></span> | <span data-ttu-id="dee24-182">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="dee24-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="dee24-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="dee24-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-185">System-Only</span></span>            | <span data-ttu-id="dee24-186">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-186">False</span></span>                                                             |
| <span data-ttu-id="dee24-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-188">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-188">False</span></span>                                                             |
| <span data-ttu-id="dee24-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-189">Is Indexed</span></span>             | <span data-ttu-id="dee24-190">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-190">False</span></span>                                                             |
| <span data-ttu-id="dee24-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-191">In Global Catalog</span></span>      | <span data-ttu-id="dee24-192">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-192">False</span></span>                                                             |
| <span data-ttu-id="dee24-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="dee24-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="dee24-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="dee24-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-197">Search-Flags</span></span>           | <span data-ttu-id="dee24-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="dee24-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-199">System-Flags</span></span>           | <span data-ttu-id="dee24-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="dee24-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-201">Classes used in</span></span>        | [<span data-ttu-id="dee24-202">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="dee24-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dee24-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dee24-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dee24-204">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-204">Entry</span></span> | <span data-ttu-id="dee24-205">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dee24-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-208">System-Only</span></span>            | <span data-ttu-id="dee24-209">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-209">False</span></span>                             |
| <span data-ttu-id="dee24-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-210">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-211">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-211">False</span></span>                             |
| <span data-ttu-id="dee24-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-212">Is Indexed</span></span>             | <span data-ttu-id="dee24-213">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-213">False</span></span>                             |
| <span data-ttu-id="dee24-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-214">In Global Catalog</span></span>      | <span data-ttu-id="dee24-215">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-215">False</span></span>                             |
| <span data-ttu-id="dee24-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dee24-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dee24-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dee24-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-220">Search-Flags</span></span>           | <span data-ttu-id="dee24-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-221">0x00000000</span></span>                        |
| <span data-ttu-id="dee24-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-222">System-Flags</span></span>           | <span data-ttu-id="dee24-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-223">0x00000010</span></span>                        |
| <span data-ttu-id="dee24-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-224">Classes used in</span></span>        | [<span data-ttu-id="dee24-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dee24-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dee24-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dee24-226">Windows Server 2008</span></span>



| <span data-ttu-id="dee24-227">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-227">Entry</span></span> | <span data-ttu-id="dee24-228">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dee24-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-231">System-Only</span></span>            | <span data-ttu-id="dee24-232">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-232">False</span></span>                             |
| <span data-ttu-id="dee24-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-233">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-234">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-234">False</span></span>                             |
| <span data-ttu-id="dee24-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-235">Is Indexed</span></span>             | <span data-ttu-id="dee24-236">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-236">False</span></span>                             |
| <span data-ttu-id="dee24-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-237">In Global Catalog</span></span>      | <span data-ttu-id="dee24-238">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-238">False</span></span>                             |
| <span data-ttu-id="dee24-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dee24-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dee24-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dee24-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-243">Search-Flags</span></span>           | <span data-ttu-id="dee24-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-244">0x00000000</span></span>                        |
| <span data-ttu-id="dee24-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-245">System-Flags</span></span>           | <span data-ttu-id="dee24-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-246">0x00000010</span></span>                        |
| <span data-ttu-id="dee24-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-247">Classes used in</span></span>        | [<span data-ttu-id="dee24-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dee24-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dee24-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dee24-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dee24-250">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-250">Entry</span></span> | <span data-ttu-id="dee24-251">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dee24-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-254">System-Only</span></span>            | <span data-ttu-id="dee24-255">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-255">False</span></span>                             |
| <span data-ttu-id="dee24-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-256">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-257">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-257">False</span></span>                             |
| <span data-ttu-id="dee24-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-258">Is Indexed</span></span>             | <span data-ttu-id="dee24-259">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-259">False</span></span>                             |
| <span data-ttu-id="dee24-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-260">In Global Catalog</span></span>      | <span data-ttu-id="dee24-261">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-261">False</span></span>                             |
| <span data-ttu-id="dee24-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dee24-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dee24-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dee24-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-266">Search-Flags</span></span>           | <span data-ttu-id="dee24-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-267">0x00000000</span></span>                        |
| <span data-ttu-id="dee24-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-268">System-Flags</span></span>           | <span data-ttu-id="dee24-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-269">0x00000010</span></span>                        |
| <span data-ttu-id="dee24-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-270">Classes used in</span></span>        | [<span data-ttu-id="dee24-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dee24-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dee24-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dee24-272">Windows Server 2012</span></span>



| <span data-ttu-id="dee24-273">Voce</span><span class="sxs-lookup"><span data-stu-id="dee24-273">Entry</span></span> | <span data-ttu-id="dee24-274">Valore</span><span class="sxs-lookup"><span data-stu-id="dee24-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dee24-275">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dee24-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dee24-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dee24-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="dee24-277">System-Only</span></span>            | <span data-ttu-id="dee24-278">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-278">False</span></span>                             |
| <span data-ttu-id="dee24-279">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dee24-279">Is-Single-Valued</span></span>       | <span data-ttu-id="dee24-280">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-280">False</span></span>                             |
| <span data-ttu-id="dee24-281">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dee24-281">Is Indexed</span></span>             | <span data-ttu-id="dee24-282">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-282">False</span></span>                             |
| <span data-ttu-id="dee24-283">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dee24-283">In Global Catalog</span></span>      | <span data-ttu-id="dee24-284">Falso</span><span class="sxs-lookup"><span data-stu-id="dee24-284">False</span></span>                             |
| <span data-ttu-id="dee24-285">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dee24-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="dee24-286">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dee24-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dee24-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dee24-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dee24-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dee24-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dee24-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-289">Search-Flags</span></span>           | <span data-ttu-id="dee24-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dee24-290">0x00000000</span></span>                        |
| <span data-ttu-id="dee24-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dee24-291">System-Flags</span></span>           | <span data-ttu-id="dee24-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dee24-292">0x00000010</span></span>                        |
| <span data-ttu-id="dee24-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dee24-293">Classes used in</span></span>        | [<span data-ttu-id="dee24-294">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dee24-294">**User**</span></span>](c-user.md)<br/> |



 

 





