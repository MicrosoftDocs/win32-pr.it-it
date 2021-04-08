---
title: Attributo GPC-Machine-Extension-names
description: Utilizzato dall'oggetto Criteri di gruppo per i criteri del computer.
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- GPC-Machine-Extension-names attributo AD schema
- Schema AD dell'attributo gPCMachineExtensionNames
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965305"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="b5a41-105">Attributo GPC-Machine-Extension-names</span><span class="sxs-lookup"><span data-stu-id="b5a41-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="b5a41-106">Utilizzato dall'oggetto Criteri di gruppo per i criteri del computer.</span><span class="sxs-lookup"><span data-stu-id="b5a41-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="b5a41-107">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-107">Entry</span></span> | <span data-ttu-id="b5a41-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b5a41-109">CN</span><span class="sxs-lookup"><span data-stu-id="b5a41-109">CN</span></span>                | <span data-ttu-id="b5a41-110">GPC-Machine-Extension-nomi</span><span class="sxs-lookup"><span data-stu-id="b5a41-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="b5a41-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b5a41-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b5a41-112">gPCMachineExtensionNames</span><span class="sxs-lookup"><span data-stu-id="b5a41-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="b5a41-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b5a41-113">Size</span></span>              | <span data-ttu-id="b5a41-114">Dipende dal numero di estensioni lato client che hanno un criterio in questo oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b5a41-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="b5a41-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-115">Update Privilege</span></span>  | <span data-ttu-id="b5a41-116">Amministratore del dominio o dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b5a41-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="b5a41-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-117">Update Frequency</span></span>  | <span data-ttu-id="b5a41-118">Ogni volta che un oggetto Criteri di gruppo viene aggiornato tramite il GPE.</span><span class="sxs-lookup"><span data-stu-id="b5a41-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="b5a41-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-119">Attribute-Id</span></span>      | <span data-ttu-id="b5a41-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="b5a41-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="b5a41-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b5a41-121">System-Id-Guid</span></span>    | <span data-ttu-id="b5a41-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b5a41-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="b5a41-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5a41-123">Syntax</span></span>            | [<span data-ttu-id="b5a41-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b5a41-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="b5a41-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b5a41-125">Implementations</span></span>

