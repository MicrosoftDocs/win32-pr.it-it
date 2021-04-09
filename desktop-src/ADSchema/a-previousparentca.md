---
title: Precedente-attributo padre-CA
description: Riferimento alle autorità di certificazione che hanno emesso l'ultimo certificato scaduto per un'autorità di certificazione.
ms.assetid: 9772d6cb-1105-426c-9982-473b4c1bf0d8
ms.tgt_platform: multiple
keywords:
- Precedente-schema AD dell'attributo padre-CA
- Schema AD dell'attributo previousParentCA
topic_type:
- apiref
api_name:
- Previous-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a4c89652ef7ffffdc731614cfc57572b3edcde
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104048790"
---
# <a name="previous-parent-ca-attribute"></a><span data-ttu-id="c1fcb-105">Precedente-attributo padre-CA</span><span class="sxs-lookup"><span data-stu-id="c1fcb-105">Previous-Parent-CA attribute</span></span>

<span data-ttu-id="c1fcb-106">Riferimento alle autorità di certificazione che hanno emesso l'ultimo certificato scaduto per un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="c1fcb-106">Reference to the certification authorities that issued the last expired certificate for a certification authority.</span></span>



| <span data-ttu-id="c1fcb-107">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-107">Entry</span></span> | <span data-ttu-id="c1fcb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c1fcb-109">CN</span><span class="sxs-lookup"><span data-stu-id="c1fcb-109">CN</span></span>                | <span data-ttu-id="c1fcb-110">Precedente-padre-CA</span><span class="sxs-lookup"><span data-stu-id="c1fcb-110">Previous-Parent-CA</span></span>                      |
| <span data-ttu-id="c1fcb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c1fcb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c1fcb-112">previousParentCA</span><span class="sxs-lookup"><span data-stu-id="c1fcb-112">previousParentCA</span></span>                        |
| <span data-ttu-id="c1fcb-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c1fcb-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c1fcb-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c1fcb-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c1fcb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-116">Attribute-Id</span></span>      | <span data-ttu-id="c1fcb-117">1.2.840.113556.1.4.694</span><span class="sxs-lookup"><span data-stu-id="c1fcb-117">1.2.840.113556.1.4.694</span></span>                  |
| <span data-ttu-id="c1fcb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c1fcb-118">System-Id-Guid</span></span>    | <span data-ttu-id="c1fcb-119">963d273d-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c1fcb-119">963d273d-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="c1fcb-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1fcb-120">Syntax</span></span>            | [<span data-ttu-id="c1fcb-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c1fcb-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c1fcb-122">Implementations</span></span>

