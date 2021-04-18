---
title: Attributo Is-Defunct
description: Se TRUE, la classe o l'attributo non è più utilizzabile. Le versioni precedenti di questo oggetto possono esistere, ma non è possibile crearne di nuove.
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- Schema AD Is-Defunct attribute
- Schema AD dell'attributo undefunto
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303324"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="90da0-106">Attributo Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="90da0-106">Is-Defunct attribute</span></span>

<span data-ttu-id="90da0-107">Se **true**, la classe o l'attributo non è più utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="90da0-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="90da0-108">Le versioni precedenti di questo oggetto possono esistere, ma non è possibile crearne di nuove.</span><span class="sxs-lookup"><span data-stu-id="90da0-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="90da0-109">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-109">Entry</span></span> | <span data-ttu-id="90da0-110">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="90da0-111">CN</span><span class="sxs-lookup"><span data-stu-id="90da0-111">CN</span></span>                | <span data-ttu-id="90da0-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="90da0-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="90da0-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="90da0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="90da0-114">isDefunct</span><span class="sxs-lookup"><span data-stu-id="90da0-114">isDefunct</span></span>                            |
| <span data-ttu-id="90da0-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="90da0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="90da0-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="90da0-116">Update Privilege</span></span>  | <span data-ttu-id="90da0-117">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="90da0-117">Schema administrator</span></span>                 |
| <span data-ttu-id="90da0-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="90da0-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="90da0-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-119">Attribute-Id</span></span>      | <span data-ttu-id="90da0-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="90da0-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="90da0-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="90da0-121">System-Id-Guid</span></span>    | <span data-ttu-id="90da0-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="90da0-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="90da0-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90da0-123">Syntax</span></span>            | [<span data-ttu-id="90da0-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="90da0-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="90da0-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="90da0-125">Implementations</span></span>