-   [<span data-ttu-id="b5a41-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b5a41-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b5a41-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b5a41-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b5a41-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b5a41-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b5a41-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b5a41-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b5a41-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b5a41-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b5a41-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b5a41-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b5a41-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5a41-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b5a41-133">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-133">Entry</span></span> | <span data-ttu-id="b5a41-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b5a41-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5a41-137">System-Only</span></span>            | <span data-ttu-id="b5a41-138">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-138">False</span></span>                                                               |
| <span data-ttu-id="b5a41-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5a41-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b5a41-140">Vero</span><span class="sxs-lookup"><span data-stu-id="b5a41-140">True</span></span>                                                                |
| <span data-ttu-id="b5a41-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5a41-141">Is Indexed</span></span>             | <span data-ttu-id="b5a41-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-142">False</span></span>                                                               |
| <span data-ttu-id="b5a41-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5a41-143">In Global Catalog</span></span>      | <span data-ttu-id="b5a41-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-144">False</span></span>                                                               |
| <span data-ttu-id="b5a41-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5a41-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5a41-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5a41-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b5a41-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5a41-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5a41-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-149">Search-Flags</span></span>           | <span data-ttu-id="b5a41-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5a41-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="b5a41-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-151">System-Flags</span></span>           | <span data-ttu-id="b5a41-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5a41-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="b5a41-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5a41-153">Classes used in</span></span>        | [<span data-ttu-id="b5a41-154">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="b5a41-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b5a41-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5a41-155">Windows Server 2003</span></span>



| <span data-ttu-id="b5a41-156">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-156">Entry</span></span> | <span data-ttu-id="b5a41-157">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b5a41-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5a41-160">System-Only</span></span>            | <span data-ttu-id="b5a41-161">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-161">False</span></span>                                                               |
| <span data-ttu-id="b5a41-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5a41-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b5a41-163">Vero</span><span class="sxs-lookup"><span data-stu-id="b5a41-163">True</span></span>                                                                |
| <span data-ttu-id="b5a41-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5a41-164">Is Indexed</span></span>             | <span data-ttu-id="b5a41-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-165">False</span></span>                                                               |
| <span data-ttu-id="b5a41-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5a41-166">In Global Catalog</span></span>      | <span data-ttu-id="b5a41-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-167">False</span></span>                                                               |
| <span data-ttu-id="b5a41-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5a41-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5a41-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5a41-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b5a41-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5a41-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5a41-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-172">Search-Flags</span></span>           | <span data-ttu-id="b5a41-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5a41-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="b5a41-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-174">System-Flags</span></span>           | <span data-ttu-id="b5a41-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5a41-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="b5a41-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5a41-176">Classes used in</span></span>        | [<span data-ttu-id="b5a41-177">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="b5a41-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b5a41-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b5a41-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b5a41-179">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-179">Entry</span></span> | <span data-ttu-id="b5a41-180">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b5a41-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5a41-183">System-Only</span></span>            | <span data-ttu-id="b5a41-184">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-184">False</span></span>                                                               |
| <span data-ttu-id="b5a41-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5a41-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b5a41-186">Vero</span><span class="sxs-lookup"><span data-stu-id="b5a41-186">True</span></span>                                                                |
| <span data-ttu-id="b5a41-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5a41-187">Is Indexed</span></span>             | <span data-ttu-id="b5a41-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-188">False</span></span>                                                               |
| <span data-ttu-id="b5a41-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5a41-189">In Global Catalog</span></span>      | <span data-ttu-id="b5a41-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-190">False</span></span>                                                               |
| <span data-ttu-id="b5a41-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5a41-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5a41-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5a41-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b5a41-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5a41-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5a41-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-195">Search-Flags</span></span>           | <span data-ttu-id="b5a41-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5a41-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="b5a41-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-197">System-Flags</span></span>           | <span data-ttu-id="b5a41-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5a41-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="b5a41-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5a41-199">Classes used in</span></span>        | [<span data-ttu-id="b5a41-200">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="b5a41-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b5a41-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5a41-201">Windows Server 2008</span></span>



| <span data-ttu-id="b5a41-202">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-202">Entry</span></span> | <span data-ttu-id="b5a41-203">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b5a41-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5a41-206">System-Only</span></span>            | <span data-ttu-id="b5a41-207">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-207">False</span></span>                                                               |
| <span data-ttu-id="b5a41-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5a41-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b5a41-209">Vero</span><span class="sxs-lookup"><span data-stu-id="b5a41-209">True</span></span>                                                                |
| <span data-ttu-id="b5a41-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5a41-210">Is Indexed</span></span>             | <span data-ttu-id="b5a41-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-211">False</span></span>                                                               |
| <span data-ttu-id="b5a41-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5a41-212">In Global Catalog</span></span>      | <span data-ttu-id="b5a41-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-213">False</span></span>                                                               |
| <span data-ttu-id="b5a41-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5a41-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5a41-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5a41-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b5a41-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5a41-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5a41-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-218">Search-Flags</span></span>           | <span data-ttu-id="b5a41-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5a41-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="b5a41-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-220">System-Flags</span></span>           | <span data-ttu-id="b5a41-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5a41-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="b5a41-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5a41-222">Classes used in</span></span>        | [<span data-ttu-id="b5a41-223">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="b5a41-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b5a41-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5a41-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b5a41-225">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-225">Entry</span></span> | <span data-ttu-id="b5a41-226">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b5a41-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5a41-229">System-Only</span></span>            | <span data-ttu-id="b5a41-230">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-230">False</span></span>                                                               |
| <span data-ttu-id="b5a41-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5a41-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b5a41-232">Vero</span><span class="sxs-lookup"><span data-stu-id="b5a41-232">True</span></span>                                                                |
| <span data-ttu-id="b5a41-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5a41-233">Is Indexed</span></span>             | <span data-ttu-id="b5a41-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-234">False</span></span>                                                               |
| <span data-ttu-id="b5a41-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5a41-235">In Global Catalog</span></span>      | <span data-ttu-id="b5a41-236">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-236">False</span></span>                                                               |
| <span data-ttu-id="b5a41-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5a41-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5a41-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5a41-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b5a41-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5a41-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5a41-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-241">Search-Flags</span></span>           | <span data-ttu-id="b5a41-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5a41-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="b5a41-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-243">System-Flags</span></span>           | <span data-ttu-id="b5a41-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5a41-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="b5a41-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5a41-245">Classes used in</span></span>        | [<span data-ttu-id="b5a41-246">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="b5a41-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b5a41-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5a41-247">Windows Server 2012</span></span>



| <span data-ttu-id="b5a41-248">Voce</span><span class="sxs-lookup"><span data-stu-id="b5a41-248">Entry</span></span> | <span data-ttu-id="b5a41-249">Valore</span><span class="sxs-lookup"><span data-stu-id="b5a41-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b5a41-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b5a41-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b5a41-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="b5a41-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b5a41-252">System-Only</span></span>            | <span data-ttu-id="b5a41-253">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-253">False</span></span>                                                               |
| <span data-ttu-id="b5a41-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b5a41-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b5a41-255">Vero</span><span class="sxs-lookup"><span data-stu-id="b5a41-255">True</span></span>                                                                |
| <span data-ttu-id="b5a41-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b5a41-256">Is Indexed</span></span>             | <span data-ttu-id="b5a41-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-257">False</span></span>                                                               |
| <span data-ttu-id="b5a41-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b5a41-258">In Global Catalog</span></span>      | <span data-ttu-id="b5a41-259">Falso</span><span class="sxs-lookup"><span data-stu-id="b5a41-259">False</span></span>                                                               |
| <span data-ttu-id="b5a41-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b5a41-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b5a41-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b5a41-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="b5a41-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b5a41-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b5a41-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="b5a41-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-264">Search-Flags</span></span>           | <span data-ttu-id="b5a41-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5a41-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="b5a41-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b5a41-266">System-Flags</span></span>           | <span data-ttu-id="b5a41-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5a41-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="b5a41-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b5a41-268">Classes used in</span></span>        | [<span data-ttu-id="b5a41-269">**Gruppo-criteri-contenitore**</span><span class="sxs-lookup"><span data-stu-id="b5a41-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





