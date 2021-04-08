---
title: Attributo Canonical-Name
description: Nome dell'oggetto in formato canonico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Schema AD Canonical-Name attribute
- attributo CanonicalName-schema AD
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875809"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="f646c-105">Attributo Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="f646c-105">Canonical-Name attribute</span></span>

<span data-ttu-id="f646c-106">Nome dell'oggetto in formato canonico.</span><span class="sxs-lookup"><span data-stu-id="f646c-106">The name of the object in canonical format.</span></span> <span data-ttu-id="f646c-107">myserver2.fabrikam.com/users/jeffsmith è un esempio di nome distinto in formato canonico.</span><span class="sxs-lookup"><span data-stu-id="f646c-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="f646c-108">Si tratta di un attributo costruito.</span><span class="sxs-lookup"><span data-stu-id="f646c-108">This is a constructed attribute.</span></span> <span data-ttu-id="f646c-109">I risultati restituiti sono identici a quelli restituiti dalla seguente funzione Active Directory: DsCrackNames (NULL, DS \_ Name \_ flag \_ sintattical \_ ONLY, DS \_ FQDN \_ 1779 \_ nome, \_ DS \_ nome canonico,...).</span><span class="sxs-lookup"><span data-stu-id="f646c-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="f646c-110">Per ulteriori informazioni sui formati dei nomi, vedere [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="f646c-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="f646c-111">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-111">Entry</span></span> | <span data-ttu-id="f646c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f646c-113">CN</span><span class="sxs-lookup"><span data-stu-id="f646c-113">CN</span></span>                | <span data-ttu-id="f646c-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="f646c-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="f646c-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f646c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f646c-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="f646c-116">canonicalName</span></span>                               |
| <span data-ttu-id="f646c-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f646c-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="f646c-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f646c-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f646c-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f646c-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f646c-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-120">Attribute-Id</span></span>      | <span data-ttu-id="f646c-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="f646c-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="f646c-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f646c-122">System-Id-Guid</span></span>    | <span data-ttu-id="f646c-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="f646c-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="f646c-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f646c-124">Syntax</span></span>            | [<span data-ttu-id="f646c-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f646c-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f646c-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f646c-126">Implementations</span></span>

