---
title: Attributo Server-State
description: Indica se il server è abilitato o disabilitato.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Schema AD Server-State attribute
- Schema AD dell'attributo serverState
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303126"
---
# <a name="server-state-attribute"></a><span data-ttu-id="b68b0-105">Attributo Server-State</span><span class="sxs-lookup"><span data-stu-id="b68b0-105">Server-State attribute</span></span>

<span data-ttu-id="b68b0-106">Indica se il server è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b68b0-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="b68b0-107">Il valore 1 indica che il server è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b68b0-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="b68b0-108">Il valore 2 indica che il server è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b68b0-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="b68b0-109">Tutti gli altri valori non sono validi.</span><span class="sxs-lookup"><span data-stu-id="b68b0-109">All other values are invalid.</span></span>



| <span data-ttu-id="b68b0-110">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-110">Entry</span></span> | <span data-ttu-id="b68b0-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b68b0-112">CN</span><span class="sxs-lookup"><span data-stu-id="b68b0-112">CN</span></span>                | <span data-ttu-id="b68b0-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="b68b0-113">Server-State</span></span>                         |
| <span data-ttu-id="b68b0-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b68b0-114">Ldap-Display-Name</span></span> | <span data-ttu-id="b68b0-115">serverState</span><span class="sxs-lookup"><span data-stu-id="b68b0-115">serverState</span></span>                          |
| <span data-ttu-id="b68b0-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b68b0-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="b68b0-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-117">Update Privilege</span></span>  | <span data-ttu-id="b68b0-118">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b68b0-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="b68b0-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-119">Update Frequency</span></span>  | <span data-ttu-id="b68b0-120">Quando vengono modificati i criteri di un utente.</span><span class="sxs-lookup"><span data-stu-id="b68b0-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="b68b0-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-121">Attribute-Id</span></span>      | <span data-ttu-id="b68b0-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="b68b0-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="b68b0-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b68b0-123">System-Id-Guid</span></span>    | <span data-ttu-id="b68b0-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b68b0-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b68b0-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b68b0-125">Syntax</span></span>            | [<span data-ttu-id="b68b0-126">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="b68b0-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b68b0-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b68b0-127">Implementations</span></span>

-   [<span data-ttu-id="b68b0-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b68b0-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b68b0-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b68b0-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b68b0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b68b0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b68b0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b68b0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b68b0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b68b0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b68b0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b68b0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b68b0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b68b0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b68b0-135">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-135">Entry</span></span> | <span data-ttu-id="b68b0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b68b0-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68b0-139">System-Only</span></span>            | <span data-ttu-id="b68b0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-140">False</span></span>                                                 |
| <span data-ttu-id="b68b0-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b68b0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b68b0-142">Vero</span><span class="sxs-lookup"><span data-stu-id="b68b0-142">True</span></span>                                                  |
| <span data-ttu-id="b68b0-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b68b0-143">Is Indexed</span></span>             | <span data-ttu-id="b68b0-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-144">False</span></span>                                                 |
| <span data-ttu-id="b68b0-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b68b0-145">In Global Catalog</span></span>      | <span data-ttu-id="b68b0-146">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-146">False</span></span>                                                 |
| <span data-ttu-id="b68b0-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b68b0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68b0-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b68b0-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b68b0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68b0-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68b0-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-151">Search-Flags</span></span>           | <span data-ttu-id="b68b0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68b0-152">0x00000000</span></span>                                            |
| <span data-ttu-id="b68b0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-153">System-Flags</span></span>           | <span data-ttu-id="b68b0-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b68b0-154">0x00000011</span></span>                                            |
| <span data-ttu-id="b68b0-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b68b0-155">Classes used in</span></span>        | [<span data-ttu-id="b68b0-156">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b68b0-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b68b0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b68b0-157">Windows Server 2003</span></span>



| <span data-ttu-id="b68b0-158">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-158">Entry</span></span> | <span data-ttu-id="b68b0-159">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b68b0-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68b0-162">System-Only</span></span>            | <span data-ttu-id="b68b0-163">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-163">False</span></span>                                                 |
| <span data-ttu-id="b68b0-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b68b0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b68b0-165">Vero</span><span class="sxs-lookup"><span data-stu-id="b68b0-165">True</span></span>                                                  |
| <span data-ttu-id="b68b0-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b68b0-166">Is Indexed</span></span>             | <span data-ttu-id="b68b0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-167">False</span></span>                                                 |
| <span data-ttu-id="b68b0-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b68b0-168">In Global Catalog</span></span>      | <span data-ttu-id="b68b0-169">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-169">False</span></span>                                                 |
| <span data-ttu-id="b68b0-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b68b0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68b0-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b68b0-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b68b0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68b0-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68b0-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-174">Search-Flags</span></span>           | <span data-ttu-id="b68b0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68b0-175">0x00000000</span></span>                                            |
| <span data-ttu-id="b68b0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-176">System-Flags</span></span>           | <span data-ttu-id="b68b0-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b68b0-177">0x00000011</span></span>                                            |
| <span data-ttu-id="b68b0-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b68b0-178">Classes used in</span></span>        | [<span data-ttu-id="b68b0-179">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b68b0-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b68b0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b68b0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b68b0-181">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-181">Entry</span></span> | <span data-ttu-id="b68b0-182">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b68b0-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68b0-185">System-Only</span></span>            | <span data-ttu-id="b68b0-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-186">False</span></span>                                                 |
| <span data-ttu-id="b68b0-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b68b0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b68b0-188">Vero</span><span class="sxs-lookup"><span data-stu-id="b68b0-188">True</span></span>                                                  |
| <span data-ttu-id="b68b0-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b68b0-189">Is Indexed</span></span>             | <span data-ttu-id="b68b0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-190">False</span></span>                                                 |
| <span data-ttu-id="b68b0-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b68b0-191">In Global Catalog</span></span>      | <span data-ttu-id="b68b0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-192">False</span></span>                                                 |
| <span data-ttu-id="b68b0-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b68b0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68b0-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b68b0-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b68b0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68b0-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68b0-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-197">Search-Flags</span></span>           | <span data-ttu-id="b68b0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68b0-198">0x00000000</span></span>                                            |
| <span data-ttu-id="b68b0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-199">System-Flags</span></span>           | <span data-ttu-id="b68b0-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b68b0-200">0x00000011</span></span>                                            |
| <span data-ttu-id="b68b0-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b68b0-201">Classes used in</span></span>        | [<span data-ttu-id="b68b0-202">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b68b0-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b68b0-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b68b0-203">Windows Server 2008</span></span>



| <span data-ttu-id="b68b0-204">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-204">Entry</span></span> | <span data-ttu-id="b68b0-205">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b68b0-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68b0-208">System-Only</span></span>            | <span data-ttu-id="b68b0-209">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-209">False</span></span>                                                 |
| <span data-ttu-id="b68b0-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b68b0-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b68b0-211">Vero</span><span class="sxs-lookup"><span data-stu-id="b68b0-211">True</span></span>                                                  |
| <span data-ttu-id="b68b0-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b68b0-212">Is Indexed</span></span>             | <span data-ttu-id="b68b0-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-213">False</span></span>                                                 |
| <span data-ttu-id="b68b0-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b68b0-214">In Global Catalog</span></span>      | <span data-ttu-id="b68b0-215">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-215">False</span></span>                                                 |
| <span data-ttu-id="b68b0-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b68b0-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68b0-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b68b0-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b68b0-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68b0-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68b0-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-220">Search-Flags</span></span>           | <span data-ttu-id="b68b0-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68b0-221">0x00000000</span></span>                                            |
| <span data-ttu-id="b68b0-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-222">System-Flags</span></span>           | <span data-ttu-id="b68b0-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b68b0-223">0x00000011</span></span>                                            |
| <span data-ttu-id="b68b0-224">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b68b0-224">Classes used in</span></span>        | [<span data-ttu-id="b68b0-225">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b68b0-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b68b0-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b68b0-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b68b0-227">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-227">Entry</span></span> | <span data-ttu-id="b68b0-228">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b68b0-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68b0-231">System-Only</span></span>            | <span data-ttu-id="b68b0-232">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-232">False</span></span>                                                 |
| <span data-ttu-id="b68b0-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b68b0-233">Is-Single-Valued</span></span>       | <span data-ttu-id="b68b0-234">Vero</span><span class="sxs-lookup"><span data-stu-id="b68b0-234">True</span></span>                                                  |
| <span data-ttu-id="b68b0-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b68b0-235">Is Indexed</span></span>             | <span data-ttu-id="b68b0-236">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-236">False</span></span>                                                 |
| <span data-ttu-id="b68b0-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b68b0-237">In Global Catalog</span></span>      | <span data-ttu-id="b68b0-238">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-238">False</span></span>                                                 |
| <span data-ttu-id="b68b0-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b68b0-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68b0-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b68b0-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b68b0-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68b0-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68b0-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-243">Search-Flags</span></span>           | <span data-ttu-id="b68b0-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68b0-244">0x00000000</span></span>                                            |
| <span data-ttu-id="b68b0-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-245">System-Flags</span></span>           | <span data-ttu-id="b68b0-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b68b0-246">0x00000011</span></span>                                            |
| <span data-ttu-id="b68b0-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b68b0-247">Classes used in</span></span>        | [<span data-ttu-id="b68b0-248">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b68b0-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b68b0-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b68b0-249">Windows Server 2012</span></span>



| <span data-ttu-id="b68b0-250">Voce</span><span class="sxs-lookup"><span data-stu-id="b68b0-250">Entry</span></span> | <span data-ttu-id="b68b0-251">Valore</span><span class="sxs-lookup"><span data-stu-id="b68b0-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b68b0-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b68b0-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b68b0-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b68b0-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="b68b0-254">System-Only</span></span>            | <span data-ttu-id="b68b0-255">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-255">False</span></span>                                                 |
| <span data-ttu-id="b68b0-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b68b0-256">Is-Single-Valued</span></span>       | <span data-ttu-id="b68b0-257">Vero</span><span class="sxs-lookup"><span data-stu-id="b68b0-257">True</span></span>                                                  |
| <span data-ttu-id="b68b0-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b68b0-258">Is Indexed</span></span>             | <span data-ttu-id="b68b0-259">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-259">False</span></span>                                                 |
| <span data-ttu-id="b68b0-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b68b0-260">In Global Catalog</span></span>      | <span data-ttu-id="b68b0-261">Falso</span><span class="sxs-lookup"><span data-stu-id="b68b0-261">False</span></span>                                                 |
| <span data-ttu-id="b68b0-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b68b0-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="b68b0-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b68b0-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b68b0-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b68b0-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b68b0-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b68b0-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-266">Search-Flags</span></span>           | <span data-ttu-id="b68b0-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b68b0-267">0x00000000</span></span>                                            |
| <span data-ttu-id="b68b0-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b68b0-268">System-Flags</span></span>           | <span data-ttu-id="b68b0-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b68b0-269">0x00000011</span></span>                                            |
| <span data-ttu-id="b68b0-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b68b0-270">Classes used in</span></span>        | [<span data-ttu-id="b68b0-271">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b68b0-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





