---
title: Attributo Script-Path
description: Questo attributo specifica il percorso per lo script di accesso dell'utente. La stringa può essere null.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Schema AD Script-Path attribute
- Schema AD dell'attributo scriptPath
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122682"
---
# <a name="script-path-attribute"></a><span data-ttu-id="dc2b4-106">Attributo Script-Path</span><span class="sxs-lookup"><span data-stu-id="dc2b4-106">Script-Path attribute</span></span>

<span data-ttu-id="dc2b4-107">Questo attributo specifica il percorso per lo script di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dc2b4-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="dc2b4-108">La stringa può essere null.</span><span class="sxs-lookup"><span data-stu-id="dc2b4-108">The string can be null.</span></span>



| <span data-ttu-id="dc2b4-109">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-109">Entry</span></span> | <span data-ttu-id="dc2b4-110">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc2b4-111">CN</span><span class="sxs-lookup"><span data-stu-id="dc2b4-111">CN</span></span>                | <span data-ttu-id="dc2b4-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="dc2b4-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="dc2b4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dc2b4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dc2b4-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="dc2b4-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="dc2b4-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dc2b4-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="dc2b4-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-116">Update Privilege</span></span>  | <span data-ttu-id="dc2b4-117">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="dc2b4-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="dc2b4-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-118">Update Frequency</span></span>  | <span data-ttu-id="dc2b4-119">Quando viene creato il record utente e ogni volta che è necessario modificare il percorso.</span><span class="sxs-lookup"><span data-stu-id="dc2b4-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="dc2b4-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-120">Attribute-Id</span></span>      | <span data-ttu-id="dc2b4-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="dc2b4-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="dc2b4-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dc2b4-122">System-Id-Guid</span></span>    | <span data-ttu-id="dc2b4-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dc2b4-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="dc2b4-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc2b4-124">Syntax</span></span>            | [<span data-ttu-id="dc2b4-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="dc2b4-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dc2b4-126">Implementations</span></span>

-   [<span data-ttu-id="dc2b4-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc2b4-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc2b4-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc2b4-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc2b4-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc2b4-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc2b4-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc2b4-133">Windows 2000 Server</span></span>



| <span data-ttu-id="dc2b4-134">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-134">Entry</span></span> | <span data-ttu-id="dc2b4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dc2b4-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b4-138">System-Only</span></span>            | <span data-ttu-id="dc2b4-139">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-139">False</span></span>                             |
| <span data-ttu-id="dc2b4-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc2b4-140">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b4-141">Vero</span><span class="sxs-lookup"><span data-stu-id="dc2b4-141">True</span></span>                              |
| <span data-ttu-id="dc2b4-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc2b4-142">Is Indexed</span></span>             | <span data-ttu-id="dc2b4-143">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-143">False</span></span>                             |
| <span data-ttu-id="dc2b4-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc2b4-144">In Global Catalog</span></span>      | <span data-ttu-id="dc2b4-145">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-145">False</span></span>                             |
| <span data-ttu-id="dc2b4-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b4-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc2b4-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dc2b4-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b4-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b4-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-150">Search-Flags</span></span>           | <span data-ttu-id="dc2b4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-151">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-152">System-Flags</span></span>           | <span data-ttu-id="dc2b4-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-153">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc2b4-154">Classes used in</span></span>        | [<span data-ttu-id="dc2b4-155">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc2b4-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc2b4-156">Windows Server 2003</span></span>



| <span data-ttu-id="dc2b4-157">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-157">Entry</span></span> | <span data-ttu-id="dc2b4-158">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dc2b4-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b4-161">System-Only</span></span>            | <span data-ttu-id="dc2b4-162">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-162">False</span></span>                             |
| <span data-ttu-id="dc2b4-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc2b4-163">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b4-164">Vero</span><span class="sxs-lookup"><span data-stu-id="dc2b4-164">True</span></span>                              |
| <span data-ttu-id="dc2b4-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc2b4-165">Is Indexed</span></span>             | <span data-ttu-id="dc2b4-166">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-166">False</span></span>                             |
| <span data-ttu-id="dc2b4-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc2b4-167">In Global Catalog</span></span>      | <span data-ttu-id="dc2b4-168">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-168">False</span></span>                             |
| <span data-ttu-id="dc2b4-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b4-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc2b4-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dc2b4-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b4-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b4-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-173">Search-Flags</span></span>           | <span data-ttu-id="dc2b4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-174">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-175">System-Flags</span></span>           | <span data-ttu-id="dc2b4-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-176">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc2b4-177">Classes used in</span></span>        | [<span data-ttu-id="dc2b4-178">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc2b4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc2b4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc2b4-180">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-180">Entry</span></span> | <span data-ttu-id="dc2b4-181">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dc2b4-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b4-184">System-Only</span></span>            | <span data-ttu-id="dc2b4-185">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-185">False</span></span>                             |
| <span data-ttu-id="dc2b4-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc2b4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b4-187">Vero</span><span class="sxs-lookup"><span data-stu-id="dc2b4-187">True</span></span>                              |
| <span data-ttu-id="dc2b4-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc2b4-188">Is Indexed</span></span>             | <span data-ttu-id="dc2b4-189">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-189">False</span></span>                             |
| <span data-ttu-id="dc2b4-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc2b4-190">In Global Catalog</span></span>      | <span data-ttu-id="dc2b4-191">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-191">False</span></span>                             |
| <span data-ttu-id="dc2b4-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b4-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc2b4-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dc2b4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b4-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b4-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-196">Search-Flags</span></span>           | <span data-ttu-id="dc2b4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-197">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-198">System-Flags</span></span>           | <span data-ttu-id="dc2b4-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-199">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc2b4-200">Classes used in</span></span>        | [<span data-ttu-id="dc2b4-201">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc2b4-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc2b4-202">Windows Server 2008</span></span>



| <span data-ttu-id="dc2b4-203">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-203">Entry</span></span> | <span data-ttu-id="dc2b4-204">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dc2b4-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b4-207">System-Only</span></span>            | <span data-ttu-id="dc2b4-208">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-208">False</span></span>                             |
| <span data-ttu-id="dc2b4-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc2b4-209">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b4-210">Vero</span><span class="sxs-lookup"><span data-stu-id="dc2b4-210">True</span></span>                              |
| <span data-ttu-id="dc2b4-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc2b4-211">Is Indexed</span></span>             | <span data-ttu-id="dc2b4-212">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-212">False</span></span>                             |
| <span data-ttu-id="dc2b4-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc2b4-213">In Global Catalog</span></span>      | <span data-ttu-id="dc2b4-214">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-214">False</span></span>                             |
| <span data-ttu-id="dc2b4-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b4-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc2b4-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dc2b4-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b4-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b4-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-219">Search-Flags</span></span>           | <span data-ttu-id="dc2b4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-220">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-221">System-Flags</span></span>           | <span data-ttu-id="dc2b4-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-222">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc2b4-223">Classes used in</span></span>        | [<span data-ttu-id="dc2b4-224">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc2b4-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc2b4-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc2b4-226">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-226">Entry</span></span> | <span data-ttu-id="dc2b4-227">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dc2b4-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b4-230">System-Only</span></span>            | <span data-ttu-id="dc2b4-231">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-231">False</span></span>                             |
| <span data-ttu-id="dc2b4-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc2b4-232">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b4-233">Vero</span><span class="sxs-lookup"><span data-stu-id="dc2b4-233">True</span></span>                              |
| <span data-ttu-id="dc2b4-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc2b4-234">Is Indexed</span></span>             | <span data-ttu-id="dc2b4-235">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-235">False</span></span>                             |
| <span data-ttu-id="dc2b4-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc2b4-236">In Global Catalog</span></span>      | <span data-ttu-id="dc2b4-237">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-237">False</span></span>                             |
| <span data-ttu-id="dc2b4-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b4-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc2b4-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dc2b4-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b4-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b4-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-242">Search-Flags</span></span>           | <span data-ttu-id="dc2b4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-243">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-244">System-Flags</span></span>           | <span data-ttu-id="dc2b4-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-245">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc2b4-246">Classes used in</span></span>        | [<span data-ttu-id="dc2b4-247">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc2b4-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc2b4-248">Windows Server 2012</span></span>



| <span data-ttu-id="dc2b4-249">Voce</span><span class="sxs-lookup"><span data-stu-id="dc2b4-249">Entry</span></span> | <span data-ttu-id="dc2b4-250">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="dc2b4-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dc2b4-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b4-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="dc2b4-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b4-253">System-Only</span></span>            | <span data-ttu-id="dc2b4-254">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-254">False</span></span>                             |
| <span data-ttu-id="dc2b4-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dc2b4-255">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b4-256">Vero</span><span class="sxs-lookup"><span data-stu-id="dc2b4-256">True</span></span>                              |
| <span data-ttu-id="dc2b4-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dc2b4-257">Is Indexed</span></span>             | <span data-ttu-id="dc2b4-258">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-258">False</span></span>                             |
| <span data-ttu-id="dc2b4-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dc2b4-259">In Global Catalog</span></span>      | <span data-ttu-id="dc2b4-260">Falso</span><span class="sxs-lookup"><span data-stu-id="dc2b4-260">False</span></span>                             |
| <span data-ttu-id="dc2b4-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dc2b4-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b4-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dc2b4-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="dc2b4-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b4-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b4-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="dc2b4-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-265">Search-Flags</span></span>           | <span data-ttu-id="dc2b4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-266">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b4-267">System-Flags</span></span>           | <span data-ttu-id="dc2b4-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b4-268">0x00000010</span></span>                        |
| <span data-ttu-id="dc2b4-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dc2b4-269">Classes used in</span></span>        | [<span data-ttu-id="dc2b4-270">**Utente**</span><span class="sxs-lookup"><span data-stu-id="dc2b4-270">**User**</span></span>](c-user.md)<br/> |



 

 





