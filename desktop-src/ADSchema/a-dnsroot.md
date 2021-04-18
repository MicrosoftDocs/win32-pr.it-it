---
title: Attributo Dns-Root
description: Nome di dominio DNS più alto assegnato a una partizione di dominio/directory.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Schema AD Dns-Root attribute
- Schema AD dell'attributo dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303038"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="630f0-105">Attributo Dns-Root</span><span class="sxs-lookup"><span data-stu-id="630f0-105">Dns-Root attribute</span></span>

<span data-ttu-id="630f0-106">Nome di dominio DNS più alto assegnato a una partizione di dominio/directory.</span><span class="sxs-lookup"><span data-stu-id="630f0-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="630f0-107">Viene impostato su un oggetto crossRef e, tra le altre cose, viene usato per la generazione di riferimenti.</span><span class="sxs-lookup"><span data-stu-id="630f0-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="630f0-108">Quando si esegue la ricerca in un intero albero di dominio, è necessario avviare la ricerca in corrispondenza dell'oggetto Dns-Root.</span><span class="sxs-lookup"><span data-stu-id="630f0-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="630f0-109">Questo attributo può essere multivalore, nel qual caso vengono generati più riferimenti.</span><span class="sxs-lookup"><span data-stu-id="630f0-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="630f0-110">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-110">Entry</span></span> | <span data-ttu-id="630f0-111">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="630f0-112">CN</span><span class="sxs-lookup"><span data-stu-id="630f0-112">CN</span></span>                | <span data-ttu-id="630f0-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="630f0-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="630f0-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="630f0-114">Ldap-Display-Name</span></span> | <span data-ttu-id="630f0-115">dnsRoot</span><span class="sxs-lookup"><span data-stu-id="630f0-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="630f0-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="630f0-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="630f0-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="630f0-117">Update Privilege</span></span>  | <span data-ttu-id="630f0-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="630f0-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="630f0-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="630f0-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="630f0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-120">Attribute-Id</span></span>      | <span data-ttu-id="630f0-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="630f0-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="630f0-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="630f0-122">System-Id-Guid</span></span>    | <span data-ttu-id="630f0-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="630f0-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="630f0-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="630f0-124">Syntax</span></span>            | [<span data-ttu-id="630f0-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="630f0-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="630f0-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="630f0-126">Implementations</span></span>