-   [<span data-ttu-id="c1fcb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c1fcb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1fcb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1fcb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1fcb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1fcb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c1fcb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1fcb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c1fcb-130">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-130">Entry</span></span> | <span data-ttu-id="c1fcb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1fcb-134">System-Only</span></span>            | <span data-ttu-id="c1fcb-135">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-135">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c1fcb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c1fcb-137">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-137">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c1fcb-138">Is Indexed</span></span>             | <span data-ttu-id="c1fcb-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-139">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c1fcb-140">In Global Catalog</span></span>      | <span data-ttu-id="c1fcb-141">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-141">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1fcb-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c1fcb-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c1fcb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1fcb-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1fcb-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-146">Search-Flags</span></span>           | <span data-ttu-id="c1fcb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1fcb-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="c1fcb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-148">System-Flags</span></span>           | <span data-ttu-id="c1fcb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1fcb-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="c1fcb-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c1fcb-150">Classes used in</span></span>        | [<span data-ttu-id="c1fcb-151">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c1fcb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1fcb-152">Windows Server 2003</span></span>



| <span data-ttu-id="c1fcb-153">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-153">Entry</span></span> | <span data-ttu-id="c1fcb-154">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1fcb-157">System-Only</span></span>            | <span data-ttu-id="c1fcb-158">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-158">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c1fcb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c1fcb-160">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-160">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c1fcb-161">Is Indexed</span></span>             | <span data-ttu-id="c1fcb-162">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-162">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c1fcb-163">In Global Catalog</span></span>      | <span data-ttu-id="c1fcb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-164">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1fcb-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c1fcb-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c1fcb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1fcb-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1fcb-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-169">Search-Flags</span></span>           | <span data-ttu-id="c1fcb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1fcb-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="c1fcb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-171">System-Flags</span></span>           | <span data-ttu-id="c1fcb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1fcb-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="c1fcb-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c1fcb-173">Classes used in</span></span>        | [<span data-ttu-id="c1fcb-174">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1fcb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1fcb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1fcb-176">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-176">Entry</span></span> | <span data-ttu-id="c1fcb-177">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1fcb-180">System-Only</span></span>            | <span data-ttu-id="c1fcb-181">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-181">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c1fcb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c1fcb-183">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-183">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c1fcb-184">Is Indexed</span></span>             | <span data-ttu-id="c1fcb-185">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-185">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c1fcb-186">In Global Catalog</span></span>      | <span data-ttu-id="c1fcb-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-187">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1fcb-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c1fcb-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c1fcb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1fcb-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1fcb-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-192">Search-Flags</span></span>           | <span data-ttu-id="c1fcb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1fcb-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="c1fcb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-194">System-Flags</span></span>           | <span data-ttu-id="c1fcb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1fcb-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="c1fcb-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c1fcb-196">Classes used in</span></span>        | [<span data-ttu-id="c1fcb-197">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1fcb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1fcb-198">Windows Server 2008</span></span>



| <span data-ttu-id="c1fcb-199">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-199">Entry</span></span> | <span data-ttu-id="c1fcb-200">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1fcb-203">System-Only</span></span>            | <span data-ttu-id="c1fcb-204">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-204">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c1fcb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c1fcb-206">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-206">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c1fcb-207">Is Indexed</span></span>             | <span data-ttu-id="c1fcb-208">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-208">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c1fcb-209">In Global Catalog</span></span>      | <span data-ttu-id="c1fcb-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-210">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1fcb-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c1fcb-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c1fcb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1fcb-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1fcb-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-215">Search-Flags</span></span>           | <span data-ttu-id="c1fcb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1fcb-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="c1fcb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-217">System-Flags</span></span>           | <span data-ttu-id="c1fcb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1fcb-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="c1fcb-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c1fcb-219">Classes used in</span></span>        | [<span data-ttu-id="c1fcb-220">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1fcb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1fcb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1fcb-222">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-222">Entry</span></span> | <span data-ttu-id="c1fcb-223">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1fcb-226">System-Only</span></span>            | <span data-ttu-id="c1fcb-227">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-227">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c1fcb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c1fcb-229">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-229">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c1fcb-230">Is Indexed</span></span>             | <span data-ttu-id="c1fcb-231">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-231">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c1fcb-232">In Global Catalog</span></span>      | <span data-ttu-id="c1fcb-233">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-233">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1fcb-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c1fcb-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c1fcb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1fcb-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1fcb-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-238">Search-Flags</span></span>           | <span data-ttu-id="c1fcb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1fcb-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="c1fcb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-240">System-Flags</span></span>           | <span data-ttu-id="c1fcb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1fcb-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="c1fcb-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c1fcb-242">Classes used in</span></span>        | [<span data-ttu-id="c1fcb-243">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1fcb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1fcb-244">Windows Server 2012</span></span>



| <span data-ttu-id="c1fcb-245">Voce</span><span class="sxs-lookup"><span data-stu-id="c1fcb-245">Entry</span></span> | <span data-ttu-id="c1fcb-246">Valore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c1fcb-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c1fcb-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1fcb-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c1fcb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1fcb-249">System-Only</span></span>            | <span data-ttu-id="c1fcb-250">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-250">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c1fcb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c1fcb-252">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-252">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c1fcb-253">Is Indexed</span></span>             | <span data-ttu-id="c1fcb-254">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-254">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c1fcb-255">In Global Catalog</span></span>      | <span data-ttu-id="c1fcb-256">Falso</span><span class="sxs-lookup"><span data-stu-id="c1fcb-256">False</span></span>                                                                  |
| <span data-ttu-id="c1fcb-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c1fcb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1fcb-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c1fcb-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c1fcb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1fcb-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1fcb-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c1fcb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-261">Search-Flags</span></span>           | <span data-ttu-id="c1fcb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1fcb-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="c1fcb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1fcb-263">System-Flags</span></span>           | <span data-ttu-id="c1fcb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1fcb-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="c1fcb-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c1fcb-265">Classes used in</span></span>        | [<span data-ttu-id="c1fcb-266">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="c1fcb-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





