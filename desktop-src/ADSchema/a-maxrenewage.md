---
title: Attributo max-Renew-Age
description: Questo attributo determina il periodo di tempo, in giorni, durante il quale il ticket di concessione ticket (TGT) di un utente può essere rinnovato per finalità di autenticazione Kerberos. L'impostazione predefinita è 7 giorni nell'oggetto Criteri di gruppo dominio predefinito (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo max-Renew-Age
- Schema AD dell'attributo maxRenewAge
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302998"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="078fc-106">Attributo max-Renew-Age</span><span class="sxs-lookup"><span data-stu-id="078fc-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="078fc-107">Questo attributo determina il periodo di tempo, in giorni, durante il quale il ticket di concessione ticket (TGT) di un utente può essere rinnovato per finalità di autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="078fc-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="078fc-108">L'impostazione predefinita è 7 giorni nell'oggetto Criteri di gruppo dominio predefinito (GPO).</span><span class="sxs-lookup"><span data-stu-id="078fc-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="078fc-109">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-109">Entry</span></span> | <span data-ttu-id="078fc-110">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="078fc-111">CN</span><span class="sxs-lookup"><span data-stu-id="078fc-111">CN</span></span>                | <span data-ttu-id="078fc-112">Max-rinnovo-Age</span><span class="sxs-lookup"><span data-stu-id="078fc-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="078fc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="078fc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="078fc-114">maxRenewAge</span><span class="sxs-lookup"><span data-stu-id="078fc-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="078fc-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="078fc-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="078fc-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="078fc-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="078fc-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="078fc-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="078fc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-118">Attribute-Id</span></span>      | <span data-ttu-id="078fc-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="078fc-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="078fc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="078fc-120">System-Id-Guid</span></span>    | <span data-ttu-id="078fc-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="078fc-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="078fc-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="078fc-122">Syntax</span></span>            | [<span data-ttu-id="078fc-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="078fc-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="078fc-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="078fc-124">Implementations</span></span>

-   [<span data-ttu-id="078fc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="078fc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="078fc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="078fc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="078fc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="078fc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="078fc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="078fc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="078fc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="078fc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="078fc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="078fc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="078fc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="078fc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="078fc-132">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-132">Entry</span></span> | <span data-ttu-id="078fc-133">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="078fc-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="078fc-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="078fc-136">System-Only</span></span>            | <span data-ttu-id="078fc-137">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-137">False</span></span>                                              |
| <span data-ttu-id="078fc-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="078fc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="078fc-139">Vero</span><span class="sxs-lookup"><span data-stu-id="078fc-139">True</span></span>                                               |
| <span data-ttu-id="078fc-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="078fc-140">Is Indexed</span></span>             | <span data-ttu-id="078fc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-141">False</span></span>                                              |
| <span data-ttu-id="078fc-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="078fc-142">In Global Catalog</span></span>      | <span data-ttu-id="078fc-143">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-143">False</span></span>                                              |
| <span data-ttu-id="078fc-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="078fc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="078fc-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="078fc-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="078fc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="078fc-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="078fc-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-148">Search-Flags</span></span>           | <span data-ttu-id="078fc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="078fc-149">0x00000000</span></span>                                         |
| <span data-ttu-id="078fc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-150">System-Flags</span></span>           | <span data-ttu-id="078fc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="078fc-151">0x00000010</span></span>                                         |
| <span data-ttu-id="078fc-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="078fc-152">Classes used in</span></span>        | [<span data-ttu-id="078fc-153">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="078fc-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="078fc-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="078fc-154">Windows Server 2003</span></span>



| <span data-ttu-id="078fc-155">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-155">Entry</span></span> | <span data-ttu-id="078fc-156">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="078fc-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="078fc-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="078fc-159">System-Only</span></span>            | <span data-ttu-id="078fc-160">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-160">False</span></span>                                              |
| <span data-ttu-id="078fc-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="078fc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="078fc-162">Vero</span><span class="sxs-lookup"><span data-stu-id="078fc-162">True</span></span>                                               |
| <span data-ttu-id="078fc-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="078fc-163">Is Indexed</span></span>             | <span data-ttu-id="078fc-164">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-164">False</span></span>                                              |
| <span data-ttu-id="078fc-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="078fc-165">In Global Catalog</span></span>      | <span data-ttu-id="078fc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-166">False</span></span>                                              |
| <span data-ttu-id="078fc-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="078fc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="078fc-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="078fc-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="078fc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="078fc-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="078fc-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-171">Search-Flags</span></span>           | <span data-ttu-id="078fc-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="078fc-172">0x00000000</span></span>                                         |
| <span data-ttu-id="078fc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-173">System-Flags</span></span>           | <span data-ttu-id="078fc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="078fc-174">0x00000010</span></span>                                         |
| <span data-ttu-id="078fc-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="078fc-175">Classes used in</span></span>        | [<span data-ttu-id="078fc-176">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="078fc-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="078fc-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="078fc-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="078fc-178">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-178">Entry</span></span> | <span data-ttu-id="078fc-179">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="078fc-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="078fc-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="078fc-182">System-Only</span></span>            | <span data-ttu-id="078fc-183">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-183">False</span></span>                                              |
| <span data-ttu-id="078fc-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="078fc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="078fc-185">Vero</span><span class="sxs-lookup"><span data-stu-id="078fc-185">True</span></span>                                               |
| <span data-ttu-id="078fc-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="078fc-186">Is Indexed</span></span>             | <span data-ttu-id="078fc-187">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-187">False</span></span>                                              |
| <span data-ttu-id="078fc-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="078fc-188">In Global Catalog</span></span>      | <span data-ttu-id="078fc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-189">False</span></span>                                              |
| <span data-ttu-id="078fc-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="078fc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="078fc-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="078fc-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="078fc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="078fc-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="078fc-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-194">Search-Flags</span></span>           | <span data-ttu-id="078fc-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="078fc-195">0x00000000</span></span>                                         |
| <span data-ttu-id="078fc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-196">System-Flags</span></span>           | <span data-ttu-id="078fc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="078fc-197">0x00000010</span></span>                                         |
| <span data-ttu-id="078fc-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="078fc-198">Classes used in</span></span>        | [<span data-ttu-id="078fc-199">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="078fc-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="078fc-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="078fc-200">Windows Server 2008</span></span>



| <span data-ttu-id="078fc-201">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-201">Entry</span></span> | <span data-ttu-id="078fc-202">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="078fc-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="078fc-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="078fc-205">System-Only</span></span>            | <span data-ttu-id="078fc-206">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-206">False</span></span>                                              |
| <span data-ttu-id="078fc-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="078fc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="078fc-208">Vero</span><span class="sxs-lookup"><span data-stu-id="078fc-208">True</span></span>                                               |
| <span data-ttu-id="078fc-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="078fc-209">Is Indexed</span></span>             | <span data-ttu-id="078fc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-210">False</span></span>                                              |
| <span data-ttu-id="078fc-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="078fc-211">In Global Catalog</span></span>      | <span data-ttu-id="078fc-212">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-212">False</span></span>                                              |
| <span data-ttu-id="078fc-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="078fc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="078fc-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="078fc-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="078fc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="078fc-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="078fc-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-217">Search-Flags</span></span>           | <span data-ttu-id="078fc-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="078fc-218">0x00000000</span></span>                                         |
| <span data-ttu-id="078fc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-219">System-Flags</span></span>           | <span data-ttu-id="078fc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="078fc-220">0x00000010</span></span>                                         |
| <span data-ttu-id="078fc-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="078fc-221">Classes used in</span></span>        | [<span data-ttu-id="078fc-222">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="078fc-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="078fc-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="078fc-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="078fc-224">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-224">Entry</span></span> | <span data-ttu-id="078fc-225">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="078fc-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="078fc-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="078fc-228">System-Only</span></span>            | <span data-ttu-id="078fc-229">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-229">False</span></span>                                              |
| <span data-ttu-id="078fc-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="078fc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="078fc-231">Vero</span><span class="sxs-lookup"><span data-stu-id="078fc-231">True</span></span>                                               |
| <span data-ttu-id="078fc-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="078fc-232">Is Indexed</span></span>             | <span data-ttu-id="078fc-233">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-233">False</span></span>                                              |
| <span data-ttu-id="078fc-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="078fc-234">In Global Catalog</span></span>      | <span data-ttu-id="078fc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-235">False</span></span>                                              |
| <span data-ttu-id="078fc-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="078fc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="078fc-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="078fc-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="078fc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="078fc-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="078fc-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-240">Search-Flags</span></span>           | <span data-ttu-id="078fc-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="078fc-241">0x00000000</span></span>                                         |
| <span data-ttu-id="078fc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-242">System-Flags</span></span>           | <span data-ttu-id="078fc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="078fc-243">0x00000010</span></span>                                         |
| <span data-ttu-id="078fc-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="078fc-244">Classes used in</span></span>        | [<span data-ttu-id="078fc-245">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="078fc-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="078fc-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="078fc-246">Windows Server 2012</span></span>



| <span data-ttu-id="078fc-247">Voce</span><span class="sxs-lookup"><span data-stu-id="078fc-247">Entry</span></span> | <span data-ttu-id="078fc-248">Valore</span><span class="sxs-lookup"><span data-stu-id="078fc-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="078fc-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="078fc-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="078fc-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="078fc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="078fc-251">System-Only</span></span>            | <span data-ttu-id="078fc-252">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-252">False</span></span>                                              |
| <span data-ttu-id="078fc-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="078fc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="078fc-254">Vero</span><span class="sxs-lookup"><span data-stu-id="078fc-254">True</span></span>                                               |
| <span data-ttu-id="078fc-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="078fc-255">Is Indexed</span></span>             | <span data-ttu-id="078fc-256">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-256">False</span></span>                                              |
| <span data-ttu-id="078fc-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="078fc-257">In Global Catalog</span></span>      | <span data-ttu-id="078fc-258">Falso</span><span class="sxs-lookup"><span data-stu-id="078fc-258">False</span></span>                                              |
| <span data-ttu-id="078fc-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="078fc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="078fc-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="078fc-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="078fc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="078fc-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="078fc-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="078fc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-263">Search-Flags</span></span>           | <span data-ttu-id="078fc-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="078fc-264">0x00000000</span></span>                                         |
| <span data-ttu-id="078fc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="078fc-265">System-Flags</span></span>           | <span data-ttu-id="078fc-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="078fc-266">0x00000010</span></span>                                         |
| <span data-ttu-id="078fc-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="078fc-267">Classes used in</span></span>        | [<span data-ttu-id="078fc-268">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="078fc-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





