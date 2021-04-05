---
title: attributo ms-PKI-Certificate-Policy
description: Contiene l'elenco dei criteri di OID e i rispettivi CSP facoltativi nel certificato emesso.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-PKI-Certificate-Policy
- msPKI-Certificate-attributo criterio AD schema
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875294"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="a25b4-105">attributo ms-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="a25b4-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="a25b4-106">Contiene l'elenco dei criteri di OID e i rispettivi CSP facoltativi nel certificato emesso.</span><span class="sxs-lookup"><span data-stu-id="a25b4-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="a25b4-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a25b4-107">Entry</span></span> | <span data-ttu-id="a25b4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a25b4-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25b4-109">CN</span><span class="sxs-lookup"><span data-stu-id="a25b4-109">CN</span></span>                | <span data-ttu-id="a25b4-110">ms-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="a25b4-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="a25b4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a25b4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a25b4-112">msPKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="a25b4-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="a25b4-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a25b4-113">Size</span></span>              | <span data-ttu-id="a25b4-114">64 byte per il numero di voci.</span><span class="sxs-lookup"><span data-stu-id="a25b4-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="a25b4-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-115">Update Privilege</span></span>  | <span data-ttu-id="a25b4-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="a25b4-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="a25b4-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-117">Update Frequency</span></span>  | <span data-ttu-id="a25b4-118">Quando l'oggetto modello di certificato (ms-PKI-certificate-template) viene modificato, creato o clonato.</span><span class="sxs-lookup"><span data-stu-id="a25b4-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="a25b4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a25b4-119">Attribute-Id</span></span>      | <span data-ttu-id="a25b4-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="a25b4-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="a25b4-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a25b4-121">System-Id-Guid</span></span>    | <span data-ttu-id="a25b4-122">38942346-cc5b-424B-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="a25b4-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="a25b4-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a25b4-123">Syntax</span></span>            | [<span data-ttu-id="a25b4-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a25b4-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="a25b4-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a25b4-125">Implementations</span></span>

-   [<span data-ttu-id="a25b4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a25b4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a25b4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a25b4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a25b4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a25b4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a25b4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a25b4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a25b4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a25b4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a25b4-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a25b4-131">Windows Server 2003</span></span>



| <span data-ttu-id="a25b4-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a25b4-132">Entry</span></span> | <span data-ttu-id="a25b4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a25b4-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25b4-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25b4-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25b4-136">System-Only</span></span>            | <span data-ttu-id="a25b4-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-137">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25b4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a25b4-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-139">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25b4-140">Is Indexed</span></span>             | <span data-ttu-id="a25b4-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-141">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25b4-142">In Global Catalog</span></span>      | <span data-ttu-id="a25b4-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-143">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25b4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25b4-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25b4-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25b4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25b4-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25b4-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-148">Search-Flags</span></span>           | <span data-ttu-id="a25b4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25b4-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25b4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-150">System-Flags</span></span>           | <span data-ttu-id="a25b4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25b4-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25b4-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25b4-152">Classes used in</span></span>        | [<span data-ttu-id="a25b4-153">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25b4-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a25b4-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a25b4-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a25b4-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a25b4-155">Entry</span></span> | <span data-ttu-id="a25b4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a25b4-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25b4-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25b4-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25b4-159">System-Only</span></span>            | <span data-ttu-id="a25b4-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-160">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25b4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a25b4-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-162">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25b4-163">Is Indexed</span></span>             | <span data-ttu-id="a25b4-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-164">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25b4-165">In Global Catalog</span></span>      | <span data-ttu-id="a25b4-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-166">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25b4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25b4-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25b4-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25b4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25b4-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25b4-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-171">Search-Flags</span></span>           | <span data-ttu-id="a25b4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25b4-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25b4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-173">System-Flags</span></span>           | <span data-ttu-id="a25b4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25b4-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25b4-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25b4-175">Classes used in</span></span>        | [<span data-ttu-id="a25b4-176">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25b4-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a25b4-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a25b4-177">Windows Server 2008</span></span>



| <span data-ttu-id="a25b4-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a25b4-178">Entry</span></span> | <span data-ttu-id="a25b4-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a25b4-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25b4-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25b4-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25b4-182">System-Only</span></span>            | <span data-ttu-id="a25b4-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-183">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25b4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a25b4-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-185">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25b4-186">Is Indexed</span></span>             | <span data-ttu-id="a25b4-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-187">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25b4-188">In Global Catalog</span></span>      | <span data-ttu-id="a25b4-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-189">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25b4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25b4-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25b4-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25b4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25b4-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25b4-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-194">Search-Flags</span></span>           | <span data-ttu-id="a25b4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25b4-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25b4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-196">System-Flags</span></span>           | <span data-ttu-id="a25b4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25b4-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25b4-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25b4-198">Classes used in</span></span>        | [<span data-ttu-id="a25b4-199">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25b4-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a25b4-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a25b4-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a25b4-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a25b4-201">Entry</span></span> | <span data-ttu-id="a25b4-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a25b4-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25b4-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25b4-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25b4-205">System-Only</span></span>            | <span data-ttu-id="a25b4-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-206">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25b4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a25b4-208">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-208">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25b4-209">Is Indexed</span></span>             | <span data-ttu-id="a25b4-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-210">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25b4-211">In Global Catalog</span></span>      | <span data-ttu-id="a25b4-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-212">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25b4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25b4-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25b4-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25b4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25b4-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25b4-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-217">Search-Flags</span></span>           | <span data-ttu-id="a25b4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25b4-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25b4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-219">System-Flags</span></span>           | <span data-ttu-id="a25b4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25b4-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25b4-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25b4-221">Classes used in</span></span>        | [<span data-ttu-id="a25b4-222">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25b4-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a25b4-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a25b4-223">Windows Server 2012</span></span>



| <span data-ttu-id="a25b4-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a25b4-224">Entry</span></span> | <span data-ttu-id="a25b4-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a25b4-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25b4-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25b4-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25b4-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25b4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25b4-228">System-Only</span></span>            | <span data-ttu-id="a25b4-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-229">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25b4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a25b4-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-231">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25b4-232">Is Indexed</span></span>             | <span data-ttu-id="a25b4-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-233">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25b4-234">In Global Catalog</span></span>      | <span data-ttu-id="a25b4-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a25b4-235">False</span></span>                                                                   |
| <span data-ttu-id="a25b4-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25b4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25b4-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25b4-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25b4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25b4-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25b4-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25b4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-240">Search-Flags</span></span>           | <span data-ttu-id="a25b4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25b4-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25b4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25b4-242">System-Flags</span></span>           | <span data-ttu-id="a25b4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25b4-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25b4-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25b4-244">Classes used in</span></span>        | [<span data-ttu-id="a25b4-245">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25b4-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





