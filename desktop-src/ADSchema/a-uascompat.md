---
title: Attributo UAS-Compat
description: Indica se il gestore degli account di sicurezza imporrà le dimensioni dei dati per rendere Active Directory compatibile con LanManager user account System (UAS).
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Schema AD UAS-Compat attribute
- Schema AD dell'attributo uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303352"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="3718d-105">Attributo UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="3718d-105">UAS-Compat attribute</span></span>

<span data-ttu-id="3718d-106">Indica se il gestore degli account di sicurezza imporrà le dimensioni dei dati per rendere Active Directory compatibile con LanManager user account System (UAS).</span><span class="sxs-lookup"><span data-stu-id="3718d-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="3718d-107">Se questo valore è 0, non viene applicato alcun limite.</span><span class="sxs-lookup"><span data-stu-id="3718d-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="3718d-108">Se questo valore è 1, vengono applicati i limiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="3718d-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="3718d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-109">Value</span></span>                          | <span data-ttu-id="3718d-110">Length</span><span class="sxs-lookup"><span data-stu-id="3718d-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="3718d-111">Password</span><span class="sxs-lookup"><span data-stu-id="3718d-111">Password</span></span><br/>            | <span data-ttu-id="3718d-112">da 0 a 14 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="3718d-113">Nome account</span><span class="sxs-lookup"><span data-stu-id="3718d-113">Account Name</span></span><br/>        | <span data-ttu-id="3718d-114">da 0 a 20 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="3718d-115">Nome dominio</span><span class="sxs-lookup"><span data-stu-id="3718d-115">Domain Name</span></span><br/>         | <span data-ttu-id="3718d-116">da 0 a 15 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="3718d-117">Nome computer</span><span class="sxs-lookup"><span data-stu-id="3718d-117">Computer Name</span></span><br/>       | <span data-ttu-id="3718d-118">da 0 a 15 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="3718d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3718d-119">Comments</span></span><br/>            | <span data-ttu-id="3718d-120">da 0 a 48 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="3718d-121">Home directory</span><span class="sxs-lookup"><span data-stu-id="3718d-121">Home Directory</span></span><br/>      | <span data-ttu-id="3718d-122">da 0 a 256 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="3718d-123">Percorso script</span><span class="sxs-lookup"><span data-stu-id="3718d-123">Script Path</span></span><br/>         | <span data-ttu-id="3718d-124">da 0 a 256 caratteri</span><span class="sxs-lookup"><span data-stu-id="3718d-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="3718d-125">Unità di tempo per settimana</span><span class="sxs-lookup"><span data-stu-id="3718d-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="3718d-126">168 bit (21 byte)</span><span class="sxs-lookup"><span data-stu-id="3718d-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="3718d-127">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-127">Entry</span></span> | <span data-ttu-id="3718d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3718d-129">CN</span><span class="sxs-lookup"><span data-stu-id="3718d-129">CN</span></span>                | <span data-ttu-id="3718d-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="3718d-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="3718d-131">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3718d-131">Ldap-Display-Name</span></span> | <span data-ttu-id="3718d-132">uASCompat</span><span class="sxs-lookup"><span data-stu-id="3718d-132">uASCompat</span></span>                            |
| <span data-ttu-id="3718d-133">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3718d-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="3718d-134">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3718d-134">Update Privilege</span></span>  | <span data-ttu-id="3718d-135">Eseguita da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="3718d-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="3718d-136">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3718d-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3718d-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-137">Attribute-Id</span></span>      | <span data-ttu-id="3718d-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="3718d-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="3718d-139">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3718d-139">System-Id-Guid</span></span>    | <span data-ttu-id="3718d-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3718d-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3718d-141">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3718d-141">Syntax</span></span>            | [<span data-ttu-id="3718d-142">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="3718d-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3718d-143">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3718d-143">Implementations</span></span>

