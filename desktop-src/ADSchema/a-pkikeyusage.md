---
title: Attributo PKI-Key-Usage
description: Estensione utilizzo chiave per il modello di certificato.
ms.assetid: 9b3bb28e-7519-4911-9777-f9612bff2d51
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo PKI-Key-Usage
- Schema AD dell'attributo pKIKeyUsage
topic_type:
- apiref
api_name:
- PKI-Key-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08c5c5b72091060fb475f3becba4f230293c875
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875190"
---
# <a name="pki-key-usage-attribute"></a><span data-ttu-id="4f95d-105">Attributo PKI-Key-Usage</span><span class="sxs-lookup"><span data-stu-id="4f95d-105">PKI-Key-Usage attribute</span></span>

<span data-ttu-id="4f95d-106">Estensione utilizzo chiave per il modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="4f95d-106">The key usage extension for the certificate template.</span></span>



| <span data-ttu-id="4f95d-107">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-107">Entry</span></span> | <span data-ttu-id="4f95d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4f95d-109">CN</span><span class="sxs-lookup"><span data-stu-id="4f95d-109">CN</span></span>                | <span data-ttu-id="4f95d-110">Utilizzo chiave PKI</span><span class="sxs-lookup"><span data-stu-id="4f95d-110">PKI-Key-Usage</span></span>                                         |
| <span data-ttu-id="4f95d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f95d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4f95d-112">pKIKeyUsage</span><span class="sxs-lookup"><span data-stu-id="4f95d-112">pKIKeyUsage</span></span>                                           |
| <span data-ttu-id="4f95d-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4f95d-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4f95d-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="4f95d-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="4f95d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-116">Attribute-Id</span></span>      | <span data-ttu-id="4f95d-117">1.2.840.113556.1.4.1328</span><span class="sxs-lookup"><span data-stu-id="4f95d-117">1.2.840.113556.1.4.1328</span></span>                               |
| <span data-ttu-id="4f95d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f95d-118">System-Id-Guid</span></span>    | <span data-ttu-id="4f95d-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="4f95d-119">e9b0a87e-3b9d-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="4f95d-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f95d-120">Syntax</span></span>            | [<span data-ttu-id="4f95d-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="4f95d-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4f95d-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4f95d-122">Implementations</span></span>

