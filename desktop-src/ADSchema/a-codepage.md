---
title: Attributo Code-Page
description: Specifica la tabella codici per la lingua scelta dall'utente. Questo valore non viene utilizzato da Windows 2000.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Schema AD Code-Page attribute
- Schema AD dell'attributo codepage
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744402"
---
# <a name="code-page-attribute"></a><span data-ttu-id="da82d-106">Attributo Code-Page</span><span class="sxs-lookup"><span data-stu-id="da82d-106">Code-Page attribute</span></span>

<span data-ttu-id="da82d-107">Specifica la tabella codici per la lingua scelta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="da82d-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="da82d-108">Questo valore non viene utilizzato da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="da82d-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="da82d-109">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-109">Entry</span></span> | <span data-ttu-id="da82d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="da82d-111">CN</span><span class="sxs-lookup"><span data-stu-id="da82d-111">CN</span></span>                | <span data-ttu-id="da82d-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="da82d-112">Code-Page</span></span>                                             |
| <span data-ttu-id="da82d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da82d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="da82d-114">codePage</span><span class="sxs-lookup"><span data-stu-id="da82d-114">codePage</span></span>                                              |
| <span data-ttu-id="da82d-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="da82d-115">Size</span></span>              | <span data-ttu-id="da82d-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="da82d-116">4 bytes</span></span>                                               |
| <span data-ttu-id="da82d-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="da82d-117">Update Privilege</span></span>  | <span data-ttu-id="da82d-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="da82d-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="da82d-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="da82d-119">Update Frequency</span></span>  | <span data-ttu-id="da82d-120">Quando l'utente desidera modificare la lingua predefinita.</span><span class="sxs-lookup"><span data-stu-id="da82d-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="da82d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-121">Attribute-Id</span></span>      | <span data-ttu-id="da82d-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="da82d-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="da82d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da82d-123">System-Id-Guid</span></span>    | <span data-ttu-id="da82d-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="da82d-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="da82d-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da82d-125">Syntax</span></span>            | [<span data-ttu-id="da82d-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="da82d-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="da82d-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="da82d-127">Implementations</span></span>

