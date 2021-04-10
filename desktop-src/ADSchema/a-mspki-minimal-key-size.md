---
title: attributo ms-PKI-minimal-key-size
description: Indica la dimensione minima della chiave privata.
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-PKI-minimal-size
- msPKI-schema AD dell'attributo con dimensione minima della chiave
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122466"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="9677f-105">attributo ms-PKI-minimal-key-size</span><span class="sxs-lookup"><span data-stu-id="9677f-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="9677f-106">Indica la dimensione minima della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="9677f-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="9677f-107">Voce</span><span class="sxs-lookup"><span data-stu-id="9677f-107">Entry</span></span> | <span data-ttu-id="9677f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9677f-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9677f-109">CN</span><span class="sxs-lookup"><span data-stu-id="9677f-109">CN</span></span>                | <span data-ttu-id="9677f-110">ms-PKI-minimo-chiave-dimensioni</span><span class="sxs-lookup"><span data-stu-id="9677f-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="9677f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9677f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9677f-112">msPKI-minime-chiave-dimensioni</span><span class="sxs-lookup"><span data-stu-id="9677f-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="9677f-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9677f-113">Size</span></span>              | <span data-ttu-id="9677f-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="9677f-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="9677f-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9677f-115">Update Privilege</span></span>  | <span data-ttu-id="9677f-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="9677f-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="9677f-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9677f-117">Update Frequency</span></span>  | <span data-ttu-id="9677f-118">Quando l'oggetto modello di certificato (ms-PKI-certificate-template) viene modificato, creato o clonato.</span><span class="sxs-lookup"><span data-stu-id="9677f-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="9677f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9677f-119">Attribute-Id</span></span>      | <span data-ttu-id="9677f-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="9677f-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="9677f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9677f-121">System-Id-Guid</span></span>    | <span data-ttu-id="9677f-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="9677f-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="9677f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9677f-123">Syntax</span></span>            | [<span data-ttu-id="9677f-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="9677f-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="9677f-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9677f-125">Implementations</span></span>

-   [<span data-ttu-id="9677f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9677f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9677f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9677f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9677f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9677f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9677f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9677f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9677f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9677f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9677f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9677f-131">Windows Server 2003</span></span>



| <span data-ttu-id="9677f-132">Voce</span><span class="sxs-lookup"><span data-stu-id="9677f-132">Entry</span></span> | <span data-ttu-id="9677f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9677f-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9677f-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9677f-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9677f-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9677f-136">System-Only</span></span>            | <span data-ttu-id="9677f-137">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-137">False</span></span>                                                                   |
| <span data-ttu-id="9677f-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9677f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9677f-139">Vero</span><span class="sxs-lookup"><span data-stu-id="9677f-139">True</span></span>                                                                    |
| <span data-ttu-id="9677f-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9677f-140">Is Indexed</span></span>             | <span data-ttu-id="9677f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-141">False</span></span>                                                                   |
| <span data-ttu-id="9677f-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9677f-142">In Global Catalog</span></span>      | <span data-ttu-id="9677f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-143">False</span></span>                                                                   |
| <span data-ttu-id="9677f-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9677f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9677f-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9677f-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9677f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9677f-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9677f-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-148">Search-Flags</span></span>           | <span data-ttu-id="9677f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9677f-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="9677f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-150">System-Flags</span></span>           | <span data-ttu-id="9677f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9677f-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="9677f-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9677f-152">Classes used in</span></span>        | [<span data-ttu-id="9677f-153">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="9677f-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9677f-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9677f-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9677f-155">Voce</span><span class="sxs-lookup"><span data-stu-id="9677f-155">Entry</span></span> | <span data-ttu-id="9677f-156">Valore</span><span class="sxs-lookup"><span data-stu-id="9677f-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9677f-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9677f-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9677f-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9677f-159">System-Only</span></span>            | <span data-ttu-id="9677f-160">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-160">False</span></span>                                                                   |
| <span data-ttu-id="9677f-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9677f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9677f-162">Vero</span><span class="sxs-lookup"><span data-stu-id="9677f-162">True</span></span>                                                                    |
| <span data-ttu-id="9677f-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9677f-163">Is Indexed</span></span>             | <span data-ttu-id="9677f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-164">False</span></span>                                                                   |
| <span data-ttu-id="9677f-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9677f-165">In Global Catalog</span></span>      | <span data-ttu-id="9677f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-166">False</span></span>                                                                   |
| <span data-ttu-id="9677f-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9677f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9677f-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9677f-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9677f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9677f-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9677f-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-171">Search-Flags</span></span>           | <span data-ttu-id="9677f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9677f-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="9677f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-173">System-Flags</span></span>           | <span data-ttu-id="9677f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9677f-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="9677f-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9677f-175">Classes used in</span></span>        | [<span data-ttu-id="9677f-176">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="9677f-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9677f-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9677f-177">Windows Server 2008</span></span>



| <span data-ttu-id="9677f-178">Voce</span><span class="sxs-lookup"><span data-stu-id="9677f-178">Entry</span></span> | <span data-ttu-id="9677f-179">Valore</span><span class="sxs-lookup"><span data-stu-id="9677f-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9677f-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9677f-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9677f-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9677f-182">System-Only</span></span>            | <span data-ttu-id="9677f-183">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-183">False</span></span>                                                                   |
| <span data-ttu-id="9677f-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9677f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9677f-185">Vero</span><span class="sxs-lookup"><span data-stu-id="9677f-185">True</span></span>                                                                    |
| <span data-ttu-id="9677f-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9677f-186">Is Indexed</span></span>             | <span data-ttu-id="9677f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-187">False</span></span>                                                                   |
| <span data-ttu-id="9677f-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9677f-188">In Global Catalog</span></span>      | <span data-ttu-id="9677f-189">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-189">False</span></span>                                                                   |
| <span data-ttu-id="9677f-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9677f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9677f-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9677f-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9677f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9677f-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9677f-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-194">Search-Flags</span></span>           | <span data-ttu-id="9677f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9677f-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="9677f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-196">System-Flags</span></span>           | <span data-ttu-id="9677f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9677f-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="9677f-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9677f-198">Classes used in</span></span>        | [<span data-ttu-id="9677f-199">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="9677f-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9677f-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9677f-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9677f-201">Voce</span><span class="sxs-lookup"><span data-stu-id="9677f-201">Entry</span></span> | <span data-ttu-id="9677f-202">Valore</span><span class="sxs-lookup"><span data-stu-id="9677f-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9677f-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9677f-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9677f-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9677f-205">System-Only</span></span>            | <span data-ttu-id="9677f-206">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-206">False</span></span>                                                                   |
| <span data-ttu-id="9677f-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9677f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9677f-208">Vero</span><span class="sxs-lookup"><span data-stu-id="9677f-208">True</span></span>                                                                    |
| <span data-ttu-id="9677f-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9677f-209">Is Indexed</span></span>             | <span data-ttu-id="9677f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-210">False</span></span>                                                                   |
| <span data-ttu-id="9677f-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9677f-211">In Global Catalog</span></span>      | <span data-ttu-id="9677f-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-212">False</span></span>                                                                   |
| <span data-ttu-id="9677f-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9677f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9677f-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9677f-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9677f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9677f-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9677f-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-217">Search-Flags</span></span>           | <span data-ttu-id="9677f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9677f-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="9677f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-219">System-Flags</span></span>           | <span data-ttu-id="9677f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9677f-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="9677f-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9677f-221">Classes used in</span></span>        | [<span data-ttu-id="9677f-222">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="9677f-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9677f-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9677f-223">Windows Server 2012</span></span>



| <span data-ttu-id="9677f-224">Voce</span><span class="sxs-lookup"><span data-stu-id="9677f-224">Entry</span></span> | <span data-ttu-id="9677f-225">Valore</span><span class="sxs-lookup"><span data-stu-id="9677f-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9677f-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9677f-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9677f-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="9677f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9677f-228">System-Only</span></span>            | <span data-ttu-id="9677f-229">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-229">False</span></span>                                                                   |
| <span data-ttu-id="9677f-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9677f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9677f-231">Vero</span><span class="sxs-lookup"><span data-stu-id="9677f-231">True</span></span>                                                                    |
| <span data-ttu-id="9677f-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9677f-232">Is Indexed</span></span>             | <span data-ttu-id="9677f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-233">False</span></span>                                                                   |
| <span data-ttu-id="9677f-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9677f-234">In Global Catalog</span></span>      | <span data-ttu-id="9677f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9677f-235">False</span></span>                                                                   |
| <span data-ttu-id="9677f-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9677f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9677f-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9677f-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="9677f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9677f-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9677f-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="9677f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-240">Search-Flags</span></span>           | <span data-ttu-id="9677f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9677f-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="9677f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9677f-242">System-Flags</span></span>           | <span data-ttu-id="9677f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9677f-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="9677f-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9677f-244">Classes used in</span></span>        | [<span data-ttu-id="9677f-245">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="9677f-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





