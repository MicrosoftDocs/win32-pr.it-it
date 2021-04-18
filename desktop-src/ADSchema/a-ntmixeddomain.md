---
title: NT-attributo di dominio misto
description: Indica che il dominio è in modalità nativa o mista. Questo attributo si trova nell'oggetto domainDNS (Head) per il dominio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- NT-schema AD dell'attributo di dominio misto
- Schema AD dell'attributo nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303176"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="7bf2b-106">NT-attributo di dominio misto</span><span class="sxs-lookup"><span data-stu-id="7bf2b-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="7bf2b-107">Indica che il dominio è in modalità nativa o mista.</span><span class="sxs-lookup"><span data-stu-id="7bf2b-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="7bf2b-108">Questo attributo si trova nell'oggetto domainDNS (Head) per il dominio.</span><span class="sxs-lookup"><span data-stu-id="7bf2b-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="7bf2b-109">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-109">Entry</span></span> | <span data-ttu-id="7bf2b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="7bf2b-111">CN</span><span class="sxs-lookup"><span data-stu-id="7bf2b-111">CN</span></span>                | <span data-ttu-id="7bf2b-112">NT-misto-dominio</span><span class="sxs-lookup"><span data-stu-id="7bf2b-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="7bf2b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7bf2b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7bf2b-114">nTMixedDomain</span><span class="sxs-lookup"><span data-stu-id="7bf2b-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="7bf2b-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="7bf2b-115">Size</span></span>              | <span data-ttu-id="7bf2b-116">4 byte.</span><span class="sxs-lookup"><span data-stu-id="7bf2b-116">4 bytes.</span></span> <span data-ttu-id="7bf2b-117">Modalità mista 1, modalità nativa 0.</span><span class="sxs-lookup"><span data-stu-id="7bf2b-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="7bf2b-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="7bf2b-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="7bf2b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-120">Attribute-Id</span></span>      | <span data-ttu-id="7bf2b-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="7bf2b-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="7bf2b-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7bf2b-122">System-Id-Guid</span></span>    | <span data-ttu-id="7bf2b-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7bf2b-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="7bf2b-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bf2b-124">Syntax</span></span>            | [<span data-ttu-id="7bf2b-125">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="7bf2b-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="7bf2b-126">Implementations</span></span>

-   [<span data-ttu-id="7bf2b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7bf2b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7bf2b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7bf2b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7bf2b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7bf2b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7bf2b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bf2b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="7bf2b-134">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-134">Entry</span></span> | <span data-ttu-id="7bf2b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7bf2b-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bf2b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7bf2b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bf2b-138">System-Only</span></span>            | <span data-ttu-id="7bf2b-139">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-139">False</span></span>                                        |
| <span data-ttu-id="7bf2b-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7bf2b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7bf2b-141">Vero</span><span class="sxs-lookup"><span data-stu-id="7bf2b-141">True</span></span>                                         |
| <span data-ttu-id="7bf2b-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7bf2b-142">Is Indexed</span></span>             | <span data-ttu-id="7bf2b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-143">False</span></span>                                        |
| <span data-ttu-id="7bf2b-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7bf2b-144">In Global Catalog</span></span>      | <span data-ttu-id="7bf2b-145">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-145">False</span></span>                                        |
| <span data-ttu-id="7bf2b-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bf2b-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7bf2b-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7bf2b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bf2b-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7bf2b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bf2b-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7bf2b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-150">Search-Flags</span></span>           | <span data-ttu-id="7bf2b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bf2b-151">0x00000000</span></span>                                   |
| <span data-ttu-id="7bf2b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-152">System-Flags</span></span>           | <span data-ttu-id="7bf2b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bf2b-153">0x00000010</span></span>                                   |
| <span data-ttu-id="7bf2b-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7bf2b-154">Classes used in</span></span>        | [<span data-ttu-id="7bf2b-155">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7bf2b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bf2b-156">Windows Server 2003</span></span>



| <span data-ttu-id="7bf2b-157">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-157">Entry</span></span> | <span data-ttu-id="7bf2b-158">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf2b-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bf2b-161">System-Only</span></span>            | <span data-ttu-id="7bf2b-162">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-162">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7bf2b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7bf2b-164">Vero</span><span class="sxs-lookup"><span data-stu-id="7bf2b-164">True</span></span>                                                                                    |
| <span data-ttu-id="7bf2b-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7bf2b-165">Is Indexed</span></span>             | <span data-ttu-id="7bf2b-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-166">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7bf2b-167">In Global Catalog</span></span>      | <span data-ttu-id="7bf2b-168">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-168">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bf2b-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7bf2b-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="7bf2b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bf2b-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bf2b-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-173">Search-Flags</span></span>           | <span data-ttu-id="7bf2b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bf2b-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="7bf2b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-175">System-Flags</span></span>           | <span data-ttu-id="7bf2b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bf2b-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="7bf2b-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7bf2b-177">Classes used in</span></span>        | [<span data-ttu-id="7bf2b-178">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="7bf2b-179">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7bf2b-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7bf2b-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7bf2b-181">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-181">Entry</span></span> | <span data-ttu-id="7bf2b-182">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf2b-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bf2b-185">System-Only</span></span>            | <span data-ttu-id="7bf2b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-186">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7bf2b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7bf2b-188">Vero</span><span class="sxs-lookup"><span data-stu-id="7bf2b-188">True</span></span>                                                                                    |
| <span data-ttu-id="7bf2b-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7bf2b-189">Is Indexed</span></span>             | <span data-ttu-id="7bf2b-190">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-190">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7bf2b-191">In Global Catalog</span></span>      | <span data-ttu-id="7bf2b-192">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-192">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bf2b-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7bf2b-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="7bf2b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bf2b-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bf2b-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-197">Search-Flags</span></span>           | <span data-ttu-id="7bf2b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bf2b-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="7bf2b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-199">System-Flags</span></span>           | <span data-ttu-id="7bf2b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bf2b-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="7bf2b-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7bf2b-201">Classes used in</span></span>        | [<span data-ttu-id="7bf2b-202">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="7bf2b-203">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7bf2b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bf2b-204">Windows Server 2008</span></span>



| <span data-ttu-id="7bf2b-205">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-205">Entry</span></span> | <span data-ttu-id="7bf2b-206">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf2b-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bf2b-209">System-Only</span></span>            | <span data-ttu-id="7bf2b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-210">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7bf2b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="7bf2b-212">Vero</span><span class="sxs-lookup"><span data-stu-id="7bf2b-212">True</span></span>                                                                                    |
| <span data-ttu-id="7bf2b-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7bf2b-213">Is Indexed</span></span>             | <span data-ttu-id="7bf2b-214">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-214">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7bf2b-215">In Global Catalog</span></span>      | <span data-ttu-id="7bf2b-216">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-216">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bf2b-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7bf2b-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="7bf2b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bf2b-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bf2b-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-221">Search-Flags</span></span>           | <span data-ttu-id="7bf2b-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bf2b-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="7bf2b-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-223">System-Flags</span></span>           | <span data-ttu-id="7bf2b-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bf2b-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="7bf2b-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7bf2b-225">Classes used in</span></span>        | [<span data-ttu-id="7bf2b-226">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="7bf2b-227">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7bf2b-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7bf2b-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7bf2b-229">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-229">Entry</span></span> | <span data-ttu-id="7bf2b-230">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf2b-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bf2b-233">System-Only</span></span>            | <span data-ttu-id="7bf2b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-234">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7bf2b-235">Is-Single-Valued</span></span>       | <span data-ttu-id="7bf2b-236">Vero</span><span class="sxs-lookup"><span data-stu-id="7bf2b-236">True</span></span>                                                                                    |
| <span data-ttu-id="7bf2b-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7bf2b-237">Is Indexed</span></span>             | <span data-ttu-id="7bf2b-238">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-238">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7bf2b-239">In Global Catalog</span></span>      | <span data-ttu-id="7bf2b-240">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-240">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bf2b-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7bf2b-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="7bf2b-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bf2b-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bf2b-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-245">Search-Flags</span></span>           | <span data-ttu-id="7bf2b-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bf2b-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="7bf2b-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-247">System-Flags</span></span>           | <span data-ttu-id="7bf2b-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bf2b-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="7bf2b-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7bf2b-249">Classes used in</span></span>        | [<span data-ttu-id="7bf2b-250">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="7bf2b-251">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7bf2b-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bf2b-252">Windows Server 2012</span></span>



| <span data-ttu-id="7bf2b-253">Voce</span><span class="sxs-lookup"><span data-stu-id="7bf2b-253">Entry</span></span> | <span data-ttu-id="7bf2b-254">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf2b-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="7bf2b-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bf2b-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="7bf2b-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bf2b-257">System-Only</span></span>            | <span data-ttu-id="7bf2b-258">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-258">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-259">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="7bf2b-259">Is-Single-Valued</span></span>       | <span data-ttu-id="7bf2b-260">Vero</span><span class="sxs-lookup"><span data-stu-id="7bf2b-260">True</span></span>                                                                                    |
| <span data-ttu-id="7bf2b-261">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="7bf2b-261">Is Indexed</span></span>             | <span data-ttu-id="7bf2b-262">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-262">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-263">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="7bf2b-263">In Global Catalog</span></span>      | <span data-ttu-id="7bf2b-264">Falso</span><span class="sxs-lookup"><span data-stu-id="7bf2b-264">False</span></span>                                                                                   |
| <span data-ttu-id="7bf2b-265">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="7bf2b-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bf2b-266">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="7bf2b-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="7bf2b-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bf2b-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bf2b-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="7bf2b-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-269">Search-Flags</span></span>           | <span data-ttu-id="7bf2b-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bf2b-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="7bf2b-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bf2b-271">System-Flags</span></span>           | <span data-ttu-id="7bf2b-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bf2b-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="7bf2b-273">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="7bf2b-273">Classes used in</span></span>        | [<span data-ttu-id="7bf2b-274">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="7bf2b-275">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="7bf2b-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





