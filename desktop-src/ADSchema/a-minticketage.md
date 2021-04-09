---
title: Attributo min-ticket-Age
description: Questo attributo determina il periodo di tempo minimo, in ore, per cui un ticket di concessione ticket (TGT) di un utente può essere utilizzato per l'autenticazione Kerberos prima che sia possibile effettuare una richiesta per rinnovare il ticket.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo min-ticket-Age
- Schema AD dell'attributo minTicketAge
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122118"
---
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="5a6ad-105">Attributo min-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="5a6ad-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="5a6ad-106">Questo attributo determina il periodo di tempo minimo, in ore, per cui un ticket di concessione ticket (TGT) di un utente può essere utilizzato per l'autenticazione Kerberos prima che sia possibile effettuare una richiesta per rinnovare il ticket.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="5a6ad-107">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-107">Entry</span></span> | <span data-ttu-id="5a6ad-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5a6ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="5a6ad-109">CN</span></span>                | <span data-ttu-id="5a6ad-110">Min-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="5a6ad-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="5a6ad-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5a6ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5a6ad-112">minTicketAge</span><span class="sxs-lookup"><span data-stu-id="5a6ad-112">minTicketAge</span></span>                         |
| <span data-ttu-id="5a6ad-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5a6ad-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="5a6ad-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5a6ad-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5a6ad-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-116">Attribute-Id</span></span>      | <span data-ttu-id="5a6ad-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="5a6ad-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="5a6ad-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5a6ad-118">System-Id-Guid</span></span>    | <span data-ttu-id="5a6ad-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5a6ad-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5a6ad-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a6ad-120">Syntax</span></span>            | [<span data-ttu-id="5a6ad-121">**Interval**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5a6ad-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="5a6ad-122">Implementations</span></span>

