---
title: Attributo COM-TypeLib-ID
description: Questo attributo archivia l'elenco degli ID della libreria dei tipi contenuti nel pacchetto dell'applicazione.
ms.assetid: 3dcd2d1f-8b6d-46f6-9707-4af006f0e610
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo COM-TypeLib-ID
- Schema AD dell'attributo cOMTypelibId
topic_type:
- apiref
api_name:
- COM-Typelib-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0be116963137dcdba4d97aa3de751bdf7308c335
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303607"
---
# <a name="com-typelib-id-attribute"></a><span data-ttu-id="f13e7-105">Attributo COM-TypeLib-ID</span><span class="sxs-lookup"><span data-stu-id="f13e7-105">COM-Typelib-Id attribute</span></span>

<span data-ttu-id="f13e7-106">Questo attributo archivia l'elenco degli ID della libreria dei tipi contenuti nel pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f13e7-106">This attribute stores the list of type library IDs contained in this application package.</span></span>



| <span data-ttu-id="f13e7-107">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-107">Entry</span></span> | <span data-ttu-id="f13e7-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f13e7-109">CN</span><span class="sxs-lookup"><span data-stu-id="f13e7-109">CN</span></span>                | <span data-ttu-id="f13e7-110">COM-TypeLib-ID</span><span class="sxs-lookup"><span data-stu-id="f13e7-110">COM-Typelib-Id</span></span>                                                                   |
| <span data-ttu-id="f13e7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f13e7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f13e7-112">cOMTypelibId</span><span class="sxs-lookup"><span data-stu-id="f13e7-112">cOMTypelibId</span></span>                                                                     |
| <span data-ttu-id="f13e7-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f13e7-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="f13e7-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-114">Update Privilege</span></span>  | <span data-ttu-id="f13e7-115">Chiunque può aggiornare questo oggetto in base alla sicurezza dell'oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="f13e7-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="f13e7-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="f13e7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-117">Attribute-Id</span></span>      | <span data-ttu-id="f13e7-118">1.2.840.113556.1.4.254</span><span class="sxs-lookup"><span data-stu-id="f13e7-118">1.2.840.113556.1.4.254</span></span>                                                           |
| <span data-ttu-id="f13e7-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f13e7-119">System-Id-Guid</span></span>    | <span data-ttu-id="f13e7-120">281416de-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f13e7-120">281416de-1968-11d0-a28f-00aa003049e2</span></span>                                             |
| <span data-ttu-id="f13e7-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f13e7-121">Syntax</span></span>            | [<span data-ttu-id="f13e7-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f13e7-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="f13e7-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f13e7-123">Implementations</span></span>

-   [<span data-ttu-id="f13e7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f13e7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f13e7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f13e7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f13e7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f13e7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f13e7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f13e7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f13e7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f13e7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f13e7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f13e7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f13e7-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f13e7-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f13e7-131">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-131">Entry</span></span> | <span data-ttu-id="f13e7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f13e7-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f13e7-135">System-Only</span></span>            | <span data-ttu-id="f13e7-136">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-136">False</span></span>                                                            |
| <span data-ttu-id="f13e7-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f13e7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f13e7-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-138">False</span></span>                                                            |
| <span data-ttu-id="f13e7-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f13e7-139">Is Indexed</span></span>             | <span data-ttu-id="f13e7-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-140">False</span></span>                                                            |
| <span data-ttu-id="f13e7-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f13e7-141">In Global Catalog</span></span>      | <span data-ttu-id="f13e7-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-142">False</span></span>                                                            |
| <span data-ttu-id="f13e7-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f13e7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f13e7-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f13e7-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f13e7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f13e7-145">Range-Lower</span></span>            | <span data-ttu-id="f13e7-146">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-146">36</span></span>                                                               |
| <span data-ttu-id="f13e7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f13e7-147">Range-Upper</span></span>            | <span data-ttu-id="f13e7-148">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-148">36</span></span>                                                               |
| <span data-ttu-id="f13e7-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-149">Search-Flags</span></span>           | <span data-ttu-id="f13e7-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f13e7-150">0x00000000</span></span>                                                       |
| <span data-ttu-id="f13e7-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-151">System-Flags</span></span>           | <span data-ttu-id="f13e7-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f13e7-152">0x00000010</span></span>                                                       |
| <span data-ttu-id="f13e7-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f13e7-153">Classes used in</span></span>        | [<span data-ttu-id="f13e7-154">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f13e7-154">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f13e7-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f13e7-155">Windows Server 2003</span></span>



| <span data-ttu-id="f13e7-156">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-156">Entry</span></span> | <span data-ttu-id="f13e7-157">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-157">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f13e7-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-158">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-159">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f13e7-160">System-Only</span></span>            | <span data-ttu-id="f13e7-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-161">False</span></span>                                                            |
| <span data-ttu-id="f13e7-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f13e7-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f13e7-163">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-163">False</span></span>                                                            |
| <span data-ttu-id="f13e7-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f13e7-164">Is Indexed</span></span>             | <span data-ttu-id="f13e7-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-165">False</span></span>                                                            |
| <span data-ttu-id="f13e7-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f13e7-166">In Global Catalog</span></span>      | <span data-ttu-id="f13e7-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-167">False</span></span>                                                            |
| <span data-ttu-id="f13e7-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f13e7-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f13e7-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f13e7-169">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f13e7-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f13e7-170">Range-Lower</span></span>            | <span data-ttu-id="f13e7-171">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-171">36</span></span>                                                               |
| <span data-ttu-id="f13e7-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f13e7-172">Range-Upper</span></span>            | <span data-ttu-id="f13e7-173">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-173">36</span></span>                                                               |
| <span data-ttu-id="f13e7-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-174">Search-Flags</span></span>           | <span data-ttu-id="f13e7-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f13e7-175">0x00000000</span></span>                                                       |
| <span data-ttu-id="f13e7-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-176">System-Flags</span></span>           | <span data-ttu-id="f13e7-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f13e7-177">0x00000010</span></span>                                                       |
| <span data-ttu-id="f13e7-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f13e7-178">Classes used in</span></span>        | [<span data-ttu-id="f13e7-179">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f13e7-179">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f13e7-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f13e7-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f13e7-181">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-181">Entry</span></span> | <span data-ttu-id="f13e7-182">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-182">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f13e7-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-183">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-184">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f13e7-185">System-Only</span></span>            | <span data-ttu-id="f13e7-186">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-186">False</span></span>                                                            |
| <span data-ttu-id="f13e7-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f13e7-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f13e7-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-188">False</span></span>                                                            |
| <span data-ttu-id="f13e7-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f13e7-189">Is Indexed</span></span>             | <span data-ttu-id="f13e7-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-190">False</span></span>                                                            |
| <span data-ttu-id="f13e7-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f13e7-191">In Global Catalog</span></span>      | <span data-ttu-id="f13e7-192">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-192">False</span></span>                                                            |
| <span data-ttu-id="f13e7-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f13e7-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f13e7-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f13e7-194">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f13e7-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f13e7-195">Range-Lower</span></span>            | <span data-ttu-id="f13e7-196">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-196">36</span></span>                                                               |
| <span data-ttu-id="f13e7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f13e7-197">Range-Upper</span></span>            | <span data-ttu-id="f13e7-198">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-198">36</span></span>                                                               |
| <span data-ttu-id="f13e7-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-199">Search-Flags</span></span>           | <span data-ttu-id="f13e7-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f13e7-200">0x00000000</span></span>                                                       |
| <span data-ttu-id="f13e7-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-201">System-Flags</span></span>           | <span data-ttu-id="f13e7-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f13e7-202">0x00000010</span></span>                                                       |
| <span data-ttu-id="f13e7-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f13e7-203">Classes used in</span></span>        | [<span data-ttu-id="f13e7-204">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f13e7-204">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f13e7-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f13e7-205">Windows Server 2008</span></span>



| <span data-ttu-id="f13e7-206">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-206">Entry</span></span> | <span data-ttu-id="f13e7-207">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-207">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f13e7-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-208">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-209">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="f13e7-210">System-Only</span></span>            | <span data-ttu-id="f13e7-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-211">False</span></span>                                                            |
| <span data-ttu-id="f13e7-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f13e7-212">Is-Single-Valued</span></span>       | <span data-ttu-id="f13e7-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-213">False</span></span>                                                            |
| <span data-ttu-id="f13e7-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f13e7-214">Is Indexed</span></span>             | <span data-ttu-id="f13e7-215">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-215">False</span></span>                                                            |
| <span data-ttu-id="f13e7-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f13e7-216">In Global Catalog</span></span>      | <span data-ttu-id="f13e7-217">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-217">False</span></span>                                                            |
| <span data-ttu-id="f13e7-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f13e7-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="f13e7-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f13e7-219">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f13e7-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f13e7-220">Range-Lower</span></span>            | <span data-ttu-id="f13e7-221">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-221">36</span></span>                                                               |
| <span data-ttu-id="f13e7-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f13e7-222">Range-Upper</span></span>            | <span data-ttu-id="f13e7-223">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-223">36</span></span>                                                               |
| <span data-ttu-id="f13e7-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-224">Search-Flags</span></span>           | <span data-ttu-id="f13e7-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f13e7-225">0x00000000</span></span>                                                       |
| <span data-ttu-id="f13e7-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-226">System-Flags</span></span>           | <span data-ttu-id="f13e7-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f13e7-227">0x00000010</span></span>                                                       |
| <span data-ttu-id="f13e7-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f13e7-228">Classes used in</span></span>        | [<span data-ttu-id="f13e7-229">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f13e7-229">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f13e7-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f13e7-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f13e7-231">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-231">Entry</span></span> | <span data-ttu-id="f13e7-232">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-232">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f13e7-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-233">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-234">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="f13e7-235">System-Only</span></span>            | <span data-ttu-id="f13e7-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-236">False</span></span>                                                            |
| <span data-ttu-id="f13e7-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f13e7-237">Is-Single-Valued</span></span>       | <span data-ttu-id="f13e7-238">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-238">False</span></span>                                                            |
| <span data-ttu-id="f13e7-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f13e7-239">Is Indexed</span></span>             | <span data-ttu-id="f13e7-240">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-240">False</span></span>                                                            |
| <span data-ttu-id="f13e7-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f13e7-241">In Global Catalog</span></span>      | <span data-ttu-id="f13e7-242">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-242">False</span></span>                                                            |
| <span data-ttu-id="f13e7-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f13e7-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="f13e7-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f13e7-244">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f13e7-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f13e7-245">Range-Lower</span></span>            | <span data-ttu-id="f13e7-246">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-246">36</span></span>                                                               |
| <span data-ttu-id="f13e7-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f13e7-247">Range-Upper</span></span>            | <span data-ttu-id="f13e7-248">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-248">36</span></span>                                                               |
| <span data-ttu-id="f13e7-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-249">Search-Flags</span></span>           | <span data-ttu-id="f13e7-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f13e7-250">0x00000000</span></span>                                                       |
| <span data-ttu-id="f13e7-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-251">System-Flags</span></span>           | <span data-ttu-id="f13e7-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f13e7-252">0x00000010</span></span>                                                       |
| <span data-ttu-id="f13e7-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f13e7-253">Classes used in</span></span>        | [<span data-ttu-id="f13e7-254">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f13e7-254">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f13e7-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f13e7-255">Windows Server 2012</span></span>



| <span data-ttu-id="f13e7-256">Voce</span><span class="sxs-lookup"><span data-stu-id="f13e7-256">Entry</span></span> | <span data-ttu-id="f13e7-257">Valore</span><span class="sxs-lookup"><span data-stu-id="f13e7-257">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f13e7-258">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f13e7-258">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f13e7-259">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f13e7-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="f13e7-260">System-Only</span></span>            | <span data-ttu-id="f13e7-261">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-261">False</span></span>                                                            |
| <span data-ttu-id="f13e7-262">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f13e7-262">Is-Single-Valued</span></span>       | <span data-ttu-id="f13e7-263">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-263">False</span></span>                                                            |
| <span data-ttu-id="f13e7-264">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f13e7-264">Is Indexed</span></span>             | <span data-ttu-id="f13e7-265">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-265">False</span></span>                                                            |
| <span data-ttu-id="f13e7-266">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f13e7-266">In Global Catalog</span></span>      | <span data-ttu-id="f13e7-267">Falso</span><span class="sxs-lookup"><span data-stu-id="f13e7-267">False</span></span>                                                            |
| <span data-ttu-id="f13e7-268">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f13e7-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="f13e7-269">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f13e7-269">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f13e7-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f13e7-270">Range-Lower</span></span>            | <span data-ttu-id="f13e7-271">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-271">36</span></span>                                                               |
| <span data-ttu-id="f13e7-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f13e7-272">Range-Upper</span></span>            | <span data-ttu-id="f13e7-273">36</span><span class="sxs-lookup"><span data-stu-id="f13e7-273">36</span></span>                                                               |
| <span data-ttu-id="f13e7-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-274">Search-Flags</span></span>           | <span data-ttu-id="f13e7-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f13e7-275">0x00000000</span></span>                                                       |
| <span data-ttu-id="f13e7-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f13e7-276">System-Flags</span></span>           | <span data-ttu-id="f13e7-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f13e7-277">0x00000010</span></span>                                                       |
| <span data-ttu-id="f13e7-278">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f13e7-278">Classes used in</span></span>        | [<span data-ttu-id="f13e7-279">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f13e7-279">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





