---
title: Attributo UPN-Suffixes
description: Elenco di suffissi di nome dell'entità utente per un dominio.
ms.assetid: ad861d2d-b643-468c-a346-36ad6a828359
ms.tgt_platform: multiple
keywords:
- Schema AD UPN-Suffixes attribute
- Schema AD dell'attributo uPNSuffixes
topic_type:
- apiref
api_name:
- UPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4aa5fb9398478e4b91fb8f36b8cf96a244935fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875498"
---
# <a name="upn-suffixes-attribute"></a><span data-ttu-id="582d6-105">Attributo UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="582d6-105">UPN-Suffixes attribute</span></span>

<span data-ttu-id="582d6-106">Elenco di suffissi di nome dell'entità utente per un dominio.</span><span class="sxs-lookup"><span data-stu-id="582d6-106">The list of User-Principal-Name suffixes for a domain.</span></span>



| <span data-ttu-id="582d6-107">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-107">Entry</span></span> | <span data-ttu-id="582d6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="582d6-109">CN</span><span class="sxs-lookup"><span data-stu-id="582d6-109">CN</span></span>                | <span data-ttu-id="582d6-110">UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="582d6-110">UPN-Suffixes</span></span>                                |
| <span data-ttu-id="582d6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="582d6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="582d6-112">uPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="582d6-112">uPNSuffixes</span></span>                                 |
| <span data-ttu-id="582d6-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="582d6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="582d6-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="582d6-114">Update Privilege</span></span>  | <span data-ttu-id="582d6-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="582d6-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="582d6-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="582d6-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="582d6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-117">Attribute-Id</span></span>      | <span data-ttu-id="582d6-118">1.2.840.113556.1.4.890</span><span class="sxs-lookup"><span data-stu-id="582d6-118">1.2.840.113556.1.4.890</span></span>                      |
| <span data-ttu-id="582d6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="582d6-119">System-Id-Guid</span></span>    | <span data-ttu-id="582d6-120">032160bf-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="582d6-120">032160bf-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="582d6-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="582d6-121">Syntax</span></span>            | [<span data-ttu-id="582d6-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="582d6-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="582d6-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="582d6-123">Implementations</span></span>

-   [<span data-ttu-id="582d6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="582d6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="582d6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="582d6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="582d6-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="582d6-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="582d6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="582d6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="582d6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="582d6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="582d6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="582d6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="582d6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="582d6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="582d6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="582d6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="582d6-132">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-132">Entry</span></span> | <span data-ttu-id="582d6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-133">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-134">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-135">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-136">System-Only</span></span>            | <span data-ttu-id="582d6-137">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-137">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-139">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-139">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-140">Is Indexed</span></span>             | <span data-ttu-id="582d6-141">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-141">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-142">In Global Catalog</span></span>      | <span data-ttu-id="582d6-143">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-143">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-145">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-146">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-147">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-148">Search-Flags</span></span>           | <span data-ttu-id="582d6-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-149">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-150">System-Flags</span></span>           | <span data-ttu-id="582d6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-151">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-152">Classes used in</span></span>        | [<span data-ttu-id="582d6-153">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-153">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-154">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-154">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="582d6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="582d6-155">Windows Server 2003</span></span>



| <span data-ttu-id="582d6-156">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-156">Entry</span></span> | <span data-ttu-id="582d6-157">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-158">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-159">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-160">System-Only</span></span>            | <span data-ttu-id="582d6-161">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-161">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-163">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-163">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-164">Is Indexed</span></span>             | <span data-ttu-id="582d6-165">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-165">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-166">In Global Catalog</span></span>      | <span data-ttu-id="582d6-167">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-167">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-169">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-170">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-171">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-172">Search-Flags</span></span>           | <span data-ttu-id="582d6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-173">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-174">System-Flags</span></span>           | <span data-ttu-id="582d6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-175">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-176">Classes used in</span></span>        | [<span data-ttu-id="582d6-177">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-178">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-178">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="582d6-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="582d6-179">ADAM</span></span>



| <span data-ttu-id="582d6-180">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-180">Entry</span></span> | <span data-ttu-id="582d6-181">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-181">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-182">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-183">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-184">System-Only</span></span>            | <span data-ttu-id="582d6-185">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-185">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-186">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-187">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-187">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-188">Is Indexed</span></span>             | <span data-ttu-id="582d6-189">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-189">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-190">In Global Catalog</span></span>      | <span data-ttu-id="582d6-191">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-191">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-193">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-194">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-195">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-196">Search-Flags</span></span>           | <span data-ttu-id="582d6-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-197">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-198">System-Flags</span></span>           | <span data-ttu-id="582d6-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-199">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-200">Classes used in</span></span>        | [<span data-ttu-id="582d6-201">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-202">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-202">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="582d6-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="582d6-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="582d6-204">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-204">Entry</span></span> | <span data-ttu-id="582d6-205">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-205">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-206">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-207">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-208">System-Only</span></span>            | <span data-ttu-id="582d6-209">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-209">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-210">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-211">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-211">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-212">Is Indexed</span></span>             | <span data-ttu-id="582d6-213">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-213">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-214">In Global Catalog</span></span>      | <span data-ttu-id="582d6-215">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-215">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-217">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-218">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-219">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-220">Search-Flags</span></span>           | <span data-ttu-id="582d6-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-221">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-222">System-Flags</span></span>           | <span data-ttu-id="582d6-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-223">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-224">Classes used in</span></span>        | [<span data-ttu-id="582d6-225">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-225">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-226">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-226">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="582d6-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="582d6-227">Windows Server 2008</span></span>



| <span data-ttu-id="582d6-228">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-228">Entry</span></span> | <span data-ttu-id="582d6-229">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-229">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-230">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-231">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-232">System-Only</span></span>            | <span data-ttu-id="582d6-233">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-233">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-234">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-235">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-235">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-236">Is Indexed</span></span>             | <span data-ttu-id="582d6-237">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-237">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-238">In Global Catalog</span></span>      | <span data-ttu-id="582d6-239">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-239">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-241">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-242">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-243">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-244">Search-Flags</span></span>           | <span data-ttu-id="582d6-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-245">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-246">System-Flags</span></span>           | <span data-ttu-id="582d6-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-247">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-248">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-248">Classes used in</span></span>        | [<span data-ttu-id="582d6-249">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-249">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-250">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-250">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="582d6-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="582d6-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="582d6-252">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-252">Entry</span></span> | <span data-ttu-id="582d6-253">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-253">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-254">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-255">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-256">System-Only</span></span>            | <span data-ttu-id="582d6-257">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-257">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-258">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-259">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-259">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-260">Is Indexed</span></span>             | <span data-ttu-id="582d6-261">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-261">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-262">In Global Catalog</span></span>      | <span data-ttu-id="582d6-263">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-263">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-265">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-266">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-267">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-268">Search-Flags</span></span>           | <span data-ttu-id="582d6-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-269">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-270">System-Flags</span></span>           | <span data-ttu-id="582d6-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-271">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-272">Classes used in</span></span>        | [<span data-ttu-id="582d6-273">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-273">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-274">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-274">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="582d6-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="582d6-275">Windows Server 2012</span></span>



| <span data-ttu-id="582d6-276">Voce</span><span class="sxs-lookup"><span data-stu-id="582d6-276">Entry</span></span> | <span data-ttu-id="582d6-277">Valore</span><span class="sxs-lookup"><span data-stu-id="582d6-277">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d6-278">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="582d6-278">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="582d6-279">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="582d6-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="582d6-280">System-Only</span></span>            | <span data-ttu-id="582d6-281">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-281">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-282">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="582d6-282">Is-Single-Valued</span></span>       | <span data-ttu-id="582d6-283">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-283">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-284">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="582d6-284">Is Indexed</span></span>             | <span data-ttu-id="582d6-285">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-285">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-286">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="582d6-286">In Global Catalog</span></span>      | <span data-ttu-id="582d6-287">Falso</span><span class="sxs-lookup"><span data-stu-id="582d6-287">False</span></span>                                                                                                                        |
| <span data-ttu-id="582d6-288">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="582d6-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="582d6-289">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="582d6-289">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="582d6-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="582d6-290">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="582d6-291">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="582d6-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-292">Search-Flags</span></span>           | <span data-ttu-id="582d6-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="582d6-293">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="582d6-294">System-Flags</span></span>           | <span data-ttu-id="582d6-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="582d6-295">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="582d6-296">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="582d6-296">Classes used in</span></span>        | [<span data-ttu-id="582d6-297">**Cross-Ref-container**</span><span class="sxs-lookup"><span data-stu-id="582d6-297">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="582d6-298">**Unità organizzativa**</span><span class="sxs-lookup"><span data-stu-id="582d6-298">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





