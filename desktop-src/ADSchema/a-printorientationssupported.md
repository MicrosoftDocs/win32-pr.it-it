---
title: Per gli orientamenti alla stampa-attributo supportato
description: Rotazione della pagina per la stampa orizzontale.
ms.assetid: a3e910f1-452e-4b85-8ede-50b7274475a0
ms.tgt_platform: multiple
keywords:
- Orientamento Stampa-schema AD dell'attributo supportato
- Schema AD dell'attributo printOrientationsSupported
topic_type:
- apiref
api_name:
- Print-Orientations-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49888caa713de7dd12616dcb9932e52b15b2a454
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303154"
---
# <a name="print-orientations-supported-attribute"></a><span data-ttu-id="4ab27-105">Per gli orientamenti alla stampa-attributo supportato</span><span class="sxs-lookup"><span data-stu-id="4ab27-105">Print-Orientations-Supported attribute</span></span>

<span data-ttu-id="4ab27-106">Rotazione della pagina per la stampa orizzontale.</span><span class="sxs-lookup"><span data-stu-id="4ab27-106">The page rotation for landscape printing.</span></span>



| <span data-ttu-id="4ab27-107">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-107">Entry</span></span> | <span data-ttu-id="4ab27-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-108">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="4ab27-109">CN</span><span class="sxs-lookup"><span data-stu-id="4ab27-109">CN</span></span>                | <span data-ttu-id="4ab27-110">Orientamento stampa-supportato</span><span class="sxs-lookup"><span data-stu-id="4ab27-110">Print-Orientations-Supported</span></span>                                |
| <span data-ttu-id="4ab27-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4ab27-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4ab27-112">printOrientationsSupported</span><span class="sxs-lookup"><span data-stu-id="4ab27-112">printOrientationsSupported</span></span>                                  |
| <span data-ttu-id="4ab27-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4ab27-113">Size</span></span>              | <span data-ttu-id="4ab27-114">4 byte.</span><span class="sxs-lookup"><span data-stu-id="4ab27-114">4 bytes.</span></span> <span data-ttu-id="4ab27-115">Valori possibili: 0, 90, 270 e 0 = nessun orizzontale.</span><span class="sxs-lookup"><span data-stu-id="4ab27-115">Possible values: 0, 90, 270, and 0 = no landscape.</span></span> |
| <span data-ttu-id="4ab27-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-116">Update Privilege</span></span>  | \-                                                          |
| <span data-ttu-id="4ab27-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-117">Update Frequency</span></span>  | \-                                                          |
| <span data-ttu-id="4ab27-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-118">Attribute-Id</span></span>      | <span data-ttu-id="4ab27-119">1.2.840.113556.1.4.240</span><span class="sxs-lookup"><span data-stu-id="4ab27-119">1.2.840.113556.1.4.240</span></span>                                      |
| <span data-ttu-id="4ab27-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4ab27-120">System-Id-Guid</span></span>    | <span data-ttu-id="4ab27-121">281416d0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4ab27-121">281416d0-1968-11d0-a28f-00aa003049e2</span></span>                        |
| <span data-ttu-id="4ab27-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ab27-122">Syntax</span></span>            | [<span data-ttu-id="4ab27-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4ab27-123">**String(Unicode)**</span></span>](s-string-unicode.md)                 |



## <a name="implementations"></a><span data-ttu-id="4ab27-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4ab27-124">Implementations</span></span>

