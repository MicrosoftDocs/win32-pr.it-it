---
title: LDAP-Display-Name-attributo
description: Nome usato dai client LDAP, ad esempio il provider LDAP ADSI, per leggere e scrivere l'attributo usando il protocollo LDAP.
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- Attributo LDAP-Display-Name-schema AD
- Schema AD dell'attributo lDAPDisplayName
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ffa25777ec4b5139a41ba9e56d8d5f0a9a3d92
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104225255"
---
# <a name="ldap-display-name-attribute"></a><span data-ttu-id="3300f-105">LDAP-Display-Name-attributo</span><span class="sxs-lookup"><span data-stu-id="3300f-105">LDAP-Display-Name attribute</span></span>

<span data-ttu-id="3300f-106">Nome usato dai client LDAP, ad esempio il provider LDAP ADSI, per leggere e scrivere l'attributo usando il protocollo LDAP.</span><span class="sxs-lookup"><span data-stu-id="3300f-106">The name used by LDAP clients, such as the ADSI LDAP provider, to read and write the attribute by using the LDAP protocol.</span></span>



| <span data-ttu-id="3300f-107">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-107">Entry</span></span> | <span data-ttu-id="3300f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3300f-109">CN</span><span class="sxs-lookup"><span data-stu-id="3300f-109">CN</span></span>                | <span data-ttu-id="3300f-110">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3300f-110">LDAP-Display-Name</span></span>                           |
| <span data-ttu-id="3300f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3300f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3300f-112">lDAPDisplayName</span><span class="sxs-lookup"><span data-stu-id="3300f-112">lDAPDisplayName</span></span>                             |
| <span data-ttu-id="3300f-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3300f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="3300f-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3300f-114">Update Privilege</span></span>  | <span data-ttu-id="3300f-115">Amministratore schema</span><span class="sxs-lookup"><span data-stu-id="3300f-115">Schema administrator</span></span>                        |
| <span data-ttu-id="3300f-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="3300f-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3300f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-117">Attribute-Id</span></span>      | <span data-ttu-id="3300f-118">1.2.840.113556.1.2.460</span><span class="sxs-lookup"><span data-stu-id="3300f-118">1.2.840.113556.1.2.460</span></span>                      |
| <span data-ttu-id="3300f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3300f-119">System-Id-Guid</span></span>    | <span data-ttu-id="3300f-120">bf96799a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3300f-120">bf96799a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="3300f-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3300f-121">Syntax</span></span>            | [<span data-ttu-id="3300f-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3300f-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3300f-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="3300f-123">Implementations</span></span>

