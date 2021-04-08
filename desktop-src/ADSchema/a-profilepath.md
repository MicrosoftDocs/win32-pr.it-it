---
title: Attributo Profile-Path
description: Specifica il percorso del profilo utente. Questo valore può essere una stringa null, un percorso assoluto locale o un percorso UNC.
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- Schema AD Profile-Path attribute
- Schema AD dell'attributo propath
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965344"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="91bd0-106">Attributo Profile-Path</span><span class="sxs-lookup"><span data-stu-id="91bd0-106">Profile-Path attribute</span></span>

<span data-ttu-id="91bd0-107">Specifica il percorso del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="91bd0-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="91bd0-108">Questo valore può essere una stringa null, un percorso assoluto locale o un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="91bd0-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="91bd0-109">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-109">Entry</span></span> | <span data-ttu-id="91bd0-110">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="91bd0-111">CN</span><span class="sxs-lookup"><span data-stu-id="91bd0-111">CN</span></span>                | <span data-ttu-id="91bd0-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="91bd0-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="91bd0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="91bd0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="91bd0-114">PercorsoProfilo</span><span class="sxs-lookup"><span data-stu-id="91bd0-114">profilePath</span></span>                                                              |
| <span data-ttu-id="91bd0-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="91bd0-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="91bd0-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-116">Update Privilege</span></span>  | <span data-ttu-id="91bd0-117">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="91bd0-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="91bd0-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-118">Update Frequency</span></span>  | <span data-ttu-id="91bd0-119">Quando il record dell'utente viene creato e ogni volta che è necessario modificare il percorso.</span><span class="sxs-lookup"><span data-stu-id="91bd0-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="91bd0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-120">Attribute-Id</span></span>      | <span data-ttu-id="91bd0-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="91bd0-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="91bd0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="91bd0-122">System-Id-Guid</span></span>    | <span data-ttu-id="91bd0-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="91bd0-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="91bd0-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91bd0-124">Syntax</span></span>            | [<span data-ttu-id="91bd0-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="91bd0-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="91bd0-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="91bd0-126">Implementations</span></span>

