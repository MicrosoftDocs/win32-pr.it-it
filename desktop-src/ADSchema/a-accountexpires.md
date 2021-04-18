---
title: Attributo Account-Expires
description: Data di scadenza dell'account.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Schema AD Account-Expires attribute
- Schema AD dell'attributo accountExpires
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303590"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="6d617-105">Attributo Account-Expires</span><span class="sxs-lookup"><span data-stu-id="6d617-105">Account-Expires attribute</span></span>

<span data-ttu-id="6d617-106">Data di scadenza dell'account.</span><span class="sxs-lookup"><span data-stu-id="6d617-106">The date when the account expires.</span></span> <span data-ttu-id="6d617-107">Questo valore rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="6d617-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="6d617-108">Il valore 0 o 0x7FFFFFFFFFFFFFFF (9223372036854775807) indica che l'account non scade mai.</span><span class="sxs-lookup"><span data-stu-id="6d617-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="6d617-109">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-109">Entry</span></span> | <span data-ttu-id="6d617-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6d617-111">CN</span><span class="sxs-lookup"><span data-stu-id="6d617-111">CN</span></span>                | <span data-ttu-id="6d617-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="6d617-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="6d617-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6d617-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6d617-114">accountExpires</span><span class="sxs-lookup"><span data-stu-id="6d617-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="6d617-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6d617-115">Size</span></span>              | <span data-ttu-id="6d617-116">8 byte</span><span class="sxs-lookup"><span data-stu-id="6d617-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="6d617-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6d617-117">Update Privilege</span></span>  | <span data-ttu-id="6d617-118">Questo attributo viene impostato dall'amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="6d617-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="6d617-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6d617-119">Update Frequency</span></span>  | <span data-ttu-id="6d617-120">Ogni volta che la data di scadenza precedente scade e deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6d617-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="6d617-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-121">Attribute-Id</span></span>      | <span data-ttu-id="6d617-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="6d617-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="6d617-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6d617-123">System-Id-Guid</span></span>    | <span data-ttu-id="6d617-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6d617-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="6d617-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d617-125">Syntax</span></span>            | [<span data-ttu-id="6d617-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6d617-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="6d617-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6d617-127">Implementations</span></span>