-   [<span data-ttu-id="3718d-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3718d-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3718d-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3718d-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3718d-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3718d-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3718d-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3718d-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3718d-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3718d-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3718d-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3718d-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3718d-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3718d-150">Windows 2000 Server</span></span>



| <span data-ttu-id="3718d-151">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-151">Entry</span></span> | <span data-ttu-id="3718d-152">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3718d-153">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3718d-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="3718d-155">System-Only</span></span>            | <span data-ttu-id="3718d-156">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-156">False</span></span>                                                 |
| <span data-ttu-id="3718d-157">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3718d-157">Is-Single-Valued</span></span>       | <span data-ttu-id="3718d-158">Vero</span><span class="sxs-lookup"><span data-stu-id="3718d-158">True</span></span>                                                  |
| <span data-ttu-id="3718d-159">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3718d-159">Is Indexed</span></span>             | <span data-ttu-id="3718d-160">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-160">False</span></span>                                                 |
| <span data-ttu-id="3718d-161">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3718d-161">In Global Catalog</span></span>      | <span data-ttu-id="3718d-162">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-162">False</span></span>                                                 |
| <span data-ttu-id="3718d-163">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3718d-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="3718d-164">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3718d-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3718d-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3718d-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3718d-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-167">Search-Flags</span></span>           | <span data-ttu-id="3718d-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3718d-168">0x00000000</span></span>                                            |
| <span data-ttu-id="3718d-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-169">System-Flags</span></span>           | <span data-ttu-id="3718d-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3718d-170">0x00000010</span></span>                                            |
| <span data-ttu-id="3718d-171">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3718d-171">Classes used in</span></span>        | [<span data-ttu-id="3718d-172">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="3718d-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3718d-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3718d-173">Windows Server 2003</span></span>



| <span data-ttu-id="3718d-174">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-174">Entry</span></span> | <span data-ttu-id="3718d-175">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3718d-176">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3718d-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="3718d-178">System-Only</span></span>            | <span data-ttu-id="3718d-179">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-179">False</span></span>                                                 |
| <span data-ttu-id="3718d-180">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3718d-180">Is-Single-Valued</span></span>       | <span data-ttu-id="3718d-181">Vero</span><span class="sxs-lookup"><span data-stu-id="3718d-181">True</span></span>                                                  |
| <span data-ttu-id="3718d-182">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3718d-182">Is Indexed</span></span>             | <span data-ttu-id="3718d-183">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-183">False</span></span>                                                 |
| <span data-ttu-id="3718d-184">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3718d-184">In Global Catalog</span></span>      | <span data-ttu-id="3718d-185">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-185">False</span></span>                                                 |
| <span data-ttu-id="3718d-186">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3718d-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="3718d-187">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3718d-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3718d-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3718d-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3718d-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-190">Search-Flags</span></span>           | <span data-ttu-id="3718d-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3718d-191">0x00000000</span></span>                                            |
| <span data-ttu-id="3718d-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-192">System-Flags</span></span>           | <span data-ttu-id="3718d-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3718d-193">0x00000010</span></span>                                            |
| <span data-ttu-id="3718d-194">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3718d-194">Classes used in</span></span>        | [<span data-ttu-id="3718d-195">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="3718d-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3718d-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3718d-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3718d-197">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-197">Entry</span></span> | <span data-ttu-id="3718d-198">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3718d-199">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3718d-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="3718d-201">System-Only</span></span>            | <span data-ttu-id="3718d-202">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-202">False</span></span>                                                 |
| <span data-ttu-id="3718d-203">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3718d-203">Is-Single-Valued</span></span>       | <span data-ttu-id="3718d-204">Vero</span><span class="sxs-lookup"><span data-stu-id="3718d-204">True</span></span>                                                  |
| <span data-ttu-id="3718d-205">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3718d-205">Is Indexed</span></span>             | <span data-ttu-id="3718d-206">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-206">False</span></span>                                                 |
| <span data-ttu-id="3718d-207">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3718d-207">In Global Catalog</span></span>      | <span data-ttu-id="3718d-208">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-208">False</span></span>                                                 |
| <span data-ttu-id="3718d-209">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3718d-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="3718d-210">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3718d-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3718d-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3718d-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3718d-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-213">Search-Flags</span></span>           | <span data-ttu-id="3718d-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3718d-214">0x00000000</span></span>                                            |
| <span data-ttu-id="3718d-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-215">System-Flags</span></span>           | <span data-ttu-id="3718d-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3718d-216">0x00000010</span></span>                                            |
| <span data-ttu-id="3718d-217">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3718d-217">Classes used in</span></span>        | [<span data-ttu-id="3718d-218">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="3718d-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3718d-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3718d-219">Windows Server 2008</span></span>



| <span data-ttu-id="3718d-220">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-220">Entry</span></span> | <span data-ttu-id="3718d-221">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3718d-222">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3718d-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="3718d-224">System-Only</span></span>            | <span data-ttu-id="3718d-225">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-225">False</span></span>                                                 |
| <span data-ttu-id="3718d-226">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3718d-226">Is-Single-Valued</span></span>       | <span data-ttu-id="3718d-227">Vero</span><span class="sxs-lookup"><span data-stu-id="3718d-227">True</span></span>                                                  |
| <span data-ttu-id="3718d-228">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3718d-228">Is Indexed</span></span>             | <span data-ttu-id="3718d-229">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-229">False</span></span>                                                 |
| <span data-ttu-id="3718d-230">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3718d-230">In Global Catalog</span></span>      | <span data-ttu-id="3718d-231">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-231">False</span></span>                                                 |
| <span data-ttu-id="3718d-232">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3718d-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="3718d-233">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3718d-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3718d-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3718d-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3718d-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-236">Search-Flags</span></span>           | <span data-ttu-id="3718d-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3718d-237">0x00000000</span></span>                                            |
| <span data-ttu-id="3718d-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-238">System-Flags</span></span>           | <span data-ttu-id="3718d-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3718d-239">0x00000010</span></span>                                            |
| <span data-ttu-id="3718d-240">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3718d-240">Classes used in</span></span>        | [<span data-ttu-id="3718d-241">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="3718d-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3718d-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3718d-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3718d-243">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-243">Entry</span></span> | <span data-ttu-id="3718d-244">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3718d-245">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3718d-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="3718d-247">System-Only</span></span>            | <span data-ttu-id="3718d-248">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-248">False</span></span>                                                 |
| <span data-ttu-id="3718d-249">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3718d-249">Is-Single-Valued</span></span>       | <span data-ttu-id="3718d-250">Vero</span><span class="sxs-lookup"><span data-stu-id="3718d-250">True</span></span>                                                  |
| <span data-ttu-id="3718d-251">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3718d-251">Is Indexed</span></span>             | <span data-ttu-id="3718d-252">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-252">False</span></span>                                                 |
| <span data-ttu-id="3718d-253">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3718d-253">In Global Catalog</span></span>      | <span data-ttu-id="3718d-254">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-254">False</span></span>                                                 |
| <span data-ttu-id="3718d-255">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3718d-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="3718d-256">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3718d-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3718d-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3718d-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3718d-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-259">Search-Flags</span></span>           | <span data-ttu-id="3718d-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3718d-260">0x00000000</span></span>                                            |
| <span data-ttu-id="3718d-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-261">System-Flags</span></span>           | <span data-ttu-id="3718d-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3718d-262">0x00000010</span></span>                                            |
| <span data-ttu-id="3718d-263">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3718d-263">Classes used in</span></span>        | [<span data-ttu-id="3718d-264">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="3718d-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3718d-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3718d-265">Windows Server 2012</span></span>



| <span data-ttu-id="3718d-266">Voce</span><span class="sxs-lookup"><span data-stu-id="3718d-266">Entry</span></span> | <span data-ttu-id="3718d-267">Valore</span><span class="sxs-lookup"><span data-stu-id="3718d-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3718d-268">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3718d-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3718d-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="3718d-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="3718d-270">System-Only</span></span>            | <span data-ttu-id="3718d-271">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-271">False</span></span>                                                 |
| <span data-ttu-id="3718d-272">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3718d-272">Is-Single-Valued</span></span>       | <span data-ttu-id="3718d-273">Vero</span><span class="sxs-lookup"><span data-stu-id="3718d-273">True</span></span>                                                  |
| <span data-ttu-id="3718d-274">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3718d-274">Is Indexed</span></span>             | <span data-ttu-id="3718d-275">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-275">False</span></span>                                                 |
| <span data-ttu-id="3718d-276">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3718d-276">In Global Catalog</span></span>      | <span data-ttu-id="3718d-277">Falso</span><span class="sxs-lookup"><span data-stu-id="3718d-277">False</span></span>                                                 |
| <span data-ttu-id="3718d-278">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3718d-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="3718d-279">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3718d-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="3718d-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3718d-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3718d-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="3718d-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-282">Search-Flags</span></span>           | <span data-ttu-id="3718d-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3718d-283">0x00000000</span></span>                                            |
| <span data-ttu-id="3718d-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3718d-284">System-Flags</span></span>           | <span data-ttu-id="3718d-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3718d-285">0x00000010</span></span>                                            |
| <span data-ttu-id="3718d-286">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3718d-286">Classes used in</span></span>        | [<span data-ttu-id="3718d-287">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="3718d-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





