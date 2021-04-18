---
title: Attributo Home-Drive
description: Specifica la lettera di unità in cui eseguire il mapping del percorso UNC specificato da homeDirectory.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Schema AD Home-Drive attribute
- Schema AD dell'attributo homeDrive
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302892"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="758ae-105">Attributo Home-Drive</span><span class="sxs-lookup"><span data-stu-id="758ae-105">Home-Drive attribute</span></span>

<span data-ttu-id="758ae-106">Specifica la lettera di unità in cui eseguire il mapping del percorso UNC specificato da [**HomeDirectory**](a-homedirectory.md).</span><span class="sxs-lookup"><span data-stu-id="758ae-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="758ae-107">La lettera di unità deve essere specificata nel formato *LetteraUnità \* \* *:** dove *LetteraUnità* è la lettera dell'unità da mappare.</span><span class="sxs-lookup"><span data-stu-id="758ae-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="758ae-108">*LetteraUnità* deve essere costituito da una singola lettera maiuscola e dai due punti (:) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="758ae-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="758ae-109">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-109">Entry</span></span> | <span data-ttu-id="758ae-110">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="758ae-111">CN</span><span class="sxs-lookup"><span data-stu-id="758ae-111">CN</span></span>                | <span data-ttu-id="758ae-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="758ae-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="758ae-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="758ae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="758ae-114">homeDrive</span><span class="sxs-lookup"><span data-stu-id="758ae-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="758ae-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="758ae-115">Size</span></span>              | <span data-ttu-id="758ae-116">2 byte</span><span class="sxs-lookup"><span data-stu-id="758ae-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="758ae-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="758ae-117">Update Privilege</span></span>  | <span data-ttu-id="758ae-118">Questo valore viene impostato dall'amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="758ae-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="758ae-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="758ae-119">Update Frequency</span></span>  | <span data-ttu-id="758ae-120">Quando viene creato il record di un utente e ogni volta che è necessario modificare l'unità Home.</span><span class="sxs-lookup"><span data-stu-id="758ae-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="758ae-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-121">Attribute-Id</span></span>      | <span data-ttu-id="758ae-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="758ae-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="758ae-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="758ae-123">System-Id-Guid</span></span>    | <span data-ttu-id="758ae-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="758ae-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="758ae-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="758ae-125">Syntax</span></span>            | [<span data-ttu-id="758ae-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="758ae-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="758ae-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="758ae-127">Implementations</span></span>