-   [<span data-ttu-id="4ab27-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4ab27-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4ab27-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ab27-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ab27-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ab27-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ab27-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ab27-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ab27-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ab27-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ab27-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ab27-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4ab27-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ab27-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4ab27-132">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-132">Entry</span></span> | <span data-ttu-id="4ab27-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4ab27-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ab27-136">System-Only</span></span>            | <span data-ttu-id="4ab27-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-137">False</span></span>                                          |
| <span data-ttu-id="4ab27-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4ab27-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4ab27-139">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-139">False</span></span>                                          |
| <span data-ttu-id="4ab27-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4ab27-140">Is Indexed</span></span>             | <span data-ttu-id="4ab27-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-141">False</span></span>                                          |
| <span data-ttu-id="4ab27-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4ab27-142">In Global Catalog</span></span>      | <span data-ttu-id="4ab27-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-143">False</span></span>                                          |
| <span data-ttu-id="4ab27-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4ab27-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ab27-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4ab27-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4ab27-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ab27-146">Range-Lower</span></span>            | <span data-ttu-id="4ab27-147">1</span><span class="sxs-lookup"><span data-stu-id="4ab27-147">1</span></span>                                              |
| <span data-ttu-id="4ab27-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ab27-148">Range-Upper</span></span>            | <span data-ttu-id="4ab27-149">256</span><span class="sxs-lookup"><span data-stu-id="4ab27-149">256</span></span>                                            |
| <span data-ttu-id="4ab27-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-150">Search-Flags</span></span>           | <span data-ttu-id="4ab27-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ab27-151">0x00000000</span></span>                                     |
| <span data-ttu-id="4ab27-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-152">System-Flags</span></span>           | <span data-ttu-id="4ab27-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ab27-153">0x00000010</span></span>                                     |
| <span data-ttu-id="4ab27-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4ab27-154">Classes used in</span></span>        | [<span data-ttu-id="4ab27-155">**Coda di stampa**</span><span class="sxs-lookup"><span data-stu-id="4ab27-155">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4ab27-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ab27-156">Windows Server 2003</span></span>



| <span data-ttu-id="4ab27-157">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-157">Entry</span></span> | <span data-ttu-id="4ab27-158">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-158">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4ab27-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-159">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-160">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ab27-161">System-Only</span></span>            | <span data-ttu-id="4ab27-162">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-162">False</span></span>                                          |
| <span data-ttu-id="4ab27-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4ab27-163">Is-Single-Valued</span></span>       | <span data-ttu-id="4ab27-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-164">False</span></span>                                          |
| <span data-ttu-id="4ab27-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4ab27-165">Is Indexed</span></span>             | <span data-ttu-id="4ab27-166">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-166">False</span></span>                                          |
| <span data-ttu-id="4ab27-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4ab27-167">In Global Catalog</span></span>      | <span data-ttu-id="4ab27-168">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-168">False</span></span>                                          |
| <span data-ttu-id="4ab27-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4ab27-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ab27-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4ab27-170">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4ab27-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ab27-171">Range-Lower</span></span>            | <span data-ttu-id="4ab27-172">1</span><span class="sxs-lookup"><span data-stu-id="4ab27-172">1</span></span>                                              |
| <span data-ttu-id="4ab27-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ab27-173">Range-Upper</span></span>            | <span data-ttu-id="4ab27-174">256</span><span class="sxs-lookup"><span data-stu-id="4ab27-174">256</span></span>                                            |
| <span data-ttu-id="4ab27-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-175">Search-Flags</span></span>           | <span data-ttu-id="4ab27-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ab27-176">0x00000000</span></span>                                     |
| <span data-ttu-id="4ab27-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-177">System-Flags</span></span>           | <span data-ttu-id="4ab27-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ab27-178">0x00000010</span></span>                                     |
| <span data-ttu-id="4ab27-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4ab27-179">Classes used in</span></span>        | [<span data-ttu-id="4ab27-180">**Coda di stampa**</span><span class="sxs-lookup"><span data-stu-id="4ab27-180">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ab27-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ab27-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ab27-182">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-182">Entry</span></span> | <span data-ttu-id="4ab27-183">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-183">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4ab27-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-184">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-185">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ab27-186">System-Only</span></span>            | <span data-ttu-id="4ab27-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-187">False</span></span>                                          |
| <span data-ttu-id="4ab27-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4ab27-188">Is-Single-Valued</span></span>       | <span data-ttu-id="4ab27-189">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-189">False</span></span>                                          |
| <span data-ttu-id="4ab27-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4ab27-190">Is Indexed</span></span>             | <span data-ttu-id="4ab27-191">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-191">False</span></span>                                          |
| <span data-ttu-id="4ab27-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4ab27-192">In Global Catalog</span></span>      | <span data-ttu-id="4ab27-193">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-193">False</span></span>                                          |
| <span data-ttu-id="4ab27-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4ab27-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ab27-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4ab27-195">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4ab27-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ab27-196">Range-Lower</span></span>            | <span data-ttu-id="4ab27-197">1</span><span class="sxs-lookup"><span data-stu-id="4ab27-197">1</span></span>                                              |
| <span data-ttu-id="4ab27-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ab27-198">Range-Upper</span></span>            | <span data-ttu-id="4ab27-199">256</span><span class="sxs-lookup"><span data-stu-id="4ab27-199">256</span></span>                                            |
| <span data-ttu-id="4ab27-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-200">Search-Flags</span></span>           | <span data-ttu-id="4ab27-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ab27-201">0x00000000</span></span>                                     |
| <span data-ttu-id="4ab27-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-202">System-Flags</span></span>           | <span data-ttu-id="4ab27-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ab27-203">0x00000010</span></span>                                     |
| <span data-ttu-id="4ab27-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4ab27-204">Classes used in</span></span>        | [<span data-ttu-id="4ab27-205">**Coda di stampa**</span><span class="sxs-lookup"><span data-stu-id="4ab27-205">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ab27-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ab27-206">Windows Server 2008</span></span>



| <span data-ttu-id="4ab27-207">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-207">Entry</span></span> | <span data-ttu-id="4ab27-208">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-208">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4ab27-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-209">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-210">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ab27-211">System-Only</span></span>            | <span data-ttu-id="4ab27-212">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-212">False</span></span>                                          |
| <span data-ttu-id="4ab27-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4ab27-213">Is-Single-Valued</span></span>       | <span data-ttu-id="4ab27-214">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-214">False</span></span>                                          |
| <span data-ttu-id="4ab27-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4ab27-215">Is Indexed</span></span>             | <span data-ttu-id="4ab27-216">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-216">False</span></span>                                          |
| <span data-ttu-id="4ab27-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4ab27-217">In Global Catalog</span></span>      | <span data-ttu-id="4ab27-218">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-218">False</span></span>                                          |
| <span data-ttu-id="4ab27-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4ab27-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ab27-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4ab27-220">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4ab27-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ab27-221">Range-Lower</span></span>            | <span data-ttu-id="4ab27-222">1</span><span class="sxs-lookup"><span data-stu-id="4ab27-222">1</span></span>                                              |
| <span data-ttu-id="4ab27-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ab27-223">Range-Upper</span></span>            | <span data-ttu-id="4ab27-224">256</span><span class="sxs-lookup"><span data-stu-id="4ab27-224">256</span></span>                                            |
| <span data-ttu-id="4ab27-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-225">Search-Flags</span></span>           | <span data-ttu-id="4ab27-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ab27-226">0x00000000</span></span>                                     |
| <span data-ttu-id="4ab27-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-227">System-Flags</span></span>           | <span data-ttu-id="4ab27-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ab27-228">0x00000010</span></span>                                     |
| <span data-ttu-id="4ab27-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4ab27-229">Classes used in</span></span>        | [<span data-ttu-id="4ab27-230">**Coda di stampa**</span><span class="sxs-lookup"><span data-stu-id="4ab27-230">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ab27-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ab27-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ab27-232">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-232">Entry</span></span> | <span data-ttu-id="4ab27-233">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-233">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4ab27-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-234">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-235">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ab27-236">System-Only</span></span>            | <span data-ttu-id="4ab27-237">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-237">False</span></span>                                          |
| <span data-ttu-id="4ab27-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4ab27-238">Is-Single-Valued</span></span>       | <span data-ttu-id="4ab27-239">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-239">False</span></span>                                          |
| <span data-ttu-id="4ab27-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4ab27-240">Is Indexed</span></span>             | <span data-ttu-id="4ab27-241">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-241">False</span></span>                                          |
| <span data-ttu-id="4ab27-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4ab27-242">In Global Catalog</span></span>      | <span data-ttu-id="4ab27-243">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-243">False</span></span>                                          |
| <span data-ttu-id="4ab27-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4ab27-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ab27-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4ab27-245">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4ab27-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ab27-246">Range-Lower</span></span>            | <span data-ttu-id="4ab27-247">1</span><span class="sxs-lookup"><span data-stu-id="4ab27-247">1</span></span>                                              |
| <span data-ttu-id="4ab27-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ab27-248">Range-Upper</span></span>            | <span data-ttu-id="4ab27-249">256</span><span class="sxs-lookup"><span data-stu-id="4ab27-249">256</span></span>                                            |
| <span data-ttu-id="4ab27-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-250">Search-Flags</span></span>           | <span data-ttu-id="4ab27-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ab27-251">0x00000000</span></span>                                     |
| <span data-ttu-id="4ab27-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-252">System-Flags</span></span>           | <span data-ttu-id="4ab27-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ab27-253">0x00000010</span></span>                                     |
| <span data-ttu-id="4ab27-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4ab27-254">Classes used in</span></span>        | [<span data-ttu-id="4ab27-255">**Coda di stampa**</span><span class="sxs-lookup"><span data-stu-id="4ab27-255">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ab27-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ab27-256">Windows Server 2012</span></span>



| <span data-ttu-id="4ab27-257">Voce</span><span class="sxs-lookup"><span data-stu-id="4ab27-257">Entry</span></span> | <span data-ttu-id="4ab27-258">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab27-258">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="4ab27-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4ab27-259">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ab27-260">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="4ab27-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ab27-261">System-Only</span></span>            | <span data-ttu-id="4ab27-262">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-262">False</span></span>                                          |
| <span data-ttu-id="4ab27-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4ab27-263">Is-Single-Valued</span></span>       | <span data-ttu-id="4ab27-264">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-264">False</span></span>                                          |
| <span data-ttu-id="4ab27-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4ab27-265">Is Indexed</span></span>             | <span data-ttu-id="4ab27-266">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-266">False</span></span>                                          |
| <span data-ttu-id="4ab27-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4ab27-267">In Global Catalog</span></span>      | <span data-ttu-id="4ab27-268">Falso</span><span class="sxs-lookup"><span data-stu-id="4ab27-268">False</span></span>                                          |
| <span data-ttu-id="4ab27-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4ab27-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ab27-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4ab27-270">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="4ab27-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ab27-271">Range-Lower</span></span>            | <span data-ttu-id="4ab27-272">1</span><span class="sxs-lookup"><span data-stu-id="4ab27-272">1</span></span>                                              |
| <span data-ttu-id="4ab27-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ab27-273">Range-Upper</span></span>            | <span data-ttu-id="4ab27-274">256</span><span class="sxs-lookup"><span data-stu-id="4ab27-274">256</span></span>                                            |
| <span data-ttu-id="4ab27-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-275">Search-Flags</span></span>           | <span data-ttu-id="4ab27-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ab27-276">0x00000000</span></span>                                     |
| <span data-ttu-id="4ab27-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ab27-277">System-Flags</span></span>           | <span data-ttu-id="4ab27-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4ab27-278">0x00000010</span></span>                                     |
| <span data-ttu-id="4ab27-279">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4ab27-279">Classes used in</span></span>        | [<span data-ttu-id="4ab27-280">**Coda di stampa**</span><span class="sxs-lookup"><span data-stu-id="4ab27-280">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