-   [<span data-ttu-id="630f0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="630f0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="630f0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="630f0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="630f0-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="630f0-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="630f0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="630f0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="630f0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="630f0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="630f0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="630f0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="630f0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="630f0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="630f0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="630f0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="630f0-135">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-135">Entry</span></span> | <span data-ttu-id="630f0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-139">System-Only</span></span>            | <span data-ttu-id="630f0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-140">False</span></span>                                      |
| <span data-ttu-id="630f0-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-142">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-142">False</span></span>                                      |
| <span data-ttu-id="630f0-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-143">Is Indexed</span></span>             | <span data-ttu-id="630f0-144">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-144">True</span></span>                                       |
| <span data-ttu-id="630f0-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-145">In Global Catalog</span></span>      | <span data-ttu-id="630f0-146">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-146">False</span></span>                                      |
| <span data-ttu-id="630f0-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-149">Range-Lower</span></span>            | <span data-ttu-id="630f0-150">1</span><span class="sxs-lookup"><span data-stu-id="630f0-150">1</span></span>                                          |
| <span data-ttu-id="630f0-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-151">Range-Upper</span></span>            | <span data-ttu-id="630f0-152">255</span><span class="sxs-lookup"><span data-stu-id="630f0-152">255</span></span>                                        |
| <span data-ttu-id="630f0-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-153">Search-Flags</span></span>           | <span data-ttu-id="630f0-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-154">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-155">System-Flags</span></span>           | <span data-ttu-id="630f0-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-156">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-157">Classes used in</span></span>        | [<span data-ttu-id="630f0-158">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="630f0-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="630f0-159">Windows Server 2003</span></span>



| <span data-ttu-id="630f0-160">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-160">Entry</span></span> | <span data-ttu-id="630f0-161">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-164">System-Only</span></span>            | <span data-ttu-id="630f0-165">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-165">False</span></span>                                      |
| <span data-ttu-id="630f0-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-166">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-167">False</span></span>                                      |
| <span data-ttu-id="630f0-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-168">Is Indexed</span></span>             | <span data-ttu-id="630f0-169">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-169">True</span></span>                                       |
| <span data-ttu-id="630f0-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-170">In Global Catalog</span></span>      | <span data-ttu-id="630f0-171">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-171">False</span></span>                                      |
| <span data-ttu-id="630f0-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-174">Range-Lower</span></span>            | <span data-ttu-id="630f0-175">1</span><span class="sxs-lookup"><span data-stu-id="630f0-175">1</span></span>                                          |
| <span data-ttu-id="630f0-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-176">Range-Upper</span></span>            | <span data-ttu-id="630f0-177">255</span><span class="sxs-lookup"><span data-stu-id="630f0-177">255</span></span>                                        |
| <span data-ttu-id="630f0-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-178">Search-Flags</span></span>           | <span data-ttu-id="630f0-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-179">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-180">System-Flags</span></span>           | <span data-ttu-id="630f0-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-181">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-182">Classes used in</span></span>        | [<span data-ttu-id="630f0-183">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="630f0-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="630f0-184">ADAM</span></span>



| <span data-ttu-id="630f0-185">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-185">Entry</span></span> | <span data-ttu-id="630f0-186">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-189">System-Only</span></span>            | <span data-ttu-id="630f0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-190">False</span></span>                                      |
| <span data-ttu-id="630f0-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-191">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-192">False</span></span>                                      |
| <span data-ttu-id="630f0-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-193">Is Indexed</span></span>             | <span data-ttu-id="630f0-194">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-194">True</span></span>                                       |
| <span data-ttu-id="630f0-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-195">In Global Catalog</span></span>      | <span data-ttu-id="630f0-196">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-196">False</span></span>                                      |
| <span data-ttu-id="630f0-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-199">Range-Lower</span></span>            | <span data-ttu-id="630f0-200">1</span><span class="sxs-lookup"><span data-stu-id="630f0-200">1</span></span>                                          |
| <span data-ttu-id="630f0-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-201">Range-Upper</span></span>            | <span data-ttu-id="630f0-202">255</span><span class="sxs-lookup"><span data-stu-id="630f0-202">255</span></span>                                        |
| <span data-ttu-id="630f0-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-203">Search-Flags</span></span>           | <span data-ttu-id="630f0-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-204">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-205">System-Flags</span></span>           | <span data-ttu-id="630f0-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-206">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-207">Classes used in</span></span>        | [<span data-ttu-id="630f0-208">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="630f0-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="630f0-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="630f0-210">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-210">Entry</span></span> | <span data-ttu-id="630f0-211">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-214">System-Only</span></span>            | <span data-ttu-id="630f0-215">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-215">False</span></span>                                      |
| <span data-ttu-id="630f0-216">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-216">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-217">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-217">False</span></span>                                      |
| <span data-ttu-id="630f0-218">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-218">Is Indexed</span></span>             | <span data-ttu-id="630f0-219">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-219">True</span></span>                                       |
| <span data-ttu-id="630f0-220">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-220">In Global Catalog</span></span>      | <span data-ttu-id="630f0-221">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-221">False</span></span>                                      |
| <span data-ttu-id="630f0-222">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-223">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-224">Range-Lower</span></span>            | <span data-ttu-id="630f0-225">1</span><span class="sxs-lookup"><span data-stu-id="630f0-225">1</span></span>                                          |
| <span data-ttu-id="630f0-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-226">Range-Upper</span></span>            | <span data-ttu-id="630f0-227">255</span><span class="sxs-lookup"><span data-stu-id="630f0-227">255</span></span>                                        |
| <span data-ttu-id="630f0-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-228">Search-Flags</span></span>           | <span data-ttu-id="630f0-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-229">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-230">System-Flags</span></span>           | <span data-ttu-id="630f0-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-231">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-232">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-232">Classes used in</span></span>        | [<span data-ttu-id="630f0-233">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="630f0-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="630f0-234">Windows Server 2008</span></span>



| <span data-ttu-id="630f0-235">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-235">Entry</span></span> | <span data-ttu-id="630f0-236">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-237">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-239">System-Only</span></span>            | <span data-ttu-id="630f0-240">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-240">False</span></span>                                      |
| <span data-ttu-id="630f0-241">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-241">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-242">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-242">False</span></span>                                      |
| <span data-ttu-id="630f0-243">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-243">Is Indexed</span></span>             | <span data-ttu-id="630f0-244">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-244">True</span></span>                                       |
| <span data-ttu-id="630f0-245">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-245">In Global Catalog</span></span>      | <span data-ttu-id="630f0-246">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-246">False</span></span>                                      |
| <span data-ttu-id="630f0-247">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-248">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-249">Range-Lower</span></span>            | <span data-ttu-id="630f0-250">1</span><span class="sxs-lookup"><span data-stu-id="630f0-250">1</span></span>                                          |
| <span data-ttu-id="630f0-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-251">Range-Upper</span></span>            | <span data-ttu-id="630f0-252">255</span><span class="sxs-lookup"><span data-stu-id="630f0-252">255</span></span>                                        |
| <span data-ttu-id="630f0-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-253">Search-Flags</span></span>           | <span data-ttu-id="630f0-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-254">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-255">System-Flags</span></span>           | <span data-ttu-id="630f0-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-256">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-257">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-257">Classes used in</span></span>        | [<span data-ttu-id="630f0-258">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="630f0-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="630f0-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="630f0-260">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-260">Entry</span></span> | <span data-ttu-id="630f0-261">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-262">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-264">System-Only</span></span>            | <span data-ttu-id="630f0-265">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-265">False</span></span>                                      |
| <span data-ttu-id="630f0-266">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-266">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-267">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-267">False</span></span>                                      |
| <span data-ttu-id="630f0-268">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-268">Is Indexed</span></span>             | <span data-ttu-id="630f0-269">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-269">True</span></span>                                       |
| <span data-ttu-id="630f0-270">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-270">In Global Catalog</span></span>      | <span data-ttu-id="630f0-271">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-271">False</span></span>                                      |
| <span data-ttu-id="630f0-272">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-273">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-274">Range-Lower</span></span>            | <span data-ttu-id="630f0-275">1</span><span class="sxs-lookup"><span data-stu-id="630f0-275">1</span></span>                                          |
| <span data-ttu-id="630f0-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-276">Range-Upper</span></span>            | <span data-ttu-id="630f0-277">255</span><span class="sxs-lookup"><span data-stu-id="630f0-277">255</span></span>                                        |
| <span data-ttu-id="630f0-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-278">Search-Flags</span></span>           | <span data-ttu-id="630f0-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-279">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-280">System-Flags</span></span>           | <span data-ttu-id="630f0-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-281">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-282">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-282">Classes used in</span></span>        | [<span data-ttu-id="630f0-283">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="630f0-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="630f0-284">Windows Server 2012</span></span>



| <span data-ttu-id="630f0-285">Voce</span><span class="sxs-lookup"><span data-stu-id="630f0-285">Entry</span></span> | <span data-ttu-id="630f0-286">Valore</span><span class="sxs-lookup"><span data-stu-id="630f0-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="630f0-287">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="630f0-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="630f0-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="630f0-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="630f0-289">System-Only</span></span>            | <span data-ttu-id="630f0-290">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-290">False</span></span>                                      |
| <span data-ttu-id="630f0-291">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="630f0-291">Is-Single-Valued</span></span>       | <span data-ttu-id="630f0-292">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-292">False</span></span>                                      |
| <span data-ttu-id="630f0-293">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="630f0-293">Is Indexed</span></span>             | <span data-ttu-id="630f0-294">Vero</span><span class="sxs-lookup"><span data-stu-id="630f0-294">True</span></span>                                       |
| <span data-ttu-id="630f0-295">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="630f0-295">In Global Catalog</span></span>      | <span data-ttu-id="630f0-296">Falso</span><span class="sxs-lookup"><span data-stu-id="630f0-296">False</span></span>                                      |
| <span data-ttu-id="630f0-297">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="630f0-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="630f0-298">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="630f0-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="630f0-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="630f0-299">Range-Lower</span></span>            | <span data-ttu-id="630f0-300">1</span><span class="sxs-lookup"><span data-stu-id="630f0-300">1</span></span>                                          |
| <span data-ttu-id="630f0-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="630f0-301">Range-Upper</span></span>            | <span data-ttu-id="630f0-302">255</span><span class="sxs-lookup"><span data-stu-id="630f0-302">255</span></span>                                        |
| <span data-ttu-id="630f0-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-303">Search-Flags</span></span>           | <span data-ttu-id="630f0-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="630f0-304">0x00000001</span></span>                                 |
| <span data-ttu-id="630f0-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="630f0-305">System-Flags</span></span>           | <span data-ttu-id="630f0-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="630f0-306">0x00000010</span></span>                                 |
| <span data-ttu-id="630f0-307">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="630f0-307">Classes used in</span></span>        | [<span data-ttu-id="630f0-308">**Riferimento incrociato**</span><span class="sxs-lookup"><span data-stu-id="630f0-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





