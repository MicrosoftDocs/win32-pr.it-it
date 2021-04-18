---
title: attributo ms-DS-allowed-to-delegate-to
description: Si tratta di un attributo sugli oggetti account del servizio (computer o account utente).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-allowed-to-delegate-to
- attributo msDS-AllowedToDelegateTo-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303288"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="37c3e-105">attributo ms-DS-allowed-to-delegate-to</span><span class="sxs-lookup"><span data-stu-id="37c3e-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="37c3e-106">Si tratta di un attributo sugli oggetti account del servizio (computer o account utente).</span><span class="sxs-lookup"><span data-stu-id="37c3e-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="37c3e-107">Contiene un elenco di nomi di entità servizio (SPN).</span><span class="sxs-lookup"><span data-stu-id="37c3e-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="37c3e-108">Questo attributo viene utilizzato per configurare un servizio in modo che possa ottenere ticket di servizio che possono essere utilizzati per la delega vincolata.</span><span class="sxs-lookup"><span data-stu-id="37c3e-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="37c3e-109">Voce</span><span class="sxs-lookup"><span data-stu-id="37c3e-109">Entry</span></span> | <span data-ttu-id="37c3e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="37c3e-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="37c3e-111">CN</span><span class="sxs-lookup"><span data-stu-id="37c3e-111">CN</span></span>                | <span data-ttu-id="37c3e-112">ms-DS-consentito da delegare a</span><span class="sxs-lookup"><span data-stu-id="37c3e-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="37c3e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="37c3e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="37c3e-114">msDS-AllowedToDelegateTo</span><span class="sxs-lookup"><span data-stu-id="37c3e-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="37c3e-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="37c3e-115">Size</span></span>              | <span data-ttu-id="37c3e-116">da 0 a 64K</span><span class="sxs-lookup"><span data-stu-id="37c3e-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="37c3e-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="37c3e-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-118">Update Frequency</span></span>  | <span data-ttu-id="37c3e-119">Raramente</span><span class="sxs-lookup"><span data-stu-id="37c3e-119">Infrequently</span></span>                                |
| <span data-ttu-id="37c3e-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37c3e-120">Attribute-Id</span></span>      | <span data-ttu-id="37c3e-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="37c3e-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="37c3e-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="37c3e-122">System-Id-Guid</span></span>    | <span data-ttu-id="37c3e-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="37c3e-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="37c3e-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37c3e-124">Syntax</span></span>            | [<span data-ttu-id="37c3e-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="37c3e-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="37c3e-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="37c3e-126">Implementations</span></span>

