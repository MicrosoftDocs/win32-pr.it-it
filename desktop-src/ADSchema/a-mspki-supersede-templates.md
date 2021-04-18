---
title: attributo ms-PKI-sostituisce-Templates
description: Specifica i nomi dei modelli di certificato sostituiti dal modello corrente.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- attributo di AD per l'attributo ms-PKI-sostituisce-Templates
- msPKI-sostituisce lo schema AD dell'attributo Templates
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519758"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="15019-105">attributo ms-PKI-sostituisce-Templates</span><span class="sxs-lookup"><span data-stu-id="15019-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="15019-106">Specifica i nomi dei modelli di certificato sostituiti dal modello corrente.</span><span class="sxs-lookup"><span data-stu-id="15019-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="15019-107">Voce</span><span class="sxs-lookup"><span data-stu-id="15019-107">Entry</span></span> | <span data-ttu-id="15019-108">Valore</span><span class="sxs-lookup"><span data-stu-id="15019-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15019-109">CN</span><span class="sxs-lookup"><span data-stu-id="15019-109">CN</span></span>                | <span data-ttu-id="15019-110">ms-PKI-sostituisce-modelli</span><span class="sxs-lookup"><span data-stu-id="15019-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="15019-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="15019-111">Ldap-Display-Name</span></span> | <span data-ttu-id="15019-112">msPKI-sostituisce-modelli</span><span class="sxs-lookup"><span data-stu-id="15019-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="15019-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="15019-113">Size</span></span>              | <span data-ttu-id="15019-114">64 byte</span><span class="sxs-lookup"><span data-stu-id="15019-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="15019-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="15019-115">Update Privilege</span></span>  | <span data-ttu-id="15019-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="15019-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="15019-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="15019-117">Update Frequency</span></span>  | <span data-ttu-id="15019-118">Quando l'oggetto modello di certificato (ms-PKI-certificate-template) viene modificato, creato o clonato.</span><span class="sxs-lookup"><span data-stu-id="15019-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="15019-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="15019-119">Attribute-Id</span></span>      | <span data-ttu-id="15019-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="15019-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="15019-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="15019-121">System-Id-Guid</span></span>    | <span data-ttu-id="15019-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="15019-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="15019-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15019-123">Syntax</span></span>            | [<span data-ttu-id="15019-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="15019-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="15019-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="15019-125">Implementations</span></span>

