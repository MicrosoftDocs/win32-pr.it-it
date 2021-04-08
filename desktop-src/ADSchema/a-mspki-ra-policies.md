---
title: attributo ms-PKI-RA-Policies
description: Contiene l'elenco di OID di criteri richiesti dalle autorità di registrazione che firmano la richiesta di registrazione.
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-PKI-RA-Policies
- Schema AD dell'attributo msPKI-RA-Policies
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965368"
---
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="a25fb-105">attributo ms-PKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="a25fb-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="a25fb-106">Contiene l'elenco di OID di criteri richiesti dalle autorità di registrazione che firmano la richiesta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a25fb-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="a25fb-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a25fb-107">Entry</span></span> | <span data-ttu-id="a25fb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a25fb-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25fb-109">CN</span><span class="sxs-lookup"><span data-stu-id="a25fb-109">CN</span></span>                | <span data-ttu-id="a25fb-110">ms-PKI-RA-criteri</span><span class="sxs-lookup"><span data-stu-id="a25fb-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="a25fb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a25fb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a25fb-112">msPKI-RA-criteri</span><span class="sxs-lookup"><span data-stu-id="a25fb-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="a25fb-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a25fb-113">Size</span></span>              | <span data-ttu-id="a25fb-114">64 byte per il numero di voci.</span><span class="sxs-lookup"><span data-stu-id="a25fb-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="a25fb-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-115">Update Privilege</span></span>  | <span data-ttu-id="a25fb-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="a25fb-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="a25fb-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-117">Update Frequency</span></span>  | <span data-ttu-id="a25fb-118">Quando l'oggetto modello di certificato (ms-PKI-certificate-template) viene modificato, creato o clonato.</span><span class="sxs-lookup"><span data-stu-id="a25fb-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="a25fb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a25fb-119">Attribute-Id</span></span>      | <span data-ttu-id="a25fb-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="a25fb-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="a25fb-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a25fb-121">System-Id-Guid</span></span>    | <span data-ttu-id="a25fb-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="a25fb-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="a25fb-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a25fb-123">Syntax</span></span>            | [<span data-ttu-id="a25fb-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a25fb-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="a25fb-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a25fb-125">Implementations</span></span>

-   [<span data-ttu-id="a25fb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a25fb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a25fb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a25fb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a25fb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a25fb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a25fb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a25fb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a25fb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a25fb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a25fb-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a25fb-131">Windows Server 2003</span></span>



| <span data-ttu-id="a25fb-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a25fb-132">Entry</span></span> | <span data-ttu-id="a25fb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a25fb-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25fb-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25fb-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25fb-136">System-Only</span></span>            | <span data-ttu-id="a25fb-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-137">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25fb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a25fb-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-139">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25fb-140">Is Indexed</span></span>             | <span data-ttu-id="a25fb-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-141">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25fb-142">In Global Catalog</span></span>      | <span data-ttu-id="a25fb-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-143">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25fb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25fb-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25fb-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25fb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25fb-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25fb-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-148">Search-Flags</span></span>           | <span data-ttu-id="a25fb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25fb-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25fb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-150">System-Flags</span></span>           | <span data-ttu-id="a25fb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25fb-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25fb-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25fb-152">Classes used in</span></span>        | [<span data-ttu-id="a25fb-153">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25fb-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a25fb-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a25fb-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a25fb-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a25fb-155">Entry</span></span> | <span data-ttu-id="a25fb-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a25fb-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25fb-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25fb-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25fb-159">System-Only</span></span>            | <span data-ttu-id="a25fb-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-160">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25fb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a25fb-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-162">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25fb-163">Is Indexed</span></span>             | <span data-ttu-id="a25fb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-164">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25fb-165">In Global Catalog</span></span>      | <span data-ttu-id="a25fb-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-166">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25fb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25fb-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25fb-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25fb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25fb-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25fb-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-171">Search-Flags</span></span>           | <span data-ttu-id="a25fb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25fb-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25fb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-173">System-Flags</span></span>           | <span data-ttu-id="a25fb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25fb-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25fb-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25fb-175">Classes used in</span></span>        | [<span data-ttu-id="a25fb-176">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25fb-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a25fb-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a25fb-177">Windows Server 2008</span></span>



| <span data-ttu-id="a25fb-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a25fb-178">Entry</span></span> | <span data-ttu-id="a25fb-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a25fb-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25fb-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25fb-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25fb-182">System-Only</span></span>            | <span data-ttu-id="a25fb-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-183">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25fb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a25fb-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-185">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25fb-186">Is Indexed</span></span>             | <span data-ttu-id="a25fb-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-187">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25fb-188">In Global Catalog</span></span>      | <span data-ttu-id="a25fb-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-189">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25fb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25fb-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25fb-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25fb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25fb-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25fb-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-194">Search-Flags</span></span>           | <span data-ttu-id="a25fb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25fb-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25fb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-196">System-Flags</span></span>           | <span data-ttu-id="a25fb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25fb-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25fb-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25fb-198">Classes used in</span></span>        | [<span data-ttu-id="a25fb-199">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25fb-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a25fb-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a25fb-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a25fb-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a25fb-201">Entry</span></span> | <span data-ttu-id="a25fb-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a25fb-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25fb-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25fb-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25fb-205">System-Only</span></span>            | <span data-ttu-id="a25fb-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-206">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25fb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a25fb-208">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-208">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25fb-209">Is Indexed</span></span>             | <span data-ttu-id="a25fb-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-210">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25fb-211">In Global Catalog</span></span>      | <span data-ttu-id="a25fb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-212">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25fb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25fb-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25fb-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25fb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25fb-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25fb-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-217">Search-Flags</span></span>           | <span data-ttu-id="a25fb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25fb-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25fb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-219">System-Flags</span></span>           | <span data-ttu-id="a25fb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25fb-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25fb-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25fb-221">Classes used in</span></span>        | [<span data-ttu-id="a25fb-222">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25fb-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a25fb-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a25fb-223">Windows Server 2012</span></span>



| <span data-ttu-id="a25fb-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a25fb-224">Entry</span></span> | <span data-ttu-id="a25fb-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a25fb-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a25fb-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a25fb-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a25fb-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a25fb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a25fb-228">System-Only</span></span>            | <span data-ttu-id="a25fb-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-229">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a25fb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a25fb-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-231">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a25fb-232">Is Indexed</span></span>             | <span data-ttu-id="a25fb-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-233">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a25fb-234">In Global Catalog</span></span>      | <span data-ttu-id="a25fb-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a25fb-235">False</span></span>                                                                   |
| <span data-ttu-id="a25fb-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a25fb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a25fb-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a25fb-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a25fb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a25fb-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a25fb-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a25fb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-240">Search-Flags</span></span>           | <span data-ttu-id="a25fb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a25fb-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="a25fb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a25fb-242">System-Flags</span></span>           | <span data-ttu-id="a25fb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a25fb-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="a25fb-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a25fb-244">Classes used in</span></span>        | [<span data-ttu-id="a25fb-245">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a25fb-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