-   [<span data-ttu-id="37c3e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37c3e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37c3e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37c3e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37c3e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37c3e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37c3e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37c3e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37c3e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37c3e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="37c3e-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37c3e-132">Windows Server 2003</span></span>



| <span data-ttu-id="37c3e-133">Voce</span><span class="sxs-lookup"><span data-stu-id="37c3e-133">Entry</span></span> | <span data-ttu-id="37c3e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="37c3e-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="37c3e-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3e-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3e-137">System-Only</span></span>            | <span data-ttu-id="37c3e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-138">False</span></span>                                                              |
| <span data-ttu-id="37c3e-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="37c3e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-140">False</span></span>                                                              |
| <span data-ttu-id="37c3e-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="37c3e-141">Is Indexed</span></span>             | <span data-ttu-id="37c3e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-142">False</span></span>                                                              |
| <span data-ttu-id="37c3e-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="37c3e-143">In Global Catalog</span></span>      | <span data-ttu-id="37c3e-144">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-144">False</span></span>                                                              |
| <span data-ttu-id="37c3e-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="37c3e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3e-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="37c3e-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="37c3e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3e-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3e-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-149">Search-Flags</span></span>           | <span data-ttu-id="37c3e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3e-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="37c3e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-151">System-Flags</span></span>           | <span data-ttu-id="37c3e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3e-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="37c3e-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="37c3e-153">Classes used in</span></span>        | [<span data-ttu-id="37c3e-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="37c3e-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37c3e-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37c3e-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37c3e-156">Voce</span><span class="sxs-lookup"><span data-stu-id="37c3e-156">Entry</span></span> | <span data-ttu-id="37c3e-157">Valore</span><span class="sxs-lookup"><span data-stu-id="37c3e-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="37c3e-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3e-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3e-160">System-Only</span></span>            | <span data-ttu-id="37c3e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-161">False</span></span>                                                              |
| <span data-ttu-id="37c3e-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="37c3e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-163">False</span></span>                                                              |
| <span data-ttu-id="37c3e-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="37c3e-164">Is Indexed</span></span>             | <span data-ttu-id="37c3e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-165">False</span></span>                                                              |
| <span data-ttu-id="37c3e-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="37c3e-166">In Global Catalog</span></span>      | <span data-ttu-id="37c3e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-167">False</span></span>                                                              |
| <span data-ttu-id="37c3e-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="37c3e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3e-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="37c3e-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="37c3e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3e-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3e-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-172">Search-Flags</span></span>           | <span data-ttu-id="37c3e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3e-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="37c3e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-174">System-Flags</span></span>           | <span data-ttu-id="37c3e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3e-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="37c3e-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="37c3e-176">Classes used in</span></span>        | [<span data-ttu-id="37c3e-177">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="37c3e-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37c3e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37c3e-178">Windows Server 2008</span></span>



| <span data-ttu-id="37c3e-179">Voce</span><span class="sxs-lookup"><span data-stu-id="37c3e-179">Entry</span></span> | <span data-ttu-id="37c3e-180">Valore</span><span class="sxs-lookup"><span data-stu-id="37c3e-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="37c3e-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3e-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3e-183">System-Only</span></span>            | <span data-ttu-id="37c3e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-184">False</span></span>                                                              |
| <span data-ttu-id="37c3e-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="37c3e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-186">False</span></span>                                                              |
| <span data-ttu-id="37c3e-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="37c3e-187">Is Indexed</span></span>             | <span data-ttu-id="37c3e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-188">False</span></span>                                                              |
| <span data-ttu-id="37c3e-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="37c3e-189">In Global Catalog</span></span>      | <span data-ttu-id="37c3e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-190">False</span></span>                                                              |
| <span data-ttu-id="37c3e-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="37c3e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3e-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="37c3e-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="37c3e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3e-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3e-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-195">Search-Flags</span></span>           | <span data-ttu-id="37c3e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3e-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="37c3e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-197">System-Flags</span></span>           | <span data-ttu-id="37c3e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3e-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="37c3e-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="37c3e-199">Classes used in</span></span>        | [<span data-ttu-id="37c3e-200">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="37c3e-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37c3e-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37c3e-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37c3e-202">Voce</span><span class="sxs-lookup"><span data-stu-id="37c3e-202">Entry</span></span> | <span data-ttu-id="37c3e-203">Valore</span><span class="sxs-lookup"><span data-stu-id="37c3e-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="37c3e-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3e-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3e-206">System-Only</span></span>            | <span data-ttu-id="37c3e-207">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-207">False</span></span>                                                              |
| <span data-ttu-id="37c3e-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="37c3e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3e-209">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-209">False</span></span>                                                              |
| <span data-ttu-id="37c3e-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="37c3e-210">Is Indexed</span></span>             | <span data-ttu-id="37c3e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-211">False</span></span>                                                              |
| <span data-ttu-id="37c3e-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="37c3e-212">In Global Catalog</span></span>      | <span data-ttu-id="37c3e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-213">False</span></span>                                                              |
| <span data-ttu-id="37c3e-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="37c3e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3e-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="37c3e-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="37c3e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3e-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3e-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-218">Search-Flags</span></span>           | <span data-ttu-id="37c3e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3e-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="37c3e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-220">System-Flags</span></span>           | <span data-ttu-id="37c3e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3e-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="37c3e-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="37c3e-222">Classes used in</span></span>        | [<span data-ttu-id="37c3e-223">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="37c3e-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37c3e-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37c3e-224">Windows Server 2012</span></span>



| <span data-ttu-id="37c3e-225">Voce</span><span class="sxs-lookup"><span data-stu-id="37c3e-225">Entry</span></span> | <span data-ttu-id="37c3e-226">Valore</span><span class="sxs-lookup"><span data-stu-id="37c3e-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="37c3e-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="37c3e-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37c3e-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="37c3e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="37c3e-229">System-Only</span></span>            | <span data-ttu-id="37c3e-230">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-230">False</span></span>                                                              |
| <span data-ttu-id="37c3e-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="37c3e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="37c3e-232">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-232">False</span></span>                                                              |
| <span data-ttu-id="37c3e-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="37c3e-233">Is Indexed</span></span>             | <span data-ttu-id="37c3e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-234">False</span></span>                                                              |
| <span data-ttu-id="37c3e-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="37c3e-235">In Global Catalog</span></span>      | <span data-ttu-id="37c3e-236">Falso</span><span class="sxs-lookup"><span data-stu-id="37c3e-236">False</span></span>                                                              |
| <span data-ttu-id="37c3e-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="37c3e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="37c3e-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="37c3e-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="37c3e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37c3e-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37c3e-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="37c3e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-241">Search-Flags</span></span>           | <span data-ttu-id="37c3e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37c3e-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="37c3e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37c3e-243">System-Flags</span></span>           | <span data-ttu-id="37c3e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37c3e-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="37c3e-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="37c3e-245">Classes used in</span></span>        | [<span data-ttu-id="37c3e-246">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="37c3e-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





