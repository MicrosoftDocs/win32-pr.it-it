---
title: l'attributo di installazione locale-Local-OS
description: L'attributo di installazione a livello locale è riservato per uso interno.
ms.assetid: fb59183b-26dd-4f51-955e-32f7a706a59c
ms.tgt_platform: multiple
keywords:
- Schema di AD per l'attributo di servizi di installazione locale
- Schema AD dell'attributo netbootLocallyInstalledOSes
topic_type:
- apiref
api_name:
- netboot-Locally-Installed-OSes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff07c4e4ab605a90eb2f828443c8111fd30d009
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303409"
---
# <a name="netboot-locally-installed-oses-attribute"></a><span data-ttu-id="0a5bb-105">l'attributo di installazione locale-Local-OS</span><span class="sxs-lookup"><span data-stu-id="0a5bb-105">netboot-Locally-Installed-OSes attribute</span></span>

<span data-ttu-id="0a5bb-106">L'attributo di **installazione a livello locale** è riservato per uso interno.</span><span class="sxs-lookup"><span data-stu-id="0a5bb-106">The **netboot-Locally-Installed-OSes** attribute is reserved for internal use.</span></span>



| <span data-ttu-id="0a5bb-107">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-107">Entry</span></span> | <span data-ttu-id="0a5bb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0a5bb-109">CN</span><span class="sxs-lookup"><span data-stu-id="0a5bb-109">CN</span></span>                | <span data-ttu-id="0a5bb-110">modalità di installazione a livello locale-sistemi operativi</span><span class="sxs-lookup"><span data-stu-id="0a5bb-110">netboot-Locally-Installed-OSes</span></span>              |
| <span data-ttu-id="0a5bb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0a5bb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0a5bb-112">netbootLocallyInstalledOSes</span><span class="sxs-lookup"><span data-stu-id="0a5bb-112">netbootLocallyInstalledOSes</span></span>                 |
| <span data-ttu-id="0a5bb-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0a5bb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0a5bb-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-114">Update Privilege</span></span>  | <span data-ttu-id="0a5bb-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0a5bb-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="0a5bb-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0a5bb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-117">Attribute-Id</span></span>      | <span data-ttu-id="0a5bb-118">1.2.840.113556.1.4.859</span><span class="sxs-lookup"><span data-stu-id="0a5bb-118">1.2.840.113556.1.4.859</span></span>                      |
| <span data-ttu-id="0a5bb-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0a5bb-119">System-Id-Guid</span></span>    | <span data-ttu-id="0a5bb-120">07383080-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0a5bb-120">07383080-91df-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="0a5bb-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a5bb-121">Syntax</span></span>            | [<span data-ttu-id="0a5bb-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0a5bb-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="0a5bb-123">Implementations</span></span>

