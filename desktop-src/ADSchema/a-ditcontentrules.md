---
title: Attributo DIT-Content-Rules
description: Consente di specificare il contenuto consentito delle voci di una determinata classe di oggetti strutturali utilizzando l'identificazione di un set facoltativo di classi di oggetti ausiliarie e gli attributi obbligatori, facoltativi e preclusi.
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo DIT-Content-Rules
- Schema AD dell'attributo dITContentRules
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123084"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="969eb-105">Attributo DIT-Content-Rules</span><span class="sxs-lookup"><span data-stu-id="969eb-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="969eb-106">Consente di specificare il contenuto consentito delle voci di una determinata classe di oggetti strutturali utilizzando l'identificazione di un set facoltativo di classi di oggetti ausiliarie e gli attributi obbligatori, facoltativi e preclusi.</span><span class="sxs-lookup"><span data-stu-id="969eb-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="969eb-107">Gli attributi collettivi sono inclusi in DIT-Content-Rules come definito nella specifica RFC 2251.</span><span class="sxs-lookup"><span data-stu-id="969eb-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="969eb-108">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-108">Entry</span></span> | <span data-ttu-id="969eb-109">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="969eb-110">CN</span><span class="sxs-lookup"><span data-stu-id="969eb-110">CN</span></span>                | <span data-ttu-id="969eb-111">DIT-Content-Rules</span><span class="sxs-lookup"><span data-stu-id="969eb-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="969eb-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="969eb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="969eb-113">dITContentRules</span><span class="sxs-lookup"><span data-stu-id="969eb-113">dITContentRules</span></span>                             |
| <span data-ttu-id="969eb-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="969eb-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="969eb-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="969eb-115">Update Privilege</span></span>  | <span data-ttu-id="969eb-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="969eb-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="969eb-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="969eb-117">Update Frequency</span></span>  | <span data-ttu-id="969eb-118">Ogni volta che viene creata una nuova classe.</span><span class="sxs-lookup"><span data-stu-id="969eb-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="969eb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-119">Attribute-Id</span></span>      | <span data-ttu-id="969eb-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="969eb-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="969eb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="969eb-121">System-Id-Guid</span></span>    | <span data-ttu-id="969eb-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="969eb-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="969eb-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="969eb-123">Syntax</span></span>            | [<span data-ttu-id="969eb-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="969eb-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="969eb-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="969eb-125">Implementations</span></span>

