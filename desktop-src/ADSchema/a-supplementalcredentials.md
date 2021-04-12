---
title: Attributo Supplemental-Credentials
description: Credenziali archiviate da utilizzare per l'autenticazione. Versione crittografata della password dell'utente. Questo attributo non è leggibile né scrivibile.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Schema AD Supplemental-Credentials attribute
- Schema AD dell'attributo supplementalCredentials
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519654"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="c39d5-107">Attributo Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="c39d5-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="c39d5-108">Credenziali archiviate da utilizzare per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c39d5-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="c39d5-109">Versione crittografata della password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c39d5-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="c39d5-110">Questo attributo non è leggibile né scrivibile.</span><span class="sxs-lookup"><span data-stu-id="c39d5-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="c39d5-111">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-111">Entry</span></span> | <span data-ttu-id="c39d5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c39d5-113">CN</span><span class="sxs-lookup"><span data-stu-id="c39d5-113">CN</span></span>                | <span data-ttu-id="c39d5-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="c39d5-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="c39d5-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c39d5-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c39d5-116">supplementalCredentials</span><span class="sxs-lookup"><span data-stu-id="c39d5-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="c39d5-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c39d5-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c39d5-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-118">Update Privilege</span></span>  | <span data-ttu-id="c39d5-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c39d5-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="c39d5-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-120">Update Frequency</span></span>  | <span data-ttu-id="c39d5-121">Quando la password dell'utente viene modificata.</span><span class="sxs-lookup"><span data-stu-id="c39d5-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="c39d5-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-122">Attribute-Id</span></span>      | <span data-ttu-id="c39d5-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="c39d5-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="c39d5-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c39d5-124">System-Id-Guid</span></span>    | <span data-ttu-id="c39d5-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c39d5-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="c39d5-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c39d5-126">Syntax</span></span>            | [<span data-ttu-id="c39d5-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="c39d5-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c39d5-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c39d5-128">Implementations</span></span>

