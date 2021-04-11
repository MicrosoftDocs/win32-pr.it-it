---
title: attributo di dominio ms-DS-SD-Reference
description: Nome del dominio da utilizzare per la conversione del descrittore di sicurezza per un contesto di denominazione non di dominio.
ms.assetid: 5e0591e8-bf2a-4788-867e-c15c35b35a14
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di dominio ms-DS-SD-Reference
- attributo msDS-SDReferenceDomain-schema AD
topic_type:
- apiref
api_name:
- ms-DS-SD-Reference-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df717205937bc50c394835f2e3c00f182b8ab91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122934"
---
# <a name="ms-ds-sd-reference-domain-attribute"></a><span data-ttu-id="5818a-105">attributo di dominio ms-DS-SD-Reference</span><span class="sxs-lookup"><span data-stu-id="5818a-105">ms-DS-SD-Reference-Domain attribute</span></span>

<span data-ttu-id="5818a-106">Nome del dominio da utilizzare per la conversione del descrittore di sicurezza per un contesto di denominazione non di dominio.</span><span class="sxs-lookup"><span data-stu-id="5818a-106">The name of the domain to be used for security descriptor translation for a non-domain-naming context.</span></span>



| <span data-ttu-id="5818a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-107">Entry</span></span> | <span data-ttu-id="5818a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5818a-109">CN</span><span class="sxs-lookup"><span data-stu-id="5818a-109">CN</span></span>                | <span data-ttu-id="5818a-110">ms-DS-SD-Reference-Domain</span><span class="sxs-lookup"><span data-stu-id="5818a-110">ms-DS-SD-Reference-Domain</span></span>               |
| <span data-ttu-id="5818a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5818a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5818a-112">msDS-SDReferenceDomain</span><span class="sxs-lookup"><span data-stu-id="5818a-112">msDS-SDReferenceDomain</span></span>                  |
| <span data-ttu-id="5818a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5818a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="5818a-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5818a-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="5818a-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5818a-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="5818a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-116">Attribute-Id</span></span>      | <span data-ttu-id="5818a-117">1.2.840.113556.1.4.1711</span><span class="sxs-lookup"><span data-stu-id="5818a-117">1.2.840.113556.1.4.1711</span></span>                 |
| <span data-ttu-id="5818a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5818a-118">System-Id-Guid</span></span>    | <span data-ttu-id="5818a-119">4c51e316-f628-43a5-b06b-ffb695fcb4f3</span><span class="sxs-lookup"><span data-stu-id="5818a-119">4c51e316-f628-43a5-b06b-ffb695fcb4f3</span></span>    |
| <span data-ttu-id="5818a-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5818a-120">Syntax</span></span>            | [<span data-ttu-id="5818a-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5818a-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5818a-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="5818a-122">Implementations</span></span>

-   [<span data-ttu-id="5818a-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5818a-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5818a-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5818a-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5818a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5818a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5818a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5818a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5818a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5818a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5818a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5818a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5818a-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5818a-129">Windows Server 2003</span></span>



| <span data-ttu-id="5818a-130">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-130">Entry</span></span> | <span data-ttu-id="5818a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5818a-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5818a-132">Link-Id</span></span>                | <span data-ttu-id="5818a-133">2000</span><span class="sxs-lookup"><span data-stu-id="5818a-133">2000</span></span>                                       |
| <span data-ttu-id="5818a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5818a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5818a-135">System-Only</span></span>            | <span data-ttu-id="5818a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-136">False</span></span>                                      |
| <span data-ttu-id="5818a-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5818a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5818a-138">Vero</span><span class="sxs-lookup"><span data-stu-id="5818a-138">True</span></span>                                       |
| <span data-ttu-id="5818a-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5818a-139">Is Indexed</span></span>             | <span data-ttu-id="5818a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-140">False</span></span>                                      |
| <span data-ttu-id="5818a-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5818a-141">In Global Catalog</span></span>      | <span data-ttu-id="5818a-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-142">False</span></span>                                      |
| <span data-ttu-id="5818a-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5818a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5818a-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5818a-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5818a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5818a-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5818a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5818a-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5818a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-147">Search-Flags</span></span>           | <span data-ttu-id="5818a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5818a-148">0x00000000</span></span>                                 |
| <span data-ttu-id="5818a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-149">System-Flags</span></span>           | <span data-ttu-id="5818a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5818a-150">0x00000010</span></span>                                 |
| <span data-ttu-id="5818a-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5818a-151">Classes used in</span></span>        | [<span data-ttu-id="5818a-152">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="5818a-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5818a-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="5818a-153">ADAM</span></span>



| <span data-ttu-id="5818a-154">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-154">Entry</span></span> | <span data-ttu-id="5818a-155">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5818a-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5818a-156">Link-Id</span></span>                | <span data-ttu-id="5818a-157">2000</span><span class="sxs-lookup"><span data-stu-id="5818a-157">2000</span></span>                                       |
| <span data-ttu-id="5818a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5818a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5818a-159">System-Only</span></span>            | <span data-ttu-id="5818a-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-160">False</span></span>                                      |
| <span data-ttu-id="5818a-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5818a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5818a-162">Vero</span><span class="sxs-lookup"><span data-stu-id="5818a-162">True</span></span>                                       |
| <span data-ttu-id="5818a-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5818a-163">Is Indexed</span></span>             | <span data-ttu-id="5818a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-164">False</span></span>                                      |
| <span data-ttu-id="5818a-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5818a-165">In Global Catalog</span></span>      | <span data-ttu-id="5818a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-166">False</span></span>                                      |
| <span data-ttu-id="5818a-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5818a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5818a-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5818a-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5818a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5818a-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5818a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5818a-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5818a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-171">Search-Flags</span></span>           | <span data-ttu-id="5818a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5818a-172">0x00000000</span></span>                                 |
| <span data-ttu-id="5818a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-173">System-Flags</span></span>           | <span data-ttu-id="5818a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5818a-174">0x00000010</span></span>                                 |
| <span data-ttu-id="5818a-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5818a-175">Classes used in</span></span>        | [<span data-ttu-id="5818a-176">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="5818a-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5818a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5818a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5818a-178">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-178">Entry</span></span> | <span data-ttu-id="5818a-179">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5818a-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5818a-180">Link-Id</span></span>                | <span data-ttu-id="5818a-181">2000</span><span class="sxs-lookup"><span data-stu-id="5818a-181">2000</span></span>                                       |
| <span data-ttu-id="5818a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5818a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5818a-183">System-Only</span></span>            | <span data-ttu-id="5818a-184">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-184">False</span></span>                                      |
| <span data-ttu-id="5818a-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5818a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5818a-186">Vero</span><span class="sxs-lookup"><span data-stu-id="5818a-186">True</span></span>                                       |
| <span data-ttu-id="5818a-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5818a-187">Is Indexed</span></span>             | <span data-ttu-id="5818a-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-188">False</span></span>                                      |
| <span data-ttu-id="5818a-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5818a-189">In Global Catalog</span></span>      | <span data-ttu-id="5818a-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-190">False</span></span>                                      |
| <span data-ttu-id="5818a-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5818a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5818a-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5818a-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5818a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5818a-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5818a-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5818a-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5818a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-195">Search-Flags</span></span>           | <span data-ttu-id="5818a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5818a-196">0x00000000</span></span>                                 |
| <span data-ttu-id="5818a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-197">System-Flags</span></span>           | <span data-ttu-id="5818a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5818a-198">0x00000010</span></span>                                 |
| <span data-ttu-id="5818a-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5818a-199">Classes used in</span></span>        | [<span data-ttu-id="5818a-200">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="5818a-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5818a-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5818a-201">Windows Server 2008</span></span>



| <span data-ttu-id="5818a-202">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-202">Entry</span></span> | <span data-ttu-id="5818a-203">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5818a-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5818a-204">Link-Id</span></span>                | <span data-ttu-id="5818a-205">2000</span><span class="sxs-lookup"><span data-stu-id="5818a-205">2000</span></span>                                       |
| <span data-ttu-id="5818a-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-206">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5818a-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="5818a-207">System-Only</span></span>            | <span data-ttu-id="5818a-208">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-208">False</span></span>                                      |
| <span data-ttu-id="5818a-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5818a-209">Is-Single-Valued</span></span>       | <span data-ttu-id="5818a-210">Vero</span><span class="sxs-lookup"><span data-stu-id="5818a-210">True</span></span>                                       |
| <span data-ttu-id="5818a-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5818a-211">Is Indexed</span></span>             | <span data-ttu-id="5818a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-212">False</span></span>                                      |
| <span data-ttu-id="5818a-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5818a-213">In Global Catalog</span></span>      | <span data-ttu-id="5818a-214">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-214">False</span></span>                                      |
| <span data-ttu-id="5818a-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5818a-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="5818a-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5818a-216">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5818a-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5818a-217">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5818a-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5818a-218">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5818a-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-219">Search-Flags</span></span>           | <span data-ttu-id="5818a-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5818a-220">0x00000000</span></span>                                 |
| <span data-ttu-id="5818a-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-221">System-Flags</span></span>           | <span data-ttu-id="5818a-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5818a-222">0x00000010</span></span>                                 |
| <span data-ttu-id="5818a-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5818a-223">Classes used in</span></span>        | [<span data-ttu-id="5818a-224">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="5818a-224">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5818a-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5818a-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5818a-226">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-226">Entry</span></span> | <span data-ttu-id="5818a-227">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-227">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5818a-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5818a-228">Link-Id</span></span>                | <span data-ttu-id="5818a-229">2000</span><span class="sxs-lookup"><span data-stu-id="5818a-229">2000</span></span>                                       |
| <span data-ttu-id="5818a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-230">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5818a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="5818a-231">System-Only</span></span>            | <span data-ttu-id="5818a-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-232">False</span></span>                                      |
| <span data-ttu-id="5818a-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5818a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="5818a-234">Vero</span><span class="sxs-lookup"><span data-stu-id="5818a-234">True</span></span>                                       |
| <span data-ttu-id="5818a-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5818a-235">Is Indexed</span></span>             | <span data-ttu-id="5818a-236">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-236">False</span></span>                                      |
| <span data-ttu-id="5818a-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5818a-237">In Global Catalog</span></span>      | <span data-ttu-id="5818a-238">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-238">False</span></span>                                      |
| <span data-ttu-id="5818a-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5818a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="5818a-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5818a-240">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5818a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5818a-241">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5818a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5818a-242">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5818a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-243">Search-Flags</span></span>           | <span data-ttu-id="5818a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5818a-244">0x00000000</span></span>                                 |
| <span data-ttu-id="5818a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-245">System-Flags</span></span>           | <span data-ttu-id="5818a-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5818a-246">0x00000010</span></span>                                 |
| <span data-ttu-id="5818a-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5818a-247">Classes used in</span></span>        | [<span data-ttu-id="5818a-248">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="5818a-248">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5818a-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5818a-249">Windows Server 2012</span></span>



| <span data-ttu-id="5818a-250">Voce</span><span class="sxs-lookup"><span data-stu-id="5818a-250">Entry</span></span> | <span data-ttu-id="5818a-251">Valore</span><span class="sxs-lookup"><span data-stu-id="5818a-251">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="5818a-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5818a-252">Link-Id</span></span>                | <span data-ttu-id="5818a-253">2000</span><span class="sxs-lookup"><span data-stu-id="5818a-253">2000</span></span>                                       |
| <span data-ttu-id="5818a-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5818a-254">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="5818a-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="5818a-255">System-Only</span></span>            | <span data-ttu-id="5818a-256">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-256">False</span></span>                                      |
| <span data-ttu-id="5818a-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5818a-257">Is-Single-Valued</span></span>       | <span data-ttu-id="5818a-258">Vero</span><span class="sxs-lookup"><span data-stu-id="5818a-258">True</span></span>                                       |
| <span data-ttu-id="5818a-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5818a-259">Is Indexed</span></span>             | <span data-ttu-id="5818a-260">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-260">False</span></span>                                      |
| <span data-ttu-id="5818a-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5818a-261">In Global Catalog</span></span>      | <span data-ttu-id="5818a-262">Falso</span><span class="sxs-lookup"><span data-stu-id="5818a-262">False</span></span>                                      |
| <span data-ttu-id="5818a-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5818a-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="5818a-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5818a-264">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="5818a-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5818a-265">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="5818a-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5818a-266">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="5818a-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-267">Search-Flags</span></span>           | <span data-ttu-id="5818a-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5818a-268">0x00000000</span></span>                                 |
| <span data-ttu-id="5818a-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5818a-269">System-Flags</span></span>           | <span data-ttu-id="5818a-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5818a-270">0x00000010</span></span>                                 |
| <span data-ttu-id="5818a-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5818a-271">Classes used in</span></span>        | [<span data-ttu-id="5818a-272">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="5818a-272">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





