---
title: Attributo comment
description: Commenti dell'utente. Questa stringa può essere una stringa null.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo comment
- attributo info-schema AD
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744210"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="58e2b-106">Attributo comment (schema AD)</span><span class="sxs-lookup"><span data-stu-id="58e2b-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="58e2b-107">Commenti dell'utente.</span><span class="sxs-lookup"><span data-stu-id="58e2b-107">The user's comments.</span></span> <span data-ttu-id="58e2b-108">Questa stringa può essere una stringa null.</span><span class="sxs-lookup"><span data-stu-id="58e2b-108">This string can be a null string.</span></span>



| <span data-ttu-id="58e2b-109">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-109">Entry</span></span> | <span data-ttu-id="58e2b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="58e2b-111">CN</span><span class="sxs-lookup"><span data-stu-id="58e2b-111">CN</span></span>                | <span data-ttu-id="58e2b-112">Commento</span><span class="sxs-lookup"><span data-stu-id="58e2b-112">Comment</span></span>                                                                  |
| <span data-ttu-id="58e2b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="58e2b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="58e2b-114">info</span><span class="sxs-lookup"><span data-stu-id="58e2b-114">info</span></span>                                                                     |
| <span data-ttu-id="58e2b-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="58e2b-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="58e2b-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-116">Update Privilege</span></span>  | <span data-ttu-id="58e2b-117">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="58e2b-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="58e2b-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-118">Update Frequency</span></span>  | <span data-ttu-id="58e2b-119">Ogni volta che l'utente o l'amministratore deve aggiungere commenti per l'account.</span><span class="sxs-lookup"><span data-stu-id="58e2b-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="58e2b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-120">Attribute-Id</span></span>      | <span data-ttu-id="58e2b-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="58e2b-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="58e2b-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="58e2b-122">System-Id-Guid</span></span>    | <span data-ttu-id="58e2b-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="58e2b-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="58e2b-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58e2b-124">Syntax</span></span>            | [<span data-ttu-id="58e2b-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="58e2b-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="58e2b-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="58e2b-126">Implementations</span></span>