-   [<span data-ttu-id="da82d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="da82d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="da82d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da82d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da82d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da82d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da82d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da82d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da82d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da82d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da82d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da82d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="da82d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da82d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="da82d-135">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-135">Entry</span></span> | <span data-ttu-id="da82d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da82d-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da82d-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="da82d-139">System-Only</span></span>            | <span data-ttu-id="da82d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-140">False</span></span>                             |
| <span data-ttu-id="da82d-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da82d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="da82d-142">Vero</span><span class="sxs-lookup"><span data-stu-id="da82d-142">True</span></span>                              |
| <span data-ttu-id="da82d-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da82d-143">Is Indexed</span></span>             | <span data-ttu-id="da82d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-144">False</span></span>                             |
| <span data-ttu-id="da82d-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da82d-145">In Global Catalog</span></span>      | <span data-ttu-id="da82d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-146">False</span></span>                             |
| <span data-ttu-id="da82d-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da82d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="da82d-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da82d-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da82d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da82d-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="da82d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da82d-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="da82d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-151">Search-Flags</span></span>           | <span data-ttu-id="da82d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-152">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-153">System-Flags</span></span>           | <span data-ttu-id="da82d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-154">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da82d-155">Classes used in</span></span>        | [<span data-ttu-id="da82d-156">**Utente**</span><span class="sxs-lookup"><span data-stu-id="da82d-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="da82d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da82d-157">Windows Server 2003</span></span>



| <span data-ttu-id="da82d-158">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-158">Entry</span></span> | <span data-ttu-id="da82d-159">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da82d-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da82d-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="da82d-162">System-Only</span></span>            | <span data-ttu-id="da82d-163">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-163">False</span></span>                             |
| <span data-ttu-id="da82d-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da82d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="da82d-165">Vero</span><span class="sxs-lookup"><span data-stu-id="da82d-165">True</span></span>                              |
| <span data-ttu-id="da82d-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da82d-166">Is Indexed</span></span>             | <span data-ttu-id="da82d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-167">False</span></span>                             |
| <span data-ttu-id="da82d-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da82d-168">In Global Catalog</span></span>      | <span data-ttu-id="da82d-169">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-169">False</span></span>                             |
| <span data-ttu-id="da82d-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da82d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="da82d-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da82d-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da82d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da82d-172">Range-Lower</span></span>            | <span data-ttu-id="da82d-173">0</span><span class="sxs-lookup"><span data-stu-id="da82d-173">0</span></span>                                 |
| <span data-ttu-id="da82d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da82d-174">Range-Upper</span></span>            | <span data-ttu-id="da82d-175">65535</span><span class="sxs-lookup"><span data-stu-id="da82d-175">65535</span></span>                             |
| <span data-ttu-id="da82d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-176">Search-Flags</span></span>           | <span data-ttu-id="da82d-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-177">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-178">System-Flags</span></span>           | <span data-ttu-id="da82d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-179">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da82d-180">Classes used in</span></span>        | [<span data-ttu-id="da82d-181">**Utente**</span><span class="sxs-lookup"><span data-stu-id="da82d-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da82d-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da82d-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da82d-183">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-183">Entry</span></span> | <span data-ttu-id="da82d-184">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da82d-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da82d-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="da82d-187">System-Only</span></span>            | <span data-ttu-id="da82d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-188">False</span></span>                             |
| <span data-ttu-id="da82d-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da82d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="da82d-190">Vero</span><span class="sxs-lookup"><span data-stu-id="da82d-190">True</span></span>                              |
| <span data-ttu-id="da82d-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da82d-191">Is Indexed</span></span>             | <span data-ttu-id="da82d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-192">False</span></span>                             |
| <span data-ttu-id="da82d-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da82d-193">In Global Catalog</span></span>      | <span data-ttu-id="da82d-194">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-194">False</span></span>                             |
| <span data-ttu-id="da82d-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da82d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="da82d-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da82d-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da82d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da82d-197">Range-Lower</span></span>            | <span data-ttu-id="da82d-198">0</span><span class="sxs-lookup"><span data-stu-id="da82d-198">0</span></span>                                 |
| <span data-ttu-id="da82d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da82d-199">Range-Upper</span></span>            | <span data-ttu-id="da82d-200">65535</span><span class="sxs-lookup"><span data-stu-id="da82d-200">65535</span></span>                             |
| <span data-ttu-id="da82d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-201">Search-Flags</span></span>           | <span data-ttu-id="da82d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-202">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-203">System-Flags</span></span>           | <span data-ttu-id="da82d-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-204">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da82d-205">Classes used in</span></span>        | [<span data-ttu-id="da82d-206">**Utente**</span><span class="sxs-lookup"><span data-stu-id="da82d-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="da82d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da82d-207">Windows Server 2008</span></span>



| <span data-ttu-id="da82d-208">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-208">Entry</span></span> | <span data-ttu-id="da82d-209">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da82d-210">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da82d-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="da82d-212">System-Only</span></span>            | <span data-ttu-id="da82d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-213">False</span></span>                             |
| <span data-ttu-id="da82d-214">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da82d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="da82d-215">Vero</span><span class="sxs-lookup"><span data-stu-id="da82d-215">True</span></span>                              |
| <span data-ttu-id="da82d-216">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da82d-216">Is Indexed</span></span>             | <span data-ttu-id="da82d-217">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-217">False</span></span>                             |
| <span data-ttu-id="da82d-218">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da82d-218">In Global Catalog</span></span>      | <span data-ttu-id="da82d-219">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-219">False</span></span>                             |
| <span data-ttu-id="da82d-220">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da82d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="da82d-221">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da82d-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da82d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da82d-222">Range-Lower</span></span>            | <span data-ttu-id="da82d-223">0</span><span class="sxs-lookup"><span data-stu-id="da82d-223">0</span></span>                                 |
| <span data-ttu-id="da82d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da82d-224">Range-Upper</span></span>            | <span data-ttu-id="da82d-225">65535</span><span class="sxs-lookup"><span data-stu-id="da82d-225">65535</span></span>                             |
| <span data-ttu-id="da82d-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-226">Search-Flags</span></span>           | <span data-ttu-id="da82d-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-227">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-228">System-Flags</span></span>           | <span data-ttu-id="da82d-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-229">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-230">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da82d-230">Classes used in</span></span>        | [<span data-ttu-id="da82d-231">**Utente**</span><span class="sxs-lookup"><span data-stu-id="da82d-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da82d-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da82d-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da82d-233">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-233">Entry</span></span> | <span data-ttu-id="da82d-234">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da82d-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da82d-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="da82d-237">System-Only</span></span>            | <span data-ttu-id="da82d-238">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-238">False</span></span>                             |
| <span data-ttu-id="da82d-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da82d-239">Is-Single-Valued</span></span>       | <span data-ttu-id="da82d-240">Vero</span><span class="sxs-lookup"><span data-stu-id="da82d-240">True</span></span>                              |
| <span data-ttu-id="da82d-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da82d-241">Is Indexed</span></span>             | <span data-ttu-id="da82d-242">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-242">False</span></span>                             |
| <span data-ttu-id="da82d-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da82d-243">In Global Catalog</span></span>      | <span data-ttu-id="da82d-244">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-244">False</span></span>                             |
| <span data-ttu-id="da82d-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da82d-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="da82d-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da82d-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da82d-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da82d-247">Range-Lower</span></span>            | <span data-ttu-id="da82d-248">0</span><span class="sxs-lookup"><span data-stu-id="da82d-248">0</span></span>                                 |
| <span data-ttu-id="da82d-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da82d-249">Range-Upper</span></span>            | <span data-ttu-id="da82d-250">65535</span><span class="sxs-lookup"><span data-stu-id="da82d-250">65535</span></span>                             |
| <span data-ttu-id="da82d-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-251">Search-Flags</span></span>           | <span data-ttu-id="da82d-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-252">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-253">System-Flags</span></span>           | <span data-ttu-id="da82d-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-254">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-255">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da82d-255">Classes used in</span></span>        | [<span data-ttu-id="da82d-256">**Utente**</span><span class="sxs-lookup"><span data-stu-id="da82d-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="da82d-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da82d-257">Windows Server 2012</span></span>



| <span data-ttu-id="da82d-258">Voce</span><span class="sxs-lookup"><span data-stu-id="da82d-258">Entry</span></span> | <span data-ttu-id="da82d-259">Valore</span><span class="sxs-lookup"><span data-stu-id="da82d-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="da82d-260">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="da82d-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da82d-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="da82d-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="da82d-262">System-Only</span></span>            | <span data-ttu-id="da82d-263">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-263">False</span></span>                             |
| <span data-ttu-id="da82d-264">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="da82d-264">Is-Single-Valued</span></span>       | <span data-ttu-id="da82d-265">Vero</span><span class="sxs-lookup"><span data-stu-id="da82d-265">True</span></span>                              |
| <span data-ttu-id="da82d-266">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="da82d-266">Is Indexed</span></span>             | <span data-ttu-id="da82d-267">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-267">False</span></span>                             |
| <span data-ttu-id="da82d-268">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="da82d-268">In Global Catalog</span></span>      | <span data-ttu-id="da82d-269">Falso</span><span class="sxs-lookup"><span data-stu-id="da82d-269">False</span></span>                             |
| <span data-ttu-id="da82d-270">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="da82d-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="da82d-271">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="da82d-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="da82d-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da82d-272">Range-Lower</span></span>            | <span data-ttu-id="da82d-273">0</span><span class="sxs-lookup"><span data-stu-id="da82d-273">0</span></span>                                 |
| <span data-ttu-id="da82d-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da82d-274">Range-Upper</span></span>            | <span data-ttu-id="da82d-275">65535</span><span class="sxs-lookup"><span data-stu-id="da82d-275">65535</span></span>                             |
| <span data-ttu-id="da82d-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-276">Search-Flags</span></span>           | <span data-ttu-id="da82d-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-277">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da82d-278">System-Flags</span></span>           | <span data-ttu-id="da82d-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da82d-279">0x00000010</span></span>                        |
| <span data-ttu-id="da82d-280">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="da82d-280">Classes used in</span></span>        | [<span data-ttu-id="da82d-281">**Utente**</span><span class="sxs-lookup"><span data-stu-id="da82d-281">**User**</span></span>](c-user.md)<br/> |



 

 





