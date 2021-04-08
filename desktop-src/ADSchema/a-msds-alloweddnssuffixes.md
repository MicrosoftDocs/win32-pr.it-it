---
title: attributo ms-DS-allowed-DNS-suffissi
description: Elenco di suffissi consentiti per l'attributo dNSHostName negli oggetti computer.
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- ms-DS-allowed-DNS-suffissi attributo AD schema
- attributo msDS-AllowedDNSSuffixes-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744746"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="dd336-105">attributo ms-DS-allowed-DNS-suffissi</span><span class="sxs-lookup"><span data-stu-id="dd336-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="dd336-106">Elenco di suffissi consentiti per l'attributo dNSHostName negli oggetti computer.</span><span class="sxs-lookup"><span data-stu-id="dd336-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="dd336-107">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-107">Entry</span></span> | <span data-ttu-id="dd336-108">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dd336-109">CN</span><span class="sxs-lookup"><span data-stu-id="dd336-109">CN</span></span>                | <span data-ttu-id="dd336-110">ms-DS-allowed-DNS-suffissi</span><span class="sxs-lookup"><span data-stu-id="dd336-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="dd336-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dd336-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dd336-112">msDS-AllowedDNSSuffixes</span><span class="sxs-lookup"><span data-stu-id="dd336-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="dd336-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dd336-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="dd336-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dd336-114">Update Privilege</span></span>  | <span data-ttu-id="dd336-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="dd336-115">Domain administrator</span></span>                        |
| <span data-ttu-id="dd336-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dd336-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="dd336-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-117">Attribute-Id</span></span>      | <span data-ttu-id="dd336-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="dd336-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="dd336-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dd336-119">System-Id-Guid</span></span>    | <span data-ttu-id="dd336-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="dd336-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="dd336-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd336-121">Syntax</span></span>            | [<span data-ttu-id="dd336-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dd336-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dd336-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dd336-123">Implementations</span></span>

