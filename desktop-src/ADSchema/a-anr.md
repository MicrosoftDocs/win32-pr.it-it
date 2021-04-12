---
title: Attributo ANR
description: Attributo di risoluzione dei nomi ambiguo da usare quando si sceglie tra oggetti.
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ANR
- Schema AD dell'attributo aNR
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480488"
---
# <a name="anr-attribute"></a><span data-ttu-id="cc7b5-105">Attributo ANR</span><span class="sxs-lookup"><span data-stu-id="cc7b5-105">ANR attribute</span></span>

<span data-ttu-id="cc7b5-106">Attributo di risoluzione dei nomi ambiguo da usare quando si sceglie tra oggetti.</span><span class="sxs-lookup"><span data-stu-id="cc7b5-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="cc7b5-107">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-107">Entry</span></span> | <span data-ttu-id="cc7b5-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc7b5-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc7b5-109">CN</span></span>                | <span data-ttu-id="cc7b5-110">ANR</span><span class="sxs-lookup"><span data-stu-id="cc7b5-110">ANR</span></span>                                                               |
| <span data-ttu-id="cc7b5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cc7b5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc7b5-112">aNR</span><span class="sxs-lookup"><span data-stu-id="cc7b5-112">aNR</span></span>                                                               |
| <span data-ttu-id="cc7b5-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cc7b5-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="cc7b5-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-114">Update Privilege</span></span>  | <span data-ttu-id="cc7b5-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="cc7b5-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="cc7b5-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-116">Update Frequency</span></span>  | <span data-ttu-id="cc7b5-117">Quando è necessario aggiungere o rimuovere un attributo dall'elenco ANR.</span><span class="sxs-lookup"><span data-stu-id="cc7b5-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="cc7b5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-118">Attribute-Id</span></span>      | <span data-ttu-id="cc7b5-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="cc7b5-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="cc7b5-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc7b5-120">System-Id-Guid</span></span>    | <span data-ttu-id="cc7b5-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="cc7b5-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="cc7b5-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc7b5-122">Syntax</span></span>            | [<span data-ttu-id="cc7b5-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="cc7b5-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="cc7b5-124">Implementations</span></span>

-   [<span data-ttu-id="cc7b5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc7b5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc7b5-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cc7b5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc7b5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc7b5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc7b5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc7b5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc7b5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc7b5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="cc7b5-133">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-133">Entry</span></span> | <span data-ttu-id="cc7b5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-137">System-Only</span></span>            | <span data-ttu-id="cc7b5-138">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-138">False</span></span>        |
| <span data-ttu-id="cc7b5-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-140">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-140">True</span></span>         |
| <span data-ttu-id="cc7b5-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-141">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-142">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-142">False</span></span>        |
| <span data-ttu-id="cc7b5-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-143">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-144">False</span></span>        |
| <span data-ttu-id="cc7b5-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-149">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-150">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-151">System-Flags</span></span>           | <span data-ttu-id="cc7b5-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-152">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="cc7b5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc7b5-154">Windows Server 2003</span></span>



| <span data-ttu-id="cc7b5-155">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-155">Entry</span></span> | <span data-ttu-id="cc7b5-156">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-159">System-Only</span></span>            | <span data-ttu-id="cc7b5-160">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-160">False</span></span>        |
| <span data-ttu-id="cc7b5-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-162">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-162">True</span></span>         |
| <span data-ttu-id="cc7b5-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-163">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-164">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-164">False</span></span>        |
| <span data-ttu-id="cc7b5-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-165">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-166">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-166">False</span></span>        |
| <span data-ttu-id="cc7b5-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-171">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-172">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-173">System-Flags</span></span>           | <span data-ttu-id="cc7b5-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-174">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="cc7b5-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="cc7b5-176">ADAM</span></span>



| <span data-ttu-id="cc7b5-177">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-177">Entry</span></span> | <span data-ttu-id="cc7b5-178">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-181">System-Only</span></span>            | <span data-ttu-id="cc7b5-182">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-182">False</span></span>        |
| <span data-ttu-id="cc7b5-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-184">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-184">True</span></span>         |
| <span data-ttu-id="cc7b5-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-185">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-186">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-186">False</span></span>        |
| <span data-ttu-id="cc7b5-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-187">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-188">False</span></span>        |
| <span data-ttu-id="cc7b5-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-193">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-194">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-195">System-Flags</span></span>           | <span data-ttu-id="cc7b5-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-196">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc7b5-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc7b5-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc7b5-199">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-199">Entry</span></span> | <span data-ttu-id="cc7b5-200">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-203">System-Only</span></span>            | <span data-ttu-id="cc7b5-204">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-204">False</span></span>        |
| <span data-ttu-id="cc7b5-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-205">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-206">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-206">True</span></span>         |
| <span data-ttu-id="cc7b5-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-207">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-208">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-208">False</span></span>        |
| <span data-ttu-id="cc7b5-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-209">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-210">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-210">False</span></span>        |
| <span data-ttu-id="cc7b5-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-215">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-216">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-217">System-Flags</span></span>           | <span data-ttu-id="cc7b5-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-218">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="cc7b5-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc7b5-220">Windows Server 2008</span></span>



| <span data-ttu-id="cc7b5-221">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-221">Entry</span></span> | <span data-ttu-id="cc7b5-222">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-223">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-225">System-Only</span></span>            | <span data-ttu-id="cc7b5-226">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-226">False</span></span>        |
| <span data-ttu-id="cc7b5-227">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-227">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-228">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-228">True</span></span>         |
| <span data-ttu-id="cc7b5-229">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-229">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-230">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-230">False</span></span>        |
| <span data-ttu-id="cc7b5-231">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-231">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-232">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-232">False</span></span>        |
| <span data-ttu-id="cc7b5-233">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-234">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-237">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-238">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-239">System-Flags</span></span>           | <span data-ttu-id="cc7b5-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-240">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-241">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc7b5-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc7b5-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc7b5-243">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-243">Entry</span></span> | <span data-ttu-id="cc7b5-244">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-245">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-247">System-Only</span></span>            | <span data-ttu-id="cc7b5-248">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-248">False</span></span>        |
| <span data-ttu-id="cc7b5-249">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-249">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-250">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-250">True</span></span>         |
| <span data-ttu-id="cc7b5-251">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-251">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-252">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-252">False</span></span>        |
| <span data-ttu-id="cc7b5-253">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-253">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-254">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-254">False</span></span>        |
| <span data-ttu-id="cc7b5-255">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-256">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-259">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-260">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-261">System-Flags</span></span>           | <span data-ttu-id="cc7b5-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-262">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-263">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="cc7b5-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc7b5-264">Windows Server 2012</span></span>



| <span data-ttu-id="cc7b5-265">Voce</span><span class="sxs-lookup"><span data-stu-id="cc7b5-265">Entry</span></span> | <span data-ttu-id="cc7b5-266">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="cc7b5-267">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cc7b5-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc7b5-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="cc7b5-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc7b5-269">System-Only</span></span>            | <span data-ttu-id="cc7b5-270">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-270">False</span></span>        |
| <span data-ttu-id="cc7b5-271">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cc7b5-271">Is-Single-Valued</span></span>       | <span data-ttu-id="cc7b5-272">Vero</span><span class="sxs-lookup"><span data-stu-id="cc7b5-272">True</span></span>         |
| <span data-ttu-id="cc7b5-273">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cc7b5-273">Is Indexed</span></span>             | <span data-ttu-id="cc7b5-274">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-274">False</span></span>        |
| <span data-ttu-id="cc7b5-275">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cc7b5-275">In Global Catalog</span></span>      | <span data-ttu-id="cc7b5-276">Falso</span><span class="sxs-lookup"><span data-stu-id="cc7b5-276">False</span></span>        |
| <span data-ttu-id="cc7b5-277">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cc7b5-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc7b5-278">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cc7b5-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="cc7b5-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc7b5-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="cc7b5-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc7b5-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="cc7b5-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-281">Search-Flags</span></span>           | <span data-ttu-id="cc7b5-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc7b5-282">0x00000000</span></span>   |
| <span data-ttu-id="cc7b5-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc7b5-283">System-Flags</span></span>           | <span data-ttu-id="cc7b5-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cc7b5-284">0x08000014</span></span>   |
| <span data-ttu-id="cc7b5-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cc7b5-285">Classes used in</span></span>        | \-           |



 

 




