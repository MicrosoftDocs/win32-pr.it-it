---
title: Attributo max-ticket-Age
description: Questo attributo determina la quantità massima di tempo, in ore, che un ticket di concessione ticket (TGT) di un utente può essere utilizzato per l'autenticazione Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo max-ticket-Age
- Schema AD dell'attributo maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744346"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="ddd21-105">Attributo max-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="ddd21-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="ddd21-106">Questo attributo determina la quantità massima di tempo, in ore, che un ticket di concessione ticket (TGT) di un utente può essere utilizzato per l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ddd21-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="ddd21-107">Quando il TGT di un utente scade, ne deve essere richiesto uno nuovo oppure è necessario rinnovarne uno esistente.</span><span class="sxs-lookup"><span data-stu-id="ddd21-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="ddd21-108">Per impostazione predefinita, questa impostazione è impostata su 10 ore nell'oggetto Criteri di gruppo dominio predefinito (GPO).</span><span class="sxs-lookup"><span data-stu-id="ddd21-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="ddd21-109">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-109">Entry</span></span> | <span data-ttu-id="ddd21-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ddd21-111">CN</span><span class="sxs-lookup"><span data-stu-id="ddd21-111">CN</span></span>                | <span data-ttu-id="ddd21-112">Numero massimo-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="ddd21-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="ddd21-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ddd21-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ddd21-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="ddd21-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="ddd21-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ddd21-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="ddd21-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ddd21-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ddd21-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-118">Attribute-Id</span></span>      | <span data-ttu-id="ddd21-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="ddd21-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="ddd21-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ddd21-120">System-Id-Guid</span></span>    | <span data-ttu-id="ddd21-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ddd21-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ddd21-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddd21-122">Syntax</span></span>            | [<span data-ttu-id="ddd21-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="ddd21-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ddd21-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ddd21-124">Implementations</span></span>

-   [<span data-ttu-id="ddd21-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ddd21-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ddd21-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ddd21-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ddd21-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ddd21-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ddd21-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ddd21-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ddd21-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ddd21-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ddd21-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ddd21-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ddd21-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddd21-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ddd21-132">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-132">Entry</span></span> | <span data-ttu-id="ddd21-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ddd21-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddd21-136">System-Only</span></span>            | <span data-ttu-id="ddd21-137">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-137">False</span></span>                                              |
| <span data-ttu-id="ddd21-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddd21-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ddd21-139">Vero</span><span class="sxs-lookup"><span data-stu-id="ddd21-139">True</span></span>                                               |
| <span data-ttu-id="ddd21-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddd21-140">Is Indexed</span></span>             | <span data-ttu-id="ddd21-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-141">False</span></span>                                              |
| <span data-ttu-id="ddd21-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddd21-142">In Global Catalog</span></span>      | <span data-ttu-id="ddd21-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-143">False</span></span>                                              |
| <span data-ttu-id="ddd21-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddd21-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddd21-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddd21-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ddd21-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddd21-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddd21-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-148">Search-Flags</span></span>           | <span data-ttu-id="ddd21-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddd21-149">0x00000000</span></span>                                         |
| <span data-ttu-id="ddd21-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-150">System-Flags</span></span>           | <span data-ttu-id="ddd21-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddd21-151">0x00000010</span></span>                                         |
| <span data-ttu-id="ddd21-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddd21-152">Classes used in</span></span>        | [<span data-ttu-id="ddd21-153">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ddd21-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ddd21-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddd21-154">Windows Server 2003</span></span>



| <span data-ttu-id="ddd21-155">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-155">Entry</span></span> | <span data-ttu-id="ddd21-156">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ddd21-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddd21-159">System-Only</span></span>            | <span data-ttu-id="ddd21-160">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-160">False</span></span>                                              |
| <span data-ttu-id="ddd21-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddd21-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ddd21-162">Vero</span><span class="sxs-lookup"><span data-stu-id="ddd21-162">True</span></span>                                               |
| <span data-ttu-id="ddd21-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddd21-163">Is Indexed</span></span>             | <span data-ttu-id="ddd21-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-164">False</span></span>                                              |
| <span data-ttu-id="ddd21-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddd21-165">In Global Catalog</span></span>      | <span data-ttu-id="ddd21-166">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-166">False</span></span>                                              |
| <span data-ttu-id="ddd21-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddd21-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddd21-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddd21-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ddd21-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddd21-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddd21-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-171">Search-Flags</span></span>           | <span data-ttu-id="ddd21-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddd21-172">0x00000000</span></span>                                         |
| <span data-ttu-id="ddd21-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-173">System-Flags</span></span>           | <span data-ttu-id="ddd21-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddd21-174">0x00000010</span></span>                                         |
| <span data-ttu-id="ddd21-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddd21-175">Classes used in</span></span>        | [<span data-ttu-id="ddd21-176">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ddd21-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ddd21-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ddd21-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ddd21-178">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-178">Entry</span></span> | <span data-ttu-id="ddd21-179">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ddd21-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddd21-182">System-Only</span></span>            | <span data-ttu-id="ddd21-183">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-183">False</span></span>                                              |
| <span data-ttu-id="ddd21-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddd21-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ddd21-185">Vero</span><span class="sxs-lookup"><span data-stu-id="ddd21-185">True</span></span>                                               |
| <span data-ttu-id="ddd21-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddd21-186">Is Indexed</span></span>             | <span data-ttu-id="ddd21-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-187">False</span></span>                                              |
| <span data-ttu-id="ddd21-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddd21-188">In Global Catalog</span></span>      | <span data-ttu-id="ddd21-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-189">False</span></span>                                              |
| <span data-ttu-id="ddd21-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddd21-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddd21-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddd21-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ddd21-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddd21-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddd21-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-194">Search-Flags</span></span>           | <span data-ttu-id="ddd21-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddd21-195">0x00000000</span></span>                                         |
| <span data-ttu-id="ddd21-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-196">System-Flags</span></span>           | <span data-ttu-id="ddd21-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddd21-197">0x00000010</span></span>                                         |
| <span data-ttu-id="ddd21-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddd21-198">Classes used in</span></span>        | [<span data-ttu-id="ddd21-199">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ddd21-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ddd21-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddd21-200">Windows Server 2008</span></span>



| <span data-ttu-id="ddd21-201">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-201">Entry</span></span> | <span data-ttu-id="ddd21-202">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ddd21-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddd21-205">System-Only</span></span>            | <span data-ttu-id="ddd21-206">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-206">False</span></span>                                              |
| <span data-ttu-id="ddd21-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddd21-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ddd21-208">Vero</span><span class="sxs-lookup"><span data-stu-id="ddd21-208">True</span></span>                                               |
| <span data-ttu-id="ddd21-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddd21-209">Is Indexed</span></span>             | <span data-ttu-id="ddd21-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-210">False</span></span>                                              |
| <span data-ttu-id="ddd21-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddd21-211">In Global Catalog</span></span>      | <span data-ttu-id="ddd21-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-212">False</span></span>                                              |
| <span data-ttu-id="ddd21-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddd21-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddd21-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddd21-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ddd21-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddd21-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddd21-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-217">Search-Flags</span></span>           | <span data-ttu-id="ddd21-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddd21-218">0x00000000</span></span>                                         |
| <span data-ttu-id="ddd21-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-219">System-Flags</span></span>           | <span data-ttu-id="ddd21-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddd21-220">0x00000010</span></span>                                         |
| <span data-ttu-id="ddd21-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddd21-221">Classes used in</span></span>        | [<span data-ttu-id="ddd21-222">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ddd21-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ddd21-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ddd21-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ddd21-224">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-224">Entry</span></span> | <span data-ttu-id="ddd21-225">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ddd21-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddd21-228">System-Only</span></span>            | <span data-ttu-id="ddd21-229">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-229">False</span></span>                                              |
| <span data-ttu-id="ddd21-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddd21-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ddd21-231">Vero</span><span class="sxs-lookup"><span data-stu-id="ddd21-231">True</span></span>                                               |
| <span data-ttu-id="ddd21-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddd21-232">Is Indexed</span></span>             | <span data-ttu-id="ddd21-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-233">False</span></span>                                              |
| <span data-ttu-id="ddd21-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddd21-234">In Global Catalog</span></span>      | <span data-ttu-id="ddd21-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-235">False</span></span>                                              |
| <span data-ttu-id="ddd21-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddd21-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddd21-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddd21-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ddd21-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddd21-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddd21-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-240">Search-Flags</span></span>           | <span data-ttu-id="ddd21-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddd21-241">0x00000000</span></span>                                         |
| <span data-ttu-id="ddd21-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-242">System-Flags</span></span>           | <span data-ttu-id="ddd21-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddd21-243">0x00000010</span></span>                                         |
| <span data-ttu-id="ddd21-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddd21-244">Classes used in</span></span>        | [<span data-ttu-id="ddd21-245">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ddd21-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ddd21-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddd21-246">Windows Server 2012</span></span>



| <span data-ttu-id="ddd21-247">Voce</span><span class="sxs-lookup"><span data-stu-id="ddd21-247">Entry</span></span> | <span data-ttu-id="ddd21-248">Valore</span><span class="sxs-lookup"><span data-stu-id="ddd21-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ddd21-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddd21-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddd21-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ddd21-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddd21-251">System-Only</span></span>            | <span data-ttu-id="ddd21-252">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-252">False</span></span>                                              |
| <span data-ttu-id="ddd21-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddd21-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ddd21-254">Vero</span><span class="sxs-lookup"><span data-stu-id="ddd21-254">True</span></span>                                               |
| <span data-ttu-id="ddd21-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddd21-255">Is Indexed</span></span>             | <span data-ttu-id="ddd21-256">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-256">False</span></span>                                              |
| <span data-ttu-id="ddd21-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddd21-257">In Global Catalog</span></span>      | <span data-ttu-id="ddd21-258">Falso</span><span class="sxs-lookup"><span data-stu-id="ddd21-258">False</span></span>                                              |
| <span data-ttu-id="ddd21-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddd21-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddd21-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddd21-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ddd21-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddd21-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddd21-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ddd21-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-263">Search-Flags</span></span>           | <span data-ttu-id="ddd21-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddd21-264">0x00000000</span></span>                                         |
| <span data-ttu-id="ddd21-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddd21-265">System-Flags</span></span>           | <span data-ttu-id="ddd21-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddd21-266">0x00000010</span></span>                                         |
| <span data-ttu-id="ddd21-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddd21-267">Classes used in</span></span>        | [<span data-ttu-id="ddd21-268">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="ddd21-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