-   [<span data-ttu-id="15019-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="15019-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="15019-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="15019-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="15019-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="15019-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="15019-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="15019-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="15019-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="15019-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="15019-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15019-131">Windows Server 2003</span></span>



| <span data-ttu-id="15019-132">Voce</span><span class="sxs-lookup"><span data-stu-id="15019-132">Entry</span></span> | <span data-ttu-id="15019-133">Valore</span><span class="sxs-lookup"><span data-stu-id="15019-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="15019-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="15019-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15019-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="15019-136">System-Only</span></span>            | <span data-ttu-id="15019-137">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-137">False</span></span>                                                                   |
| <span data-ttu-id="15019-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="15019-138">Is-Single-Valued</span></span>       | <span data-ttu-id="15019-139">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-139">False</span></span>                                                                   |
| <span data-ttu-id="15019-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="15019-140">Is Indexed</span></span>             | <span data-ttu-id="15019-141">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-141">False</span></span>                                                                   |
| <span data-ttu-id="15019-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="15019-142">In Global Catalog</span></span>      | <span data-ttu-id="15019-143">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-143">False</span></span>                                                                   |
| <span data-ttu-id="15019-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="15019-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="15019-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="15019-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="15019-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15019-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15019-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-148">Search-Flags</span></span>           | <span data-ttu-id="15019-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15019-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="15019-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-150">System-Flags</span></span>           | <span data-ttu-id="15019-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15019-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="15019-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="15019-152">Classes used in</span></span>        | [<span data-ttu-id="15019-153">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="15019-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="15019-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15019-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="15019-155">Voce</span><span class="sxs-lookup"><span data-stu-id="15019-155">Entry</span></span> | <span data-ttu-id="15019-156">Valore</span><span class="sxs-lookup"><span data-stu-id="15019-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="15019-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="15019-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15019-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="15019-159">System-Only</span></span>            | <span data-ttu-id="15019-160">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-160">False</span></span>                                                                   |
| <span data-ttu-id="15019-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="15019-161">Is-Single-Valued</span></span>       | <span data-ttu-id="15019-162">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-162">False</span></span>                                                                   |
| <span data-ttu-id="15019-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="15019-163">Is Indexed</span></span>             | <span data-ttu-id="15019-164">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-164">False</span></span>                                                                   |
| <span data-ttu-id="15019-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="15019-165">In Global Catalog</span></span>      | <span data-ttu-id="15019-166">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-166">False</span></span>                                                                   |
| <span data-ttu-id="15019-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="15019-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="15019-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="15019-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="15019-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15019-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15019-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-171">Search-Flags</span></span>           | <span data-ttu-id="15019-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15019-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="15019-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-173">System-Flags</span></span>           | <span data-ttu-id="15019-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15019-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="15019-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="15019-175">Classes used in</span></span>        | [<span data-ttu-id="15019-176">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="15019-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="15019-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15019-177">Windows Server 2008</span></span>



| <span data-ttu-id="15019-178">Voce</span><span class="sxs-lookup"><span data-stu-id="15019-178">Entry</span></span> | <span data-ttu-id="15019-179">Valore</span><span class="sxs-lookup"><span data-stu-id="15019-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="15019-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="15019-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15019-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="15019-182">System-Only</span></span>            | <span data-ttu-id="15019-183">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-183">False</span></span>                                                                   |
| <span data-ttu-id="15019-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="15019-184">Is-Single-Valued</span></span>       | <span data-ttu-id="15019-185">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-185">False</span></span>                                                                   |
| <span data-ttu-id="15019-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="15019-186">Is Indexed</span></span>             | <span data-ttu-id="15019-187">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-187">False</span></span>                                                                   |
| <span data-ttu-id="15019-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="15019-188">In Global Catalog</span></span>      | <span data-ttu-id="15019-189">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-189">False</span></span>                                                                   |
| <span data-ttu-id="15019-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="15019-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="15019-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="15019-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="15019-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15019-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15019-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-194">Search-Flags</span></span>           | <span data-ttu-id="15019-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15019-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="15019-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-196">System-Flags</span></span>           | <span data-ttu-id="15019-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15019-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="15019-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="15019-198">Classes used in</span></span>        | [<span data-ttu-id="15019-199">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="15019-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="15019-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15019-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="15019-201">Voce</span><span class="sxs-lookup"><span data-stu-id="15019-201">Entry</span></span> | <span data-ttu-id="15019-202">Valore</span><span class="sxs-lookup"><span data-stu-id="15019-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="15019-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="15019-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15019-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="15019-205">System-Only</span></span>            | <span data-ttu-id="15019-206">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-206">False</span></span>                                                                   |
| <span data-ttu-id="15019-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="15019-207">Is-Single-Valued</span></span>       | <span data-ttu-id="15019-208">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-208">False</span></span>                                                                   |
| <span data-ttu-id="15019-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="15019-209">Is Indexed</span></span>             | <span data-ttu-id="15019-210">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-210">False</span></span>                                                                   |
| <span data-ttu-id="15019-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="15019-211">In Global Catalog</span></span>      | <span data-ttu-id="15019-212">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-212">False</span></span>                                                                   |
| <span data-ttu-id="15019-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="15019-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="15019-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="15019-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="15019-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15019-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15019-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-217">Search-Flags</span></span>           | <span data-ttu-id="15019-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15019-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="15019-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-219">System-Flags</span></span>           | <span data-ttu-id="15019-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15019-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="15019-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="15019-221">Classes used in</span></span>        | [<span data-ttu-id="15019-222">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="15019-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="15019-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15019-223">Windows Server 2012</span></span>



| <span data-ttu-id="15019-224">Voce</span><span class="sxs-lookup"><span data-stu-id="15019-224">Entry</span></span> | <span data-ttu-id="15019-225">Valore</span><span class="sxs-lookup"><span data-stu-id="15019-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="15019-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="15019-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15019-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="15019-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="15019-228">System-Only</span></span>            | <span data-ttu-id="15019-229">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-229">False</span></span>                                                                   |
| <span data-ttu-id="15019-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="15019-230">Is-Single-Valued</span></span>       | <span data-ttu-id="15019-231">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-231">False</span></span>                                                                   |
| <span data-ttu-id="15019-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="15019-232">Is Indexed</span></span>             | <span data-ttu-id="15019-233">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-233">False</span></span>                                                                   |
| <span data-ttu-id="15019-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="15019-234">In Global Catalog</span></span>      | <span data-ttu-id="15019-235">Falso</span><span class="sxs-lookup"><span data-stu-id="15019-235">False</span></span>                                                                   |
| <span data-ttu-id="15019-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="15019-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="15019-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="15019-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="15019-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15019-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15019-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="15019-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-240">Search-Flags</span></span>           | <span data-ttu-id="15019-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15019-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="15019-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15019-242">System-Flags</span></span>           | <span data-ttu-id="15019-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15019-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="15019-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="15019-244">Classes used in</span></span>        | [<span data-ttu-id="15019-245">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="15019-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





