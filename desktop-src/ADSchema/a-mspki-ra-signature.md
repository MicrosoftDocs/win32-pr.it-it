---
title: attributo ms-PKI-RA-Signature
description: Specifica il numero di firme dell'autorità di registrazione delle registrazioni richieste in una richiesta di registrazione.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-PKI-RA-Signature
- Schema AD dell'attributo msPKI-RA-Signature
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303211"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="a5a4a-105">attributo ms-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="a5a4a-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="a5a4a-106">Specifica il numero di firme dell'autorità di registrazione delle registrazioni richieste in una richiesta di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a5a4a-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="a5a4a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a5a4a-107">Entry</span></span> | <span data-ttu-id="a5a4a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a4a-109">CN</span><span class="sxs-lookup"><span data-stu-id="a5a4a-109">CN</span></span>                | <span data-ttu-id="a5a4a-110">ms-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="a5a4a-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="a5a4a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a5a4a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a5a4a-112">msPKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="a5a4a-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="a5a4a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a5a4a-113">Size</span></span>              | <span data-ttu-id="a5a4a-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="a5a4a-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="a5a4a-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-115">Update Privilege</span></span>  | <span data-ttu-id="a5a4a-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="a5a4a-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="a5a4a-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-117">Update Frequency</span></span>  | <span data-ttu-id="a5a4a-118">Quando l'oggetto modello di certificato (ms-PKI-certificate-template) viene modificato, creato o clonato.</span><span class="sxs-lookup"><span data-stu-id="a5a4a-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="a5a4a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5a4a-119">Attribute-Id</span></span>      | <span data-ttu-id="a5a4a-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="a5a4a-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="a5a4a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a5a4a-121">System-Id-Guid</span></span>    | <span data-ttu-id="a5a4a-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="a5a4a-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="a5a4a-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5a4a-123">Syntax</span></span>            | [<span data-ttu-id="a5a4a-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="a5a4a-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a5a4a-125">Implementations</span></span>

-   [<span data-ttu-id="a5a4a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5a4a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5a4a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5a4a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5a4a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a5a4a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5a4a-131">Windows Server 2003</span></span>



| <span data-ttu-id="a5a4a-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a5a4a-132">Entry</span></span> | <span data-ttu-id="a5a4a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a5a4a-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5a4a-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5a4a-136">System-Only</span></span>            | <span data-ttu-id="a5a4a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-137">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5a4a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a5a4a-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a5a4a-139">True</span></span>                                                                    |
| <span data-ttu-id="a5a4a-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5a4a-140">Is Indexed</span></span>             | <span data-ttu-id="a5a4a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-141">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5a4a-142">In Global Catalog</span></span>      | <span data-ttu-id="a5a4a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-143">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5a4a-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5a4a-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a5a4a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5a4a-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5a4a-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-148">Search-Flags</span></span>           | <span data-ttu-id="a5a4a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5a4a-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="a5a4a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-150">System-Flags</span></span>           | <span data-ttu-id="a5a4a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5a4a-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="a5a4a-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5a4a-152">Classes used in</span></span>        | [<span data-ttu-id="a5a4a-153">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5a4a-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5a4a-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5a4a-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a5a4a-155">Entry</span></span> | <span data-ttu-id="a5a4a-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a5a4a-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5a4a-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5a4a-159">System-Only</span></span>            | <span data-ttu-id="a5a4a-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-160">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5a4a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a5a4a-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a5a4a-162">True</span></span>                                                                    |
| <span data-ttu-id="a5a4a-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5a4a-163">Is Indexed</span></span>             | <span data-ttu-id="a5a4a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-164">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5a4a-165">In Global Catalog</span></span>      | <span data-ttu-id="a5a4a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-166">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5a4a-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5a4a-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a5a4a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5a4a-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5a4a-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-171">Search-Flags</span></span>           | <span data-ttu-id="a5a4a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5a4a-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="a5a4a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-173">System-Flags</span></span>           | <span data-ttu-id="a5a4a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5a4a-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="a5a4a-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5a4a-175">Classes used in</span></span>        | [<span data-ttu-id="a5a4a-176">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5a4a-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5a4a-177">Windows Server 2008</span></span>



| <span data-ttu-id="a5a4a-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a5a4a-178">Entry</span></span> | <span data-ttu-id="a5a4a-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a5a4a-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5a4a-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5a4a-182">System-Only</span></span>            | <span data-ttu-id="a5a4a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-183">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5a4a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a5a4a-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a5a4a-185">True</span></span>                                                                    |
| <span data-ttu-id="a5a4a-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5a4a-186">Is Indexed</span></span>             | <span data-ttu-id="a5a4a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-187">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5a4a-188">In Global Catalog</span></span>      | <span data-ttu-id="a5a4a-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-189">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5a4a-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5a4a-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a5a4a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5a4a-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5a4a-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-194">Search-Flags</span></span>           | <span data-ttu-id="a5a4a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5a4a-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="a5a4a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-196">System-Flags</span></span>           | <span data-ttu-id="a5a4a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5a4a-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="a5a4a-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5a4a-198">Classes used in</span></span>        | [<span data-ttu-id="a5a4a-199">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5a4a-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5a4a-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5a4a-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a5a4a-201">Entry</span></span> | <span data-ttu-id="a5a4a-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a5a4a-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5a4a-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5a4a-205">System-Only</span></span>            | <span data-ttu-id="a5a4a-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-206">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5a4a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a5a4a-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a5a4a-208">True</span></span>                                                                    |
| <span data-ttu-id="a5a4a-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5a4a-209">Is Indexed</span></span>             | <span data-ttu-id="a5a4a-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-210">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5a4a-211">In Global Catalog</span></span>      | <span data-ttu-id="a5a4a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-212">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5a4a-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5a4a-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a5a4a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5a4a-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5a4a-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-217">Search-Flags</span></span>           | <span data-ttu-id="a5a4a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5a4a-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="a5a4a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-219">System-Flags</span></span>           | <span data-ttu-id="a5a4a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5a4a-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="a5a4a-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5a4a-221">Classes used in</span></span>        | [<span data-ttu-id="a5a4a-222">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5a4a-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5a4a-223">Windows Server 2012</span></span>



| <span data-ttu-id="a5a4a-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a5a4a-224">Entry</span></span> | <span data-ttu-id="a5a4a-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a5a4a-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a5a4a-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5a4a-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="a5a4a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5a4a-228">System-Only</span></span>            | <span data-ttu-id="a5a4a-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-229">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a5a4a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a5a4a-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a5a4a-231">True</span></span>                                                                    |
| <span data-ttu-id="a5a4a-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a5a4a-232">Is Indexed</span></span>             | <span data-ttu-id="a5a4a-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-233">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a5a4a-234">In Global Catalog</span></span>      | <span data-ttu-id="a5a4a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a5a4a-235">False</span></span>                                                                   |
| <span data-ttu-id="a5a4a-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a5a4a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5a4a-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a5a4a-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="a5a4a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5a4a-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5a4a-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="a5a4a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-240">Search-Flags</span></span>           | <span data-ttu-id="a5a4a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5a4a-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="a5a4a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5a4a-242">System-Flags</span></span>           | <span data-ttu-id="a5a4a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5a4a-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="a5a4a-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a5a4a-244">Classes used in</span></span>        | [<span data-ttu-id="a5a4a-245">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="a5a4a-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





