---
title: Attributo Signature-Algorithms
description: Questo attributo indica il tipo di algoritmo che deve essere utilizzato per decodificare una firma digitale durante il processo di autenticazione.
ms.assetid: f602a009-6823-42e7-b5e4-fb433535b4cc
ms.tgt_platform: multiple
keywords:
- Schema AD Signature-Algorithms attribute
- Schema AD dell'attributo signatureAlgorithms
topic_type:
- apiref
api_name:
- Signature-Algorithms
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6487155ed8d13735a8201a41c9d1d5b087bb3711
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104225275"
---
# <a name="signature-algorithms-attribute"></a><span data-ttu-id="a4c8f-105">Attributo Signature-Algorithms</span><span class="sxs-lookup"><span data-stu-id="a4c8f-105">Signature-Algorithms attribute</span></span>

<span data-ttu-id="a4c8f-106">Questo attributo indica il tipo di algoritmo che deve essere utilizzato per decodificare una firma digitale durante il processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a4c8f-106">This attribute indicates the type of algorithm that must be used to decode a digital signature during the authentication process.</span></span>



| <span data-ttu-id="a4c8f-107">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-107">Entry</span></span> | <span data-ttu-id="a4c8f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a4c8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="a4c8f-109">CN</span></span>                | <span data-ttu-id="a4c8f-110">Signature-Algorithms</span><span class="sxs-lookup"><span data-stu-id="a4c8f-110">Signature-Algorithms</span></span>                        |
| <span data-ttu-id="a4c8f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a4c8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a4c8f-112">signatureAlgorithms</span><span class="sxs-lookup"><span data-stu-id="a4c8f-112">signatureAlgorithms</span></span>                         |
| <span data-ttu-id="a4c8f-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a4c8f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a4c8f-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a4c8f-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a4c8f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-116">Attribute-Id</span></span>      | <span data-ttu-id="a4c8f-117">1.2.840.113556.1.4.824</span><span class="sxs-lookup"><span data-stu-id="a4c8f-117">1.2.840.113556.1.4.824</span></span>                      |
| <span data-ttu-id="a4c8f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a4c8f-118">System-Id-Guid</span></span>    | <span data-ttu-id="a4c8f-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a4c8f-119">2a39c5b2-8960-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="a4c8f-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4c8f-120">Syntax</span></span>            | [<span data-ttu-id="a4c8f-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a4c8f-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a4c8f-122">Implementations</span></span>

-   [<span data-ttu-id="a4c8f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a4c8f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4c8f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4c8f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4c8f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4c8f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a4c8f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4c8f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="a4c8f-130">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-130">Entry</span></span> | <span data-ttu-id="a4c8f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8f-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-133">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4c8f-134">System-Only</span></span>            | <span data-ttu-id="a4c8f-135">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-135">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4c8f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a4c8f-137">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-137">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4c8f-138">Is Indexed</span></span>             | <span data-ttu-id="a4c8f-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-139">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4c8f-140">In Global Catalog</span></span>      | <span data-ttu-id="a4c8f-141">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-141">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4c8f-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4c8f-143">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="a4c8f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4c8f-144">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4c8f-145">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-146">Search-Flags</span></span>           | <span data-ttu-id="a4c8f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4c8f-147">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-148">System-Flags</span></span>           | <span data-ttu-id="a4c8f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4c8f-149">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4c8f-150">Classes used in</span></span>        | [<span data-ttu-id="a4c8f-151">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="a4c8f-152">**PKI-registrazione-servizio**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-152">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a4c8f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4c8f-153">Windows Server 2003</span></span>



| <span data-ttu-id="a4c8f-154">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-154">Entry</span></span> | <span data-ttu-id="a4c8f-155">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8f-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4c8f-158">System-Only</span></span>            | <span data-ttu-id="a4c8f-159">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4c8f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a4c8f-161">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-161">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4c8f-162">Is Indexed</span></span>             | <span data-ttu-id="a4c8f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4c8f-164">In Global Catalog</span></span>      | <span data-ttu-id="a4c8f-165">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-165">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4c8f-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4c8f-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="a4c8f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4c8f-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4c8f-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-170">Search-Flags</span></span>           | <span data-ttu-id="a4c8f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4c8f-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-172">System-Flags</span></span>           | <span data-ttu-id="a4c8f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4c8f-173">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4c8f-174">Classes used in</span></span>        | [<span data-ttu-id="a4c8f-175">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-175">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="a4c8f-176">**PKI-registrazione-servizio**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-176">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4c8f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4c8f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4c8f-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-178">Entry</span></span> | <span data-ttu-id="a4c8f-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8f-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-180">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-181">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4c8f-182">System-Only</span></span>            | <span data-ttu-id="a4c8f-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-183">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4c8f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a4c8f-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-185">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4c8f-186">Is Indexed</span></span>             | <span data-ttu-id="a4c8f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-187">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4c8f-188">In Global Catalog</span></span>      | <span data-ttu-id="a4c8f-189">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-189">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4c8f-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4c8f-191">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="a4c8f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4c8f-192">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4c8f-193">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-194">Search-Flags</span></span>           | <span data-ttu-id="a4c8f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4c8f-195">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-196">System-Flags</span></span>           | <span data-ttu-id="a4c8f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4c8f-197">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4c8f-198">Classes used in</span></span>        | [<span data-ttu-id="a4c8f-199">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-199">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="a4c8f-200">**PKI-registrazione-servizio**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-200">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a4c8f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4c8f-201">Windows Server 2008</span></span>



| <span data-ttu-id="a4c8f-202">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-202">Entry</span></span> | <span data-ttu-id="a4c8f-203">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8f-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-204">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-205">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4c8f-206">System-Only</span></span>            | <span data-ttu-id="a4c8f-207">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-207">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4c8f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a4c8f-209">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-209">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4c8f-210">Is Indexed</span></span>             | <span data-ttu-id="a4c8f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4c8f-212">In Global Catalog</span></span>      | <span data-ttu-id="a4c8f-213">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-213">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4c8f-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4c8f-215">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="a4c8f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4c8f-216">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4c8f-217">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-218">Search-Flags</span></span>           | <span data-ttu-id="a4c8f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4c8f-219">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-220">System-Flags</span></span>           | <span data-ttu-id="a4c8f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4c8f-221">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4c8f-222">Classes used in</span></span>        | [<span data-ttu-id="a4c8f-223">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-223">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="a4c8f-224">**PKI-registrazione-servizio**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-224">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4c8f-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4c8f-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4c8f-226">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-226">Entry</span></span> | <span data-ttu-id="a4c8f-227">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8f-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-228">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-229">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4c8f-230">System-Only</span></span>            | <span data-ttu-id="a4c8f-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-231">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4c8f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a4c8f-233">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-233">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4c8f-234">Is Indexed</span></span>             | <span data-ttu-id="a4c8f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-235">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4c8f-236">In Global Catalog</span></span>      | <span data-ttu-id="a4c8f-237">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-237">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4c8f-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4c8f-239">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="a4c8f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4c8f-240">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4c8f-241">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-242">Search-Flags</span></span>           | <span data-ttu-id="a4c8f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4c8f-243">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-244">System-Flags</span></span>           | <span data-ttu-id="a4c8f-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4c8f-245">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4c8f-246">Classes used in</span></span>        | [<span data-ttu-id="a4c8f-247">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-247">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="a4c8f-248">**PKI-registrazione-servizio**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-248">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a4c8f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4c8f-249">Windows Server 2012</span></span>



| <span data-ttu-id="a4c8f-250">Voce</span><span class="sxs-lookup"><span data-stu-id="a4c8f-250">Entry</span></span> | <span data-ttu-id="a4c8f-251">Valore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8f-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a4c8f-252">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4c8f-253">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4c8f-254">System-Only</span></span>            | <span data-ttu-id="a4c8f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-255">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a4c8f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="a4c8f-257">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-257">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a4c8f-258">Is Indexed</span></span>             | <span data-ttu-id="a4c8f-259">Falso</span><span class="sxs-lookup"><span data-stu-id="a4c8f-259">False</span></span>                                                                                                                                      |
| <span data-ttu-id="a4c8f-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a4c8f-260">In Global Catalog</span></span>      | <span data-ttu-id="a4c8f-261">Vero</span><span class="sxs-lookup"><span data-stu-id="a4c8f-261">True</span></span>                                                                                                                                       |
| <span data-ttu-id="a4c8f-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a4c8f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4c8f-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a4c8f-263">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="a4c8f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4c8f-264">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4c8f-265">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="a4c8f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-266">Search-Flags</span></span>           | <span data-ttu-id="a4c8f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4c8f-267">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4c8f-268">System-Flags</span></span>           | <span data-ttu-id="a4c8f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4c8f-269">0x00000010</span></span>                                                                                                                                 |
| <span data-ttu-id="a4c8f-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a4c8f-270">Classes used in</span></span>        | [<span data-ttu-id="a4c8f-271">**Autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-271">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="a4c8f-272">**PKI-registrazione-servizio**</span><span class="sxs-lookup"><span data-stu-id="a4c8f-272">**PKI-Enrollment-Service**</span></span>](c-pkienrollmentservice.md)<br/> |



 

 