-   [<span data-ttu-id="f646c-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f646c-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f646c-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f646c-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f646c-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f646c-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f646c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f646c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f646c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f646c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f646c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f646c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f646c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f646c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f646c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f646c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f646c-135">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-135">Entry</span></span> | <span data-ttu-id="f646c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-139">System-Only</span></span>            | <span data-ttu-id="f646c-140">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-140">True</span></span>                            |
| <span data-ttu-id="f646c-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-142">False</span></span>                           |
| <span data-ttu-id="f646c-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-143">Is Indexed</span></span>             | <span data-ttu-id="f646c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-144">False</span></span>                           |
| <span data-ttu-id="f646c-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-145">In Global Catalog</span></span>      | <span data-ttu-id="f646c-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-146">False</span></span>                           |
| <span data-ttu-id="f646c-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-151">Search-Flags</span></span>           | <span data-ttu-id="f646c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-152">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-153">System-Flags</span></span>           | <span data-ttu-id="f646c-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-154">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-155">Classes used in</span></span>        | [<span data-ttu-id="f646c-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f646c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f646c-157">Windows Server 2003</span></span>



| <span data-ttu-id="f646c-158">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-158">Entry</span></span> | <span data-ttu-id="f646c-159">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-162">System-Only</span></span>            | <span data-ttu-id="f646c-163">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-163">True</span></span>                            |
| <span data-ttu-id="f646c-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-165">False</span></span>                           |
| <span data-ttu-id="f646c-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-166">Is Indexed</span></span>             | <span data-ttu-id="f646c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-167">False</span></span>                           |
| <span data-ttu-id="f646c-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-168">In Global Catalog</span></span>      | <span data-ttu-id="f646c-169">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-169">False</span></span>                           |
| <span data-ttu-id="f646c-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-174">Search-Flags</span></span>           | <span data-ttu-id="f646c-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-175">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-176">System-Flags</span></span>           | <span data-ttu-id="f646c-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-177">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-178">Classes used in</span></span>        | [<span data-ttu-id="f646c-179">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f646c-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="f646c-180">ADAM</span></span>



| <span data-ttu-id="f646c-181">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-181">Entry</span></span> | <span data-ttu-id="f646c-182">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-185">System-Only</span></span>            | <span data-ttu-id="f646c-186">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-186">True</span></span>                            |
| <span data-ttu-id="f646c-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-188">False</span></span>                           |
| <span data-ttu-id="f646c-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-189">Is Indexed</span></span>             | <span data-ttu-id="f646c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-190">False</span></span>                           |
| <span data-ttu-id="f646c-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-191">In Global Catalog</span></span>      | <span data-ttu-id="f646c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-192">False</span></span>                           |
| <span data-ttu-id="f646c-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-197">Search-Flags</span></span>           | <span data-ttu-id="f646c-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-198">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-199">System-Flags</span></span>           | <span data-ttu-id="f646c-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-200">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-201">Classes used in</span></span>        | [<span data-ttu-id="f646c-202">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f646c-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f646c-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f646c-204">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-204">Entry</span></span> | <span data-ttu-id="f646c-205">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-208">System-Only</span></span>            | <span data-ttu-id="f646c-209">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-209">True</span></span>                            |
| <span data-ttu-id="f646c-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-211">False</span></span>                           |
| <span data-ttu-id="f646c-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-212">Is Indexed</span></span>             | <span data-ttu-id="f646c-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-213">False</span></span>                           |
| <span data-ttu-id="f646c-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-214">In Global Catalog</span></span>      | <span data-ttu-id="f646c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-215">False</span></span>                           |
| <span data-ttu-id="f646c-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-220">Search-Flags</span></span>           | <span data-ttu-id="f646c-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-221">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-222">System-Flags</span></span>           | <span data-ttu-id="f646c-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-223">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-224">Classes used in</span></span>        | [<span data-ttu-id="f646c-225">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f646c-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f646c-226">Windows Server 2008</span></span>



| <span data-ttu-id="f646c-227">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-227">Entry</span></span> | <span data-ttu-id="f646c-228">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-231">System-Only</span></span>            | <span data-ttu-id="f646c-232">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-232">True</span></span>                            |
| <span data-ttu-id="f646c-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-234">False</span></span>                           |
| <span data-ttu-id="f646c-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-235">Is Indexed</span></span>             | <span data-ttu-id="f646c-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-236">False</span></span>                           |
| <span data-ttu-id="f646c-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-237">In Global Catalog</span></span>      | <span data-ttu-id="f646c-238">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-238">False</span></span>                           |
| <span data-ttu-id="f646c-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-243">Search-Flags</span></span>           | <span data-ttu-id="f646c-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-244">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-245">System-Flags</span></span>           | <span data-ttu-id="f646c-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-246">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-247">Classes used in</span></span>        | [<span data-ttu-id="f646c-248">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f646c-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f646c-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f646c-250">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-250">Entry</span></span> | <span data-ttu-id="f646c-251">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-254">System-Only</span></span>            | <span data-ttu-id="f646c-255">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-255">True</span></span>                            |
| <span data-ttu-id="f646c-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-257">False</span></span>                           |
| <span data-ttu-id="f646c-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-258">Is Indexed</span></span>             | <span data-ttu-id="f646c-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-259">False</span></span>                           |
| <span data-ttu-id="f646c-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-260">In Global Catalog</span></span>      | <span data-ttu-id="f646c-261">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-261">False</span></span>                           |
| <span data-ttu-id="f646c-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-266">Search-Flags</span></span>           | <span data-ttu-id="f646c-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-267">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-268">System-Flags</span></span>           | <span data-ttu-id="f646c-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-269">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-270">Classes used in</span></span>        | [<span data-ttu-id="f646c-271">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f646c-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f646c-272">Windows Server 2012</span></span>



| <span data-ttu-id="f646c-273">Voce</span><span class="sxs-lookup"><span data-stu-id="f646c-273">Entry</span></span> | <span data-ttu-id="f646c-274">Valore</span><span class="sxs-lookup"><span data-stu-id="f646c-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f646c-275">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f646c-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f646c-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f646c-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="f646c-277">System-Only</span></span>            | <span data-ttu-id="f646c-278">Vero</span><span class="sxs-lookup"><span data-stu-id="f646c-278">True</span></span>                            |
| <span data-ttu-id="f646c-279">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f646c-279">Is-Single-Valued</span></span>       | <span data-ttu-id="f646c-280">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-280">False</span></span>                           |
| <span data-ttu-id="f646c-281">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f646c-281">Is Indexed</span></span>             | <span data-ttu-id="f646c-282">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-282">False</span></span>                           |
| <span data-ttu-id="f646c-283">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f646c-283">In Global Catalog</span></span>      | <span data-ttu-id="f646c-284">Falso</span><span class="sxs-lookup"><span data-stu-id="f646c-284">False</span></span>                           |
| <span data-ttu-id="f646c-285">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f646c-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="f646c-286">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f646c-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f646c-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f646c-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f646c-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f646c-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f646c-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-289">Search-Flags</span></span>           | <span data-ttu-id="f646c-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f646c-290">0x00000000</span></span>                      |
| <span data-ttu-id="f646c-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f646c-291">System-Flags</span></span>           | <span data-ttu-id="f646c-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="f646c-292">0x08000014</span></span>                      |
| <span data-ttu-id="f646c-293">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f646c-293">Classes used in</span></span>        | [<span data-ttu-id="f646c-294">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f646c-294">**Top**</span></span>](c-top.md)<br/> |



 

