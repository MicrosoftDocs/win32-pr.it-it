---
title: RDN (attributo)
description: Nome distinto relativo (RDN) di un oggetto.
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo RDN
- nome attributo AD schema
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303417"
---
# <a name="rdn-attribute"></a><span data-ttu-id="f9ebc-105">RDN (attributo)</span><span class="sxs-lookup"><span data-stu-id="f9ebc-105">RDN attribute</span></span>

<span data-ttu-id="f9ebc-106">Nome distinto relativo (RDN) di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="f9ebc-107">Un RDN è la parte relativa di un nome distinto (DN), che identifica in modo univoco un oggetto LDAP.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="f9ebc-108">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-108">Entry</span></span> | <span data-ttu-id="f9ebc-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="f9ebc-110">CN</span><span class="sxs-lookup"><span data-stu-id="f9ebc-110">CN</span></span>                | <span data-ttu-id="f9ebc-111">RDN</span><span class="sxs-lookup"><span data-stu-id="f9ebc-111">RDN</span></span>                                            |
| <span data-ttu-id="f9ebc-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f9ebc-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f9ebc-113">name</span><span class="sxs-lookup"><span data-stu-id="f9ebc-113">name</span></span>                                           |
| <span data-ttu-id="f9ebc-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f9ebc-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="f9ebc-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-115">Update Privilege</span></span>  | <span data-ttu-id="f9ebc-116">Questo valore viene impostato dall'amministratore dello schema.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="f9ebc-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="f9ebc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-118">Attribute-Id</span></span>      | <span data-ttu-id="f9ebc-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="f9ebc-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f9ebc-120">System-Id-Guid</span></span>    | <span data-ttu-id="f9ebc-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f9ebc-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="f9ebc-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9ebc-122">Syntax</span></span>            | [<span data-ttu-id="f9ebc-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="f9ebc-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f9ebc-124">Implementations</span></span>

-   [<span data-ttu-id="f9ebc-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f9ebc-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f9ebc-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f9ebc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f9ebc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f9ebc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f9ebc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f9ebc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9ebc-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f9ebc-133">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-133">Entry</span></span> | <span data-ttu-id="f9ebc-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-136">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-137">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-138">System-Only</span></span>            | <span data-ttu-id="f9ebc-139">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-139">True</span></span>                            |
| <span data-ttu-id="f9ebc-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-141">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-141">True</span></span>                            |
| <span data-ttu-id="f9ebc-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-142">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-143">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-143">True</span></span>                            |
| <span data-ttu-id="f9ebc-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-144">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-145">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-145">True</span></span>                            |
| <span data-ttu-id="f9ebc-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-148">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-149">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-149">1</span></span>                               |
| <span data-ttu-id="f9ebc-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-150">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-151">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-151">255</span></span>                             |
| <span data-ttu-id="f9ebc-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-152">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-153">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-153">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-154">System-Flags</span></span>           | <span data-ttu-id="f9ebc-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-155">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-156">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-156">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-157">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f9ebc-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9ebc-158">Windows Server 2003</span></span>



| <span data-ttu-id="f9ebc-159">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-159">Entry</span></span> | <span data-ttu-id="f9ebc-160">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-161">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-162">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-163">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-164">System-Only</span></span>            | <span data-ttu-id="f9ebc-165">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-165">True</span></span>                            |
| <span data-ttu-id="f9ebc-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-166">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-167">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-167">True</span></span>                            |
| <span data-ttu-id="f9ebc-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-168">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-169">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-169">True</span></span>                            |
| <span data-ttu-id="f9ebc-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-170">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-171">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-171">True</span></span>                            |
| <span data-ttu-id="f9ebc-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-174">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-175">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-175">1</span></span>                               |
| <span data-ttu-id="f9ebc-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-176">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-177">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-177">255</span></span>                             |
| <span data-ttu-id="f9ebc-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-178">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-179">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-179">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-180">System-Flags</span></span>           | <span data-ttu-id="f9ebc-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-181">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-182">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-183">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f9ebc-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="f9ebc-184">ADAM</span></span>



| <span data-ttu-id="f9ebc-185">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-185">Entry</span></span> | <span data-ttu-id="f9ebc-186">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-188">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-189">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-190">System-Only</span></span>            | <span data-ttu-id="f9ebc-191">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-191">True</span></span>                            |
| <span data-ttu-id="f9ebc-192">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-192">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-193">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-193">True</span></span>                            |
| <span data-ttu-id="f9ebc-194">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-194">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-195">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-195">True</span></span>                            |
| <span data-ttu-id="f9ebc-196">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-196">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-197">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-197">True</span></span>                            |
| <span data-ttu-id="f9ebc-198">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-199">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-200">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-201">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-201">1</span></span>                               |
| <span data-ttu-id="f9ebc-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-202">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-203">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-203">255</span></span>                             |
| <span data-ttu-id="f9ebc-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-204">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-205">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-206">System-Flags</span></span>           | <span data-ttu-id="f9ebc-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-207">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-208">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-209">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f9ebc-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f9ebc-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f9ebc-211">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-211">Entry</span></span> | <span data-ttu-id="f9ebc-212">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-214">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-215">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-216">System-Only</span></span>            | <span data-ttu-id="f9ebc-217">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-217">True</span></span>                            |
| <span data-ttu-id="f9ebc-218">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-218">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-219">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-219">True</span></span>                            |
| <span data-ttu-id="f9ebc-220">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-220">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-221">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-221">True</span></span>                            |
| <span data-ttu-id="f9ebc-222">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-222">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-223">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-223">True</span></span>                            |
| <span data-ttu-id="f9ebc-224">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-225">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-226">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-227">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-227">1</span></span>                               |
| <span data-ttu-id="f9ebc-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-228">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-229">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-229">255</span></span>                             |
| <span data-ttu-id="f9ebc-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-230">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-231">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-231">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-232">System-Flags</span></span>           | <span data-ttu-id="f9ebc-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-233">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-234">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-234">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-235">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f9ebc-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9ebc-236">Windows Server 2008</span></span>



| <span data-ttu-id="f9ebc-237">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-237">Entry</span></span> | <span data-ttu-id="f9ebc-238">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-239">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-240">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-241">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-242">System-Only</span></span>            | <span data-ttu-id="f9ebc-243">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-243">True</span></span>                            |
| <span data-ttu-id="f9ebc-244">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-244">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-245">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-245">True</span></span>                            |
| <span data-ttu-id="f9ebc-246">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-246">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-247">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-247">True</span></span>                            |
| <span data-ttu-id="f9ebc-248">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-248">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-249">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-249">True</span></span>                            |
| <span data-ttu-id="f9ebc-250">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-251">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-252">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-253">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-253">1</span></span>                               |
| <span data-ttu-id="f9ebc-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-254">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-255">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-255">255</span></span>                             |
| <span data-ttu-id="f9ebc-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-256">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-257">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-257">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-258">System-Flags</span></span>           | <span data-ttu-id="f9ebc-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-259">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-260">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-260">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-261">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f9ebc-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9ebc-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f9ebc-263">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-263">Entry</span></span> | <span data-ttu-id="f9ebc-264">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-265">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-266">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-267">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-268">System-Only</span></span>            | <span data-ttu-id="f9ebc-269">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-269">True</span></span>                            |
| <span data-ttu-id="f9ebc-270">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-270">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-271">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-271">True</span></span>                            |
| <span data-ttu-id="f9ebc-272">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-272">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-273">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-273">True</span></span>                            |
| <span data-ttu-id="f9ebc-274">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-274">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-275">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-275">True</span></span>                            |
| <span data-ttu-id="f9ebc-276">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-277">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-278">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-279">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-279">1</span></span>                               |
| <span data-ttu-id="f9ebc-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-280">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-281">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-281">255</span></span>                             |
| <span data-ttu-id="f9ebc-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-282">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-283">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-283">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-284">System-Flags</span></span>           | <span data-ttu-id="f9ebc-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-285">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-286">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-286">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-287">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f9ebc-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-288">Windows Server 2012</span></span>



| <span data-ttu-id="f9ebc-289">Voce</span><span class="sxs-lookup"><span data-stu-id="f9ebc-289">Entry</span></span> | <span data-ttu-id="f9ebc-290">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9ebc-291">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f9ebc-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9ebc-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9ebc-292">MAPI-Id</span></span>                | <span data-ttu-id="f9ebc-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="f9ebc-293">0x8202</span></span>                          |
| <span data-ttu-id="f9ebc-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9ebc-294">System-Only</span></span>            | <span data-ttu-id="f9ebc-295">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-295">True</span></span>                            |
| <span data-ttu-id="f9ebc-296">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f9ebc-296">Is-Single-Valued</span></span>       | <span data-ttu-id="f9ebc-297">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-297">True</span></span>                            |
| <span data-ttu-id="f9ebc-298">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f9ebc-298">Is Indexed</span></span>             | <span data-ttu-id="f9ebc-299">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-299">True</span></span>                            |
| <span data-ttu-id="f9ebc-300">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f9ebc-300">In Global Catalog</span></span>      | <span data-ttu-id="f9ebc-301">Vero</span><span class="sxs-lookup"><span data-stu-id="f9ebc-301">True</span></span>                            |
| <span data-ttu-id="f9ebc-302">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f9ebc-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9ebc-303">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f9ebc-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9ebc-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9ebc-304">Range-Lower</span></span>            | <span data-ttu-id="f9ebc-305">1</span><span class="sxs-lookup"><span data-stu-id="f9ebc-305">1</span></span>                               |
| <span data-ttu-id="f9ebc-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9ebc-306">Range-Upper</span></span>            | <span data-ttu-id="f9ebc-307">255</span><span class="sxs-lookup"><span data-stu-id="f9ebc-307">255</span></span>                             |
| <span data-ttu-id="f9ebc-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-308">Search-Flags</span></span>           | <span data-ttu-id="f9ebc-309">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-309">0x0000000D</span></span>                      |
| <span data-ttu-id="f9ebc-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9ebc-310">System-Flags</span></span>           | <span data-ttu-id="f9ebc-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f9ebc-311">0x00000012</span></span>                      |
| <span data-ttu-id="f9ebc-312">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f9ebc-312">Classes used in</span></span>        | [<span data-ttu-id="f9ebc-313">**In alto**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-313">**Top**</span></span>](c-top.md)<br/> |



 

 