-   [<span data-ttu-id="58e2b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="58e2b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="58e2b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58e2b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58e2b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58e2b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58e2b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58e2b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58e2b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58e2b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58e2b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58e2b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="58e2b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58e2b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="58e2b-134">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-134">Entry</span></span> | <span data-ttu-id="58e2b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="58e2b-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="58e2b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-137">MAPI-Id</span></span>                | <span data-ttu-id="58e2b-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="58e2b-138">0x3004</span></span>                                               |
| <span data-ttu-id="58e2b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e2b-139">System-Only</span></span>            | <span data-ttu-id="58e2b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-140">False</span></span>                                                |
| <span data-ttu-id="58e2b-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58e2b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="58e2b-142">Vero</span><span class="sxs-lookup"><span data-stu-id="58e2b-142">True</span></span>                                                 |
| <span data-ttu-id="58e2b-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58e2b-143">Is Indexed</span></span>             | <span data-ttu-id="58e2b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-144">False</span></span>                                                |
| <span data-ttu-id="58e2b-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58e2b-145">In Global Catalog</span></span>      | <span data-ttu-id="58e2b-146">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-146">False</span></span>                                                |
| <span data-ttu-id="58e2b-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58e2b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e2b-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58e2b-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="58e2b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e2b-149">Range-Lower</span></span>            | <span data-ttu-id="58e2b-150">1</span><span class="sxs-lookup"><span data-stu-id="58e2b-150">1</span></span>                                                    |
| <span data-ttu-id="58e2b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e2b-151">Range-Upper</span></span>            | <span data-ttu-id="58e2b-152">1024</span><span class="sxs-lookup"><span data-stu-id="58e2b-152">1024</span></span>                                                 |
| <span data-ttu-id="58e2b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-153">Search-Flags</span></span>           | <span data-ttu-id="58e2b-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e2b-154">0x00000000</span></span>                                           |
| <span data-ttu-id="58e2b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-155">System-Flags</span></span>           | <span data-ttu-id="58e2b-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e2b-156">0x00000010</span></span>                                           |
| <span data-ttu-id="58e2b-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58e2b-157">Classes used in</span></span>        | [<span data-ttu-id="58e2b-158">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="58e2b-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="58e2b-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58e2b-159">Windows Server 2003</span></span>



| <span data-ttu-id="58e2b-160">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-160">Entry</span></span> | <span data-ttu-id="58e2b-161">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="58e2b-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="58e2b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-163">MAPI-Id</span></span>                | <span data-ttu-id="58e2b-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="58e2b-164">0x3004</span></span>                                               |
| <span data-ttu-id="58e2b-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e2b-165">System-Only</span></span>            | <span data-ttu-id="58e2b-166">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-166">False</span></span>                                                |
| <span data-ttu-id="58e2b-167">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58e2b-167">Is-Single-Valued</span></span>       | <span data-ttu-id="58e2b-168">Vero</span><span class="sxs-lookup"><span data-stu-id="58e2b-168">True</span></span>                                                 |
| <span data-ttu-id="58e2b-169">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58e2b-169">Is Indexed</span></span>             | <span data-ttu-id="58e2b-170">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-170">False</span></span>                                                |
| <span data-ttu-id="58e2b-171">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58e2b-171">In Global Catalog</span></span>      | <span data-ttu-id="58e2b-172">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-172">False</span></span>                                                |
| <span data-ttu-id="58e2b-173">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58e2b-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e2b-174">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58e2b-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="58e2b-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e2b-175">Range-Lower</span></span>            | <span data-ttu-id="58e2b-176">1</span><span class="sxs-lookup"><span data-stu-id="58e2b-176">1</span></span>                                                    |
| <span data-ttu-id="58e2b-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e2b-177">Range-Upper</span></span>            | <span data-ttu-id="58e2b-178">1024</span><span class="sxs-lookup"><span data-stu-id="58e2b-178">1024</span></span>                                                 |
| <span data-ttu-id="58e2b-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-179">Search-Flags</span></span>           | <span data-ttu-id="58e2b-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e2b-180">0x00000000</span></span>                                           |
| <span data-ttu-id="58e2b-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-181">System-Flags</span></span>           | <span data-ttu-id="58e2b-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e2b-182">0x00000010</span></span>                                           |
| <span data-ttu-id="58e2b-183">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58e2b-183">Classes used in</span></span>        | [<span data-ttu-id="58e2b-184">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="58e2b-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58e2b-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58e2b-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58e2b-186">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-186">Entry</span></span> | <span data-ttu-id="58e2b-187">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="58e2b-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="58e2b-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-189">MAPI-Id</span></span>                | <span data-ttu-id="58e2b-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="58e2b-190">0x3004</span></span>                                               |
| <span data-ttu-id="58e2b-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e2b-191">System-Only</span></span>            | <span data-ttu-id="58e2b-192">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-192">False</span></span>                                                |
| <span data-ttu-id="58e2b-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58e2b-193">Is-Single-Valued</span></span>       | <span data-ttu-id="58e2b-194">Vero</span><span class="sxs-lookup"><span data-stu-id="58e2b-194">True</span></span>                                                 |
| <span data-ttu-id="58e2b-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58e2b-195">Is Indexed</span></span>             | <span data-ttu-id="58e2b-196">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-196">False</span></span>                                                |
| <span data-ttu-id="58e2b-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58e2b-197">In Global Catalog</span></span>      | <span data-ttu-id="58e2b-198">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-198">False</span></span>                                                |
| <span data-ttu-id="58e2b-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58e2b-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e2b-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58e2b-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="58e2b-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e2b-201">Range-Lower</span></span>            | <span data-ttu-id="58e2b-202">1</span><span class="sxs-lookup"><span data-stu-id="58e2b-202">1</span></span>                                                    |
| <span data-ttu-id="58e2b-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e2b-203">Range-Upper</span></span>            | <span data-ttu-id="58e2b-204">1024</span><span class="sxs-lookup"><span data-stu-id="58e2b-204">1024</span></span>                                                 |
| <span data-ttu-id="58e2b-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-205">Search-Flags</span></span>           | <span data-ttu-id="58e2b-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e2b-206">0x00000000</span></span>                                           |
| <span data-ttu-id="58e2b-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-207">System-Flags</span></span>           | <span data-ttu-id="58e2b-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e2b-208">0x00000010</span></span>                                           |
| <span data-ttu-id="58e2b-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58e2b-209">Classes used in</span></span>        | [<span data-ttu-id="58e2b-210">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="58e2b-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58e2b-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58e2b-211">Windows Server 2008</span></span>



| <span data-ttu-id="58e2b-212">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-212">Entry</span></span> | <span data-ttu-id="58e2b-213">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="58e2b-214">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="58e2b-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-215">MAPI-Id</span></span>                | <span data-ttu-id="58e2b-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="58e2b-216">0x3004</span></span>                                               |
| <span data-ttu-id="58e2b-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e2b-217">System-Only</span></span>            | <span data-ttu-id="58e2b-218">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-218">False</span></span>                                                |
| <span data-ttu-id="58e2b-219">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58e2b-219">Is-Single-Valued</span></span>       | <span data-ttu-id="58e2b-220">Vero</span><span class="sxs-lookup"><span data-stu-id="58e2b-220">True</span></span>                                                 |
| <span data-ttu-id="58e2b-221">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58e2b-221">Is Indexed</span></span>             | <span data-ttu-id="58e2b-222">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-222">False</span></span>                                                |
| <span data-ttu-id="58e2b-223">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58e2b-223">In Global Catalog</span></span>      | <span data-ttu-id="58e2b-224">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-224">False</span></span>                                                |
| <span data-ttu-id="58e2b-225">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58e2b-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e2b-226">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58e2b-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="58e2b-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e2b-227">Range-Lower</span></span>            | <span data-ttu-id="58e2b-228">1</span><span class="sxs-lookup"><span data-stu-id="58e2b-228">1</span></span>                                                    |
| <span data-ttu-id="58e2b-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e2b-229">Range-Upper</span></span>            | <span data-ttu-id="58e2b-230">1024</span><span class="sxs-lookup"><span data-stu-id="58e2b-230">1024</span></span>                                                 |
| <span data-ttu-id="58e2b-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-231">Search-Flags</span></span>           | <span data-ttu-id="58e2b-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e2b-232">0x00000000</span></span>                                           |
| <span data-ttu-id="58e2b-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-233">System-Flags</span></span>           | <span data-ttu-id="58e2b-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e2b-234">0x00000010</span></span>                                           |
| <span data-ttu-id="58e2b-235">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58e2b-235">Classes used in</span></span>        | [<span data-ttu-id="58e2b-236">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="58e2b-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58e2b-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58e2b-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58e2b-238">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-238">Entry</span></span> | <span data-ttu-id="58e2b-239">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="58e2b-240">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="58e2b-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-241">MAPI-Id</span></span>                | <span data-ttu-id="58e2b-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="58e2b-242">0x3004</span></span>                                               |
| <span data-ttu-id="58e2b-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e2b-243">System-Only</span></span>            | <span data-ttu-id="58e2b-244">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-244">False</span></span>                                                |
| <span data-ttu-id="58e2b-245">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58e2b-245">Is-Single-Valued</span></span>       | <span data-ttu-id="58e2b-246">Vero</span><span class="sxs-lookup"><span data-stu-id="58e2b-246">True</span></span>                                                 |
| <span data-ttu-id="58e2b-247">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58e2b-247">Is Indexed</span></span>             | <span data-ttu-id="58e2b-248">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-248">False</span></span>                                                |
| <span data-ttu-id="58e2b-249">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58e2b-249">In Global Catalog</span></span>      | <span data-ttu-id="58e2b-250">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-250">False</span></span>                                                |
| <span data-ttu-id="58e2b-251">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58e2b-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e2b-252">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58e2b-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="58e2b-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e2b-253">Range-Lower</span></span>            | <span data-ttu-id="58e2b-254">1</span><span class="sxs-lookup"><span data-stu-id="58e2b-254">1</span></span>                                                    |
| <span data-ttu-id="58e2b-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e2b-255">Range-Upper</span></span>            | <span data-ttu-id="58e2b-256">1024</span><span class="sxs-lookup"><span data-stu-id="58e2b-256">1024</span></span>                                                 |
| <span data-ttu-id="58e2b-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-257">Search-Flags</span></span>           | <span data-ttu-id="58e2b-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e2b-258">0x00000000</span></span>                                           |
| <span data-ttu-id="58e2b-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-259">System-Flags</span></span>           | <span data-ttu-id="58e2b-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e2b-260">0x00000010</span></span>                                           |
| <span data-ttu-id="58e2b-261">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58e2b-261">Classes used in</span></span>        | [<span data-ttu-id="58e2b-262">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="58e2b-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58e2b-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58e2b-263">Windows Server 2012</span></span>



| <span data-ttu-id="58e2b-264">Voce</span><span class="sxs-lookup"><span data-stu-id="58e2b-264">Entry</span></span> | <span data-ttu-id="58e2b-265">Valore</span><span class="sxs-lookup"><span data-stu-id="58e2b-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="58e2b-266">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="58e2b-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="58e2b-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e2b-267">MAPI-Id</span></span>                | <span data-ttu-id="58e2b-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="58e2b-268">0x3004</span></span>                                               |
| <span data-ttu-id="58e2b-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e2b-269">System-Only</span></span>            | <span data-ttu-id="58e2b-270">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-270">False</span></span>                                                |
| <span data-ttu-id="58e2b-271">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="58e2b-271">Is-Single-Valued</span></span>       | <span data-ttu-id="58e2b-272">Vero</span><span class="sxs-lookup"><span data-stu-id="58e2b-272">True</span></span>                                                 |
| <span data-ttu-id="58e2b-273">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="58e2b-273">Is Indexed</span></span>             | <span data-ttu-id="58e2b-274">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-274">False</span></span>                                                |
| <span data-ttu-id="58e2b-275">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="58e2b-275">In Global Catalog</span></span>      | <span data-ttu-id="58e2b-276">Falso</span><span class="sxs-lookup"><span data-stu-id="58e2b-276">False</span></span>                                                |
| <span data-ttu-id="58e2b-277">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="58e2b-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e2b-278">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="58e2b-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="58e2b-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e2b-279">Range-Lower</span></span>            | <span data-ttu-id="58e2b-280">1</span><span class="sxs-lookup"><span data-stu-id="58e2b-280">1</span></span>                                                    |
| <span data-ttu-id="58e2b-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e2b-281">Range-Upper</span></span>            | <span data-ttu-id="58e2b-282">1024</span><span class="sxs-lookup"><span data-stu-id="58e2b-282">1024</span></span>                                                 |
| <span data-ttu-id="58e2b-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-283">Search-Flags</span></span>           | <span data-ttu-id="58e2b-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e2b-284">0x00000000</span></span>                                           |
| <span data-ttu-id="58e2b-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e2b-285">System-Flags</span></span>           | <span data-ttu-id="58e2b-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e2b-286">0x00000010</span></span>                                           |
| <span data-ttu-id="58e2b-287">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="58e2b-287">Classes used in</span></span>        | [<span data-ttu-id="58e2b-288">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="58e2b-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





