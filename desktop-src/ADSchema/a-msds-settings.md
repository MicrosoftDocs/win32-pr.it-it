---
title: attributo ms-DS-Settings
description: Utilizzato per archiviare le impostazioni per un oggetto. Il suo utilizzo è determinato esclusivamente dal proprietario dell'oggetto. È consigliabile usarlo per archiviare le coppie nome/valore. Ad esempio, color blu.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- Microsoft-DS-impostazioni attributo AD schema
- msDS-impostazioni attributo AD schema
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875349"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="17f2c-108">attributo ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="17f2c-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="17f2c-109">Utilizzato per archiviare le impostazioni per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="17f2c-109">Used to store settings for an object.</span></span> <span data-ttu-id="17f2c-110">Il suo utilizzo è determinato esclusivamente dal proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="17f2c-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="17f2c-111">È consigliabile usarlo per archiviare le coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="17f2c-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="17f2c-112">Ad esempio, color = Blue.</span><span class="sxs-lookup"><span data-stu-id="17f2c-112">For example, color=blue.</span></span>



| <span data-ttu-id="17f2c-113">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-113">Entry</span></span> | <span data-ttu-id="17f2c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="17f2c-115">CN</span><span class="sxs-lookup"><span data-stu-id="17f2c-115">CN</span></span>                | <span data-ttu-id="17f2c-116">ms-DS-impostazioni</span><span class="sxs-lookup"><span data-stu-id="17f2c-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="17f2c-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="17f2c-117">Ldap-Display-Name</span></span> | <span data-ttu-id="17f2c-118">msDS-impostazioni</span><span class="sxs-lookup"><span data-stu-id="17f2c-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="17f2c-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="17f2c-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="17f2c-120">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-120">Update Privilege</span></span>  | <span data-ttu-id="17f2c-121">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="17f2c-121">Domain administrator</span></span>                        |
| <span data-ttu-id="17f2c-122">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-122">Update Frequency</span></span>  | <span data-ttu-id="17f2c-123">Ogni volta che i valori delle impostazioni cambiano.</span><span class="sxs-lookup"><span data-stu-id="17f2c-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="17f2c-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-124">Attribute-Id</span></span>      | <span data-ttu-id="17f2c-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="17f2c-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="17f2c-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="17f2c-126">System-Id-Guid</span></span>    | <span data-ttu-id="17f2c-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="17f2c-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="17f2c-128">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17f2c-128">Syntax</span></span>            | [<span data-ttu-id="17f2c-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="17f2c-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="17f2c-130">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="17f2c-130">Implementations</span></span>

-   [<span data-ttu-id="17f2c-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17f2c-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17f2c-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="17f2c-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="17f2c-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17f2c-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17f2c-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17f2c-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17f2c-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17f2c-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17f2c-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17f2c-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="17f2c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17f2c-137">Windows Server 2003</span></span>



| <span data-ttu-id="17f2c-138">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-138">Entry</span></span> | <span data-ttu-id="17f2c-139">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f2c-140">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="17f2c-142">System-Only</span></span>            | <span data-ttu-id="17f2c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-144">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17f2c-144">Is-Single-Valued</span></span>       | <span data-ttu-id="17f2c-145">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-146">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17f2c-146">Is Indexed</span></span>             | <span data-ttu-id="17f2c-147">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-148">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17f2c-148">In Global Catalog</span></span>      | <span data-ttu-id="17f2c-149">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-150">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17f2c-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="17f2c-151">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17f2c-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="17f2c-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17f2c-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17f2c-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-154">Search-Flags</span></span>           | <span data-ttu-id="17f2c-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-156">System-Flags</span></span>           | <span data-ttu-id="17f2c-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17f2c-158">Classes used in</span></span>        | [<span data-ttu-id="17f2c-159">**Impostazioni applicazione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="17f2c-160">**Punto di connessione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="17f2c-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="17f2c-161">ADAM</span></span>



| <span data-ttu-id="17f2c-162">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-162">Entry</span></span> | <span data-ttu-id="17f2c-163">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="17f2c-164">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="17f2c-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="17f2c-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="17f2c-166">System-Only</span></span>            | <span data-ttu-id="17f2c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-167">False</span></span>                                                            |
| <span data-ttu-id="17f2c-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17f2c-168">Is-Single-Valued</span></span>       | <span data-ttu-id="17f2c-169">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-169">False</span></span>                                                            |
| <span data-ttu-id="17f2c-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17f2c-170">Is Indexed</span></span>             | <span data-ttu-id="17f2c-171">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-171">False</span></span>                                                            |
| <span data-ttu-id="17f2c-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17f2c-172">In Global Catalog</span></span>      | <span data-ttu-id="17f2c-173">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-173">False</span></span>                                                            |
| <span data-ttu-id="17f2c-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17f2c-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="17f2c-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17f2c-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="17f2c-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17f2c-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="17f2c-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17f2c-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="17f2c-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-178">Search-Flags</span></span>           | <span data-ttu-id="17f2c-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="17f2c-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-180">System-Flags</span></span>           | <span data-ttu-id="17f2c-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="17f2c-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17f2c-182">Classes used in</span></span>        | [<span data-ttu-id="17f2c-183">**Impostazioni applicazione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17f2c-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17f2c-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17f2c-185">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-185">Entry</span></span> | <span data-ttu-id="17f2c-186">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f2c-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="17f2c-189">System-Only</span></span>            | <span data-ttu-id="17f2c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17f2c-191">Is-Single-Valued</span></span>       | <span data-ttu-id="17f2c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17f2c-193">Is Indexed</span></span>             | <span data-ttu-id="17f2c-194">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17f2c-195">In Global Catalog</span></span>      | <span data-ttu-id="17f2c-196">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17f2c-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="17f2c-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17f2c-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="17f2c-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17f2c-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17f2c-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-201">Search-Flags</span></span>           | <span data-ttu-id="17f2c-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-203">System-Flags</span></span>           | <span data-ttu-id="17f2c-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-205">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17f2c-205">Classes used in</span></span>        | [<span data-ttu-id="17f2c-206">**Impostazioni applicazione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="17f2c-207">**Punto di connessione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17f2c-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17f2c-208">Windows Server 2008</span></span>



| <span data-ttu-id="17f2c-209">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-209">Entry</span></span> | <span data-ttu-id="17f2c-210">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f2c-211">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="17f2c-213">System-Only</span></span>            | <span data-ttu-id="17f2c-214">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-215">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17f2c-215">Is-Single-Valued</span></span>       | <span data-ttu-id="17f2c-216">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-217">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17f2c-217">Is Indexed</span></span>             | <span data-ttu-id="17f2c-218">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-219">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17f2c-219">In Global Catalog</span></span>      | <span data-ttu-id="17f2c-220">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-221">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17f2c-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="17f2c-222">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17f2c-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="17f2c-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17f2c-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17f2c-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-225">Search-Flags</span></span>           | <span data-ttu-id="17f2c-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-227">System-Flags</span></span>           | <span data-ttu-id="17f2c-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17f2c-229">Classes used in</span></span>        | [<span data-ttu-id="17f2c-230">**Impostazioni applicazione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="17f2c-231">**Punto di connessione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17f2c-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17f2c-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17f2c-233">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-233">Entry</span></span> | <span data-ttu-id="17f2c-234">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f2c-235">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="17f2c-237">System-Only</span></span>            | <span data-ttu-id="17f2c-238">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-239">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17f2c-239">Is-Single-Valued</span></span>       | <span data-ttu-id="17f2c-240">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-241">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17f2c-241">Is Indexed</span></span>             | <span data-ttu-id="17f2c-242">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-243">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17f2c-243">In Global Catalog</span></span>      | <span data-ttu-id="17f2c-244">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-245">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17f2c-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="17f2c-246">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17f2c-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="17f2c-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17f2c-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17f2c-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-249">Search-Flags</span></span>           | <span data-ttu-id="17f2c-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-251">System-Flags</span></span>           | <span data-ttu-id="17f2c-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17f2c-253">Classes used in</span></span>        | [<span data-ttu-id="17f2c-254">**Impostazioni applicazione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="17f2c-255">**Punto di connessione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17f2c-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17f2c-256">Windows Server 2012</span></span>



| <span data-ttu-id="17f2c-257">Voce</span><span class="sxs-lookup"><span data-stu-id="17f2c-257">Entry</span></span> | <span data-ttu-id="17f2c-258">Valore</span><span class="sxs-lookup"><span data-stu-id="17f2c-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f2c-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="17f2c-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17f2c-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="17f2c-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="17f2c-261">System-Only</span></span>            | <span data-ttu-id="17f2c-262">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="17f2c-263">Is-Single-Valued</span></span>       | <span data-ttu-id="17f2c-264">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="17f2c-265">Is Indexed</span></span>             | <span data-ttu-id="17f2c-266">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="17f2c-267">In Global Catalog</span></span>      | <span data-ttu-id="17f2c-268">Falso</span><span class="sxs-lookup"><span data-stu-id="17f2c-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="17f2c-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="17f2c-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="17f2c-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="17f2c-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="17f2c-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17f2c-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17f2c-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="17f2c-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-273">Search-Flags</span></span>           | <span data-ttu-id="17f2c-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17f2c-275">System-Flags</span></span>           | <span data-ttu-id="17f2c-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17f2c-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="17f2c-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="17f2c-277">Classes used in</span></span>        | [<span data-ttu-id="17f2c-278">**Impostazioni applicazione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="17f2c-279">**Punto di connessione**</span><span class="sxs-lookup"><span data-stu-id="17f2c-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