-   [<span data-ttu-id="4f95d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4f95d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4f95d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f95d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f95d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f95d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f95d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f95d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f95d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f95d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f95d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f95d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4f95d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f95d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="4f95d-130">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-130">Entry</span></span> | <span data-ttu-id="4f95d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4f95d-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f95d-134">System-Only</span></span>            | <span data-ttu-id="4f95d-135">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-135">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4f95d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="4f95d-137">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-137">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4f95d-138">Is Indexed</span></span>             | <span data-ttu-id="4f95d-139">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-139">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4f95d-140">In Global Catalog</span></span>      | <span data-ttu-id="4f95d-141">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-141">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4f95d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f95d-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4f95d-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4f95d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f95d-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f95d-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-146">Search-Flags</span></span>           | <span data-ttu-id="4f95d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f95d-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="4f95d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-148">System-Flags</span></span>           | <span data-ttu-id="4f95d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f95d-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="4f95d-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4f95d-150">Classes used in</span></span>        | [<span data-ttu-id="4f95d-151">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="4f95d-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4f95d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f95d-152">Windows Server 2003</span></span>



| <span data-ttu-id="4f95d-153">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-153">Entry</span></span> | <span data-ttu-id="4f95d-154">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4f95d-155">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f95d-157">System-Only</span></span>            | <span data-ttu-id="4f95d-158">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-158">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-159">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4f95d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="4f95d-160">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-160">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-161">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4f95d-161">Is Indexed</span></span>             | <span data-ttu-id="4f95d-162">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-162">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-163">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4f95d-163">In Global Catalog</span></span>      | <span data-ttu-id="4f95d-164">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-164">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-165">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4f95d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f95d-166">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4f95d-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4f95d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f95d-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f95d-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-169">Search-Flags</span></span>           | <span data-ttu-id="4f95d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f95d-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="4f95d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-171">System-Flags</span></span>           | <span data-ttu-id="4f95d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f95d-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="4f95d-173">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4f95d-173">Classes used in</span></span>        | [<span data-ttu-id="4f95d-174">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="4f95d-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f95d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f95d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f95d-176">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-176">Entry</span></span> | <span data-ttu-id="4f95d-177">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4f95d-178">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f95d-180">System-Only</span></span>            | <span data-ttu-id="4f95d-181">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-181">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-182">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4f95d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="4f95d-183">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-183">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-184">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4f95d-184">Is Indexed</span></span>             | <span data-ttu-id="4f95d-185">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-185">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-186">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4f95d-186">In Global Catalog</span></span>      | <span data-ttu-id="4f95d-187">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-187">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-188">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4f95d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f95d-189">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4f95d-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4f95d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f95d-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f95d-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-192">Search-Flags</span></span>           | <span data-ttu-id="4f95d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f95d-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="4f95d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-194">System-Flags</span></span>           | <span data-ttu-id="4f95d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f95d-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="4f95d-196">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4f95d-196">Classes used in</span></span>        | [<span data-ttu-id="4f95d-197">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="4f95d-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f95d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f95d-198">Windows Server 2008</span></span>



| <span data-ttu-id="4f95d-199">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-199">Entry</span></span> | <span data-ttu-id="4f95d-200">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4f95d-201">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f95d-203">System-Only</span></span>            | <span data-ttu-id="4f95d-204">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-204">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-205">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4f95d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="4f95d-206">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-206">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-207">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4f95d-207">Is Indexed</span></span>             | <span data-ttu-id="4f95d-208">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-208">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-209">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4f95d-209">In Global Catalog</span></span>      | <span data-ttu-id="4f95d-210">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-210">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-211">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4f95d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f95d-212">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4f95d-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4f95d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f95d-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f95d-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-215">Search-Flags</span></span>           | <span data-ttu-id="4f95d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f95d-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="4f95d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-217">System-Flags</span></span>           | <span data-ttu-id="4f95d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f95d-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="4f95d-219">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4f95d-219">Classes used in</span></span>        | [<span data-ttu-id="4f95d-220">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="4f95d-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f95d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f95d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f95d-222">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-222">Entry</span></span> | <span data-ttu-id="4f95d-223">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4f95d-224">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f95d-226">System-Only</span></span>            | <span data-ttu-id="4f95d-227">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-227">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-228">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4f95d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="4f95d-229">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-229">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-230">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4f95d-230">Is Indexed</span></span>             | <span data-ttu-id="4f95d-231">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-231">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-232">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4f95d-232">In Global Catalog</span></span>      | <span data-ttu-id="4f95d-233">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-233">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-234">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4f95d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f95d-235">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4f95d-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4f95d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f95d-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f95d-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-238">Search-Flags</span></span>           | <span data-ttu-id="4f95d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f95d-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="4f95d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-240">System-Flags</span></span>           | <span data-ttu-id="4f95d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f95d-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="4f95d-242">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4f95d-242">Classes used in</span></span>        | [<span data-ttu-id="4f95d-243">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="4f95d-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f95d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f95d-244">Windows Server 2012</span></span>



| <span data-ttu-id="4f95d-245">Voce</span><span class="sxs-lookup"><span data-stu-id="4f95d-245">Entry</span></span> | <span data-ttu-id="4f95d-246">Valore</span><span class="sxs-lookup"><span data-stu-id="4f95d-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4f95d-247">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4f95d-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f95d-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="4f95d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f95d-249">System-Only</span></span>            | <span data-ttu-id="4f95d-250">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-250">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-251">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4f95d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="4f95d-252">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-252">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-253">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4f95d-253">Is Indexed</span></span>             | <span data-ttu-id="4f95d-254">Falso</span><span class="sxs-lookup"><span data-stu-id="4f95d-254">False</span></span>                                                                   |
| <span data-ttu-id="4f95d-255">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4f95d-255">In Global Catalog</span></span>      | <span data-ttu-id="4f95d-256">Vero</span><span class="sxs-lookup"><span data-stu-id="4f95d-256">True</span></span>                                                                    |
| <span data-ttu-id="4f95d-257">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4f95d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f95d-258">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4f95d-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="4f95d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f95d-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f95d-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="4f95d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-261">Search-Flags</span></span>           | <span data-ttu-id="4f95d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f95d-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="4f95d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f95d-263">System-Flags</span></span>           | <span data-ttu-id="4f95d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f95d-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="4f95d-265">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4f95d-265">Classes used in</span></span>        | [<span data-ttu-id="4f95d-266">**PKI-certificate-template**</span><span class="sxs-lookup"><span data-stu-id="4f95d-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





