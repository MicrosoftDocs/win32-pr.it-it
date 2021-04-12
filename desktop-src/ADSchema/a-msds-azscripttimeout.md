---
title: attributo ms-DS-AZ-script-timeout
description: Tempo massimo, in millisecondi, di attesa per il completamento del controllo di un criterio specifico da parte di uno script.
ms.assetid: 166d87a3-8768-42d9-9041-21f272059fbf
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-AZ-script-timeout
- attributo msDS-AzScriptTimeout-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Az-Script-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67de4230c3f4710a3eefe6edab896d4fcadcb91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104401025"
---
# <a name="ms-ds-az-script-timeout-attribute"></a><span data-ttu-id="5296b-105">attributo ms-DS-AZ-script-timeout</span><span class="sxs-lookup"><span data-stu-id="5296b-105">ms-DS-Az-Script-Timeout attribute</span></span>

<span data-ttu-id="5296b-106">Tempo massimo, in millisecondi, di attesa per il completamento del controllo di un criterio specifico da parte di uno script.</span><span class="sxs-lookup"><span data-stu-id="5296b-106">The maximum time, in milliseconds, to wait for a script to finish auditing a specific policy.</span></span>



| <span data-ttu-id="5296b-107">Voce</span><span class="sxs-lookup"><span data-stu-id="5296b-107">Entry</span></span> | <span data-ttu-id="5296b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="5296b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5296b-109">CN</span><span class="sxs-lookup"><span data-stu-id="5296b-109">CN</span></span>                | <span data-ttu-id="5296b-110">ms-DS-AZ-script-timeout</span><span class="sxs-lookup"><span data-stu-id="5296b-110">ms-DS-Az-Script-Timeout</span></span>                 |
| <span data-ttu-id="5296b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5296b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5296b-112">msDS-AzScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="5296b-112">msDS-AzScriptTimeout</span></span>                    |
| <span data-ttu-id="5296b-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5296b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="5296b-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5296b-114">Update Privilege</span></span>  | <span data-ttu-id="5296b-115">Amministratore di AzRoles</span><span class="sxs-lookup"><span data-stu-id="5296b-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="5296b-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5296b-116">Update Frequency</span></span>  | <span data-ttu-id="5296b-117">Durante l'inizializzazione o la modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="5296b-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="5296b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5296b-118">Attribute-Id</span></span>      | <span data-ttu-id="5296b-119">1.2.840.113556.1.4.1797</span><span class="sxs-lookup"><span data-stu-id="5296b-119">1.2.840.113556.1.4.1797</span></span>                 |
| <span data-ttu-id="5296b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5296b-120">System-Id-Guid</span></span>    | <span data-ttu-id="5296b-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span><span class="sxs-lookup"><span data-stu-id="5296b-121">87d0fb41-2c8b-41f6-b972-11fdfd50d6b0</span></span>    |
| <span data-ttu-id="5296b-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5296b-122">Syntax</span></span>            | [<span data-ttu-id="5296b-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="5296b-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="5296b-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="5296b-124">Implementations</span></span>

-   [<span data-ttu-id="5296b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5296b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5296b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5296b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5296b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5296b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5296b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5296b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5296b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5296b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5296b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5296b-130">Windows Server 2003</span></span>



| <span data-ttu-id="5296b-131">Voce</span><span class="sxs-lookup"><span data-stu-id="5296b-131">Entry</span></span> | <span data-ttu-id="5296b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5296b-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5296b-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5296b-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5296b-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5296b-135">System-Only</span></span>            | <span data-ttu-id="5296b-136">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-136">False</span></span>                                                              |
| <span data-ttu-id="5296b-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5296b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5296b-138">Vero</span><span class="sxs-lookup"><span data-stu-id="5296b-138">True</span></span>                                                               |
| <span data-ttu-id="5296b-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5296b-139">Is Indexed</span></span>             | <span data-ttu-id="5296b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-140">False</span></span>                                                              |
| <span data-ttu-id="5296b-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5296b-141">In Global Catalog</span></span>      | <span data-ttu-id="5296b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-142">False</span></span>                                                              |
| <span data-ttu-id="5296b-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5296b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5296b-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5296b-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5296b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5296b-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5296b-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-147">Search-Flags</span></span>           | <span data-ttu-id="5296b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5296b-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="5296b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-149">System-Flags</span></span>           | <span data-ttu-id="5296b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5296b-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="5296b-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5296b-151">Classes used in</span></span>        | [<span data-ttu-id="5296b-152">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="5296b-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5296b-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5296b-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5296b-154">Voce</span><span class="sxs-lookup"><span data-stu-id="5296b-154">Entry</span></span> | <span data-ttu-id="5296b-155">Valore</span><span class="sxs-lookup"><span data-stu-id="5296b-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5296b-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5296b-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5296b-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5296b-158">System-Only</span></span>            | <span data-ttu-id="5296b-159">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-159">False</span></span>                                                              |
| <span data-ttu-id="5296b-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5296b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5296b-161">Vero</span><span class="sxs-lookup"><span data-stu-id="5296b-161">True</span></span>                                                               |
| <span data-ttu-id="5296b-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5296b-162">Is Indexed</span></span>             | <span data-ttu-id="5296b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-163">False</span></span>                                                              |
| <span data-ttu-id="5296b-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5296b-164">In Global Catalog</span></span>      | <span data-ttu-id="5296b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-165">False</span></span>                                                              |
| <span data-ttu-id="5296b-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5296b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5296b-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5296b-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5296b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5296b-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5296b-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-170">Search-Flags</span></span>           | <span data-ttu-id="5296b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5296b-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="5296b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-172">System-Flags</span></span>           | <span data-ttu-id="5296b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5296b-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="5296b-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5296b-174">Classes used in</span></span>        | [<span data-ttu-id="5296b-175">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="5296b-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5296b-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5296b-176">Windows Server 2008</span></span>



| <span data-ttu-id="5296b-177">Voce</span><span class="sxs-lookup"><span data-stu-id="5296b-177">Entry</span></span> | <span data-ttu-id="5296b-178">Valore</span><span class="sxs-lookup"><span data-stu-id="5296b-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5296b-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5296b-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5296b-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5296b-181">System-Only</span></span>            | <span data-ttu-id="5296b-182">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-182">False</span></span>                                                              |
| <span data-ttu-id="5296b-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5296b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5296b-184">Vero</span><span class="sxs-lookup"><span data-stu-id="5296b-184">True</span></span>                                                               |
| <span data-ttu-id="5296b-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5296b-185">Is Indexed</span></span>             | <span data-ttu-id="5296b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-186">False</span></span>                                                              |
| <span data-ttu-id="5296b-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5296b-187">In Global Catalog</span></span>      | <span data-ttu-id="5296b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-188">False</span></span>                                                              |
| <span data-ttu-id="5296b-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5296b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5296b-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5296b-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5296b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5296b-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5296b-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-193">Search-Flags</span></span>           | <span data-ttu-id="5296b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5296b-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="5296b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-195">System-Flags</span></span>           | <span data-ttu-id="5296b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5296b-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="5296b-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5296b-197">Classes used in</span></span>        | [<span data-ttu-id="5296b-198">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="5296b-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5296b-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5296b-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5296b-200">Voce</span><span class="sxs-lookup"><span data-stu-id="5296b-200">Entry</span></span> | <span data-ttu-id="5296b-201">Valore</span><span class="sxs-lookup"><span data-stu-id="5296b-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5296b-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5296b-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5296b-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5296b-204">System-Only</span></span>            | <span data-ttu-id="5296b-205">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-205">False</span></span>                                                              |
| <span data-ttu-id="5296b-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5296b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5296b-207">Vero</span><span class="sxs-lookup"><span data-stu-id="5296b-207">True</span></span>                                                               |
| <span data-ttu-id="5296b-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5296b-208">Is Indexed</span></span>             | <span data-ttu-id="5296b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-209">False</span></span>                                                              |
| <span data-ttu-id="5296b-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5296b-210">In Global Catalog</span></span>      | <span data-ttu-id="5296b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-211">False</span></span>                                                              |
| <span data-ttu-id="5296b-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5296b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5296b-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5296b-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5296b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5296b-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5296b-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-216">Search-Flags</span></span>           | <span data-ttu-id="5296b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5296b-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="5296b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-218">System-Flags</span></span>           | <span data-ttu-id="5296b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5296b-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="5296b-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5296b-220">Classes used in</span></span>        | [<span data-ttu-id="5296b-221">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="5296b-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5296b-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5296b-222">Windows Server 2012</span></span>



| <span data-ttu-id="5296b-223">Voce</span><span class="sxs-lookup"><span data-stu-id="5296b-223">Entry</span></span> | <span data-ttu-id="5296b-224">Valore</span><span class="sxs-lookup"><span data-stu-id="5296b-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5296b-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5296b-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5296b-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5296b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5296b-227">System-Only</span></span>            | <span data-ttu-id="5296b-228">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-228">False</span></span>                                                              |
| <span data-ttu-id="5296b-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5296b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5296b-230">Vero</span><span class="sxs-lookup"><span data-stu-id="5296b-230">True</span></span>                                                               |
| <span data-ttu-id="5296b-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5296b-231">Is Indexed</span></span>             | <span data-ttu-id="5296b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-232">False</span></span>                                                              |
| <span data-ttu-id="5296b-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5296b-233">In Global Catalog</span></span>      | <span data-ttu-id="5296b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="5296b-234">False</span></span>                                                              |
| <span data-ttu-id="5296b-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5296b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5296b-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5296b-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5296b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5296b-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5296b-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5296b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-239">Search-Flags</span></span>           | <span data-ttu-id="5296b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5296b-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="5296b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5296b-241">System-Flags</span></span>           | <span data-ttu-id="5296b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5296b-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="5296b-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5296b-243">Classes used in</span></span>        | [<span data-ttu-id="5296b-244">**ms-DS-AZ-Admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="5296b-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





