---
title: Attributo Lockout-Time
description: Data e ora (UTC) in cui l'account è stato bloccato.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Schema AD Lockout-Time attribute
- Schema AD dell'attributo lockoutTime
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303315"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="e8b39-105">Attributo Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="e8b39-105">Lockout-Time attribute</span></span>

<span data-ttu-id="e8b39-106">Data e ora (UTC) in cui l'account è stato bloccato. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="e8b39-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="e8b39-107">Un valore pari a zero indica che l'account non è attualmente bloccato.</span><span class="sxs-lookup"><span data-stu-id="e8b39-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="e8b39-108">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-108">Entry</span></span> | <span data-ttu-id="e8b39-109">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e8b39-110">CN</span><span class="sxs-lookup"><span data-stu-id="e8b39-110">CN</span></span>                | <span data-ttu-id="e8b39-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="e8b39-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="e8b39-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e8b39-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e8b39-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="e8b39-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="e8b39-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e8b39-114">Size</span></span>              | <span data-ttu-id="e8b39-115">8 byte</span><span class="sxs-lookup"><span data-stu-id="e8b39-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="e8b39-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-116">Update Privilege</span></span>  | <span data-ttu-id="e8b39-117">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="e8b39-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="e8b39-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-118">Update Frequency</span></span>  | <span data-ttu-id="e8b39-119">Quando il record dell'utente viene creato e ogni volta che è necessario modificare il tempo di blocco.</span><span class="sxs-lookup"><span data-stu-id="e8b39-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="e8b39-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-120">Attribute-Id</span></span>      | <span data-ttu-id="e8b39-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="e8b39-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="e8b39-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e8b39-122">System-Id-Guid</span></span>    | <span data-ttu-id="e8b39-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e8b39-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="e8b39-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8b39-124">Syntax</span></span>            | [<span data-ttu-id="e8b39-125">**Interval**</span><span class="sxs-lookup"><span data-stu-id="e8b39-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="e8b39-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="e8b39-126">Implementations</span></span>

