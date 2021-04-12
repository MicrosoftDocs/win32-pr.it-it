---
title: Default-Security-Descriptor-attributo
description: Descrittore di sicurezza da assegnare all'oggetto quando viene creato per la prima volta.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo default-Security-Descriptor
- Schema AD dell'attributo defaultSecurityDescriptor
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479736"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="2de5e-105">Default-Security-Descriptor-attributo</span><span class="sxs-lookup"><span data-stu-id="2de5e-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="2de5e-106">Descrittore di sicurezza da assegnare all'oggetto quando viene creato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="2de5e-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="2de5e-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-107">Entry</span></span> | <span data-ttu-id="2de5e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2de5e-109">CN</span><span class="sxs-lookup"><span data-stu-id="2de5e-109">CN</span></span>                | <span data-ttu-id="2de5e-110">Descrittore di sicurezza predefinito</span><span class="sxs-lookup"><span data-stu-id="2de5e-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="2de5e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2de5e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2de5e-112">defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="2de5e-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="2de5e-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2de5e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2de5e-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-114">Update Privilege</span></span>  | <span data-ttu-id="2de5e-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="2de5e-115">Schema administrator</span></span>                        |
| <span data-ttu-id="2de5e-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2de5e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-117">Attribute-Id</span></span>      | <span data-ttu-id="2de5e-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="2de5e-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="2de5e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2de5e-119">System-Id-Guid</span></span>    | <span data-ttu-id="2de5e-120">807a6d30-1669-11d0-a064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="2de5e-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="2de5e-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2de5e-121">Syntax</span></span>            | [<span data-ttu-id="2de5e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2de5e-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2de5e-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2de5e-123">Implementations</span></span>

