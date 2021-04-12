---
title: Attributo GPC-User-Extension-names
description: Utilizzato dall'oggetto Criteri di gruppo per i criteri utente.
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- GPC-User-Extension-names attributo AD schema
- Schema AD dell'attributo gPCUserExtensionNames
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479688"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="d50b9-105">Attributo GPC-User-Extension-names</span><span class="sxs-lookup"><span data-stu-id="d50b9-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="d50b9-106">Utilizzato dall'oggetto Criteri di gruppo per i criteri utente.</span><span class="sxs-lookup"><span data-stu-id="d50b9-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="d50b9-107">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-107">Entry</span></span> | <span data-ttu-id="d50b9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d50b9-109">CN</span><span class="sxs-lookup"><span data-stu-id="d50b9-109">CN</span></span>                | <span data-ttu-id="d50b9-110">GPC-User-Extension-nomi</span><span class="sxs-lookup"><span data-stu-id="d50b9-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="d50b9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d50b9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d50b9-112">gPCUserExtensionNames</span><span class="sxs-lookup"><span data-stu-id="d50b9-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="d50b9-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d50b9-113">Size</span></span>              | <span data-ttu-id="d50b9-114">Dipende dal numero di estensioni lato client che hanno un criterio in questo oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d50b9-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="d50b9-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-115">Update Privilege</span></span>  | <span data-ttu-id="d50b9-116">Amministratore del dominio o dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d50b9-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="d50b9-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-117">Update Frequency</span></span>  | <span data-ttu-id="d50b9-118">Ogni volta che un oggetto Criteri di gruppo viene aggiornato tramite il GPE.</span><span class="sxs-lookup"><span data-stu-id="d50b9-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="d50b9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-119">Attribute-Id</span></span>      | <span data-ttu-id="d50b9-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="d50b9-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="d50b9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d50b9-121">System-Id-Guid</span></span>    | <span data-ttu-id="d50b9-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d50b9-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="d50b9-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d50b9-123">Syntax</span></span>            | [<span data-ttu-id="d50b9-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d50b9-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="d50b9-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="d50b9-125">Implementations</span></span>

