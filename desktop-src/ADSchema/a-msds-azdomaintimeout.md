---
title: attributo ms-DS-AZ-Domain-timeout
description: Tempo, in millisecondi, dopo il rilevamento di un dominio come irraggiungibile e prima che il controller di dominio venga ritentato.
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-AZ-Domain-timeout
- attributo msDS-AzDomainTimeout-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875405"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="00d98-105">attributo ms-DS-AZ-Domain-timeout</span><span class="sxs-lookup"><span data-stu-id="00d98-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="00d98-106">Tempo, in millisecondi, dopo il rilevamento di un dominio come irraggiungibile e prima che il controller di dominio venga ritentato.</span><span class="sxs-lookup"><span data-stu-id="00d98-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="00d98-107">Voce</span><span class="sxs-lookup"><span data-stu-id="00d98-107">Entry</span></span> | <span data-ttu-id="00d98-108">Valore</span><span class="sxs-lookup"><span data-stu-id="00d98-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="00d98-109">CN</span><span class="sxs-lookup"><span data-stu-id="00d98-109">CN</span></span>                | <span data-ttu-id="00d98-110">ms-DS-AZ-Domain-timeout</span><span class="sxs-lookup"><span data-stu-id="00d98-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="00d98-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="00d98-111">Ldap-Display-Name</span></span> | <span data-ttu-id="00d98-112">msDS-AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="00d98-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="00d98-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="00d98-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="00d98-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="00d98-114">Update Privilege</span></span>  | <span data-ttu-id="00d98-115">Amministratore di AzRoles</span><span class="sxs-lookup"><span data-stu-id="00d98-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="00d98-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="00d98-116">Update Frequency</span></span>  | <span data-ttu-id="00d98-117">Durante l'inizializzazione o la modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="00d98-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="00d98-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00d98-118">Attribute-Id</span></span>      | <span data-ttu-id="00d98-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="00d98-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="00d98-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="00d98-120">System-Id-Guid</span></span>    | <span data-ttu-id="00d98-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="00d98-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="00d98-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d98-122">Syntax</span></span>            | [<span data-ttu-id="00d98-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="00d98-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="00d98-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="00d98-124">Implementations</span></span>