-   [<span data-ttu-id="3300f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3300f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3300f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3300f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3300f-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3300f-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3300f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3300f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3300f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3300f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3300f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3300f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3300f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3300f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3300f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3300f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="3300f-132">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-132">Entry</span></span> | <span data-ttu-id="3300f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-134">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-135">MAPI-Id</span></span>                | <span data-ttu-id="3300f-136">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-136">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-137">System-Only</span></span>            | <span data-ttu-id="3300f-138">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-138">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-140">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-140">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-141">Is Indexed</span></span>             | <span data-ttu-id="3300f-142">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-142">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-143">In Global Catalog</span></span>      | <span data-ttu-id="3300f-144">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-144">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-146">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-147">Range-Lower</span></span>            | <span data-ttu-id="3300f-148">1</span><span class="sxs-lookup"><span data-stu-id="3300f-148">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-149">Range-Upper</span></span>            | <span data-ttu-id="3300f-150">256</span><span class="sxs-lookup"><span data-stu-id="3300f-150">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-151">Search-Flags</span></span>           | <span data-ttu-id="3300f-152">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-152">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-153">System-Flags</span></span>           | <span data-ttu-id="3300f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-154">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-155">Classes used in</span></span>        | [<span data-ttu-id="3300f-156">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-157">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-157">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3300f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3300f-158">Windows Server 2003</span></span>



| <span data-ttu-id="3300f-159">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-159">Entry</span></span> | <span data-ttu-id="3300f-160">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-161">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-162">MAPI-Id</span></span>                | <span data-ttu-id="3300f-163">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-163">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-164">System-Only</span></span>            | <span data-ttu-id="3300f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-165">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-167">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-167">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-168">Is Indexed</span></span>             | <span data-ttu-id="3300f-169">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-169">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-170">In Global Catalog</span></span>      | <span data-ttu-id="3300f-171">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-171">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-173">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-174">Range-Lower</span></span>            | <span data-ttu-id="3300f-175">1</span><span class="sxs-lookup"><span data-stu-id="3300f-175">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-176">Range-Upper</span></span>            | <span data-ttu-id="3300f-177">256</span><span class="sxs-lookup"><span data-stu-id="3300f-177">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-178">Search-Flags</span></span>           | <span data-ttu-id="3300f-179">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-179">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-180">System-Flags</span></span>           | <span data-ttu-id="3300f-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-181">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-182">Classes used in</span></span>        | [<span data-ttu-id="3300f-183">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-183">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-184">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-184">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3300f-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="3300f-185">ADAM</span></span>



| <span data-ttu-id="3300f-186">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-186">Entry</span></span> | <span data-ttu-id="3300f-187">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-187">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-188">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-188">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-189">MAPI-Id</span></span>                | <span data-ttu-id="3300f-190">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-190">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-191">System-Only</span></span>            | <span data-ttu-id="3300f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-192">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-193">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-193">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-194">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-194">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-195">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-195">Is Indexed</span></span>             | <span data-ttu-id="3300f-196">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-196">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-197">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-197">In Global Catalog</span></span>      | <span data-ttu-id="3300f-198">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-198">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-199">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-200">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-200">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-201">Range-Lower</span></span>            | <span data-ttu-id="3300f-202">1</span><span class="sxs-lookup"><span data-stu-id="3300f-202">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-203">Range-Upper</span></span>            | <span data-ttu-id="3300f-204">256</span><span class="sxs-lookup"><span data-stu-id="3300f-204">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-205">Search-Flags</span></span>           | <span data-ttu-id="3300f-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-206">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-207">System-Flags</span></span>           | <span data-ttu-id="3300f-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-208">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-209">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-209">Classes used in</span></span>        | [<span data-ttu-id="3300f-210">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-210">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-211">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-211">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3300f-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3300f-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3300f-213">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-213">Entry</span></span> | <span data-ttu-id="3300f-214">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-214">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-215">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-215">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-216">MAPI-Id</span></span>                | <span data-ttu-id="3300f-217">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-217">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-218">System-Only</span></span>            | <span data-ttu-id="3300f-219">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-219">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-220">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-220">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-221">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-221">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-222">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-222">Is Indexed</span></span>             | <span data-ttu-id="3300f-223">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-223">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-224">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-224">In Global Catalog</span></span>      | <span data-ttu-id="3300f-225">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-225">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-226">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-227">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-227">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-228">Range-Lower</span></span>            | <span data-ttu-id="3300f-229">1</span><span class="sxs-lookup"><span data-stu-id="3300f-229">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-230">Range-Upper</span></span>            | <span data-ttu-id="3300f-231">256</span><span class="sxs-lookup"><span data-stu-id="3300f-231">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-232">Search-Flags</span></span>           | <span data-ttu-id="3300f-233">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-233">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-234">System-Flags</span></span>           | <span data-ttu-id="3300f-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-235">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-236">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-236">Classes used in</span></span>        | [<span data-ttu-id="3300f-237">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-237">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-238">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3300f-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3300f-239">Windows Server 2008</span></span>



| <span data-ttu-id="3300f-240">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-240">Entry</span></span> | <span data-ttu-id="3300f-241">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-241">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-242">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-242">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-243">MAPI-Id</span></span>                | <span data-ttu-id="3300f-244">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-244">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-245">System-Only</span></span>            | <span data-ttu-id="3300f-246">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-246">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-247">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-247">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-248">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-248">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-249">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-249">Is Indexed</span></span>             | <span data-ttu-id="3300f-250">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-250">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-251">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-251">In Global Catalog</span></span>      | <span data-ttu-id="3300f-252">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-252">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-253">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-254">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-254">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-255">Range-Lower</span></span>            | <span data-ttu-id="3300f-256">1</span><span class="sxs-lookup"><span data-stu-id="3300f-256">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-257">Range-Upper</span></span>            | <span data-ttu-id="3300f-258">256</span><span class="sxs-lookup"><span data-stu-id="3300f-258">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-259">Search-Flags</span></span>           | <span data-ttu-id="3300f-260">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-260">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-261">System-Flags</span></span>           | <span data-ttu-id="3300f-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-262">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-263">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-263">Classes used in</span></span>        | [<span data-ttu-id="3300f-264">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-264">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-265">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-265">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3300f-266">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3300f-266">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3300f-267">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-267">Entry</span></span> | <span data-ttu-id="3300f-268">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-268">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-269">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-269">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-270">MAPI-Id</span></span>                | <span data-ttu-id="3300f-271">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-271">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-272">System-Only</span></span>            | <span data-ttu-id="3300f-273">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-273">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-274">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-274">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-275">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-275">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-276">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-276">Is Indexed</span></span>             | <span data-ttu-id="3300f-277">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-277">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-278">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-278">In Global Catalog</span></span>      | <span data-ttu-id="3300f-279">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-279">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-280">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-281">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-281">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-282">Range-Lower</span></span>            | <span data-ttu-id="3300f-283">1</span><span class="sxs-lookup"><span data-stu-id="3300f-283">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-284">Range-Upper</span></span>            | <span data-ttu-id="3300f-285">256</span><span class="sxs-lookup"><span data-stu-id="3300f-285">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-286">Search-Flags</span></span>           | <span data-ttu-id="3300f-287">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-287">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-288">System-Flags</span></span>           | <span data-ttu-id="3300f-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-289">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-290">Classes used in</span></span>        | [<span data-ttu-id="3300f-291">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-291">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-292">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3300f-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3300f-293">Windows Server 2012</span></span>



| <span data-ttu-id="3300f-294">Voce</span><span class="sxs-lookup"><span data-stu-id="3300f-294">Entry</span></span> | <span data-ttu-id="3300f-295">Valore</span><span class="sxs-lookup"><span data-stu-id="3300f-295">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3300f-296">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="3300f-296">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3300f-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3300f-297">MAPI-Id</span></span>                | <span data-ttu-id="3300f-298">0x8171</span><span class="sxs-lookup"><span data-stu-id="3300f-298">0x8171</span></span>                                                                                                    |
| <span data-ttu-id="3300f-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="3300f-299">System-Only</span></span>            | <span data-ttu-id="3300f-300">Falso</span><span class="sxs-lookup"><span data-stu-id="3300f-300">False</span></span>                                                                                                     |
| <span data-ttu-id="3300f-301">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="3300f-301">Is-Single-Valued</span></span>       | <span data-ttu-id="3300f-302">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-302">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-303">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="3300f-303">Is Indexed</span></span>             | <span data-ttu-id="3300f-304">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-304">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-305">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="3300f-305">In Global Catalog</span></span>      | <span data-ttu-id="3300f-306">Vero</span><span class="sxs-lookup"><span data-stu-id="3300f-306">True</span></span>                                                                                                      |
| <span data-ttu-id="3300f-307">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="3300f-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="3300f-308">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="3300f-308">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3300f-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3300f-309">Range-Lower</span></span>            | <span data-ttu-id="3300f-310">1</span><span class="sxs-lookup"><span data-stu-id="3300f-310">1</span></span>                                                                                                         |
| <span data-ttu-id="3300f-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3300f-311">Range-Upper</span></span>            | <span data-ttu-id="3300f-312">256</span><span class="sxs-lookup"><span data-stu-id="3300f-312">256</span></span>                                                                                                       |
| <span data-ttu-id="3300f-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-313">Search-Flags</span></span>           | <span data-ttu-id="3300f-314">0x00000009</span><span class="sxs-lookup"><span data-stu-id="3300f-314">0x00000009</span></span>                                                                                                |
| <span data-ttu-id="3300f-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3300f-315">System-Flags</span></span>           | <span data-ttu-id="3300f-316">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3300f-316">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3300f-317">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="3300f-317">Classes used in</span></span>        | [<span data-ttu-id="3300f-318">**Attribute-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-318">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3300f-319">**Classe-schema**</span><span class="sxs-lookup"><span data-stu-id="3300f-319">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