-   [<span data-ttu-id="758ae-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="758ae-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="758ae-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="758ae-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="758ae-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="758ae-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="758ae-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="758ae-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="758ae-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="758ae-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="758ae-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="758ae-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="758ae-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="758ae-134">Windows 2000 Server</span></span>



| <span data-ttu-id="758ae-135">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-135">Entry</span></span> | <span data-ttu-id="758ae-136">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="758ae-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="758ae-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="758ae-139">System-Only</span></span>            | <span data-ttu-id="758ae-140">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-140">False</span></span>                             |
| <span data-ttu-id="758ae-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="758ae-141">Is-Single-Valued</span></span>       | <span data-ttu-id="758ae-142">Vero</span><span class="sxs-lookup"><span data-stu-id="758ae-142">True</span></span>                              |
| <span data-ttu-id="758ae-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="758ae-143">Is Indexed</span></span>             | <span data-ttu-id="758ae-144">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-144">False</span></span>                             |
| <span data-ttu-id="758ae-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="758ae-145">In Global Catalog</span></span>      | <span data-ttu-id="758ae-146">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-146">False</span></span>                             |
| <span data-ttu-id="758ae-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="758ae-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="758ae-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="758ae-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="758ae-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758ae-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="758ae-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758ae-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="758ae-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-151">Search-Flags</span></span>           | <span data-ttu-id="758ae-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-152">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-153">System-Flags</span></span>           | <span data-ttu-id="758ae-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-154">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="758ae-155">Classes used in</span></span>        | [<span data-ttu-id="758ae-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="758ae-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="758ae-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="758ae-157">Windows Server 2003</span></span>



| <span data-ttu-id="758ae-158">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-158">Entry</span></span> | <span data-ttu-id="758ae-159">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="758ae-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="758ae-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="758ae-162">System-Only</span></span>            | <span data-ttu-id="758ae-163">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-163">False</span></span>                             |
| <span data-ttu-id="758ae-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="758ae-164">Is-Single-Valued</span></span>       | <span data-ttu-id="758ae-165">Vero</span><span class="sxs-lookup"><span data-stu-id="758ae-165">True</span></span>                              |
| <span data-ttu-id="758ae-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="758ae-166">Is Indexed</span></span>             | <span data-ttu-id="758ae-167">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-167">False</span></span>                             |
| <span data-ttu-id="758ae-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="758ae-168">In Global Catalog</span></span>      | <span data-ttu-id="758ae-169">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-169">False</span></span>                             |
| <span data-ttu-id="758ae-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="758ae-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="758ae-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="758ae-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="758ae-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758ae-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="758ae-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758ae-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="758ae-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-174">Search-Flags</span></span>           | <span data-ttu-id="758ae-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-175">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-176">System-Flags</span></span>           | <span data-ttu-id="758ae-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-177">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="758ae-178">Classes used in</span></span>        | [<span data-ttu-id="758ae-179">**Utente**</span><span class="sxs-lookup"><span data-stu-id="758ae-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="758ae-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="758ae-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="758ae-181">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-181">Entry</span></span> | <span data-ttu-id="758ae-182">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="758ae-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="758ae-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="758ae-185">System-Only</span></span>            | <span data-ttu-id="758ae-186">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-186">False</span></span>                             |
| <span data-ttu-id="758ae-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="758ae-187">Is-Single-Valued</span></span>       | <span data-ttu-id="758ae-188">Vero</span><span class="sxs-lookup"><span data-stu-id="758ae-188">True</span></span>                              |
| <span data-ttu-id="758ae-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="758ae-189">Is Indexed</span></span>             | <span data-ttu-id="758ae-190">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-190">False</span></span>                             |
| <span data-ttu-id="758ae-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="758ae-191">In Global Catalog</span></span>      | <span data-ttu-id="758ae-192">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-192">False</span></span>                             |
| <span data-ttu-id="758ae-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="758ae-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="758ae-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="758ae-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="758ae-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758ae-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="758ae-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758ae-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="758ae-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-197">Search-Flags</span></span>           | <span data-ttu-id="758ae-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-198">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-199">System-Flags</span></span>           | <span data-ttu-id="758ae-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-200">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="758ae-201">Classes used in</span></span>        | [<span data-ttu-id="758ae-202">**Utente**</span><span class="sxs-lookup"><span data-stu-id="758ae-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="758ae-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="758ae-203">Windows Server 2008</span></span>



| <span data-ttu-id="758ae-204">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-204">Entry</span></span> | <span data-ttu-id="758ae-205">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="758ae-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="758ae-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="758ae-208">System-Only</span></span>            | <span data-ttu-id="758ae-209">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-209">False</span></span>                             |
| <span data-ttu-id="758ae-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="758ae-210">Is-Single-Valued</span></span>       | <span data-ttu-id="758ae-211">Vero</span><span class="sxs-lookup"><span data-stu-id="758ae-211">True</span></span>                              |
| <span data-ttu-id="758ae-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="758ae-212">Is Indexed</span></span>             | <span data-ttu-id="758ae-213">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-213">False</span></span>                             |
| <span data-ttu-id="758ae-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="758ae-214">In Global Catalog</span></span>      | <span data-ttu-id="758ae-215">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-215">False</span></span>                             |
| <span data-ttu-id="758ae-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="758ae-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="758ae-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="758ae-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="758ae-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758ae-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="758ae-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758ae-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="758ae-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-220">Search-Flags</span></span>           | <span data-ttu-id="758ae-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-221">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-222">System-Flags</span></span>           | <span data-ttu-id="758ae-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-223">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="758ae-224">Classes used in</span></span>        | [<span data-ttu-id="758ae-225">**Utente**</span><span class="sxs-lookup"><span data-stu-id="758ae-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="758ae-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="758ae-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="758ae-227">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-227">Entry</span></span> | <span data-ttu-id="758ae-228">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="758ae-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="758ae-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="758ae-231">System-Only</span></span>            | <span data-ttu-id="758ae-232">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-232">False</span></span>                             |
| <span data-ttu-id="758ae-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="758ae-233">Is-Single-Valued</span></span>       | <span data-ttu-id="758ae-234">Vero</span><span class="sxs-lookup"><span data-stu-id="758ae-234">True</span></span>                              |
| <span data-ttu-id="758ae-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="758ae-235">Is Indexed</span></span>             | <span data-ttu-id="758ae-236">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-236">False</span></span>                             |
| <span data-ttu-id="758ae-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="758ae-237">In Global Catalog</span></span>      | <span data-ttu-id="758ae-238">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-238">False</span></span>                             |
| <span data-ttu-id="758ae-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="758ae-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="758ae-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="758ae-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="758ae-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758ae-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="758ae-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758ae-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="758ae-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-243">Search-Flags</span></span>           | <span data-ttu-id="758ae-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-244">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-245">System-Flags</span></span>           | <span data-ttu-id="758ae-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-246">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="758ae-247">Classes used in</span></span>        | [<span data-ttu-id="758ae-248">**Utente**</span><span class="sxs-lookup"><span data-stu-id="758ae-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="758ae-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="758ae-249">Windows Server 2012</span></span>



| <span data-ttu-id="758ae-250">Voce</span><span class="sxs-lookup"><span data-stu-id="758ae-250">Entry</span></span> | <span data-ttu-id="758ae-251">Valore</span><span class="sxs-lookup"><span data-stu-id="758ae-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="758ae-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="758ae-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758ae-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="758ae-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="758ae-254">System-Only</span></span>            | <span data-ttu-id="758ae-255">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-255">False</span></span>                             |
| <span data-ttu-id="758ae-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="758ae-256">Is-Single-Valued</span></span>       | <span data-ttu-id="758ae-257">Vero</span><span class="sxs-lookup"><span data-stu-id="758ae-257">True</span></span>                              |
| <span data-ttu-id="758ae-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="758ae-258">Is Indexed</span></span>             | <span data-ttu-id="758ae-259">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-259">False</span></span>                             |
| <span data-ttu-id="758ae-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="758ae-260">In Global Catalog</span></span>      | <span data-ttu-id="758ae-261">Falso</span><span class="sxs-lookup"><span data-stu-id="758ae-261">False</span></span>                             |
| <span data-ttu-id="758ae-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="758ae-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="758ae-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="758ae-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="758ae-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758ae-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="758ae-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758ae-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="758ae-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-266">Search-Flags</span></span>           | <span data-ttu-id="758ae-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-267">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758ae-268">System-Flags</span></span>           | <span data-ttu-id="758ae-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="758ae-269">0x00000010</span></span>                        |
| <span data-ttu-id="758ae-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="758ae-270">Classes used in</span></span>        | [<span data-ttu-id="758ae-271">**Utente**</span><span class="sxs-lookup"><span data-stu-id="758ae-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="758ae-272">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="758ae-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758ae-273">**homeDirectory**</span><span class="sxs-lookup"><span data-stu-id="758ae-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 





