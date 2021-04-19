---
title: Attributo COM-ProgID
description: Questo attributo archivia l'elenco di ID di programma di oggetti COM implementati nel pacchetto dell'applicazione.
ms.assetid: 9d2945e4-f236-48f6-bed3-145d445ff653
ms.tgt_platform: multiple
keywords:
- Schema AD COM-ProgID attribute
- Schema AD dell'attributo comprogid
topic_type:
- apiref
api_name:
- COM-ProgID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686976732bedf2c4ba486186634720568d3b6c3c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303609"
---
# <a name="com-progid-attribute"></a><span data-ttu-id="03046-105">Attributo COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="03046-105">COM-ProgID attribute</span></span>

<span data-ttu-id="03046-106">Questo attributo archivia l'elenco di ID di programma di oggetti COM implementati nel pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03046-106">This attribute stores the list of COM object program IDs that are implemented in this application package.</span></span>



| <span data-ttu-id="03046-107">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-107">Entry</span></span> | <span data-ttu-id="03046-108">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03046-109">CN</span><span class="sxs-lookup"><span data-stu-id="03046-109">CN</span></span>                | <span data-ttu-id="03046-110">COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="03046-110">COM-ProgID</span></span>                                                                       |
| <span data-ttu-id="03046-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="03046-111">Ldap-Display-Name</span></span> | <span data-ttu-id="03046-112">comprogid</span><span class="sxs-lookup"><span data-stu-id="03046-112">cOMProgID</span></span>                                                                        |
| <span data-ttu-id="03046-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="03046-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="03046-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="03046-114">Update Privilege</span></span>  | <span data-ttu-id="03046-115">Chiunque può aggiornare questo oggetto in base alla sicurezza dell'oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="03046-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="03046-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="03046-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="03046-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03046-117">Attribute-Id</span></span>      | <span data-ttu-id="03046-118">1.2.840.113556.1.4.21</span><span class="sxs-lookup"><span data-stu-id="03046-118">1.2.840.113556.1.4.21</span></span>                                                            |
| <span data-ttu-id="03046-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03046-119">System-Id-Guid</span></span>    | <span data-ttu-id="03046-120">bf96793d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="03046-120">bf96793d-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="03046-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03046-121">Syntax</span></span>            | [<span data-ttu-id="03046-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="03046-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="03046-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="03046-123">Implementations</span></span>

-   [<span data-ttu-id="03046-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03046-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03046-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03046-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03046-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03046-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03046-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03046-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03046-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03046-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03046-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03046-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03046-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03046-130">Windows 2000 Server</span></span>



| <span data-ttu-id="03046-131">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-131">Entry</span></span> | <span data-ttu-id="03046-132">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03046-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="03046-133">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03046-134">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="03046-135">System-Only</span></span>            | <span data-ttu-id="03046-136">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-136">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="03046-137">Is-Single-Valued</span></span>       | <span data-ttu-id="03046-138">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-138">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="03046-139">Is Indexed</span></span>             | <span data-ttu-id="03046-140">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-140">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="03046-141">In Global Catalog</span></span>      | <span data-ttu-id="03046-142">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-142">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="03046-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="03046-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="03046-144">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="03046-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03046-145">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03046-146">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-147">Search-Flags</span></span>           | <span data-ttu-id="03046-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03046-148">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="03046-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-149">System-Flags</span></span>           | <span data-ttu-id="03046-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03046-150">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="03046-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="03046-151">Classes used in</span></span>        | [<span data-ttu-id="03046-152">**Classe-registrazione**</span><span class="sxs-lookup"><span data-stu-id="03046-152">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="03046-153">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="03046-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03046-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03046-154">Windows Server 2003</span></span>



| <span data-ttu-id="03046-155">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-155">Entry</span></span> | <span data-ttu-id="03046-156">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03046-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="03046-157">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03046-158">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="03046-159">System-Only</span></span>            | <span data-ttu-id="03046-160">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-160">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="03046-161">Is-Single-Valued</span></span>       | <span data-ttu-id="03046-162">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-162">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="03046-163">Is Indexed</span></span>             | <span data-ttu-id="03046-164">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-164">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="03046-165">In Global Catalog</span></span>      | <span data-ttu-id="03046-166">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-166">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="03046-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="03046-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="03046-168">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="03046-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03046-169">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03046-170">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-171">Search-Flags</span></span>           | <span data-ttu-id="03046-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03046-172">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="03046-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-173">System-Flags</span></span>           | <span data-ttu-id="03046-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03046-174">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="03046-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="03046-175">Classes used in</span></span>        | [<span data-ttu-id="03046-176">**Classe-registrazione**</span><span class="sxs-lookup"><span data-stu-id="03046-176">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="03046-177">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="03046-177">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03046-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03046-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03046-179">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-179">Entry</span></span> | <span data-ttu-id="03046-180">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03046-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="03046-181">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03046-182">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="03046-183">System-Only</span></span>            | <span data-ttu-id="03046-184">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-184">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="03046-185">Is-Single-Valued</span></span>       | <span data-ttu-id="03046-186">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-186">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="03046-187">Is Indexed</span></span>             | <span data-ttu-id="03046-188">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-188">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="03046-189">In Global Catalog</span></span>      | <span data-ttu-id="03046-190">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-190">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="03046-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="03046-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="03046-192">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="03046-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03046-193">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03046-194">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-195">Search-Flags</span></span>           | <span data-ttu-id="03046-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03046-196">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="03046-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-197">System-Flags</span></span>           | <span data-ttu-id="03046-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03046-198">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="03046-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="03046-199">Classes used in</span></span>        | [<span data-ttu-id="03046-200">**Classe-registrazione**</span><span class="sxs-lookup"><span data-stu-id="03046-200">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="03046-201">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="03046-201">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03046-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03046-202">Windows Server 2008</span></span>



| <span data-ttu-id="03046-203">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-203">Entry</span></span> | <span data-ttu-id="03046-204">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03046-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="03046-205">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03046-206">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="03046-207">System-Only</span></span>            | <span data-ttu-id="03046-208">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-208">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="03046-209">Is-Single-Valued</span></span>       | <span data-ttu-id="03046-210">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-210">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="03046-211">Is Indexed</span></span>             | <span data-ttu-id="03046-212">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-212">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="03046-213">In Global Catalog</span></span>      | <span data-ttu-id="03046-214">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-214">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="03046-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="03046-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="03046-216">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="03046-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03046-217">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03046-218">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-219">Search-Flags</span></span>           | <span data-ttu-id="03046-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03046-220">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="03046-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-221">System-Flags</span></span>           | <span data-ttu-id="03046-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03046-222">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="03046-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="03046-223">Classes used in</span></span>        | [<span data-ttu-id="03046-224">**Classe-registrazione**</span><span class="sxs-lookup"><span data-stu-id="03046-224">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="03046-225">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="03046-225">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03046-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03046-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03046-227">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-227">Entry</span></span> | <span data-ttu-id="03046-228">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03046-229">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="03046-229">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03046-230">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="03046-231">System-Only</span></span>            | <span data-ttu-id="03046-232">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-232">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-233">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="03046-233">Is-Single-Valued</span></span>       | <span data-ttu-id="03046-234">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-234">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-235">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="03046-235">Is Indexed</span></span>             | <span data-ttu-id="03046-236">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-236">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-237">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="03046-237">In Global Catalog</span></span>      | <span data-ttu-id="03046-238">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-238">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-239">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="03046-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="03046-240">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="03046-240">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="03046-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03046-241">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03046-242">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-243">Search-Flags</span></span>           | <span data-ttu-id="03046-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03046-244">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="03046-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-245">System-Flags</span></span>           | <span data-ttu-id="03046-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03046-246">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="03046-247">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="03046-247">Classes used in</span></span>        | [<span data-ttu-id="03046-248">**Classe-registrazione**</span><span class="sxs-lookup"><span data-stu-id="03046-248">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="03046-249">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="03046-249">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03046-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03046-250">Windows Server 2012</span></span>



| <span data-ttu-id="03046-251">Voce</span><span class="sxs-lookup"><span data-stu-id="03046-251">Entry</span></span> | <span data-ttu-id="03046-252">Valore</span><span class="sxs-lookup"><span data-stu-id="03046-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03046-253">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="03046-253">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03046-254">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="03046-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="03046-255">System-Only</span></span>            | <span data-ttu-id="03046-256">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-256">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-257">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="03046-257">Is-Single-Valued</span></span>       | <span data-ttu-id="03046-258">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-258">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-259">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="03046-259">Is Indexed</span></span>             | <span data-ttu-id="03046-260">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-260">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-261">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="03046-261">In Global Catalog</span></span>      | <span data-ttu-id="03046-262">Falso</span><span class="sxs-lookup"><span data-stu-id="03046-262">False</span></span>                                                                                                                         |
| <span data-ttu-id="03046-263">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="03046-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="03046-264">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="03046-264">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="03046-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03046-265">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03046-266">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="03046-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-267">Search-Flags</span></span>           | <span data-ttu-id="03046-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03046-268">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="03046-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03046-269">System-Flags</span></span>           | <span data-ttu-id="03046-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03046-270">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="03046-271">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="03046-271">Classes used in</span></span>        | [<span data-ttu-id="03046-272">**Classe-registrazione**</span><span class="sxs-lookup"><span data-stu-id="03046-272">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="03046-273">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="03046-273">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