-   [<span data-ttu-id="2de5e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2de5e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2de5e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2de5e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2de5e-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2de5e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2de5e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2de5e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2de5e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2de5e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2de5e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2de5e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2de5e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2de5e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2de5e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2de5e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2de5e-132">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-132">Entry</span></span> | <span data-ttu-id="2de5e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-136">System-Only</span></span>            | <span data-ttu-id="2de5e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-137">False</span></span>                                            |
| <span data-ttu-id="2de5e-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-139">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-139">True</span></span>                                             |
| <span data-ttu-id="2de5e-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-140">Is Indexed</span></span>             | <span data-ttu-id="2de5e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-141">False</span></span>                                            |
| <span data-ttu-id="2de5e-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-142">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-143">False</span></span>                                            |
| <span data-ttu-id="2de5e-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-146">Range-Lower</span></span>            | <span data-ttu-id="2de5e-147">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-147">0</span></span>                                                |
| <span data-ttu-id="2de5e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-148">Range-Upper</span></span>            | <span data-ttu-id="2de5e-149">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-149">32767</span></span>                                            |
| <span data-ttu-id="2de5e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-150">Search-Flags</span></span>           | <span data-ttu-id="2de5e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-151">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-152">System-Flags</span></span>           | <span data-ttu-id="2de5e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-153">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-154">Classes used in</span></span>        | [<span data-ttu-id="2de5e-155">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2de5e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2de5e-156">Windows Server 2003</span></span>



| <span data-ttu-id="2de5e-157">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-157">Entry</span></span> | <span data-ttu-id="2de5e-158">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-161">System-Only</span></span>            | <span data-ttu-id="2de5e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-162">False</span></span>                                            |
| <span data-ttu-id="2de5e-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-164">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-164">True</span></span>                                             |
| <span data-ttu-id="2de5e-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-165">Is Indexed</span></span>             | <span data-ttu-id="2de5e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-166">False</span></span>                                            |
| <span data-ttu-id="2de5e-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-167">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-168">False</span></span>                                            |
| <span data-ttu-id="2de5e-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-171">Range-Lower</span></span>            | <span data-ttu-id="2de5e-172">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-172">0</span></span>                                                |
| <span data-ttu-id="2de5e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-173">Range-Upper</span></span>            | <span data-ttu-id="2de5e-174">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-174">32767</span></span>                                            |
| <span data-ttu-id="2de5e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-175">Search-Flags</span></span>           | <span data-ttu-id="2de5e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-176">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-177">System-Flags</span></span>           | <span data-ttu-id="2de5e-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-178">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-179">Classes used in</span></span>        | [<span data-ttu-id="2de5e-180">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2de5e-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="2de5e-181">ADAM</span></span>



| <span data-ttu-id="2de5e-182">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-182">Entry</span></span> | <span data-ttu-id="2de5e-183">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-186">System-Only</span></span>            | <span data-ttu-id="2de5e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-187">False</span></span>                                            |
| <span data-ttu-id="2de5e-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-189">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-189">True</span></span>                                             |
| <span data-ttu-id="2de5e-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-190">Is Indexed</span></span>             | <span data-ttu-id="2de5e-191">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-191">False</span></span>                                            |
| <span data-ttu-id="2de5e-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-192">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-193">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-193">False</span></span>                                            |
| <span data-ttu-id="2de5e-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-196">Range-Lower</span></span>            | <span data-ttu-id="2de5e-197">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-197">0</span></span>                                                |
| <span data-ttu-id="2de5e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-198">Range-Upper</span></span>            | <span data-ttu-id="2de5e-199">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-199">32767</span></span>                                            |
| <span data-ttu-id="2de5e-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-200">Search-Flags</span></span>           | <span data-ttu-id="2de5e-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-201">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-202">System-Flags</span></span>           | <span data-ttu-id="2de5e-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-203">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-204">Classes used in</span></span>        | [<span data-ttu-id="2de5e-205">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2de5e-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2de5e-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2de5e-207">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-207">Entry</span></span> | <span data-ttu-id="2de5e-208">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-211">System-Only</span></span>            | <span data-ttu-id="2de5e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-212">False</span></span>                                            |
| <span data-ttu-id="2de5e-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-214">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-214">True</span></span>                                             |
| <span data-ttu-id="2de5e-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-215">Is Indexed</span></span>             | <span data-ttu-id="2de5e-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-216">False</span></span>                                            |
| <span data-ttu-id="2de5e-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-217">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-218">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-218">False</span></span>                                            |
| <span data-ttu-id="2de5e-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-221">Range-Lower</span></span>            | <span data-ttu-id="2de5e-222">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-222">0</span></span>                                                |
| <span data-ttu-id="2de5e-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-223">Range-Upper</span></span>            | <span data-ttu-id="2de5e-224">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-224">32767</span></span>                                            |
| <span data-ttu-id="2de5e-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-225">Search-Flags</span></span>           | <span data-ttu-id="2de5e-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-226">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-227">System-Flags</span></span>           | <span data-ttu-id="2de5e-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-228">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-229">Classes used in</span></span>        | [<span data-ttu-id="2de5e-230">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2de5e-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2de5e-231">Windows Server 2008</span></span>



| <span data-ttu-id="2de5e-232">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-232">Entry</span></span> | <span data-ttu-id="2de5e-233">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-236">System-Only</span></span>            | <span data-ttu-id="2de5e-237">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-237">False</span></span>                                            |
| <span data-ttu-id="2de5e-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-238">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-239">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-239">True</span></span>                                             |
| <span data-ttu-id="2de5e-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-240">Is Indexed</span></span>             | <span data-ttu-id="2de5e-241">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-241">False</span></span>                                            |
| <span data-ttu-id="2de5e-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-242">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-243">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-243">False</span></span>                                            |
| <span data-ttu-id="2de5e-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-246">Range-Lower</span></span>            | <span data-ttu-id="2de5e-247">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-247">0</span></span>                                                |
| <span data-ttu-id="2de5e-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-248">Range-Upper</span></span>            | <span data-ttu-id="2de5e-249">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-249">32767</span></span>                                            |
| <span data-ttu-id="2de5e-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-250">Search-Flags</span></span>           | <span data-ttu-id="2de5e-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-251">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-252">System-Flags</span></span>           | <span data-ttu-id="2de5e-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-253">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-254">Classes used in</span></span>        | [<span data-ttu-id="2de5e-255">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2de5e-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2de5e-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2de5e-257">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-257">Entry</span></span> | <span data-ttu-id="2de5e-258">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-261">System-Only</span></span>            | <span data-ttu-id="2de5e-262">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-262">False</span></span>                                            |
| <span data-ttu-id="2de5e-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-263">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-264">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-264">True</span></span>                                             |
| <span data-ttu-id="2de5e-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-265">Is Indexed</span></span>             | <span data-ttu-id="2de5e-266">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-266">False</span></span>                                            |
| <span data-ttu-id="2de5e-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-267">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-268">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-268">False</span></span>                                            |
| <span data-ttu-id="2de5e-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-271">Range-Lower</span></span>            | <span data-ttu-id="2de5e-272">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-272">0</span></span>                                                |
| <span data-ttu-id="2de5e-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-273">Range-Upper</span></span>            | <span data-ttu-id="2de5e-274">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-274">32767</span></span>                                            |
| <span data-ttu-id="2de5e-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-275">Search-Flags</span></span>           | <span data-ttu-id="2de5e-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-276">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-277">System-Flags</span></span>           | <span data-ttu-id="2de5e-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-278">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-279">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-279">Classes used in</span></span>        | [<span data-ttu-id="2de5e-280">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2de5e-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2de5e-281">Windows Server 2012</span></span>



| <span data-ttu-id="2de5e-282">Voce</span><span class="sxs-lookup"><span data-stu-id="2de5e-282">Entry</span></span> | <span data-ttu-id="2de5e-283">Valore</span><span class="sxs-lookup"><span data-stu-id="2de5e-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="2de5e-284">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2de5e-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2de5e-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="2de5e-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="2de5e-286">System-Only</span></span>            | <span data-ttu-id="2de5e-287">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-287">False</span></span>                                            |
| <span data-ttu-id="2de5e-288">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2de5e-288">Is-Single-Valued</span></span>       | <span data-ttu-id="2de5e-289">Vero</span><span class="sxs-lookup"><span data-stu-id="2de5e-289">True</span></span>                                             |
| <span data-ttu-id="2de5e-290">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2de5e-290">Is Indexed</span></span>             | <span data-ttu-id="2de5e-291">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-291">False</span></span>                                            |
| <span data-ttu-id="2de5e-292">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2de5e-292">In Global Catalog</span></span>      | <span data-ttu-id="2de5e-293">Falso</span><span class="sxs-lookup"><span data-stu-id="2de5e-293">False</span></span>                                            |
| <span data-ttu-id="2de5e-294">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2de5e-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="2de5e-295">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2de5e-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="2de5e-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2de5e-296">Range-Lower</span></span>            | <span data-ttu-id="2de5e-297">0</span><span class="sxs-lookup"><span data-stu-id="2de5e-297">0</span></span>                                                |
| <span data-ttu-id="2de5e-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2de5e-298">Range-Upper</span></span>            | <span data-ttu-id="2de5e-299">32767</span><span class="sxs-lookup"><span data-stu-id="2de5e-299">32767</span></span>                                            |
| <span data-ttu-id="2de5e-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-300">Search-Flags</span></span>           | <span data-ttu-id="2de5e-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2de5e-301">0x00000000</span></span>                                       |
| <span data-ttu-id="2de5e-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2de5e-302">System-Flags</span></span>           | <span data-ttu-id="2de5e-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2de5e-303">0x00000010</span></span>                                       |
| <span data-ttu-id="2de5e-304">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2de5e-304">Classes used in</span></span>        | [<span data-ttu-id="2de5e-305">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="2de5e-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