-   [<span data-ttu-id="91bd0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="91bd0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="91bd0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91bd0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91bd0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91bd0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91bd0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91bd0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91bd0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91bd0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91bd0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91bd0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="91bd0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91bd0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="91bd0-134">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-134">Entry</span></span> | <span data-ttu-id="91bd0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="91bd0-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="91bd0-138">System-Only</span></span>            | <span data-ttu-id="91bd0-139">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-139">False</span></span>                             |
| <span data-ttu-id="91bd0-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="91bd0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="91bd0-141">Vero</span><span class="sxs-lookup"><span data-stu-id="91bd0-141">True</span></span>                              |
| <span data-ttu-id="91bd0-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="91bd0-142">Is Indexed</span></span>             | <span data-ttu-id="91bd0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-143">False</span></span>                             |
| <span data-ttu-id="91bd0-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="91bd0-144">In Global Catalog</span></span>      | <span data-ttu-id="91bd0-145">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-145">False</span></span>                             |
| <span data-ttu-id="91bd0-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="91bd0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="91bd0-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="91bd0-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="91bd0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91bd0-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="91bd0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91bd0-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="91bd0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-150">Search-Flags</span></span>           | <span data-ttu-id="91bd0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-151">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-152">System-Flags</span></span>           | <span data-ttu-id="91bd0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-153">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="91bd0-154">Classes used in</span></span>        | [<span data-ttu-id="91bd0-155">**Utente**</span><span class="sxs-lookup"><span data-stu-id="91bd0-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="91bd0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91bd0-156">Windows Server 2003</span></span>



| <span data-ttu-id="91bd0-157">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-157">Entry</span></span> | <span data-ttu-id="91bd0-158">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="91bd0-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="91bd0-161">System-Only</span></span>            | <span data-ttu-id="91bd0-162">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-162">False</span></span>                             |
| <span data-ttu-id="91bd0-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="91bd0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="91bd0-164">Vero</span><span class="sxs-lookup"><span data-stu-id="91bd0-164">True</span></span>                              |
| <span data-ttu-id="91bd0-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="91bd0-165">Is Indexed</span></span>             | <span data-ttu-id="91bd0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-166">False</span></span>                             |
| <span data-ttu-id="91bd0-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="91bd0-167">In Global Catalog</span></span>      | <span data-ttu-id="91bd0-168">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-168">False</span></span>                             |
| <span data-ttu-id="91bd0-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="91bd0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="91bd0-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="91bd0-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="91bd0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91bd0-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="91bd0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91bd0-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="91bd0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-173">Search-Flags</span></span>           | <span data-ttu-id="91bd0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-174">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-175">System-Flags</span></span>           | <span data-ttu-id="91bd0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-176">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="91bd0-177">Classes used in</span></span>        | [<span data-ttu-id="91bd0-178">**Utente**</span><span class="sxs-lookup"><span data-stu-id="91bd0-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91bd0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91bd0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91bd0-180">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-180">Entry</span></span> | <span data-ttu-id="91bd0-181">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="91bd0-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="91bd0-184">System-Only</span></span>            | <span data-ttu-id="91bd0-185">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-185">False</span></span>                             |
| <span data-ttu-id="91bd0-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="91bd0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="91bd0-187">Vero</span><span class="sxs-lookup"><span data-stu-id="91bd0-187">True</span></span>                              |
| <span data-ttu-id="91bd0-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="91bd0-188">Is Indexed</span></span>             | <span data-ttu-id="91bd0-189">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-189">False</span></span>                             |
| <span data-ttu-id="91bd0-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="91bd0-190">In Global Catalog</span></span>      | <span data-ttu-id="91bd0-191">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-191">False</span></span>                             |
| <span data-ttu-id="91bd0-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="91bd0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="91bd0-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="91bd0-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="91bd0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91bd0-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="91bd0-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91bd0-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="91bd0-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-196">Search-Flags</span></span>           | <span data-ttu-id="91bd0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-197">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-198">System-Flags</span></span>           | <span data-ttu-id="91bd0-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-199">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="91bd0-200">Classes used in</span></span>        | [<span data-ttu-id="91bd0-201">**Utente**</span><span class="sxs-lookup"><span data-stu-id="91bd0-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91bd0-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91bd0-202">Windows Server 2008</span></span>



| <span data-ttu-id="91bd0-203">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-203">Entry</span></span> | <span data-ttu-id="91bd0-204">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="91bd0-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="91bd0-207">System-Only</span></span>            | <span data-ttu-id="91bd0-208">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-208">False</span></span>                             |
| <span data-ttu-id="91bd0-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="91bd0-209">Is-Single-Valued</span></span>       | <span data-ttu-id="91bd0-210">Vero</span><span class="sxs-lookup"><span data-stu-id="91bd0-210">True</span></span>                              |
| <span data-ttu-id="91bd0-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="91bd0-211">Is Indexed</span></span>             | <span data-ttu-id="91bd0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-212">False</span></span>                             |
| <span data-ttu-id="91bd0-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="91bd0-213">In Global Catalog</span></span>      | <span data-ttu-id="91bd0-214">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-214">False</span></span>                             |
| <span data-ttu-id="91bd0-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="91bd0-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="91bd0-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="91bd0-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="91bd0-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91bd0-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="91bd0-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91bd0-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="91bd0-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-219">Search-Flags</span></span>           | <span data-ttu-id="91bd0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-220">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-221">System-Flags</span></span>           | <span data-ttu-id="91bd0-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-222">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="91bd0-223">Classes used in</span></span>        | [<span data-ttu-id="91bd0-224">**Utente**</span><span class="sxs-lookup"><span data-stu-id="91bd0-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91bd0-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91bd0-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91bd0-226">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-226">Entry</span></span> | <span data-ttu-id="91bd0-227">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="91bd0-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="91bd0-230">System-Only</span></span>            | <span data-ttu-id="91bd0-231">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-231">False</span></span>                             |
| <span data-ttu-id="91bd0-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="91bd0-232">Is-Single-Valued</span></span>       | <span data-ttu-id="91bd0-233">Vero</span><span class="sxs-lookup"><span data-stu-id="91bd0-233">True</span></span>                              |
| <span data-ttu-id="91bd0-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="91bd0-234">Is Indexed</span></span>             | <span data-ttu-id="91bd0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-235">False</span></span>                             |
| <span data-ttu-id="91bd0-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="91bd0-236">In Global Catalog</span></span>      | <span data-ttu-id="91bd0-237">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-237">False</span></span>                             |
| <span data-ttu-id="91bd0-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="91bd0-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="91bd0-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="91bd0-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="91bd0-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91bd0-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="91bd0-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91bd0-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="91bd0-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-242">Search-Flags</span></span>           | <span data-ttu-id="91bd0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-243">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-244">System-Flags</span></span>           | <span data-ttu-id="91bd0-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-245">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="91bd0-246">Classes used in</span></span>        | [<span data-ttu-id="91bd0-247">**Utente**</span><span class="sxs-lookup"><span data-stu-id="91bd0-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91bd0-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91bd0-248">Windows Server 2012</span></span>



| <span data-ttu-id="91bd0-249">Voce</span><span class="sxs-lookup"><span data-stu-id="91bd0-249">Entry</span></span> | <span data-ttu-id="91bd0-250">Valore</span><span class="sxs-lookup"><span data-stu-id="91bd0-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="91bd0-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="91bd0-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91bd0-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="91bd0-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="91bd0-253">System-Only</span></span>            | <span data-ttu-id="91bd0-254">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-254">False</span></span>                             |
| <span data-ttu-id="91bd0-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="91bd0-255">Is-Single-Valued</span></span>       | <span data-ttu-id="91bd0-256">Vero</span><span class="sxs-lookup"><span data-stu-id="91bd0-256">True</span></span>                              |
| <span data-ttu-id="91bd0-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="91bd0-257">Is Indexed</span></span>             | <span data-ttu-id="91bd0-258">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-258">False</span></span>                             |
| <span data-ttu-id="91bd0-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="91bd0-259">In Global Catalog</span></span>      | <span data-ttu-id="91bd0-260">Falso</span><span class="sxs-lookup"><span data-stu-id="91bd0-260">False</span></span>                             |
| <span data-ttu-id="91bd0-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="91bd0-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="91bd0-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="91bd0-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="91bd0-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91bd0-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="91bd0-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91bd0-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="91bd0-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-265">Search-Flags</span></span>           | <span data-ttu-id="91bd0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-266">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91bd0-267">System-Flags</span></span>           | <span data-ttu-id="91bd0-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91bd0-268">0x00000010</span></span>                        |
| <span data-ttu-id="91bd0-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="91bd0-269">Classes used in</span></span>        | [<span data-ttu-id="91bd0-270">**Utente**</span><span class="sxs-lookup"><span data-stu-id="91bd0-270">**User**</span></span>](c-user.md)<br/> |



 

 





