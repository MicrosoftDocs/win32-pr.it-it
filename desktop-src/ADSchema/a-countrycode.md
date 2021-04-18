---
title: Attributo Country-Code
description: Specifica il codice paese/area geografica per la lingua scelta dall'utente. Questo valore non viene utilizzato da Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Schema AD Country-Code attribute
- Schema AD dell'attributo countryCode
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303605"
---
# <a name="country-code-attribute"></a><span data-ttu-id="632a7-106">Attributo Country-Code</span><span class="sxs-lookup"><span data-stu-id="632a7-106">Country-Code attribute</span></span>

<span data-ttu-id="632a7-107">Specifica il codice paese/area geografica per la lingua scelta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="632a7-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="632a7-108">Questo valore non viene utilizzato da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="632a7-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="632a7-109">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-109">Entry</span></span> | <span data-ttu-id="632a7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="632a7-111">CN</span><span class="sxs-lookup"><span data-stu-id="632a7-111">CN</span></span>                | <span data-ttu-id="632a7-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="632a7-112">Country-Code</span></span>                            |
| <span data-ttu-id="632a7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="632a7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="632a7-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="632a7-114">countryCode</span></span>                             |
| <span data-ttu-id="632a7-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="632a7-115">Size</span></span>              | <span data-ttu-id="632a7-116">2 byte</span><span class="sxs-lookup"><span data-stu-id="632a7-116">2 bytes</span></span>                                 |
| <span data-ttu-id="632a7-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="632a7-117">Update Privilege</span></span>  | <span data-ttu-id="632a7-118">Proprietario dell'account o amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="632a7-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="632a7-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="632a7-119">Update Frequency</span></span>  | <span data-ttu-id="632a7-120">Quando cambia il paese o l'area geografica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="632a7-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="632a7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-121">Attribute-Id</span></span>      | <span data-ttu-id="632a7-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="632a7-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="632a7-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="632a7-123">System-Id-Guid</span></span>    | <span data-ttu-id="632a7-124">5fd42471-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="632a7-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="632a7-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="632a7-125">Syntax</span></span>            | [<span data-ttu-id="632a7-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="632a7-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="632a7-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="632a7-127">Implementations</span></span>