-   [<span data-ttu-id="dd336-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dd336-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dd336-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="dd336-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dd336-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dd336-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dd336-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dd336-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dd336-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dd336-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dd336-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dd336-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="dd336-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd336-130">Windows Server 2003</span></span>



| <span data-ttu-id="dd336-131">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-131">Entry</span></span> | <span data-ttu-id="dd336-132">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dd336-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd336-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd336-135">System-Only</span></span>            | <span data-ttu-id="dd336-136">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-136">False</span></span>                                        |
| <span data-ttu-id="dd336-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd336-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dd336-138">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-138">False</span></span>                                        |
| <span data-ttu-id="dd336-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd336-139">Is Indexed</span></span>             | <span data-ttu-id="dd336-140">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-140">False</span></span>                                        |
| <span data-ttu-id="dd336-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd336-141">In Global Catalog</span></span>      | <span data-ttu-id="dd336-142">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-142">False</span></span>                                        |
| <span data-ttu-id="dd336-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd336-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd336-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd336-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dd336-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd336-145">Range-Lower</span></span>            | <span data-ttu-id="dd336-146">0</span><span class="sxs-lookup"><span data-stu-id="dd336-146">0</span></span>                                            |
| <span data-ttu-id="dd336-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd336-147">Range-Upper</span></span>            | <span data-ttu-id="dd336-148">2048</span><span class="sxs-lookup"><span data-stu-id="dd336-148">2048</span></span>                                         |
| <span data-ttu-id="dd336-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-149">Search-Flags</span></span>           | <span data-ttu-id="dd336-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd336-150">0x00000000</span></span>                                   |
| <span data-ttu-id="dd336-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-151">System-Flags</span></span>           | <span data-ttu-id="dd336-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd336-152">0x00000010</span></span>                                   |
| <span data-ttu-id="dd336-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd336-153">Classes used in</span></span>        | [<span data-ttu-id="dd336-154">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="dd336-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dd336-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="dd336-155">ADAM</span></span>



| <span data-ttu-id="dd336-156">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-156">Entry</span></span> | <span data-ttu-id="dd336-157">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dd336-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd336-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd336-160">System-Only</span></span>            | <span data-ttu-id="dd336-161">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-161">False</span></span>                                        |
| <span data-ttu-id="dd336-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd336-162">Is-Single-Valued</span></span>       | <span data-ttu-id="dd336-163">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-163">False</span></span>                                        |
| <span data-ttu-id="dd336-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd336-164">Is Indexed</span></span>             | <span data-ttu-id="dd336-165">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-165">False</span></span>                                        |
| <span data-ttu-id="dd336-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd336-166">In Global Catalog</span></span>      | <span data-ttu-id="dd336-167">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-167">False</span></span>                                        |
| <span data-ttu-id="dd336-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd336-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd336-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd336-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dd336-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd336-170">Range-Lower</span></span>            | <span data-ttu-id="dd336-171">0</span><span class="sxs-lookup"><span data-stu-id="dd336-171">0</span></span>                                            |
| <span data-ttu-id="dd336-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd336-172">Range-Upper</span></span>            | <span data-ttu-id="dd336-173">2048</span><span class="sxs-lookup"><span data-stu-id="dd336-173">2048</span></span>                                         |
| <span data-ttu-id="dd336-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-174">Search-Flags</span></span>           | <span data-ttu-id="dd336-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd336-175">0x00000000</span></span>                                   |
| <span data-ttu-id="dd336-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-176">System-Flags</span></span>           | <span data-ttu-id="dd336-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd336-177">0x00000010</span></span>                                   |
| <span data-ttu-id="dd336-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd336-178">Classes used in</span></span>        | [<span data-ttu-id="dd336-179">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="dd336-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dd336-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dd336-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dd336-181">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-181">Entry</span></span> | <span data-ttu-id="dd336-182">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dd336-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd336-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd336-185">System-Only</span></span>            | <span data-ttu-id="dd336-186">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-186">False</span></span>                                        |
| <span data-ttu-id="dd336-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd336-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dd336-188">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-188">False</span></span>                                        |
| <span data-ttu-id="dd336-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd336-189">Is Indexed</span></span>             | <span data-ttu-id="dd336-190">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-190">False</span></span>                                        |
| <span data-ttu-id="dd336-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd336-191">In Global Catalog</span></span>      | <span data-ttu-id="dd336-192">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-192">False</span></span>                                        |
| <span data-ttu-id="dd336-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd336-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd336-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd336-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dd336-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd336-195">Range-Lower</span></span>            | <span data-ttu-id="dd336-196">0</span><span class="sxs-lookup"><span data-stu-id="dd336-196">0</span></span>                                            |
| <span data-ttu-id="dd336-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd336-197">Range-Upper</span></span>            | <span data-ttu-id="dd336-198">2048</span><span class="sxs-lookup"><span data-stu-id="dd336-198">2048</span></span>                                         |
| <span data-ttu-id="dd336-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-199">Search-Flags</span></span>           | <span data-ttu-id="dd336-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd336-200">0x00000000</span></span>                                   |
| <span data-ttu-id="dd336-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-201">System-Flags</span></span>           | <span data-ttu-id="dd336-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd336-202">0x00000010</span></span>                                   |
| <span data-ttu-id="dd336-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd336-203">Classes used in</span></span>        | [<span data-ttu-id="dd336-204">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="dd336-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dd336-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd336-205">Windows Server 2008</span></span>



| <span data-ttu-id="dd336-206">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-206">Entry</span></span> | <span data-ttu-id="dd336-207">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dd336-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd336-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd336-210">System-Only</span></span>            | <span data-ttu-id="dd336-211">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-211">False</span></span>                                        |
| <span data-ttu-id="dd336-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd336-212">Is-Single-Valued</span></span>       | <span data-ttu-id="dd336-213">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-213">False</span></span>                                        |
| <span data-ttu-id="dd336-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd336-214">Is Indexed</span></span>             | <span data-ttu-id="dd336-215">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-215">False</span></span>                                        |
| <span data-ttu-id="dd336-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd336-216">In Global Catalog</span></span>      | <span data-ttu-id="dd336-217">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-217">False</span></span>                                        |
| <span data-ttu-id="dd336-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd336-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd336-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd336-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dd336-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd336-220">Range-Lower</span></span>            | <span data-ttu-id="dd336-221">0</span><span class="sxs-lookup"><span data-stu-id="dd336-221">0</span></span>                                            |
| <span data-ttu-id="dd336-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd336-222">Range-Upper</span></span>            | <span data-ttu-id="dd336-223">2048</span><span class="sxs-lookup"><span data-stu-id="dd336-223">2048</span></span>                                         |
| <span data-ttu-id="dd336-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-224">Search-Flags</span></span>           | <span data-ttu-id="dd336-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd336-225">0x00000000</span></span>                                   |
| <span data-ttu-id="dd336-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-226">System-Flags</span></span>           | <span data-ttu-id="dd336-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd336-227">0x00000010</span></span>                                   |
| <span data-ttu-id="dd336-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd336-228">Classes used in</span></span>        | [<span data-ttu-id="dd336-229">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="dd336-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dd336-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd336-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dd336-231">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-231">Entry</span></span> | <span data-ttu-id="dd336-232">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dd336-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd336-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd336-235">System-Only</span></span>            | <span data-ttu-id="dd336-236">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-236">False</span></span>                                        |
| <span data-ttu-id="dd336-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd336-237">Is-Single-Valued</span></span>       | <span data-ttu-id="dd336-238">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-238">False</span></span>                                        |
| <span data-ttu-id="dd336-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd336-239">Is Indexed</span></span>             | <span data-ttu-id="dd336-240">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-240">False</span></span>                                        |
| <span data-ttu-id="dd336-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd336-241">In Global Catalog</span></span>      | <span data-ttu-id="dd336-242">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-242">False</span></span>                                        |
| <span data-ttu-id="dd336-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd336-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd336-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd336-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dd336-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd336-245">Range-Lower</span></span>            | <span data-ttu-id="dd336-246">0</span><span class="sxs-lookup"><span data-stu-id="dd336-246">0</span></span>                                            |
| <span data-ttu-id="dd336-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd336-247">Range-Upper</span></span>            | <span data-ttu-id="dd336-248">2048</span><span class="sxs-lookup"><span data-stu-id="dd336-248">2048</span></span>                                         |
| <span data-ttu-id="dd336-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-249">Search-Flags</span></span>           | <span data-ttu-id="dd336-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd336-250">0x00000000</span></span>                                   |
| <span data-ttu-id="dd336-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-251">System-Flags</span></span>           | <span data-ttu-id="dd336-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd336-252">0x00000010</span></span>                                   |
| <span data-ttu-id="dd336-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd336-253">Classes used in</span></span>        | [<span data-ttu-id="dd336-254">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="dd336-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dd336-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd336-255">Windows Server 2012</span></span>



| <span data-ttu-id="dd336-256">Voce</span><span class="sxs-lookup"><span data-stu-id="dd336-256">Entry</span></span> | <span data-ttu-id="dd336-257">Valore</span><span class="sxs-lookup"><span data-stu-id="dd336-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dd336-258">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dd336-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd336-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dd336-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd336-260">System-Only</span></span>            | <span data-ttu-id="dd336-261">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-261">False</span></span>                                        |
| <span data-ttu-id="dd336-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dd336-262">Is-Single-Valued</span></span>       | <span data-ttu-id="dd336-263">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-263">False</span></span>                                        |
| <span data-ttu-id="dd336-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dd336-264">Is Indexed</span></span>             | <span data-ttu-id="dd336-265">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-265">False</span></span>                                        |
| <span data-ttu-id="dd336-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dd336-266">In Global Catalog</span></span>      | <span data-ttu-id="dd336-267">Falso</span><span class="sxs-lookup"><span data-stu-id="dd336-267">False</span></span>                                        |
| <span data-ttu-id="dd336-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dd336-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd336-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dd336-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dd336-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd336-270">Range-Lower</span></span>            | <span data-ttu-id="dd336-271">0</span><span class="sxs-lookup"><span data-stu-id="dd336-271">0</span></span>                                            |
| <span data-ttu-id="dd336-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd336-272">Range-Upper</span></span>            | <span data-ttu-id="dd336-273">2048</span><span class="sxs-lookup"><span data-stu-id="dd336-273">2048</span></span>                                         |
| <span data-ttu-id="dd336-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-274">Search-Flags</span></span>           | <span data-ttu-id="dd336-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd336-275">0x00000000</span></span>                                   |
| <span data-ttu-id="dd336-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd336-276">System-Flags</span></span>           | <span data-ttu-id="dd336-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd336-277">0x00000010</span></span>                                   |
| <span data-ttu-id="dd336-278">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dd336-278">Classes used in</span></span>        | [<span data-ttu-id="dd336-279">**Domain-DNS**</span><span class="sxs-lookup"><span data-stu-id="dd336-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 