-   [<span data-ttu-id="e8b39-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e8b39-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e8b39-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e8b39-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e8b39-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e8b39-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e8b39-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e8b39-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e8b39-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e8b39-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e8b39-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e8b39-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e8b39-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e8b39-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e8b39-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e8b39-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e8b39-135">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-135">Entry</span></span> | <span data-ttu-id="e8b39-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e8b39-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-139">System-Only</span></span>            | <span data-ttu-id="e8b39-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-140">False</span></span>                             |
| <span data-ttu-id="e8b39-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-142">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-142">True</span></span>                              |
| <span data-ttu-id="e8b39-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-143">Is Indexed</span></span>             | <span data-ttu-id="e8b39-144">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-144">False</span></span>                             |
| <span data-ttu-id="e8b39-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-145">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-146">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-146">False</span></span>                             |
| <span data-ttu-id="e8b39-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e8b39-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e8b39-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e8b39-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-151">Search-Flags</span></span>           | <span data-ttu-id="e8b39-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-152">0x00000000</span></span>                        |
| <span data-ttu-id="e8b39-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-153">System-Flags</span></span>           | <span data-ttu-id="e8b39-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-154">0x00000010</span></span>                        |
| <span data-ttu-id="e8b39-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-155">Classes used in</span></span>        | [<span data-ttu-id="e8b39-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e8b39-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e8b39-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8b39-157">Windows Server 2003</span></span>



| <span data-ttu-id="e8b39-158">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-158">Entry</span></span> | <span data-ttu-id="e8b39-159">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e8b39-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-162">System-Only</span></span>            | <span data-ttu-id="e8b39-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-163">False</span></span>                             |
| <span data-ttu-id="e8b39-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-165">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-165">True</span></span>                              |
| <span data-ttu-id="e8b39-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-166">Is Indexed</span></span>             | <span data-ttu-id="e8b39-167">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-167">False</span></span>                             |
| <span data-ttu-id="e8b39-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-168">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-169">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-169">False</span></span>                             |
| <span data-ttu-id="e8b39-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e8b39-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e8b39-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e8b39-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-174">Search-Flags</span></span>           | <span data-ttu-id="e8b39-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-175">0x00000000</span></span>                        |
| <span data-ttu-id="e8b39-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-176">System-Flags</span></span>           | <span data-ttu-id="e8b39-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-177">0x00000010</span></span>                        |
| <span data-ttu-id="e8b39-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-178">Classes used in</span></span>        | [<span data-ttu-id="e8b39-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e8b39-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e8b39-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="e8b39-180">ADAM</span></span>



| <span data-ttu-id="e8b39-181">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-181">Entry</span></span> | <span data-ttu-id="e8b39-182">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8b39-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8b39-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e8b39-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-185">System-Only</span></span>            | <span data-ttu-id="e8b39-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-186">False</span></span>                                                             |
| <span data-ttu-id="e8b39-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-188">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-188">True</span></span>                                                              |
| <span data-ttu-id="e8b39-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-189">Is Indexed</span></span>             | <span data-ttu-id="e8b39-190">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-190">False</span></span>                                                             |
| <span data-ttu-id="e8b39-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-191">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-192">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-192">False</span></span>                                                             |
| <span data-ttu-id="e8b39-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e8b39-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="e8b39-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="e8b39-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-197">Search-Flags</span></span>           | <span data-ttu-id="e8b39-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="e8b39-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-199">System-Flags</span></span>           | <span data-ttu-id="e8b39-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="e8b39-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-201">Classes used in</span></span>        | [<span data-ttu-id="e8b39-202">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="e8b39-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e8b39-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e8b39-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e8b39-204">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-204">Entry</span></span> | <span data-ttu-id="e8b39-205">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e8b39-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-208">System-Only</span></span>            | <span data-ttu-id="e8b39-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-209">False</span></span>                             |
| <span data-ttu-id="e8b39-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-211">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-211">True</span></span>                              |
| <span data-ttu-id="e8b39-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-212">Is Indexed</span></span>             | <span data-ttu-id="e8b39-213">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-213">False</span></span>                             |
| <span data-ttu-id="e8b39-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-214">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-215">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-215">False</span></span>                             |
| <span data-ttu-id="e8b39-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e8b39-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e8b39-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e8b39-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-220">Search-Flags</span></span>           | <span data-ttu-id="e8b39-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-221">0x00000000</span></span>                        |
| <span data-ttu-id="e8b39-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-222">System-Flags</span></span>           | <span data-ttu-id="e8b39-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-223">0x00000010</span></span>                        |
| <span data-ttu-id="e8b39-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-224">Classes used in</span></span>        | [<span data-ttu-id="e8b39-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e8b39-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e8b39-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8b39-226">Windows Server 2008</span></span>



| <span data-ttu-id="e8b39-227">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-227">Entry</span></span> | <span data-ttu-id="e8b39-228">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e8b39-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-231">System-Only</span></span>            | <span data-ttu-id="e8b39-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-232">False</span></span>                             |
| <span data-ttu-id="e8b39-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-234">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-234">True</span></span>                              |
| <span data-ttu-id="e8b39-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-235">Is Indexed</span></span>             | <span data-ttu-id="e8b39-236">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-236">False</span></span>                             |
| <span data-ttu-id="e8b39-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-237">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-238">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-238">False</span></span>                             |
| <span data-ttu-id="e8b39-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e8b39-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e8b39-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e8b39-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-243">Search-Flags</span></span>           | <span data-ttu-id="e8b39-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-244">0x00000000</span></span>                        |
| <span data-ttu-id="e8b39-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-245">System-Flags</span></span>           | <span data-ttu-id="e8b39-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-246">0x00000010</span></span>                        |
| <span data-ttu-id="e8b39-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-247">Classes used in</span></span>        | [<span data-ttu-id="e8b39-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e8b39-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e8b39-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8b39-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e8b39-250">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-250">Entry</span></span> | <span data-ttu-id="e8b39-251">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e8b39-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-254">System-Only</span></span>            | <span data-ttu-id="e8b39-255">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-255">False</span></span>                             |
| <span data-ttu-id="e8b39-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-256">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-257">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-257">True</span></span>                              |
| <span data-ttu-id="e8b39-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-258">Is Indexed</span></span>             | <span data-ttu-id="e8b39-259">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-259">False</span></span>                             |
| <span data-ttu-id="e8b39-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-260">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-261">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-261">False</span></span>                             |
| <span data-ttu-id="e8b39-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e8b39-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e8b39-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e8b39-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-266">Search-Flags</span></span>           | <span data-ttu-id="e8b39-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-267">0x00000000</span></span>                        |
| <span data-ttu-id="e8b39-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-268">System-Flags</span></span>           | <span data-ttu-id="e8b39-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-269">0x00000010</span></span>                        |
| <span data-ttu-id="e8b39-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-270">Classes used in</span></span>        | [<span data-ttu-id="e8b39-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e8b39-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e8b39-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e8b39-272">Windows Server 2012</span></span>



| <span data-ttu-id="e8b39-273">Voce</span><span class="sxs-lookup"><span data-stu-id="e8b39-273">Entry</span></span> | <span data-ttu-id="e8b39-274">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b39-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e8b39-275">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="e8b39-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e8b39-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e8b39-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="e8b39-277">System-Only</span></span>            | <span data-ttu-id="e8b39-278">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-278">False</span></span>                             |
| <span data-ttu-id="e8b39-279">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="e8b39-279">Is-Single-Valued</span></span>       | <span data-ttu-id="e8b39-280">Vero</span><span class="sxs-lookup"><span data-stu-id="e8b39-280">True</span></span>                              |
| <span data-ttu-id="e8b39-281">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="e8b39-281">Is Indexed</span></span>             | <span data-ttu-id="e8b39-282">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-282">False</span></span>                             |
| <span data-ttu-id="e8b39-283">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="e8b39-283">In Global Catalog</span></span>      | <span data-ttu-id="e8b39-284">Falso</span><span class="sxs-lookup"><span data-stu-id="e8b39-284">False</span></span>                             |
| <span data-ttu-id="e8b39-285">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="e8b39-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="e8b39-286">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="e8b39-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e8b39-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e8b39-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e8b39-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e8b39-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e8b39-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-289">Search-Flags</span></span>           | <span data-ttu-id="e8b39-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e8b39-290">0x00000000</span></span>                        |
| <span data-ttu-id="e8b39-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e8b39-291">System-Flags</span></span>           | <span data-ttu-id="e8b39-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e8b39-292">0x00000010</span></span>                        |
| <span data-ttu-id="e8b39-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="e8b39-293">Classes used in</span></span>        | [<span data-ttu-id="e8b39-294">**Utente**</span><span class="sxs-lookup"><span data-stu-id="e8b39-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e8b39-295">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8b39-295">Remarks</span></span>

<span data-ttu-id="e8b39-296">La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="e8b39-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="e8b39-297">Il valore di questo attributo viene reimpostato solo quando l'account viene registrato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e8b39-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="e8b39-298">Questo significa che questo valore può essere diverso da zero, ma l'account non è bloccato. Per determinare in modo accurato se l'account è bloccato, è necessario aggiungere la [**durata del blocco**](a-lockoutduration.md) a questa ora e confrontare il risultato con l'ora corrente, considerando i fusi orari locali e l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="e8b39-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8b39-299">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8b39-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b39-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="e8b39-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="e8b39-301">**Blocco-durata**</span><span class="sxs-lookup"><span data-stu-id="e8b39-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

