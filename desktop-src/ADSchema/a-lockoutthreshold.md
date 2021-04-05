---
title: Attributo Lockout-Threshold
description: Numero di tentativi di accesso non validi consentiti prima del blocco dell'account.
ms.assetid: c4dcbbb6-0680-45f3-9b0b-f9c4bbf2b349
ms.tgt_platform: multiple
keywords:
- Schema AD Lockout-Threshold attribute
- Schema AD dell'attributo lockoutThreshold
topic_type:
- apiref
api_name:
- Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345977055597c48d70e30a20ce9bfbc9f07f3929
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874957"
---
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="ba9b6-105">Attributo Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="ba9b6-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="ba9b6-106">Numero di tentativi di accesso non validi consentiti prima del blocco dell'account.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="ba9b6-107">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-107">Entry</span></span> | <span data-ttu-id="ba9b6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ba9b6-109">CN</span><span class="sxs-lookup"><span data-stu-id="ba9b6-109">CN</span></span>                | <span data-ttu-id="ba9b6-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="ba9b6-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="ba9b6-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ba9b6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ba9b6-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="ba9b6-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="ba9b6-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ba9b6-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ba9b6-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-114">Update Privilege</span></span>  | <span data-ttu-id="ba9b6-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="ba9b6-115">Domain administrator</span></span>                 |
| <span data-ttu-id="ba9b6-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ba9b6-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-117">Attribute-Id</span></span>      | <span data-ttu-id="ba9b6-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="ba9b6-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="ba9b6-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ba9b6-119">System-Id-Guid</span></span>    | <span data-ttu-id="ba9b6-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ba9b6-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ba9b6-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba9b6-121">Syntax</span></span>            | [<span data-ttu-id="ba9b6-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ba9b6-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ba9b6-123">Implementations</span></span>

-   [<span data-ttu-id="ba9b6-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ba9b6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ba9b6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ba9b6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ba9b6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ba9b6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ba9b6-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ba9b6-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ba9b6-131">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-131">Entry</span></span> | <span data-ttu-id="ba9b6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b6-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba9b6-135">System-Only</span></span>            | <span data-ttu-id="ba9b6-136">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba9b6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ba9b6-138">Vero</span><span class="sxs-lookup"><span data-stu-id="ba9b6-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba9b6-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba9b6-139">Is Indexed</span></span>             | <span data-ttu-id="ba9b6-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba9b6-141">In Global Catalog</span></span>      | <span data-ttu-id="ba9b6-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba9b6-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ba9b6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba9b6-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba9b6-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-147">Search-Flags</span></span>           | <span data-ttu-id="ba9b6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba9b6-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-149">System-Flags</span></span>           | <span data-ttu-id="ba9b6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba9b6-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba9b6-151">Classes used in</span></span>        | [<span data-ttu-id="ba9b6-152">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ba9b6-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ba9b6-154">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ba9b6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba9b6-155">Windows Server 2003</span></span>



| <span data-ttu-id="ba9b6-156">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-156">Entry</span></span> | <span data-ttu-id="ba9b6-157">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b6-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba9b6-160">System-Only</span></span>            | <span data-ttu-id="ba9b6-161">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba9b6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ba9b6-163">Vero</span><span class="sxs-lookup"><span data-stu-id="ba9b6-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba9b6-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba9b6-164">Is Indexed</span></span>             | <span data-ttu-id="ba9b6-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba9b6-166">In Global Catalog</span></span>      | <span data-ttu-id="ba9b6-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba9b6-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ba9b6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba9b6-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba9b6-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-172">Search-Flags</span></span>           | <span data-ttu-id="ba9b6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba9b6-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-174">System-Flags</span></span>           | <span data-ttu-id="ba9b6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba9b6-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba9b6-176">Classes used in</span></span>        | [<span data-ttu-id="ba9b6-177">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ba9b6-178">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ba9b6-179">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ba9b6-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ba9b6-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ba9b6-181">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-181">Entry</span></span> | <span data-ttu-id="ba9b6-182">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b6-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba9b6-185">System-Only</span></span>            | <span data-ttu-id="ba9b6-186">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba9b6-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ba9b6-188">Vero</span><span class="sxs-lookup"><span data-stu-id="ba9b6-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba9b6-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba9b6-189">Is Indexed</span></span>             | <span data-ttu-id="ba9b6-190">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba9b6-191">In Global Catalog</span></span>      | <span data-ttu-id="ba9b6-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba9b6-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ba9b6-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba9b6-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba9b6-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-197">Search-Flags</span></span>           | <span data-ttu-id="ba9b6-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba9b6-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-199">System-Flags</span></span>           | <span data-ttu-id="ba9b6-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba9b6-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba9b6-201">Classes used in</span></span>        | [<span data-ttu-id="ba9b6-202">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ba9b6-203">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ba9b6-204">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ba9b6-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba9b6-205">Windows Server 2008</span></span>



| <span data-ttu-id="ba9b6-206">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-206">Entry</span></span> | <span data-ttu-id="ba9b6-207">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b6-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba9b6-210">System-Only</span></span>            | <span data-ttu-id="ba9b6-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba9b6-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ba9b6-213">Vero</span><span class="sxs-lookup"><span data-stu-id="ba9b6-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba9b6-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba9b6-214">Is Indexed</span></span>             | <span data-ttu-id="ba9b6-215">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba9b6-216">In Global Catalog</span></span>      | <span data-ttu-id="ba9b6-217">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba9b6-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ba9b6-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba9b6-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba9b6-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-222">Search-Flags</span></span>           | <span data-ttu-id="ba9b6-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba9b6-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-224">System-Flags</span></span>           | <span data-ttu-id="ba9b6-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba9b6-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba9b6-226">Classes used in</span></span>        | [<span data-ttu-id="ba9b6-227">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ba9b6-228">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ba9b6-229">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ba9b6-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba9b6-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ba9b6-231">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-231">Entry</span></span> | <span data-ttu-id="ba9b6-232">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b6-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba9b6-235">System-Only</span></span>            | <span data-ttu-id="ba9b6-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba9b6-237">Is-Single-Valued</span></span>       | <span data-ttu-id="ba9b6-238">Vero</span><span class="sxs-lookup"><span data-stu-id="ba9b6-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba9b6-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba9b6-239">Is Indexed</span></span>             | <span data-ttu-id="ba9b6-240">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba9b6-241">In Global Catalog</span></span>      | <span data-ttu-id="ba9b6-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba9b6-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ba9b6-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba9b6-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba9b6-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-247">Search-Flags</span></span>           | <span data-ttu-id="ba9b6-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba9b6-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-249">System-Flags</span></span>           | <span data-ttu-id="ba9b6-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba9b6-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-251">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba9b6-251">Classes used in</span></span>        | [<span data-ttu-id="ba9b6-252">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ba9b6-253">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ba9b6-254">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ba9b6-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba9b6-255">Windows Server 2012</span></span>



| <span data-ttu-id="ba9b6-256">Voce</span><span class="sxs-lookup"><span data-stu-id="ba9b6-256">Entry</span></span> | <span data-ttu-id="ba9b6-257">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b6-258">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ba9b6-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ba9b6-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="ba9b6-260">System-Only</span></span>            | <span data-ttu-id="ba9b6-261">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ba9b6-262">Is-Single-Valued</span></span>       | <span data-ttu-id="ba9b6-263">Vero</span><span class="sxs-lookup"><span data-stu-id="ba9b6-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="ba9b6-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ba9b6-264">Is Indexed</span></span>             | <span data-ttu-id="ba9b6-265">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ba9b6-266">In Global Catalog</span></span>      | <span data-ttu-id="ba9b6-267">Falso</span><span class="sxs-lookup"><span data-stu-id="ba9b6-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="ba9b6-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ba9b6-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="ba9b6-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="ba9b6-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ba9b6-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ba9b6-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="ba9b6-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-272">Search-Flags</span></span>           | <span data-ttu-id="ba9b6-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ba9b6-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ba9b6-274">System-Flags</span></span>           | <span data-ttu-id="ba9b6-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ba9b6-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="ba9b6-276">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ba9b6-276">Classes used in</span></span>        | [<span data-ttu-id="ba9b6-277">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="ba9b6-278">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="ba9b6-279">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="ba9b6-280">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba9b6-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba9b6-281">**Blocco-durata**</span><span class="sxs-lookup"><span data-stu-id="ba9b6-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