-   [<span data-ttu-id="d50b9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d50b9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d50b9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d50b9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d50b9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d50b9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d50b9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d50b9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d50b9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d50b9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d50b9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d50b9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d50b9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d50b9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d50b9-133">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-133">Entry</span></span> | <span data-ttu-id="d50b9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d50b9-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d50b9-137">System-Only</span></span>            | <span data-ttu-id="d50b9-138">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-138">False</span></span>                                                               |
| <span data-ttu-id="d50b9-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d50b9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d50b9-140">Vero</span><span class="sxs-lookup"><span data-stu-id="d50b9-140">True</span></span>                                                                |
| <span data-ttu-id="d50b9-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d50b9-141">Is Indexed</span></span>             | <span data-ttu-id="d50b9-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-142">False</span></span>                                                               |
| <span data-ttu-id="d50b9-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d50b9-143">In Global Catalog</span></span>      | <span data-ttu-id="d50b9-144">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-144">False</span></span>                                                               |
| <span data-ttu-id="d50b9-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d50b9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d50b9-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d50b9-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d50b9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d50b9-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d50b9-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-149">Search-Flags</span></span>           | <span data-ttu-id="d50b9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d50b9-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="d50b9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-151">System-Flags</span></span>           | <span data-ttu-id="d50b9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d50b9-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="d50b9-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d50b9-153">Classes used in</span></span>        | [<span data-ttu-id="d50b9-154">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d50b9-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d50b9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d50b9-155">Windows Server 2003</span></span>



| <span data-ttu-id="d50b9-156">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-156">Entry</span></span> | <span data-ttu-id="d50b9-157">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d50b9-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d50b9-160">System-Only</span></span>            | <span data-ttu-id="d50b9-161">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-161">False</span></span>                                                               |
| <span data-ttu-id="d50b9-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d50b9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d50b9-163">Vero</span><span class="sxs-lookup"><span data-stu-id="d50b9-163">True</span></span>                                                                |
| <span data-ttu-id="d50b9-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d50b9-164">Is Indexed</span></span>             | <span data-ttu-id="d50b9-165">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-165">False</span></span>                                                               |
| <span data-ttu-id="d50b9-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d50b9-166">In Global Catalog</span></span>      | <span data-ttu-id="d50b9-167">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-167">False</span></span>                                                               |
| <span data-ttu-id="d50b9-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d50b9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d50b9-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d50b9-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d50b9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d50b9-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d50b9-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-172">Search-Flags</span></span>           | <span data-ttu-id="d50b9-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d50b9-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="d50b9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-174">System-Flags</span></span>           | <span data-ttu-id="d50b9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d50b9-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="d50b9-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d50b9-176">Classes used in</span></span>        | [<span data-ttu-id="d50b9-177">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d50b9-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d50b9-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d50b9-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d50b9-179">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-179">Entry</span></span> | <span data-ttu-id="d50b9-180">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d50b9-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d50b9-183">System-Only</span></span>            | <span data-ttu-id="d50b9-184">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-184">False</span></span>                                                               |
| <span data-ttu-id="d50b9-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d50b9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d50b9-186">Vero</span><span class="sxs-lookup"><span data-stu-id="d50b9-186">True</span></span>                                                                |
| <span data-ttu-id="d50b9-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d50b9-187">Is Indexed</span></span>             | <span data-ttu-id="d50b9-188">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-188">False</span></span>                                                               |
| <span data-ttu-id="d50b9-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d50b9-189">In Global Catalog</span></span>      | <span data-ttu-id="d50b9-190">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-190">False</span></span>                                                               |
| <span data-ttu-id="d50b9-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d50b9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d50b9-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d50b9-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d50b9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d50b9-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d50b9-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-195">Search-Flags</span></span>           | <span data-ttu-id="d50b9-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d50b9-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="d50b9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-197">System-Flags</span></span>           | <span data-ttu-id="d50b9-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d50b9-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="d50b9-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d50b9-199">Classes used in</span></span>        | [<span data-ttu-id="d50b9-200">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d50b9-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d50b9-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d50b9-201">Windows Server 2008</span></span>



| <span data-ttu-id="d50b9-202">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-202">Entry</span></span> | <span data-ttu-id="d50b9-203">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d50b9-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d50b9-206">System-Only</span></span>            | <span data-ttu-id="d50b9-207">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-207">False</span></span>                                                               |
| <span data-ttu-id="d50b9-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d50b9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d50b9-209">Vero</span><span class="sxs-lookup"><span data-stu-id="d50b9-209">True</span></span>                                                                |
| <span data-ttu-id="d50b9-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d50b9-210">Is Indexed</span></span>             | <span data-ttu-id="d50b9-211">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-211">False</span></span>                                                               |
| <span data-ttu-id="d50b9-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d50b9-212">In Global Catalog</span></span>      | <span data-ttu-id="d50b9-213">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-213">False</span></span>                                                               |
| <span data-ttu-id="d50b9-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d50b9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d50b9-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d50b9-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d50b9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d50b9-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d50b9-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-218">Search-Flags</span></span>           | <span data-ttu-id="d50b9-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d50b9-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="d50b9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-220">System-Flags</span></span>           | <span data-ttu-id="d50b9-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d50b9-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="d50b9-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d50b9-222">Classes used in</span></span>        | [<span data-ttu-id="d50b9-223">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d50b9-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d50b9-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d50b9-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d50b9-225">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-225">Entry</span></span> | <span data-ttu-id="d50b9-226">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d50b9-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d50b9-229">System-Only</span></span>            | <span data-ttu-id="d50b9-230">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-230">False</span></span>                                                               |
| <span data-ttu-id="d50b9-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d50b9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d50b9-232">Vero</span><span class="sxs-lookup"><span data-stu-id="d50b9-232">True</span></span>                                                                |
| <span data-ttu-id="d50b9-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d50b9-233">Is Indexed</span></span>             | <span data-ttu-id="d50b9-234">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-234">False</span></span>                                                               |
| <span data-ttu-id="d50b9-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d50b9-235">In Global Catalog</span></span>      | <span data-ttu-id="d50b9-236">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-236">False</span></span>                                                               |
| <span data-ttu-id="d50b9-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d50b9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d50b9-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d50b9-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d50b9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d50b9-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d50b9-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-241">Search-Flags</span></span>           | <span data-ttu-id="d50b9-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d50b9-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="d50b9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-243">System-Flags</span></span>           | <span data-ttu-id="d50b9-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d50b9-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="d50b9-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d50b9-245">Classes used in</span></span>        | [<span data-ttu-id="d50b9-246">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d50b9-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d50b9-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d50b9-247">Windows Server 2012</span></span>



| <span data-ttu-id="d50b9-248">Voce</span><span class="sxs-lookup"><span data-stu-id="d50b9-248">Entry</span></span> | <span data-ttu-id="d50b9-249">Valore</span><span class="sxs-lookup"><span data-stu-id="d50b9-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d50b9-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="d50b9-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d50b9-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="d50b9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d50b9-252">System-Only</span></span>            | <span data-ttu-id="d50b9-253">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-253">False</span></span>                                                               |
| <span data-ttu-id="d50b9-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="d50b9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d50b9-255">Vero</span><span class="sxs-lookup"><span data-stu-id="d50b9-255">True</span></span>                                                                |
| <span data-ttu-id="d50b9-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="d50b9-256">Is Indexed</span></span>             | <span data-ttu-id="d50b9-257">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-257">False</span></span>                                                               |
| <span data-ttu-id="d50b9-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="d50b9-258">In Global Catalog</span></span>      | <span data-ttu-id="d50b9-259">Falso</span><span class="sxs-lookup"><span data-stu-id="d50b9-259">False</span></span>                                                               |
| <span data-ttu-id="d50b9-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="d50b9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d50b9-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="d50b9-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="d50b9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d50b9-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d50b9-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="d50b9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-264">Search-Flags</span></span>           | <span data-ttu-id="d50b9-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d50b9-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="d50b9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d50b9-266">System-Flags</span></span>           | <span data-ttu-id="d50b9-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d50b9-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="d50b9-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="d50b9-268">Classes used in</span></span>        | [<span data-ttu-id="d50b9-269">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="d50b9-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





