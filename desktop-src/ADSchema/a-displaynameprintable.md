---
title: Display-name-attributo stampabile
description: Nome visualizzato stampabile per un oggetto.
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- Nome visualizzato-schema AD dell'attributo stampabile
- Schema AD dell'attributo displayNamePrintable
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875798"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="b4925-105">Display-name-attributo stampabile</span><span class="sxs-lookup"><span data-stu-id="b4925-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="b4925-106">Nome visualizzato stampabile per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4925-106">The printable display name for an object.</span></span> <span data-ttu-id="b4925-107">Il nome visualizzato stampabile è in genere la combinazione del nome e del cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b4925-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="b4925-108">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-108">Entry</span></span> | <span data-ttu-id="b4925-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="b4925-110">CN</span><span class="sxs-lookup"><span data-stu-id="b4925-110">CN</span></span>                | <span data-ttu-id="b4925-111">Display-Name-stampabile</span><span class="sxs-lookup"><span data-stu-id="b4925-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="b4925-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b4925-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b4925-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="b4925-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="b4925-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b4925-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="b4925-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b4925-115">Update Privilege</span></span>  | <span data-ttu-id="b4925-116">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="b4925-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="b4925-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b4925-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="b4925-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-118">Attribute-Id</span></span>      | <span data-ttu-id="b4925-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="b4925-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="b4925-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b4925-120">System-Id-Guid</span></span>    | <span data-ttu-id="b4925-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b4925-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="b4925-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4925-122">Syntax</span></span>            | [<span data-ttu-id="b4925-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="b4925-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="b4925-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b4925-124">Implementations</span></span>

-   [<span data-ttu-id="b4925-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4925-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4925-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4925-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4925-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4925-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4925-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4925-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4925-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4925-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4925-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4925-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4925-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4925-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b4925-132">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-132">Entry</span></span> | <span data-ttu-id="b4925-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4925-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b4925-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4925-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-135">MAPI-Id</span></span>                | <span data-ttu-id="b4925-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b4925-136">0x39FF</span></span>                          |
| <span data-ttu-id="b4925-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4925-137">System-Only</span></span>            | <span data-ttu-id="b4925-138">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-138">False</span></span>                           |
| <span data-ttu-id="b4925-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b4925-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b4925-140">Vero</span><span class="sxs-lookup"><span data-stu-id="b4925-140">True</span></span>                            |
| <span data-ttu-id="b4925-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b4925-141">Is Indexed</span></span>             | <span data-ttu-id="b4925-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-142">False</span></span>                           |
| <span data-ttu-id="b4925-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b4925-143">In Global Catalog</span></span>      | <span data-ttu-id="b4925-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-144">False</span></span>                           |
| <span data-ttu-id="b4925-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b4925-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4925-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b4925-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4925-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4925-147">Range-Lower</span></span>            | <span data-ttu-id="b4925-148">1</span><span class="sxs-lookup"><span data-stu-id="b4925-148">1</span></span>                               |
| <span data-ttu-id="b4925-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4925-149">Range-Upper</span></span>            | <span data-ttu-id="b4925-150">256</span><span class="sxs-lookup"><span data-stu-id="b4925-150">256</span></span>                             |
| <span data-ttu-id="b4925-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-151">Search-Flags</span></span>           | <span data-ttu-id="b4925-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4925-152">0x00000000</span></span>                      |
| <span data-ttu-id="b4925-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-153">System-Flags</span></span>           | <span data-ttu-id="b4925-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4925-154">0x00000010</span></span>                      |
| <span data-ttu-id="b4925-155">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b4925-155">Classes used in</span></span>        | [<span data-ttu-id="b4925-156">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b4925-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4925-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4925-157">Windows Server 2003</span></span>



| <span data-ttu-id="b4925-158">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-158">Entry</span></span> | <span data-ttu-id="b4925-159">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4925-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b4925-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4925-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-161">MAPI-Id</span></span>                | <span data-ttu-id="b4925-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b4925-162">0x39FF</span></span>                          |
| <span data-ttu-id="b4925-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4925-163">System-Only</span></span>            | <span data-ttu-id="b4925-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-164">False</span></span>                           |
| <span data-ttu-id="b4925-165">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b4925-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b4925-166">Vero</span><span class="sxs-lookup"><span data-stu-id="b4925-166">True</span></span>                            |
| <span data-ttu-id="b4925-167">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b4925-167">Is Indexed</span></span>             | <span data-ttu-id="b4925-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-168">False</span></span>                           |
| <span data-ttu-id="b4925-169">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b4925-169">In Global Catalog</span></span>      | <span data-ttu-id="b4925-170">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-170">False</span></span>                           |
| <span data-ttu-id="b4925-171">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b4925-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4925-172">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b4925-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4925-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4925-173">Range-Lower</span></span>            | <span data-ttu-id="b4925-174">1</span><span class="sxs-lookup"><span data-stu-id="b4925-174">1</span></span>                               |
| <span data-ttu-id="b4925-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4925-175">Range-Upper</span></span>            | <span data-ttu-id="b4925-176">256</span><span class="sxs-lookup"><span data-stu-id="b4925-176">256</span></span>                             |
| <span data-ttu-id="b4925-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-177">Search-Flags</span></span>           | <span data-ttu-id="b4925-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4925-178">0x00000000</span></span>                      |
| <span data-ttu-id="b4925-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-179">System-Flags</span></span>           | <span data-ttu-id="b4925-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4925-180">0x00000010</span></span>                      |
| <span data-ttu-id="b4925-181">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b4925-181">Classes used in</span></span>        | [<span data-ttu-id="b4925-182">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b4925-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4925-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4925-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4925-184">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-184">Entry</span></span> | <span data-ttu-id="b4925-185">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4925-186">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b4925-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4925-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-187">MAPI-Id</span></span>                | <span data-ttu-id="b4925-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b4925-188">0x39FF</span></span>                          |
| <span data-ttu-id="b4925-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4925-189">System-Only</span></span>            | <span data-ttu-id="b4925-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-190">False</span></span>                           |
| <span data-ttu-id="b4925-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b4925-191">Is-Single-Valued</span></span>       | <span data-ttu-id="b4925-192">Vero</span><span class="sxs-lookup"><span data-stu-id="b4925-192">True</span></span>                            |
| <span data-ttu-id="b4925-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b4925-193">Is Indexed</span></span>             | <span data-ttu-id="b4925-194">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-194">False</span></span>                           |
| <span data-ttu-id="b4925-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b4925-195">In Global Catalog</span></span>      | <span data-ttu-id="b4925-196">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-196">False</span></span>                           |
| <span data-ttu-id="b4925-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b4925-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4925-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b4925-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4925-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4925-199">Range-Lower</span></span>            | <span data-ttu-id="b4925-200">1</span><span class="sxs-lookup"><span data-stu-id="b4925-200">1</span></span>                               |
| <span data-ttu-id="b4925-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4925-201">Range-Upper</span></span>            | <span data-ttu-id="b4925-202">256</span><span class="sxs-lookup"><span data-stu-id="b4925-202">256</span></span>                             |
| <span data-ttu-id="b4925-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-203">Search-Flags</span></span>           | <span data-ttu-id="b4925-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4925-204">0x00000000</span></span>                      |
| <span data-ttu-id="b4925-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-205">System-Flags</span></span>           | <span data-ttu-id="b4925-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4925-206">0x00000010</span></span>                      |
| <span data-ttu-id="b4925-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b4925-207">Classes used in</span></span>        | [<span data-ttu-id="b4925-208">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b4925-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4925-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4925-209">Windows Server 2008</span></span>



| <span data-ttu-id="b4925-210">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-210">Entry</span></span> | <span data-ttu-id="b4925-211">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4925-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b4925-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4925-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-213">MAPI-Id</span></span>                | <span data-ttu-id="b4925-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b4925-214">0x39FF</span></span>                          |
| <span data-ttu-id="b4925-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4925-215">System-Only</span></span>            | <span data-ttu-id="b4925-216">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-216">False</span></span>                           |
| <span data-ttu-id="b4925-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b4925-217">Is-Single-Valued</span></span>       | <span data-ttu-id="b4925-218">Vero</span><span class="sxs-lookup"><span data-stu-id="b4925-218">True</span></span>                            |
| <span data-ttu-id="b4925-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b4925-219">Is Indexed</span></span>             | <span data-ttu-id="b4925-220">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-220">False</span></span>                           |
| <span data-ttu-id="b4925-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b4925-221">In Global Catalog</span></span>      | <span data-ttu-id="b4925-222">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-222">False</span></span>                           |
| <span data-ttu-id="b4925-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b4925-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4925-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b4925-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4925-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4925-225">Range-Lower</span></span>            | <span data-ttu-id="b4925-226">1</span><span class="sxs-lookup"><span data-stu-id="b4925-226">1</span></span>                               |
| <span data-ttu-id="b4925-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4925-227">Range-Upper</span></span>            | <span data-ttu-id="b4925-228">256</span><span class="sxs-lookup"><span data-stu-id="b4925-228">256</span></span>                             |
| <span data-ttu-id="b4925-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-229">Search-Flags</span></span>           | <span data-ttu-id="b4925-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4925-230">0x00000000</span></span>                      |
| <span data-ttu-id="b4925-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-231">System-Flags</span></span>           | <span data-ttu-id="b4925-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4925-232">0x00000010</span></span>                      |
| <span data-ttu-id="b4925-233">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b4925-233">Classes used in</span></span>        | [<span data-ttu-id="b4925-234">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b4925-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4925-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4925-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4925-236">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-236">Entry</span></span> | <span data-ttu-id="b4925-237">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4925-238">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b4925-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4925-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-239">MAPI-Id</span></span>                | <span data-ttu-id="b4925-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b4925-240">0x39FF</span></span>                          |
| <span data-ttu-id="b4925-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4925-241">System-Only</span></span>            | <span data-ttu-id="b4925-242">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-242">False</span></span>                           |
| <span data-ttu-id="b4925-243">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b4925-243">Is-Single-Valued</span></span>       | <span data-ttu-id="b4925-244">Vero</span><span class="sxs-lookup"><span data-stu-id="b4925-244">True</span></span>                            |
| <span data-ttu-id="b4925-245">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b4925-245">Is Indexed</span></span>             | <span data-ttu-id="b4925-246">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-246">False</span></span>                           |
| <span data-ttu-id="b4925-247">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b4925-247">In Global Catalog</span></span>      | <span data-ttu-id="b4925-248">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-248">False</span></span>                           |
| <span data-ttu-id="b4925-249">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b4925-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4925-250">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b4925-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4925-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4925-251">Range-Lower</span></span>            | <span data-ttu-id="b4925-252">1</span><span class="sxs-lookup"><span data-stu-id="b4925-252">1</span></span>                               |
| <span data-ttu-id="b4925-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4925-253">Range-Upper</span></span>            | <span data-ttu-id="b4925-254">256</span><span class="sxs-lookup"><span data-stu-id="b4925-254">256</span></span>                             |
| <span data-ttu-id="b4925-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-255">Search-Flags</span></span>           | <span data-ttu-id="b4925-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4925-256">0x00000000</span></span>                      |
| <span data-ttu-id="b4925-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-257">System-Flags</span></span>           | <span data-ttu-id="b4925-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4925-258">0x00000010</span></span>                      |
| <span data-ttu-id="b4925-259">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b4925-259">Classes used in</span></span>        | [<span data-ttu-id="b4925-260">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b4925-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4925-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4925-261">Windows Server 2012</span></span>



| <span data-ttu-id="b4925-262">Voce</span><span class="sxs-lookup"><span data-stu-id="b4925-262">Entry</span></span> | <span data-ttu-id="b4925-263">Valore</span><span class="sxs-lookup"><span data-stu-id="b4925-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b4925-264">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b4925-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b4925-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4925-265">MAPI-Id</span></span>                | <span data-ttu-id="b4925-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b4925-266">0x39FF</span></span>                          |
| <span data-ttu-id="b4925-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4925-267">System-Only</span></span>            | <span data-ttu-id="b4925-268">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-268">False</span></span>                           |
| <span data-ttu-id="b4925-269">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b4925-269">Is-Single-Valued</span></span>       | <span data-ttu-id="b4925-270">Vero</span><span class="sxs-lookup"><span data-stu-id="b4925-270">True</span></span>                            |
| <span data-ttu-id="b4925-271">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b4925-271">Is Indexed</span></span>             | <span data-ttu-id="b4925-272">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-272">False</span></span>                           |
| <span data-ttu-id="b4925-273">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b4925-273">In Global Catalog</span></span>      | <span data-ttu-id="b4925-274">Falso</span><span class="sxs-lookup"><span data-stu-id="b4925-274">False</span></span>                           |
| <span data-ttu-id="b4925-275">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b4925-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4925-276">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b4925-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b4925-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4925-277">Range-Lower</span></span>            | <span data-ttu-id="b4925-278">1</span><span class="sxs-lookup"><span data-stu-id="b4925-278">1</span></span>                               |
| <span data-ttu-id="b4925-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4925-279">Range-Upper</span></span>            | <span data-ttu-id="b4925-280">256</span><span class="sxs-lookup"><span data-stu-id="b4925-280">256</span></span>                             |
| <span data-ttu-id="b4925-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-281">Search-Flags</span></span>           | <span data-ttu-id="b4925-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4925-282">0x00000000</span></span>                      |
| <span data-ttu-id="b4925-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4925-283">System-Flags</span></span>           | <span data-ttu-id="b4925-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4925-284">0x00000010</span></span>                      |
| <span data-ttu-id="b4925-285">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b4925-285">Classes used in</span></span>        | [<span data-ttu-id="b4925-286">**In alto**</span><span class="sxs-lookup"><span data-stu-id="b4925-286">**Top**</span></span>](c-top.md)<br/> |



 

 