-   [<span data-ttu-id="632a7-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="632a7-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="632a7-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="632a7-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="632a7-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="632a7-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="632a7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="632a7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="632a7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="632a7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="632a7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="632a7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="632a7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="632a7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="632a7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="632a7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="632a7-136">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-136">Entry</span></span> | <span data-ttu-id="632a7-137">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632a7-138">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-140">System-Only</span></span>            | <span data-ttu-id="632a7-141">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-143">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="632a7-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-144">Is Indexed</span></span>             | <span data-ttu-id="632a7-145">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-146">In Global Catalog</span></span>      | <span data-ttu-id="632a7-147">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="632a7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="632a7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="632a7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-152">Search-Flags</span></span>           | <span data-ttu-id="632a7-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-154">System-Flags</span></span>           | <span data-ttu-id="632a7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-156">Classes used in</span></span>        | [<span data-ttu-id="632a7-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="632a7-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="632a7-158">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="632a7-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="632a7-159">Windows Server 2003</span></span>



| <span data-ttu-id="632a7-160">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-160">Entry</span></span> | <span data-ttu-id="632a7-161">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632a7-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-164">System-Only</span></span>            | <span data-ttu-id="632a7-165">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-166">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-167">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="632a7-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-168">Is Indexed</span></span>             | <span data-ttu-id="632a7-169">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-170">In Global Catalog</span></span>      | <span data-ttu-id="632a7-171">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="632a7-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-174">Range-Lower</span></span>            | <span data-ttu-id="632a7-175">0</span><span class="sxs-lookup"><span data-stu-id="632a7-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="632a7-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-176">Range-Upper</span></span>            | <span data-ttu-id="632a7-177">65535</span><span class="sxs-lookup"><span data-stu-id="632a7-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-178">Search-Flags</span></span>           | <span data-ttu-id="632a7-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-180">System-Flags</span></span>           | <span data-ttu-id="632a7-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-182">Classes used in</span></span>        | [<span data-ttu-id="632a7-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="632a7-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="632a7-184">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="632a7-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="632a7-185">ADAM</span></span>



| <span data-ttu-id="632a7-186">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-186">Entry</span></span> | <span data-ttu-id="632a7-187">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="632a7-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="632a7-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="632a7-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-190">System-Only</span></span>            | <span data-ttu-id="632a7-191">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-191">False</span></span>                                                          |
| <span data-ttu-id="632a7-192">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-192">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-193">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-193">True</span></span>                                                           |
| <span data-ttu-id="632a7-194">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-194">Is Indexed</span></span>             | <span data-ttu-id="632a7-195">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-195">False</span></span>                                                          |
| <span data-ttu-id="632a7-196">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-196">In Global Catalog</span></span>      | <span data-ttu-id="632a7-197">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-197">False</span></span>                                                          |
| <span data-ttu-id="632a7-198">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-199">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="632a7-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-200">Range-Lower</span></span>            | <span data-ttu-id="632a7-201">0</span><span class="sxs-lookup"><span data-stu-id="632a7-201">0</span></span>                                                              |
| <span data-ttu-id="632a7-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-202">Range-Upper</span></span>            | <span data-ttu-id="632a7-203">65535</span><span class="sxs-lookup"><span data-stu-id="632a7-203">65535</span></span>                                                          |
| <span data-ttu-id="632a7-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-204">Search-Flags</span></span>           | <span data-ttu-id="632a7-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="632a7-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-206">System-Flags</span></span>           | <span data-ttu-id="632a7-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="632a7-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-208">Classes used in</span></span>        | [<span data-ttu-id="632a7-209">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="632a7-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="632a7-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="632a7-211">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-211">Entry</span></span> | <span data-ttu-id="632a7-212">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632a7-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-215">System-Only</span></span>            | <span data-ttu-id="632a7-216">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-217">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-218">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="632a7-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-219">Is Indexed</span></span>             | <span data-ttu-id="632a7-220">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-221">In Global Catalog</span></span>      | <span data-ttu-id="632a7-222">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="632a7-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-225">Range-Lower</span></span>            | <span data-ttu-id="632a7-226">0</span><span class="sxs-lookup"><span data-stu-id="632a7-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="632a7-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-227">Range-Upper</span></span>            | <span data-ttu-id="632a7-228">65535</span><span class="sxs-lookup"><span data-stu-id="632a7-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-229">Search-Flags</span></span>           | <span data-ttu-id="632a7-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-231">System-Flags</span></span>           | <span data-ttu-id="632a7-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-233">Classes used in</span></span>        | [<span data-ttu-id="632a7-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="632a7-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="632a7-235">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="632a7-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="632a7-236">Windows Server 2008</span></span>



| <span data-ttu-id="632a7-237">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-237">Entry</span></span> | <span data-ttu-id="632a7-238">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632a7-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-241">System-Only</span></span>            | <span data-ttu-id="632a7-242">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-243">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-244">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="632a7-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-245">Is Indexed</span></span>             | <span data-ttu-id="632a7-246">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-247">In Global Catalog</span></span>      | <span data-ttu-id="632a7-248">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="632a7-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-251">Range-Lower</span></span>            | <span data-ttu-id="632a7-252">0</span><span class="sxs-lookup"><span data-stu-id="632a7-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="632a7-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-253">Range-Upper</span></span>            | <span data-ttu-id="632a7-254">65535</span><span class="sxs-lookup"><span data-stu-id="632a7-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-255">Search-Flags</span></span>           | <span data-ttu-id="632a7-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-257">System-Flags</span></span>           | <span data-ttu-id="632a7-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-259">Classes used in</span></span>        | [<span data-ttu-id="632a7-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="632a7-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="632a7-261">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="632a7-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="632a7-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="632a7-263">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-263">Entry</span></span> | <span data-ttu-id="632a7-264">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632a7-265">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-267">System-Only</span></span>            | <span data-ttu-id="632a7-268">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-269">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-269">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-270">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="632a7-271">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-271">Is Indexed</span></span>             | <span data-ttu-id="632a7-272">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-273">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-273">In Global Catalog</span></span>      | <span data-ttu-id="632a7-274">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-275">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-276">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="632a7-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-277">Range-Lower</span></span>            | <span data-ttu-id="632a7-278">0</span><span class="sxs-lookup"><span data-stu-id="632a7-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="632a7-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-279">Range-Upper</span></span>            | <span data-ttu-id="632a7-280">65535</span><span class="sxs-lookup"><span data-stu-id="632a7-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-281">Search-Flags</span></span>           | <span data-ttu-id="632a7-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-283">System-Flags</span></span>           | <span data-ttu-id="632a7-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-285">Classes used in</span></span>        | [<span data-ttu-id="632a7-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="632a7-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="632a7-287">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="632a7-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="632a7-288">Windows Server 2012</span></span>



| <span data-ttu-id="632a7-289">Voce</span><span class="sxs-lookup"><span data-stu-id="632a7-289">Entry</span></span> | <span data-ttu-id="632a7-290">Valore</span><span class="sxs-lookup"><span data-stu-id="632a7-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632a7-291">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="632a7-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="632a7-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="632a7-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="632a7-293">System-Only</span></span>            | <span data-ttu-id="632a7-294">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-295">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="632a7-295">Is-Single-Valued</span></span>       | <span data-ttu-id="632a7-296">Vero</span><span class="sxs-lookup"><span data-stu-id="632a7-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="632a7-297">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="632a7-297">Is Indexed</span></span>             | <span data-ttu-id="632a7-298">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-299">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="632a7-299">In Global Catalog</span></span>      | <span data-ttu-id="632a7-300">Falso</span><span class="sxs-lookup"><span data-stu-id="632a7-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-301">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="632a7-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="632a7-302">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="632a7-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="632a7-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="632a7-303">Range-Lower</span></span>            | <span data-ttu-id="632a7-304">0</span><span class="sxs-lookup"><span data-stu-id="632a7-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="632a7-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="632a7-305">Range-Upper</span></span>            | <span data-ttu-id="632a7-306">65535</span><span class="sxs-lookup"><span data-stu-id="632a7-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="632a7-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-307">Search-Flags</span></span>           | <span data-ttu-id="632a7-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="632a7-309">System-Flags</span></span>           | <span data-ttu-id="632a7-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="632a7-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="632a7-311">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="632a7-311">Classes used in</span></span>        | [<span data-ttu-id="632a7-312">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="632a7-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="632a7-313">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="632a7-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