-   [<span data-ttu-id="00d98-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00d98-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00d98-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00d98-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00d98-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00d98-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00d98-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00d98-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00d98-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00d98-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="00d98-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00d98-130">Windows Server 2003</span></span>



| <span data-ttu-id="00d98-131">Voce</span><span class="sxs-lookup"><span data-stu-id="00d98-131">Entry</span></span> | <span data-ttu-id="00d98-132">Valore</span><span class="sxs-lookup"><span data-stu-id="00d98-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="00d98-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="00d98-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d98-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d98-135">System-Only</span></span>            | <span data-ttu-id="00d98-136">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-136">False</span></span>                                                              |
| <span data-ttu-id="00d98-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="00d98-137">Is-Single-Valued</span></span>       | <span data-ttu-id="00d98-138">Vero</span><span class="sxs-lookup"><span data-stu-id="00d98-138">True</span></span>                                                               |
| <span data-ttu-id="00d98-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="00d98-139">Is Indexed</span></span>             | <span data-ttu-id="00d98-140">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-140">False</span></span>                                                              |
| <span data-ttu-id="00d98-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="00d98-141">In Global Catalog</span></span>      | <span data-ttu-id="00d98-142">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-142">False</span></span>                                                              |
| <span data-ttu-id="00d98-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="00d98-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d98-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="00d98-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="00d98-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d98-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d98-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-147">Search-Flags</span></span>           | <span data-ttu-id="00d98-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d98-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="00d98-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-149">System-Flags</span></span>           | <span data-ttu-id="00d98-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d98-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d98-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="00d98-151">Classes used in</span></span>        | [<span data-ttu-id="00d98-152">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="00d98-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00d98-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00d98-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00d98-154">Voce</span><span class="sxs-lookup"><span data-stu-id="00d98-154">Entry</span></span> | <span data-ttu-id="00d98-155">Valore</span><span class="sxs-lookup"><span data-stu-id="00d98-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="00d98-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="00d98-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d98-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d98-158">System-Only</span></span>            | <span data-ttu-id="00d98-159">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-159">False</span></span>                                                              |
| <span data-ttu-id="00d98-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="00d98-160">Is-Single-Valued</span></span>       | <span data-ttu-id="00d98-161">Vero</span><span class="sxs-lookup"><span data-stu-id="00d98-161">True</span></span>                                                               |
| <span data-ttu-id="00d98-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="00d98-162">Is Indexed</span></span>             | <span data-ttu-id="00d98-163">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-163">False</span></span>                                                              |
| <span data-ttu-id="00d98-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="00d98-164">In Global Catalog</span></span>      | <span data-ttu-id="00d98-165">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-165">False</span></span>                                                              |
| <span data-ttu-id="00d98-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="00d98-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d98-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="00d98-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="00d98-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d98-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d98-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-170">Search-Flags</span></span>           | <span data-ttu-id="00d98-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d98-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="00d98-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-172">System-Flags</span></span>           | <span data-ttu-id="00d98-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d98-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d98-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="00d98-174">Classes used in</span></span>        | [<span data-ttu-id="00d98-175">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="00d98-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00d98-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00d98-176">Windows Server 2008</span></span>



| <span data-ttu-id="00d98-177">Voce</span><span class="sxs-lookup"><span data-stu-id="00d98-177">Entry</span></span> | <span data-ttu-id="00d98-178">Valore</span><span class="sxs-lookup"><span data-stu-id="00d98-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="00d98-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="00d98-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d98-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d98-181">System-Only</span></span>            | <span data-ttu-id="00d98-182">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-182">False</span></span>                                                              |
| <span data-ttu-id="00d98-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="00d98-183">Is-Single-Valued</span></span>       | <span data-ttu-id="00d98-184">Vero</span><span class="sxs-lookup"><span data-stu-id="00d98-184">True</span></span>                                                               |
| <span data-ttu-id="00d98-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="00d98-185">Is Indexed</span></span>             | <span data-ttu-id="00d98-186">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-186">False</span></span>                                                              |
| <span data-ttu-id="00d98-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="00d98-187">In Global Catalog</span></span>      | <span data-ttu-id="00d98-188">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-188">False</span></span>                                                              |
| <span data-ttu-id="00d98-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="00d98-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d98-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="00d98-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="00d98-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d98-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d98-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-193">Search-Flags</span></span>           | <span data-ttu-id="00d98-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d98-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="00d98-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-195">System-Flags</span></span>           | <span data-ttu-id="00d98-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d98-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d98-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="00d98-197">Classes used in</span></span>        | [<span data-ttu-id="00d98-198">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="00d98-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00d98-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00d98-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00d98-200">Voce</span><span class="sxs-lookup"><span data-stu-id="00d98-200">Entry</span></span> | <span data-ttu-id="00d98-201">Valore</span><span class="sxs-lookup"><span data-stu-id="00d98-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="00d98-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="00d98-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d98-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d98-204">System-Only</span></span>            | <span data-ttu-id="00d98-205">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-205">False</span></span>                                                              |
| <span data-ttu-id="00d98-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="00d98-206">Is-Single-Valued</span></span>       | <span data-ttu-id="00d98-207">Vero</span><span class="sxs-lookup"><span data-stu-id="00d98-207">True</span></span>                                                               |
| <span data-ttu-id="00d98-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="00d98-208">Is Indexed</span></span>             | <span data-ttu-id="00d98-209">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-209">False</span></span>                                                              |
| <span data-ttu-id="00d98-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="00d98-210">In Global Catalog</span></span>      | <span data-ttu-id="00d98-211">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-211">False</span></span>                                                              |
| <span data-ttu-id="00d98-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="00d98-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d98-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="00d98-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="00d98-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d98-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d98-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-216">Search-Flags</span></span>           | <span data-ttu-id="00d98-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d98-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="00d98-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-218">System-Flags</span></span>           | <span data-ttu-id="00d98-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d98-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d98-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="00d98-220">Classes used in</span></span>        | [<span data-ttu-id="00d98-221">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="00d98-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00d98-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00d98-222">Windows Server 2012</span></span>



| <span data-ttu-id="00d98-223">Voce</span><span class="sxs-lookup"><span data-stu-id="00d98-223">Entry</span></span> | <span data-ttu-id="00d98-224">Valore</span><span class="sxs-lookup"><span data-stu-id="00d98-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="00d98-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="00d98-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d98-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="00d98-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d98-227">System-Only</span></span>            | <span data-ttu-id="00d98-228">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-228">False</span></span>                                                              |
| <span data-ttu-id="00d98-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="00d98-229">Is-Single-Valued</span></span>       | <span data-ttu-id="00d98-230">Vero</span><span class="sxs-lookup"><span data-stu-id="00d98-230">True</span></span>                                                               |
| <span data-ttu-id="00d98-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="00d98-231">Is Indexed</span></span>             | <span data-ttu-id="00d98-232">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-232">False</span></span>                                                              |
| <span data-ttu-id="00d98-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="00d98-233">In Global Catalog</span></span>      | <span data-ttu-id="00d98-234">Falso</span><span class="sxs-lookup"><span data-stu-id="00d98-234">False</span></span>                                                              |
| <span data-ttu-id="00d98-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="00d98-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d98-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="00d98-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="00d98-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d98-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d98-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="00d98-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-239">Search-Flags</span></span>           | <span data-ttu-id="00d98-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00d98-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="00d98-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d98-241">System-Flags</span></span>           | <span data-ttu-id="00d98-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d98-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d98-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="00d98-243">Classes used in</span></span>        | [<span data-ttu-id="00d98-244">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="00d98-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





