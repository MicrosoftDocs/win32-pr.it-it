---
title: Attributo DS-Heuristics
description: Contiene le impostazioni globali per l'intera foresta.
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- Schema AD DS-Heuristics attribute
- Schema AD dell'attributo dSHeuristics
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302933"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="93f70-105">Attributo DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="93f70-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="93f70-106">Contiene le impostazioni globali per l'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="93f70-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="93f70-107">Sono disponibili informazioni sui bit di esclusione di adminSDholder disponibili nel sito Web della guida e del supporto tecnico Microsoft in un articolo numero [817433, le autorizzazioni delegate non sono disponibili e l'ereditarietà viene disabilitata automaticamente](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span><span class="sxs-lookup"><span data-stu-id="93f70-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="93f70-108">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-108">Entry</span></span> | <span data-ttu-id="93f70-109">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="93f70-110">CN</span><span class="sxs-lookup"><span data-stu-id="93f70-110">CN</span></span>                | <span data-ttu-id="93f70-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="93f70-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="93f70-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="93f70-112">Ldap-Display-Name</span></span> | <span data-ttu-id="93f70-113">dSHeuristics</span><span class="sxs-lookup"><span data-stu-id="93f70-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="93f70-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="93f70-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="93f70-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="93f70-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="93f70-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="93f70-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="93f70-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-117">Attribute-Id</span></span>      | <span data-ttu-id="93f70-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="93f70-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="93f70-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="93f70-119">System-Id-Guid</span></span>    | <span data-ttu-id="93f70-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="93f70-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="93f70-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93f70-121">Syntax</span></span>            | [<span data-ttu-id="93f70-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="93f70-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="93f70-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="93f70-123">Implementations</span></span>

-   [<span data-ttu-id="93f70-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="93f70-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="93f70-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="93f70-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="93f70-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="93f70-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="93f70-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="93f70-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="93f70-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="93f70-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="93f70-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="93f70-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="93f70-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="93f70-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="93f70-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93f70-131">Windows 2000 Server</span></span>



| <span data-ttu-id="93f70-132">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-132">Entry</span></span> | <span data-ttu-id="93f70-133">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-136">System-Only</span></span>            | <span data-ttu-id="93f70-137">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-137">False</span></span>                                            |
| <span data-ttu-id="93f70-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-138">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-139">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-139">True</span></span>                                             |
| <span data-ttu-id="93f70-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-140">Is Indexed</span></span>             | <span data-ttu-id="93f70-141">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-141">False</span></span>                                            |
| <span data-ttu-id="93f70-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-142">In Global Catalog</span></span>      | <span data-ttu-id="93f70-143">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-143">False</span></span>                                            |
| <span data-ttu-id="93f70-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-148">Search-Flags</span></span>           | <span data-ttu-id="93f70-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-149">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-150">System-Flags</span></span>           | <span data-ttu-id="93f70-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-151">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-152">Classes used in</span></span>        | [<span data-ttu-id="93f70-153">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="93f70-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93f70-154">Windows Server 2003</span></span>



| <span data-ttu-id="93f70-155">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-155">Entry</span></span> | <span data-ttu-id="93f70-156">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-159">System-Only</span></span>            | <span data-ttu-id="93f70-160">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-160">False</span></span>                                            |
| <span data-ttu-id="93f70-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-161">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-162">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-162">True</span></span>                                             |
| <span data-ttu-id="93f70-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-163">Is Indexed</span></span>             | <span data-ttu-id="93f70-164">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-164">False</span></span>                                            |
| <span data-ttu-id="93f70-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-165">In Global Catalog</span></span>      | <span data-ttu-id="93f70-166">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-166">False</span></span>                                            |
| <span data-ttu-id="93f70-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-171">Search-Flags</span></span>           | <span data-ttu-id="93f70-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-172">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-173">System-Flags</span></span>           | <span data-ttu-id="93f70-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-174">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-175">Classes used in</span></span>        | [<span data-ttu-id="93f70-176">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="93f70-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="93f70-177">ADAM</span></span>



| <span data-ttu-id="93f70-178">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-178">Entry</span></span> | <span data-ttu-id="93f70-179">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-182">System-Only</span></span>            | <span data-ttu-id="93f70-183">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-183">False</span></span>                                            |
| <span data-ttu-id="93f70-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-184">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-185">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-185">True</span></span>                                             |
| <span data-ttu-id="93f70-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-186">Is Indexed</span></span>             | <span data-ttu-id="93f70-187">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-187">False</span></span>                                            |
| <span data-ttu-id="93f70-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-188">In Global Catalog</span></span>      | <span data-ttu-id="93f70-189">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-189">False</span></span>                                            |
| <span data-ttu-id="93f70-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-194">Search-Flags</span></span>           | <span data-ttu-id="93f70-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-195">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-196">System-Flags</span></span>           | <span data-ttu-id="93f70-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-197">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-198">Classes used in</span></span>        | [<span data-ttu-id="93f70-199">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="93f70-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="93f70-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="93f70-201">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-201">Entry</span></span> | <span data-ttu-id="93f70-202">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-205">System-Only</span></span>            | <span data-ttu-id="93f70-206">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-206">False</span></span>                                            |
| <span data-ttu-id="93f70-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-207">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-208">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-208">True</span></span>                                             |
| <span data-ttu-id="93f70-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-209">Is Indexed</span></span>             | <span data-ttu-id="93f70-210">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-210">False</span></span>                                            |
| <span data-ttu-id="93f70-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-211">In Global Catalog</span></span>      | <span data-ttu-id="93f70-212">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-212">False</span></span>                                            |
| <span data-ttu-id="93f70-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-217">Search-Flags</span></span>           | <span data-ttu-id="93f70-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-218">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-219">System-Flags</span></span>           | <span data-ttu-id="93f70-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-220">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-221">Classes used in</span></span>        | [<span data-ttu-id="93f70-222">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="93f70-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93f70-223">Windows Server 2008</span></span>



| <span data-ttu-id="93f70-224">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-224">Entry</span></span> | <span data-ttu-id="93f70-225">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-228">System-Only</span></span>            | <span data-ttu-id="93f70-229">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-229">False</span></span>                                            |
| <span data-ttu-id="93f70-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-230">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-231">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-231">True</span></span>                                             |
| <span data-ttu-id="93f70-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-232">Is Indexed</span></span>             | <span data-ttu-id="93f70-233">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-233">False</span></span>                                            |
| <span data-ttu-id="93f70-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-234">In Global Catalog</span></span>      | <span data-ttu-id="93f70-235">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-235">False</span></span>                                            |
| <span data-ttu-id="93f70-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-240">Search-Flags</span></span>           | <span data-ttu-id="93f70-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-241">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-242">System-Flags</span></span>           | <span data-ttu-id="93f70-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-243">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-244">Classes used in</span></span>        | [<span data-ttu-id="93f70-245">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="93f70-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93f70-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="93f70-247">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-247">Entry</span></span> | <span data-ttu-id="93f70-248">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-251">System-Only</span></span>            | <span data-ttu-id="93f70-252">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-252">False</span></span>                                            |
| <span data-ttu-id="93f70-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-253">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-254">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-254">True</span></span>                                             |
| <span data-ttu-id="93f70-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-255">Is Indexed</span></span>             | <span data-ttu-id="93f70-256">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-256">False</span></span>                                            |
| <span data-ttu-id="93f70-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-257">In Global Catalog</span></span>      | <span data-ttu-id="93f70-258">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-258">False</span></span>                                            |
| <span data-ttu-id="93f70-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-263">Search-Flags</span></span>           | <span data-ttu-id="93f70-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-264">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-265">System-Flags</span></span>           | <span data-ttu-id="93f70-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-266">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-267">Classes used in</span></span>        | [<span data-ttu-id="93f70-268">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="93f70-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93f70-269">Windows Server 2012</span></span>



| <span data-ttu-id="93f70-270">Voce</span><span class="sxs-lookup"><span data-stu-id="93f70-270">Entry</span></span> | <span data-ttu-id="93f70-271">Valore</span><span class="sxs-lookup"><span data-stu-id="93f70-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="93f70-272">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="93f70-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="93f70-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="93f70-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="93f70-274">System-Only</span></span>            | <span data-ttu-id="93f70-275">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-275">False</span></span>                                            |
| <span data-ttu-id="93f70-276">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="93f70-276">Is-Single-Valued</span></span>       | <span data-ttu-id="93f70-277">Vero</span><span class="sxs-lookup"><span data-stu-id="93f70-277">True</span></span>                                             |
| <span data-ttu-id="93f70-278">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="93f70-278">Is Indexed</span></span>             | <span data-ttu-id="93f70-279">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-279">False</span></span>                                            |
| <span data-ttu-id="93f70-280">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="93f70-280">In Global Catalog</span></span>      | <span data-ttu-id="93f70-281">Falso</span><span class="sxs-lookup"><span data-stu-id="93f70-281">False</span></span>                                            |
| <span data-ttu-id="93f70-282">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="93f70-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="93f70-283">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="93f70-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="93f70-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="93f70-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="93f70-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="93f70-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="93f70-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-286">Search-Flags</span></span>           | <span data-ttu-id="93f70-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="93f70-287">0x00000000</span></span>                                       |
| <span data-ttu-id="93f70-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="93f70-288">System-Flags</span></span>           | <span data-ttu-id="93f70-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="93f70-289">0x00000010</span></span>                                       |
| <span data-ttu-id="93f70-290">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="93f70-290">Classes used in</span></span>        | [<span data-ttu-id="93f70-291">**NTDS-Service**</span><span class="sxs-lookup"><span data-stu-id="93f70-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="93f70-292">Commenti</span><span class="sxs-lookup"><span data-stu-id="93f70-292">Remarks</span></span>

<span data-ttu-id="93f70-293">Ogni foresta Active Directory contiene un attributo DS-Heuristics che contiene le impostazioni per l'intera foresta.</span><span class="sxs-lookup"><span data-stu-id="93f70-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="93f70-294">L'attributo DS-Heuristics è un attributo dell'oggetto "CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration <Domain> ".</span><span class="sxs-lookup"><span data-stu-id="93f70-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="93f70-295">DS-Heuristics è una stringa Unicode in cui ogni carattere contiene un valore per una singola impostazione a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="93f70-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="93f70-296">La stringa DS-Heuristics accetta il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="93f70-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="93f70-297">Per consentire la convalida dei dati, ogni decimo carattere viene impostato sul numero di caratteri diviso per dieci.</span><span class="sxs-lookup"><span data-stu-id="93f70-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="93f70-298">Ad esempio, il decimo carattere è "1"; il ventesimo carattere è "2" e così via.</span><span class="sxs-lookup"><span data-stu-id="93f70-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="93f70-299">Si presuppone che qualsiasi carattere non impostato sia ' 0'.</span><span class="sxs-lookup"><span data-stu-id="93f70-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="93f70-300">Se l'attributo DS-Heuristics non è impostato, si presuppone che tutti i valori siano ' 0'.</span><span class="sxs-lookup"><span data-stu-id="93f70-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="93f70-301">Sono attualmente in uso 25 caratteri e non è necessario riempire la stringa per riempire tutti i 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="93f70-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="93f70-302">Se, ad esempio, il carattere più elevato utilizzato è 7, la stringa "0000002" è accettabile.</span><span class="sxs-lookup"><span data-stu-id="93f70-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="93f70-303">Per informazioni dettagliate su ogni carattere, vedere [dsHeuristics in \[ MS-ADTS \] Active Directory specifica tecnica](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span><span class="sxs-lookup"><span data-stu-id="93f70-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="93f70-304">Filtri di ricerca ANR</span><span class="sxs-lookup"><span data-stu-id="93f70-304">ANR Search Filters</span></span>

<span data-ttu-id="93f70-305">I caratteri 1, 2 e 4 vengono usati per modificare il comportamento dei filtri di ricerca ANR.</span><span class="sxs-lookup"><span data-stu-id="93f70-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="93f70-306">Se il carattere 1 è impostato su "1", l'espansione del filtro ANR per includere il   -  **Cognome** specificato (quando viene trovato spazio) è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="93f70-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="93f70-307">Se il carattere 2 è impostato su "1", l'espansione del filtro ANR per includere il **Cognome**  -  **specificato** è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="93f70-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="93f70-308">Se nella stringa di ricerca è presente uno spazio incorporato, la stringa di ricerca viene in genere divisa in due stringhe, che vengono confrontate a coppie con gli attributi **given** e **Cognome** .</span><span class="sxs-lookup"><span data-stu-id="93f70-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="93f70-309">Se si impostano i caratteri 1 e 2 su "1", le corrispondenze non verranno tentate.</span><span class="sxs-lookup"><span data-stu-id="93f70-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="93f70-310">Questa corrispondenza potrebbe essere disabilitata se l'amministratore è sicuro che la ricerca di "Jeff Smith" verrebbe sempre fornita come "Jeff Smith" e non "Smith, Jeff".</span><span class="sxs-lookup"><span data-stu-id="93f70-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="93f70-311">In genere, solo una o l'altra corrispondenze verrebbe evitata, in base alla convenzione locale.</span><span class="sxs-lookup"><span data-stu-id="93f70-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="93f70-312">Se il carattere 4 è impostato su "1", Active Directory eseguirà la risoluzione del nome alternativo preventivo.</span><span class="sxs-lookup"><span data-stu-id="93f70-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="93f70-313">Ovvero, se la stringa di ricerca corrisponde esattamente al nome alternativo di un oggetto nell'ambito di ricerca, viene restituito un oggetto come risultato della ricerca e il resto di ANR viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="93f70-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="93f70-314">Si noti che mentre il resto della ricerca ANR è disponibile tramite LDAP, la risoluzione del nome alternativo preventivo (nota anche come "soprannome snap") è disponibile solo tramite MAPI.</span><span class="sxs-lookup"><span data-stu-id="93f70-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="93f70-315">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93f70-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="93f70-316">[dSHeuristics in \[ MS-ADTS \] Active Directory specifica tecnica](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="93f70-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 