-   [<span data-ttu-id="969eb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="969eb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="969eb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="969eb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="969eb-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="969eb-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="969eb-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="969eb-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="969eb-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="969eb-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="969eb-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="969eb-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="969eb-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="969eb-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="969eb-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="969eb-133">Windows 2000 Server</span></span>



| <span data-ttu-id="969eb-134">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-134">Entry</span></span> | <span data-ttu-id="969eb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-138">System-Only</span></span>            | <span data-ttu-id="969eb-139">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-139">True</span></span>                                        |
| <span data-ttu-id="969eb-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-140">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-141">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-141">False</span></span>                                       |
| <span data-ttu-id="969eb-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-142">Is Indexed</span></span>             | <span data-ttu-id="969eb-143">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-143">False</span></span>                                       |
| <span data-ttu-id="969eb-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-144">In Global Catalog</span></span>      | <span data-ttu-id="969eb-145">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-145">False</span></span>                                       |
| <span data-ttu-id="969eb-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-150">Search-Flags</span></span>           | <span data-ttu-id="969eb-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-151">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-152">System-Flags</span></span>           | <span data-ttu-id="969eb-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-153">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-154">Classes used in</span></span>        | [<span data-ttu-id="969eb-155">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="969eb-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="969eb-156">Windows Server 2003</span></span>



| <span data-ttu-id="969eb-157">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-157">Entry</span></span> | <span data-ttu-id="969eb-158">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-161">System-Only</span></span>            | <span data-ttu-id="969eb-162">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-162">True</span></span>                                        |
| <span data-ttu-id="969eb-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-163">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-164">False</span></span>                                       |
| <span data-ttu-id="969eb-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-165">Is Indexed</span></span>             | <span data-ttu-id="969eb-166">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-166">False</span></span>                                       |
| <span data-ttu-id="969eb-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-167">In Global Catalog</span></span>      | <span data-ttu-id="969eb-168">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-168">False</span></span>                                       |
| <span data-ttu-id="969eb-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-173">Search-Flags</span></span>           | <span data-ttu-id="969eb-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-174">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-175">System-Flags</span></span>           | <span data-ttu-id="969eb-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-176">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-177">Classes used in</span></span>        | [<span data-ttu-id="969eb-178">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="969eb-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="969eb-179">ADAM</span></span>



| <span data-ttu-id="969eb-180">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-180">Entry</span></span> | <span data-ttu-id="969eb-181">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-184">System-Only</span></span>            | <span data-ttu-id="969eb-185">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-185">True</span></span>                                        |
| <span data-ttu-id="969eb-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-186">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-187">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-187">False</span></span>                                       |
| <span data-ttu-id="969eb-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-188">Is Indexed</span></span>             | <span data-ttu-id="969eb-189">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-189">False</span></span>                                       |
| <span data-ttu-id="969eb-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-190">In Global Catalog</span></span>      | <span data-ttu-id="969eb-191">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-191">False</span></span>                                       |
| <span data-ttu-id="969eb-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-196">Search-Flags</span></span>           | <span data-ttu-id="969eb-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-197">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-198">System-Flags</span></span>           | <span data-ttu-id="969eb-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-199">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-200">Classes used in</span></span>        | [<span data-ttu-id="969eb-201">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="969eb-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="969eb-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="969eb-203">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-203">Entry</span></span> | <span data-ttu-id="969eb-204">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-207">System-Only</span></span>            | <span data-ttu-id="969eb-208">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-208">True</span></span>                                        |
| <span data-ttu-id="969eb-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-209">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-210">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-210">False</span></span>                                       |
| <span data-ttu-id="969eb-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-211">Is Indexed</span></span>             | <span data-ttu-id="969eb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-212">False</span></span>                                       |
| <span data-ttu-id="969eb-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-213">In Global Catalog</span></span>      | <span data-ttu-id="969eb-214">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-214">False</span></span>                                       |
| <span data-ttu-id="969eb-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-219">Search-Flags</span></span>           | <span data-ttu-id="969eb-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-220">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-221">System-Flags</span></span>           | <span data-ttu-id="969eb-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-222">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-223">Classes used in</span></span>        | [<span data-ttu-id="969eb-224">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="969eb-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="969eb-225">Windows Server 2008</span></span>



| <span data-ttu-id="969eb-226">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-226">Entry</span></span> | <span data-ttu-id="969eb-227">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-230">System-Only</span></span>            | <span data-ttu-id="969eb-231">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-231">True</span></span>                                        |
| <span data-ttu-id="969eb-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-232">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-233">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-233">False</span></span>                                       |
| <span data-ttu-id="969eb-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-234">Is Indexed</span></span>             | <span data-ttu-id="969eb-235">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-235">False</span></span>                                       |
| <span data-ttu-id="969eb-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-236">In Global Catalog</span></span>      | <span data-ttu-id="969eb-237">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-237">False</span></span>                                       |
| <span data-ttu-id="969eb-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-242">Search-Flags</span></span>           | <span data-ttu-id="969eb-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-243">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-244">System-Flags</span></span>           | <span data-ttu-id="969eb-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-245">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-246">Classes used in</span></span>        | [<span data-ttu-id="969eb-247">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="969eb-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="969eb-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="969eb-249">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-249">Entry</span></span> | <span data-ttu-id="969eb-250">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-253">System-Only</span></span>            | <span data-ttu-id="969eb-254">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-254">True</span></span>                                        |
| <span data-ttu-id="969eb-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-255">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-256">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-256">False</span></span>                                       |
| <span data-ttu-id="969eb-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-257">Is Indexed</span></span>             | <span data-ttu-id="969eb-258">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-258">False</span></span>                                       |
| <span data-ttu-id="969eb-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-259">In Global Catalog</span></span>      | <span data-ttu-id="969eb-260">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-260">False</span></span>                                       |
| <span data-ttu-id="969eb-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-265">Search-Flags</span></span>           | <span data-ttu-id="969eb-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-266">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-267">System-Flags</span></span>           | <span data-ttu-id="969eb-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-268">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-269">Classes used in</span></span>        | [<span data-ttu-id="969eb-270">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="969eb-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="969eb-271">Windows Server 2012</span></span>



| <span data-ttu-id="969eb-272">Voce</span><span class="sxs-lookup"><span data-stu-id="969eb-272">Entry</span></span> | <span data-ttu-id="969eb-273">Valore</span><span class="sxs-lookup"><span data-stu-id="969eb-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="969eb-274">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="969eb-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="969eb-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="969eb-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="969eb-276">System-Only</span></span>            | <span data-ttu-id="969eb-277">Vero</span><span class="sxs-lookup"><span data-stu-id="969eb-277">True</span></span>                                        |
| <span data-ttu-id="969eb-278">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="969eb-278">Is-Single-Valued</span></span>       | <span data-ttu-id="969eb-279">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-279">False</span></span>                                       |
| <span data-ttu-id="969eb-280">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="969eb-280">Is Indexed</span></span>             | <span data-ttu-id="969eb-281">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-281">False</span></span>                                       |
| <span data-ttu-id="969eb-282">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="969eb-282">In Global Catalog</span></span>      | <span data-ttu-id="969eb-283">Falso</span><span class="sxs-lookup"><span data-stu-id="969eb-283">False</span></span>                                       |
| <span data-ttu-id="969eb-284">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="969eb-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="969eb-285">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="969eb-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="969eb-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="969eb-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="969eb-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="969eb-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="969eb-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-288">Search-Flags</span></span>           | <span data-ttu-id="969eb-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="969eb-289">0x00000000</span></span>                                  |
| <span data-ttu-id="969eb-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="969eb-290">System-Flags</span></span>           | <span data-ttu-id="969eb-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="969eb-291">0x08000014</span></span>                                  |
| <span data-ttu-id="969eb-292">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="969eb-292">Classes used in</span></span>        | [<span data-ttu-id="969eb-293">**Sottoschema**</span><span class="sxs-lookup"><span data-stu-id="969eb-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