-   [<span data-ttu-id="90da0-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90da0-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90da0-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90da0-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90da0-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="90da0-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="90da0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90da0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90da0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90da0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90da0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90da0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90da0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90da0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90da0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90da0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="90da0-134">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-134">Entry</span></span> | <span data-ttu-id="90da0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-138">System-Only</span></span>            | <span data-ttu-id="90da0-139">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-139">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-141">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-141">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-142">Is Indexed</span></span>             | <span data-ttu-id="90da0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-143">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-144">In Global Catalog</span></span>      | <span data-ttu-id="90da0-145">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-145">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-150">Search-Flags</span></span>           | <span data-ttu-id="90da0-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-152">System-Flags</span></span>           | <span data-ttu-id="90da0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-154">Classes used in</span></span>        | [<span data-ttu-id="90da0-155">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-156">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90da0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90da0-157">Windows Server 2003</span></span>



| <span data-ttu-id="90da0-158">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-158">Entry</span></span> | <span data-ttu-id="90da0-159">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-162">System-Only</span></span>            | <span data-ttu-id="90da0-163">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-163">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-165">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-165">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-166">Is Indexed</span></span>             | <span data-ttu-id="90da0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-167">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-168">In Global Catalog</span></span>      | <span data-ttu-id="90da0-169">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-169">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-174">Search-Flags</span></span>           | <span data-ttu-id="90da0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-176">System-Flags</span></span>           | <span data-ttu-id="90da0-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-178">Classes used in</span></span>        | [<span data-ttu-id="90da0-179">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-180">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="90da0-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="90da0-181">ADAM</span></span>



| <span data-ttu-id="90da0-182">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-182">Entry</span></span> | <span data-ttu-id="90da0-183">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-186">System-Only</span></span>            | <span data-ttu-id="90da0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-187">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-189">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-189">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-190">Is Indexed</span></span>             | <span data-ttu-id="90da0-191">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-191">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-192">In Global Catalog</span></span>      | <span data-ttu-id="90da0-193">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-193">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-198">Search-Flags</span></span>           | <span data-ttu-id="90da0-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-200">System-Flags</span></span>           | <span data-ttu-id="90da0-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-202">Classes used in</span></span>        | [<span data-ttu-id="90da0-203">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-204">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90da0-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90da0-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90da0-206">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-206">Entry</span></span> | <span data-ttu-id="90da0-207">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-210">System-Only</span></span>            | <span data-ttu-id="90da0-211">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-211">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-212">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-213">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-213">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-214">Is Indexed</span></span>             | <span data-ttu-id="90da0-215">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-215">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-216">In Global Catalog</span></span>      | <span data-ttu-id="90da0-217">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-217">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-222">Search-Flags</span></span>           | <span data-ttu-id="90da0-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-224">System-Flags</span></span>           | <span data-ttu-id="90da0-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-226">Classes used in</span></span>        | [<span data-ttu-id="90da0-227">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-228">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90da0-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90da0-229">Windows Server 2008</span></span>



| <span data-ttu-id="90da0-230">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-230">Entry</span></span> | <span data-ttu-id="90da0-231">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-234">System-Only</span></span>            | <span data-ttu-id="90da0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-235">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-236">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-237">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-237">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-238">Is Indexed</span></span>             | <span data-ttu-id="90da0-239">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-239">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-240">In Global Catalog</span></span>      | <span data-ttu-id="90da0-241">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-241">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-246">Search-Flags</span></span>           | <span data-ttu-id="90da0-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-248">System-Flags</span></span>           | <span data-ttu-id="90da0-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-250">Classes used in</span></span>        | [<span data-ttu-id="90da0-251">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-252">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90da0-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90da0-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90da0-254">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-254">Entry</span></span> | <span data-ttu-id="90da0-255">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-256">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-258">System-Only</span></span>            | <span data-ttu-id="90da0-259">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-259">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-260">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-260">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-261">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-261">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-262">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-262">Is Indexed</span></span>             | <span data-ttu-id="90da0-263">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-263">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-264">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-264">In Global Catalog</span></span>      | <span data-ttu-id="90da0-265">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-265">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-266">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-267">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-270">Search-Flags</span></span>           | <span data-ttu-id="90da0-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-272">System-Flags</span></span>           | <span data-ttu-id="90da0-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-274">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-274">Classes used in</span></span>        | [<span data-ttu-id="90da0-275">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-276">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90da0-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90da0-277">Windows Server 2012</span></span>



| <span data-ttu-id="90da0-278">Voce</span><span class="sxs-lookup"><span data-stu-id="90da0-278">Entry</span></span> | <span data-ttu-id="90da0-279">Valore</span><span class="sxs-lookup"><span data-stu-id="90da0-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-280">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90da0-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90da0-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="90da0-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="90da0-282">System-Only</span></span>            | <span data-ttu-id="90da0-283">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-283">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-284">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90da0-284">Is-Single-Valued</span></span>       | <span data-ttu-id="90da0-285">Vero</span><span class="sxs-lookup"><span data-stu-id="90da0-285">True</span></span>                                                                                                      |
| <span data-ttu-id="90da0-286">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90da0-286">Is Indexed</span></span>             | <span data-ttu-id="90da0-287">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-287">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-288">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90da0-288">In Global Catalog</span></span>      | <span data-ttu-id="90da0-289">Falso</span><span class="sxs-lookup"><span data-stu-id="90da0-289">False</span></span>                                                                                                     |
| <span data-ttu-id="90da0-290">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90da0-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="90da0-291">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90da0-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="90da0-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90da0-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90da0-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="90da0-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-294">Search-Flags</span></span>           | <span data-ttu-id="90da0-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90da0-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="90da0-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90da0-296">System-Flags</span></span>           | <span data-ttu-id="90da0-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90da0-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="90da0-298">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90da0-298">Classes used in</span></span>        | [<span data-ttu-id="90da0-299">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="90da0-300">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="90da0-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