-   [<span data-ttu-id="c39d5-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c39d5-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c39d5-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c39d5-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c39d5-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c39d5-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c39d5-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c39d5-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c39d5-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c39d5-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c39d5-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c39d5-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c39d5-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c39d5-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c39d5-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c39d5-136">Windows 2000 Server</span></span>



| <span data-ttu-id="c39d5-137">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-137">Entry</span></span> | <span data-ttu-id="c39d5-138">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-141">System-Only</span></span>            | <span data-ttu-id="c39d5-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-142">False</span></span>                                                        |
| <span data-ttu-id="c39d5-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-143">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-144">False</span></span>                                                        |
| <span data-ttu-id="c39d5-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-145">Is Indexed</span></span>             | <span data-ttu-id="c39d5-146">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-146">False</span></span>                                                        |
| <span data-ttu-id="c39d5-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-147">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-148">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-148">False</span></span>                                                        |
| <span data-ttu-id="c39d5-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-153">Search-Flags</span></span>           | <span data-ttu-id="c39d5-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-155">System-Flags</span></span>           | <span data-ttu-id="c39d5-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-157">Classes used in</span></span>        | [<span data-ttu-id="c39d5-158">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c39d5-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c39d5-159">Windows Server 2003</span></span>



| <span data-ttu-id="c39d5-160">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-160">Entry</span></span> | <span data-ttu-id="c39d5-161">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-164">System-Only</span></span>            | <span data-ttu-id="c39d5-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-165">False</span></span>                                                        |
| <span data-ttu-id="c39d5-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-167">False</span></span>                                                        |
| <span data-ttu-id="c39d5-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-168">Is Indexed</span></span>             | <span data-ttu-id="c39d5-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-169">False</span></span>                                                        |
| <span data-ttu-id="c39d5-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-170">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-171">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-171">False</span></span>                                                        |
| <span data-ttu-id="c39d5-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-176">Search-Flags</span></span>           | <span data-ttu-id="c39d5-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-178">System-Flags</span></span>           | <span data-ttu-id="c39d5-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-180">Classes used in</span></span>        | [<span data-ttu-id="c39d5-181">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c39d5-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="c39d5-182">ADAM</span></span>



| <span data-ttu-id="c39d5-183">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-183">Entry</span></span> | <span data-ttu-id="c39d5-184">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-187">System-Only</span></span>            | <span data-ttu-id="c39d5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-188">False</span></span>                                                        |
| <span data-ttu-id="c39d5-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-190">False</span></span>                                                        |
| <span data-ttu-id="c39d5-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-191">Is Indexed</span></span>             | <span data-ttu-id="c39d5-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-192">False</span></span>                                                        |
| <span data-ttu-id="c39d5-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-193">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-194">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-194">False</span></span>                                                        |
| <span data-ttu-id="c39d5-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-199">Search-Flags</span></span>           | <span data-ttu-id="c39d5-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-201">System-Flags</span></span>           | <span data-ttu-id="c39d5-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-203">Classes used in</span></span>        | [<span data-ttu-id="c39d5-204">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c39d5-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c39d5-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c39d5-206">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-206">Entry</span></span> | <span data-ttu-id="c39d5-207">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-210">System-Only</span></span>            | <span data-ttu-id="c39d5-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-211">False</span></span>                                                        |
| <span data-ttu-id="c39d5-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-213">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-213">False</span></span>                                                        |
| <span data-ttu-id="c39d5-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-214">Is Indexed</span></span>             | <span data-ttu-id="c39d5-215">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-215">False</span></span>                                                        |
| <span data-ttu-id="c39d5-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-216">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-217">False</span></span>                                                        |
| <span data-ttu-id="c39d5-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-222">Search-Flags</span></span>           | <span data-ttu-id="c39d5-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-224">System-Flags</span></span>           | <span data-ttu-id="c39d5-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-226">Classes used in</span></span>        | [<span data-ttu-id="c39d5-227">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c39d5-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c39d5-228">Windows Server 2008</span></span>



| <span data-ttu-id="c39d5-229">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-229">Entry</span></span> | <span data-ttu-id="c39d5-230">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-233">System-Only</span></span>            | <span data-ttu-id="c39d5-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-234">False</span></span>                                                        |
| <span data-ttu-id="c39d5-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-236">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-236">False</span></span>                                                        |
| <span data-ttu-id="c39d5-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-237">Is Indexed</span></span>             | <span data-ttu-id="c39d5-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-238">False</span></span>                                                        |
| <span data-ttu-id="c39d5-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-239">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-240">False</span></span>                                                        |
| <span data-ttu-id="c39d5-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-245">Search-Flags</span></span>           | <span data-ttu-id="c39d5-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-247">System-Flags</span></span>           | <span data-ttu-id="c39d5-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-249">Classes used in</span></span>        | [<span data-ttu-id="c39d5-250">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c39d5-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c39d5-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c39d5-252">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-252">Entry</span></span> | <span data-ttu-id="c39d5-253">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-256">System-Only</span></span>            | <span data-ttu-id="c39d5-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-257">False</span></span>                                                        |
| <span data-ttu-id="c39d5-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-258">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-259">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-259">False</span></span>                                                        |
| <span data-ttu-id="c39d5-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-260">Is Indexed</span></span>             | <span data-ttu-id="c39d5-261">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-261">False</span></span>                                                        |
| <span data-ttu-id="c39d5-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-262">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-263">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-263">False</span></span>                                                        |
| <span data-ttu-id="c39d5-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-268">Search-Flags</span></span>           | <span data-ttu-id="c39d5-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-270">System-Flags</span></span>           | <span data-ttu-id="c39d5-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-272">Classes used in</span></span>        | [<span data-ttu-id="c39d5-273">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c39d5-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c39d5-274">Windows Server 2012</span></span>



| <span data-ttu-id="c39d5-275">Voce</span><span class="sxs-lookup"><span data-stu-id="c39d5-275">Entry</span></span> | <span data-ttu-id="c39d5-276">Valore</span><span class="sxs-lookup"><span data-stu-id="c39d5-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c39d5-277">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c39d5-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c39d5-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c39d5-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="c39d5-279">System-Only</span></span>            | <span data-ttu-id="c39d5-280">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-280">False</span></span>                                                        |
| <span data-ttu-id="c39d5-281">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c39d5-281">Is-Single-Valued</span></span>       | <span data-ttu-id="c39d5-282">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-282">False</span></span>                                                        |
| <span data-ttu-id="c39d5-283">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c39d5-283">Is Indexed</span></span>             | <span data-ttu-id="c39d5-284">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-284">False</span></span>                                                        |
| <span data-ttu-id="c39d5-285">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c39d5-285">In Global Catalog</span></span>      | <span data-ttu-id="c39d5-286">Falso</span><span class="sxs-lookup"><span data-stu-id="c39d5-286">False</span></span>                                                        |
| <span data-ttu-id="c39d5-287">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c39d5-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="c39d5-288">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c39d5-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c39d5-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c39d5-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c39d5-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c39d5-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-291">Search-Flags</span></span>           | <span data-ttu-id="c39d5-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c39d5-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="c39d5-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c39d5-293">System-Flags</span></span>           | <span data-ttu-id="c39d5-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c39d5-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="c39d5-295">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c39d5-295">Classes used in</span></span>        | [<span data-ttu-id="c39d5-296">**Entità di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="c39d5-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