-   [<span data-ttu-id="6d617-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6d617-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6d617-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6d617-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6d617-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6d617-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6d617-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6d617-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6d617-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6d617-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6d617-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6d617-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6d617-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6d617-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6d617-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d617-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6d617-136">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-136">Entry</span></span> | <span data-ttu-id="6d617-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d617-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-140">System-Only</span></span>            | <span data-ttu-id="6d617-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-141">False</span></span>                             |
| <span data-ttu-id="6d617-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-143">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-143">True</span></span>                              |
| <span data-ttu-id="6d617-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-144">Is Indexed</span></span>             | <span data-ttu-id="6d617-145">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-145">False</span></span>                             |
| <span data-ttu-id="6d617-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-146">In Global Catalog</span></span>      | <span data-ttu-id="6d617-147">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-147">False</span></span>                             |
| <span data-ttu-id="6d617-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d617-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d617-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d617-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-152">Search-Flags</span></span>           | <span data-ttu-id="6d617-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-153">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-154">System-Flags</span></span>           | <span data-ttu-id="6d617-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-155">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-156">Classes used in</span></span>        | [<span data-ttu-id="6d617-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6d617-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6d617-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6d617-158">Windows Server 2003</span></span>



| <span data-ttu-id="6d617-159">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-159">Entry</span></span> | <span data-ttu-id="6d617-160">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d617-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-163">System-Only</span></span>            | <span data-ttu-id="6d617-164">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-164">False</span></span>                             |
| <span data-ttu-id="6d617-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-166">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-166">True</span></span>                              |
| <span data-ttu-id="6d617-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-167">Is Indexed</span></span>             | <span data-ttu-id="6d617-168">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-168">False</span></span>                             |
| <span data-ttu-id="6d617-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-169">In Global Catalog</span></span>      | <span data-ttu-id="6d617-170">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-170">False</span></span>                             |
| <span data-ttu-id="6d617-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d617-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d617-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d617-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-175">Search-Flags</span></span>           | <span data-ttu-id="6d617-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-176">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-177">System-Flags</span></span>           | <span data-ttu-id="6d617-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-178">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-179">Classes used in</span></span>        | [<span data-ttu-id="6d617-180">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6d617-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6d617-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="6d617-181">ADAM</span></span>



| <span data-ttu-id="6d617-182">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-182">Entry</span></span> | <span data-ttu-id="6d617-183">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6d617-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6d617-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6d617-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-186">System-Only</span></span>            | <span data-ttu-id="6d617-187">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-187">False</span></span>                                                             |
| <span data-ttu-id="6d617-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-189">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-189">True</span></span>                                                              |
| <span data-ttu-id="6d617-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-190">Is Indexed</span></span>             | <span data-ttu-id="6d617-191">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-191">False</span></span>                                                             |
| <span data-ttu-id="6d617-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-192">In Global Catalog</span></span>      | <span data-ttu-id="6d617-193">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-193">False</span></span>                                                             |
| <span data-ttu-id="6d617-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6d617-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6d617-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6d617-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-198">Search-Flags</span></span>           | <span data-ttu-id="6d617-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="6d617-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-200">System-Flags</span></span>           | <span data-ttu-id="6d617-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="6d617-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-202">Classes used in</span></span>        | [<span data-ttu-id="6d617-203">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="6d617-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6d617-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6d617-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6d617-205">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-205">Entry</span></span> | <span data-ttu-id="6d617-206">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d617-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-209">System-Only</span></span>            | <span data-ttu-id="6d617-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-210">False</span></span>                             |
| <span data-ttu-id="6d617-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-212">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-212">True</span></span>                              |
| <span data-ttu-id="6d617-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-213">Is Indexed</span></span>             | <span data-ttu-id="6d617-214">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-214">False</span></span>                             |
| <span data-ttu-id="6d617-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-215">In Global Catalog</span></span>      | <span data-ttu-id="6d617-216">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-216">False</span></span>                             |
| <span data-ttu-id="6d617-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d617-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d617-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d617-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-221">Search-Flags</span></span>           | <span data-ttu-id="6d617-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-222">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-223">System-Flags</span></span>           | <span data-ttu-id="6d617-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-224">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-225">Classes used in</span></span>        | [<span data-ttu-id="6d617-226">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6d617-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6d617-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d617-227">Windows Server 2008</span></span>



| <span data-ttu-id="6d617-228">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-228">Entry</span></span> | <span data-ttu-id="6d617-229">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d617-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-232">System-Only</span></span>            | <span data-ttu-id="6d617-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-233">False</span></span>                             |
| <span data-ttu-id="6d617-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-235">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-235">True</span></span>                              |
| <span data-ttu-id="6d617-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-236">Is Indexed</span></span>             | <span data-ttu-id="6d617-237">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-237">False</span></span>                             |
| <span data-ttu-id="6d617-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-238">In Global Catalog</span></span>      | <span data-ttu-id="6d617-239">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-239">False</span></span>                             |
| <span data-ttu-id="6d617-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d617-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d617-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d617-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-244">Search-Flags</span></span>           | <span data-ttu-id="6d617-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-245">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-246">System-Flags</span></span>           | <span data-ttu-id="6d617-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-247">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-248">Classes used in</span></span>        | [<span data-ttu-id="6d617-249">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6d617-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6d617-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6d617-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6d617-251">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-251">Entry</span></span> | <span data-ttu-id="6d617-252">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d617-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-255">System-Only</span></span>            | <span data-ttu-id="6d617-256">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-256">False</span></span>                             |
| <span data-ttu-id="6d617-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-258">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-258">True</span></span>                              |
| <span data-ttu-id="6d617-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-259">Is Indexed</span></span>             | <span data-ttu-id="6d617-260">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-260">False</span></span>                             |
| <span data-ttu-id="6d617-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-261">In Global Catalog</span></span>      | <span data-ttu-id="6d617-262">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-262">False</span></span>                             |
| <span data-ttu-id="6d617-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d617-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d617-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d617-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-267">Search-Flags</span></span>           | <span data-ttu-id="6d617-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-268">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-269">System-Flags</span></span>           | <span data-ttu-id="6d617-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-270">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-271">Classes used in</span></span>        | [<span data-ttu-id="6d617-272">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6d617-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6d617-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d617-273">Windows Server 2012</span></span>



| <span data-ttu-id="6d617-274">Voce</span><span class="sxs-lookup"><span data-stu-id="6d617-274">Entry</span></span> | <span data-ttu-id="6d617-275">Valore</span><span class="sxs-lookup"><span data-stu-id="6d617-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6d617-276">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6d617-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6d617-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6d617-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="6d617-278">System-Only</span></span>            | <span data-ttu-id="6d617-279">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-279">False</span></span>                             |
| <span data-ttu-id="6d617-280">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6d617-280">Is-Single-Valued</span></span>       | <span data-ttu-id="6d617-281">Vero</span><span class="sxs-lookup"><span data-stu-id="6d617-281">True</span></span>                              |
| <span data-ttu-id="6d617-282">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6d617-282">Is Indexed</span></span>             | <span data-ttu-id="6d617-283">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-283">False</span></span>                             |
| <span data-ttu-id="6d617-284">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6d617-284">In Global Catalog</span></span>      | <span data-ttu-id="6d617-285">Falso</span><span class="sxs-lookup"><span data-stu-id="6d617-285">False</span></span>                             |
| <span data-ttu-id="6d617-286">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6d617-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="6d617-287">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6d617-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6d617-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6d617-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6d617-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6d617-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6d617-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-290">Search-Flags</span></span>           | <span data-ttu-id="6d617-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-291">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6d617-292">System-Flags</span></span>           | <span data-ttu-id="6d617-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6d617-293">0x00000010</span></span>                        |
| <span data-ttu-id="6d617-294">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6d617-294">Classes used in</span></span>        | [<span data-ttu-id="6d617-295">**Utente**</span><span class="sxs-lookup"><span data-stu-id="6d617-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6d617-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d617-296">Remarks</span></span>

<span data-ttu-id="6d617-297">La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="6d617-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 