-   [<span data-ttu-id="0a5bb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0a5bb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0a5bb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0a5bb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0a5bb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0a5bb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0a5bb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a5bb-130">Windows 2000 Server</span></span>



| <span data-ttu-id="0a5bb-131">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-131">Entry</span></span> | <span data-ttu-id="0a5bb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a5bb-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a5bb-135">System-Only</span></span>            | <span data-ttu-id="0a5bb-136">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-136">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0a5bb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0a5bb-138">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-138">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0a5bb-139">Is Indexed</span></span>             | <span data-ttu-id="0a5bb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-140">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0a5bb-141">In Global Catalog</span></span>      | <span data-ttu-id="0a5bb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-142">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a5bb-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0a5bb-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0a5bb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a5bb-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a5bb-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-147">Search-Flags</span></span>           | <span data-ttu-id="0a5bb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a5bb-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="0a5bb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-149">System-Flags</span></span>           | <span data-ttu-id="0a5bb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a5bb-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="0a5bb-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0a5bb-151">Classes used in</span></span>        | [<span data-ttu-id="0a5bb-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0a5bb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0a5bb-153">Windows Server 2003</span></span>



| <span data-ttu-id="0a5bb-154">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-154">Entry</span></span> | <span data-ttu-id="0a5bb-155">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a5bb-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a5bb-158">System-Only</span></span>            | <span data-ttu-id="0a5bb-159">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-159">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0a5bb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="0a5bb-161">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-161">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0a5bb-162">Is Indexed</span></span>             | <span data-ttu-id="0a5bb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-163">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0a5bb-164">In Global Catalog</span></span>      | <span data-ttu-id="0a5bb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-165">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a5bb-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0a5bb-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0a5bb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a5bb-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a5bb-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-170">Search-Flags</span></span>           | <span data-ttu-id="0a5bb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a5bb-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="0a5bb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-172">System-Flags</span></span>           | <span data-ttu-id="0a5bb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a5bb-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="0a5bb-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0a5bb-174">Classes used in</span></span>        | [<span data-ttu-id="0a5bb-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0a5bb-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0a5bb-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0a5bb-177">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-177">Entry</span></span> | <span data-ttu-id="0a5bb-178">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a5bb-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a5bb-181">System-Only</span></span>            | <span data-ttu-id="0a5bb-182">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-182">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0a5bb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="0a5bb-184">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-184">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0a5bb-185">Is Indexed</span></span>             | <span data-ttu-id="0a5bb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-186">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0a5bb-187">In Global Catalog</span></span>      | <span data-ttu-id="0a5bb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-188">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a5bb-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0a5bb-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0a5bb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a5bb-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a5bb-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-193">Search-Flags</span></span>           | <span data-ttu-id="0a5bb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a5bb-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="0a5bb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-195">System-Flags</span></span>           | <span data-ttu-id="0a5bb-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a5bb-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="0a5bb-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0a5bb-197">Classes used in</span></span>        | [<span data-ttu-id="0a5bb-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0a5bb-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a5bb-199">Windows Server 2008</span></span>



| <span data-ttu-id="0a5bb-200">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-200">Entry</span></span> | <span data-ttu-id="0a5bb-201">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a5bb-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a5bb-204">System-Only</span></span>            | <span data-ttu-id="0a5bb-205">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-205">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0a5bb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="0a5bb-207">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-207">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0a5bb-208">Is Indexed</span></span>             | <span data-ttu-id="0a5bb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-209">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0a5bb-210">In Global Catalog</span></span>      | <span data-ttu-id="0a5bb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-211">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a5bb-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0a5bb-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0a5bb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a5bb-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a5bb-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-216">Search-Flags</span></span>           | <span data-ttu-id="0a5bb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a5bb-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="0a5bb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-218">System-Flags</span></span>           | <span data-ttu-id="0a5bb-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a5bb-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="0a5bb-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0a5bb-220">Classes used in</span></span>        | [<span data-ttu-id="0a5bb-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0a5bb-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0a5bb-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0a5bb-223">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-223">Entry</span></span> | <span data-ttu-id="0a5bb-224">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a5bb-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a5bb-227">System-Only</span></span>            | <span data-ttu-id="0a5bb-228">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-228">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0a5bb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="0a5bb-230">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-230">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0a5bb-231">Is Indexed</span></span>             | <span data-ttu-id="0a5bb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-232">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0a5bb-233">In Global Catalog</span></span>      | <span data-ttu-id="0a5bb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-234">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a5bb-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0a5bb-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0a5bb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a5bb-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a5bb-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-239">Search-Flags</span></span>           | <span data-ttu-id="0a5bb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a5bb-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="0a5bb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-241">System-Flags</span></span>           | <span data-ttu-id="0a5bb-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a5bb-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="0a5bb-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0a5bb-243">Classes used in</span></span>        | [<span data-ttu-id="0a5bb-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0a5bb-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0a5bb-245">Windows Server 2012</span></span>



| <span data-ttu-id="0a5bb-246">Voce</span><span class="sxs-lookup"><span data-stu-id="0a5bb-246">Entry</span></span> | <span data-ttu-id="0a5bb-247">Valore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a5bb-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0a5bb-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0a5bb-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0a5bb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="0a5bb-250">System-Only</span></span>            | <span data-ttu-id="0a5bb-251">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-251">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0a5bb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="0a5bb-253">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-253">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0a5bb-254">Is Indexed</span></span>             | <span data-ttu-id="0a5bb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-255">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0a5bb-256">In Global Catalog</span></span>      | <span data-ttu-id="0a5bb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="0a5bb-257">False</span></span>                                                      |
| <span data-ttu-id="0a5bb-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0a5bb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="0a5bb-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0a5bb-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0a5bb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0a5bb-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0a5bb-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0a5bb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-262">Search-Flags</span></span>           | <span data-ttu-id="0a5bb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0a5bb-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="0a5bb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0a5bb-264">System-Flags</span></span>           | <span data-ttu-id="0a5bb-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a5bb-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="0a5bb-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0a5bb-266">Classes used in</span></span>        | [<span data-ttu-id="0a5bb-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="0a5bb-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