-   [<span data-ttu-id="5a6ad-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5a6ad-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5a6ad-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5a6ad-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5a6ad-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5a6ad-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5a6ad-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a6ad-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5a6ad-130">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-130">Entry</span></span> | <span data-ttu-id="5a6ad-131">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5a6ad-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a6ad-134">System-Only</span></span>            | <span data-ttu-id="5a6ad-135">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-135">False</span></span>                                              |
| <span data-ttu-id="5a6ad-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5a6ad-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5a6ad-137">Vero</span><span class="sxs-lookup"><span data-stu-id="5a6ad-137">True</span></span>                                               |
| <span data-ttu-id="5a6ad-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5a6ad-138">Is Indexed</span></span>             | <span data-ttu-id="5a6ad-139">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-139">False</span></span>                                              |
| <span data-ttu-id="5a6ad-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5a6ad-140">In Global Catalog</span></span>      | <span data-ttu-id="5a6ad-141">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-141">False</span></span>                                              |
| <span data-ttu-id="5a6ad-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a6ad-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5a6ad-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5a6ad-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a6ad-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a6ad-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-146">Search-Flags</span></span>           | <span data-ttu-id="5a6ad-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a6ad-147">0x00000000</span></span>                                         |
| <span data-ttu-id="5a6ad-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-148">System-Flags</span></span>           | <span data-ttu-id="5a6ad-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a6ad-149">0x00000010</span></span>                                         |
| <span data-ttu-id="5a6ad-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5a6ad-150">Classes used in</span></span>        | [<span data-ttu-id="5a6ad-151">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5a6ad-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a6ad-152">Windows Server 2003</span></span>



| <span data-ttu-id="5a6ad-153">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-153">Entry</span></span> | <span data-ttu-id="5a6ad-154">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5a6ad-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a6ad-157">System-Only</span></span>            | <span data-ttu-id="5a6ad-158">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-158">False</span></span>                                              |
| <span data-ttu-id="5a6ad-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5a6ad-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5a6ad-160">Vero</span><span class="sxs-lookup"><span data-stu-id="5a6ad-160">True</span></span>                                               |
| <span data-ttu-id="5a6ad-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5a6ad-161">Is Indexed</span></span>             | <span data-ttu-id="5a6ad-162">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-162">False</span></span>                                              |
| <span data-ttu-id="5a6ad-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5a6ad-163">In Global Catalog</span></span>      | <span data-ttu-id="5a6ad-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-164">False</span></span>                                              |
| <span data-ttu-id="5a6ad-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a6ad-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5a6ad-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5a6ad-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a6ad-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a6ad-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-169">Search-Flags</span></span>           | <span data-ttu-id="5a6ad-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a6ad-170">0x00000000</span></span>                                         |
| <span data-ttu-id="5a6ad-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-171">System-Flags</span></span>           | <span data-ttu-id="5a6ad-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a6ad-172">0x00000010</span></span>                                         |
| <span data-ttu-id="5a6ad-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5a6ad-173">Classes used in</span></span>        | [<span data-ttu-id="5a6ad-174">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5a6ad-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5a6ad-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5a6ad-176">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-176">Entry</span></span> | <span data-ttu-id="5a6ad-177">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5a6ad-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a6ad-180">System-Only</span></span>            | <span data-ttu-id="5a6ad-181">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-181">False</span></span>                                              |
| <span data-ttu-id="5a6ad-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5a6ad-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5a6ad-183">Vero</span><span class="sxs-lookup"><span data-stu-id="5a6ad-183">True</span></span>                                               |
| <span data-ttu-id="5a6ad-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5a6ad-184">Is Indexed</span></span>             | <span data-ttu-id="5a6ad-185">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-185">False</span></span>                                              |
| <span data-ttu-id="5a6ad-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5a6ad-186">In Global Catalog</span></span>      | <span data-ttu-id="5a6ad-187">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-187">False</span></span>                                              |
| <span data-ttu-id="5a6ad-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a6ad-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5a6ad-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5a6ad-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a6ad-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a6ad-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-192">Search-Flags</span></span>           | <span data-ttu-id="5a6ad-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a6ad-193">0x00000000</span></span>                                         |
| <span data-ttu-id="5a6ad-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-194">System-Flags</span></span>           | <span data-ttu-id="5a6ad-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a6ad-195">0x00000010</span></span>                                         |
| <span data-ttu-id="5a6ad-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5a6ad-196">Classes used in</span></span>        | [<span data-ttu-id="5a6ad-197">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5a6ad-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a6ad-198">Windows Server 2008</span></span>



| <span data-ttu-id="5a6ad-199">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-199">Entry</span></span> | <span data-ttu-id="5a6ad-200">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5a6ad-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a6ad-203">System-Only</span></span>            | <span data-ttu-id="5a6ad-204">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-204">False</span></span>                                              |
| <span data-ttu-id="5a6ad-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5a6ad-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5a6ad-206">Vero</span><span class="sxs-lookup"><span data-stu-id="5a6ad-206">True</span></span>                                               |
| <span data-ttu-id="5a6ad-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5a6ad-207">Is Indexed</span></span>             | <span data-ttu-id="5a6ad-208">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-208">False</span></span>                                              |
| <span data-ttu-id="5a6ad-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5a6ad-209">In Global Catalog</span></span>      | <span data-ttu-id="5a6ad-210">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-210">False</span></span>                                              |
| <span data-ttu-id="5a6ad-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a6ad-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5a6ad-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5a6ad-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a6ad-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a6ad-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-215">Search-Flags</span></span>           | <span data-ttu-id="5a6ad-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a6ad-216">0x00000000</span></span>                                         |
| <span data-ttu-id="5a6ad-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-217">System-Flags</span></span>           | <span data-ttu-id="5a6ad-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a6ad-218">0x00000010</span></span>                                         |
| <span data-ttu-id="5a6ad-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5a6ad-219">Classes used in</span></span>        | [<span data-ttu-id="5a6ad-220">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5a6ad-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a6ad-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5a6ad-222">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-222">Entry</span></span> | <span data-ttu-id="5a6ad-223">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5a6ad-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a6ad-226">System-Only</span></span>            | <span data-ttu-id="5a6ad-227">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-227">False</span></span>                                              |
| <span data-ttu-id="5a6ad-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5a6ad-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5a6ad-229">Vero</span><span class="sxs-lookup"><span data-stu-id="5a6ad-229">True</span></span>                                               |
| <span data-ttu-id="5a6ad-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5a6ad-230">Is Indexed</span></span>             | <span data-ttu-id="5a6ad-231">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-231">False</span></span>                                              |
| <span data-ttu-id="5a6ad-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5a6ad-232">In Global Catalog</span></span>      | <span data-ttu-id="5a6ad-233">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-233">False</span></span>                                              |
| <span data-ttu-id="5a6ad-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a6ad-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5a6ad-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5a6ad-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a6ad-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a6ad-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-238">Search-Flags</span></span>           | <span data-ttu-id="5a6ad-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a6ad-239">0x00000000</span></span>                                         |
| <span data-ttu-id="5a6ad-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-240">System-Flags</span></span>           | <span data-ttu-id="5a6ad-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a6ad-241">0x00000010</span></span>                                         |
| <span data-ttu-id="5a6ad-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5a6ad-242">Classes used in</span></span>        | [<span data-ttu-id="5a6ad-243">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5a6ad-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a6ad-244">Windows Server 2012</span></span>



| <span data-ttu-id="5a6ad-245">Voce</span><span class="sxs-lookup"><span data-stu-id="5a6ad-245">Entry</span></span> | <span data-ttu-id="5a6ad-246">Valore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="5a6ad-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5a6ad-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a6ad-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="5a6ad-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a6ad-249">System-Only</span></span>            | <span data-ttu-id="5a6ad-250">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-250">False</span></span>                                              |
| <span data-ttu-id="5a6ad-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5a6ad-251">Is-Single-Valued</span></span>       | <span data-ttu-id="5a6ad-252">Vero</span><span class="sxs-lookup"><span data-stu-id="5a6ad-252">True</span></span>                                               |
| <span data-ttu-id="5a6ad-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5a6ad-253">Is Indexed</span></span>             | <span data-ttu-id="5a6ad-254">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-254">False</span></span>                                              |
| <span data-ttu-id="5a6ad-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5a6ad-255">In Global Catalog</span></span>      | <span data-ttu-id="5a6ad-256">Falso</span><span class="sxs-lookup"><span data-stu-id="5a6ad-256">False</span></span>                                              |
| <span data-ttu-id="5a6ad-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5a6ad-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a6ad-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5a6ad-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="5a6ad-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a6ad-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a6ad-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="5a6ad-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-261">Search-Flags</span></span>           | <span data-ttu-id="5a6ad-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a6ad-262">0x00000000</span></span>                                         |
| <span data-ttu-id="5a6ad-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a6ad-263">System-Flags</span></span>           | <span data-ttu-id="5a6ad-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a6ad-264">0x00000010</span></span>                                         |
| <span data-ttu-id="5a6ad-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5a6ad-265">Classes used in</span></span>        | [<span data-ttu-id="5a6ad-266">**Criteri di dominio**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





