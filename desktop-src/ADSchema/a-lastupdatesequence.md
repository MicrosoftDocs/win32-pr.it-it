---
title: Ultimo attributo Update-Sequence
description: Questo attributo contiene il numero di sequenza di aggiornamento per l'ultimo elemento nell'archivio classi che è stato modificato.
ms.assetid: fd434b8d-31b4-45f7-8d8f-048f61cabb92
ms.tgt_platform: multiple
keywords:
- Ultimo schema di AD dell'attributo di sequenza di aggiornamento
- Schema AD dell'attributo lastUpdateSequence
topic_type:
- apiref
api_name:
- Last-Update-Sequence
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e670c6784ded96a1e81d98f5f1c9bfb859efaa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303014"
---
# <a name="last-update-sequence-attribute"></a><span data-ttu-id="f4f6a-105">Ultimo attributo Update-Sequence</span><span class="sxs-lookup"><span data-stu-id="f4f6a-105">Last-Update-Sequence attribute</span></span>

<span data-ttu-id="f4f6a-106">Questo attributo contiene il numero di sequenza di aggiornamento per l'ultimo elemento nell'archivio classi che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f4f6a-106">This attribute contains the update sequence number for the last item in the class store that was changed.</span></span>



| <span data-ttu-id="f4f6a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-107">Entry</span></span> | <span data-ttu-id="f4f6a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f4f6a-109">CN</span><span class="sxs-lookup"><span data-stu-id="f4f6a-109">CN</span></span>                | <span data-ttu-id="f4f6a-110">Ultima sequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-110">Last-Update-Sequence</span></span>                        |
| <span data-ttu-id="f4f6a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f4f6a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f4f6a-112">lastUpdateSequence</span><span class="sxs-lookup"><span data-stu-id="f4f6a-112">lastUpdateSequence</span></span>                          |
| <span data-ttu-id="f4f6a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f4f6a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f4f6a-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f4f6a-115">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f4f6a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-116">Attribute-Id</span></span>      | <span data-ttu-id="f4f6a-117">1.2.840.113556.1.4.330</span><span class="sxs-lookup"><span data-stu-id="f4f6a-117">1.2.840.113556.1.4.330</span></span>                      |
| <span data-ttu-id="f4f6a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f4f6a-118">System-Id-Guid</span></span>    | <span data-ttu-id="f4f6a-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f4f6a-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span></span>        |
| <span data-ttu-id="f4f6a-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4f6a-120">Syntax</span></span>            | [<span data-ttu-id="f4f6a-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f4f6a-122">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f4f6a-122">Implementations</span></span>

-   [<span data-ttu-id="f4f6a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f4f6a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4f6a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4f6a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4f6a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4f6a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f4f6a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4f6a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f4f6a-130">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-130">Entry</span></span> | <span data-ttu-id="f4f6a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-131">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f6a-132">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-132">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-133">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4f6a-134">System-Only</span></span>            | <span data-ttu-id="f4f6a-135">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-135">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-136">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f4f6a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f4f6a-137">Vero</span><span class="sxs-lookup"><span data-stu-id="f4f6a-137">True</span></span>                                                                                                            |
| <span data-ttu-id="f4f6a-138">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f4f6a-138">Is Indexed</span></span>             | <span data-ttu-id="f4f6a-139">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-139">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-140">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f4f6a-140">In Global Catalog</span></span>      | <span data-ttu-id="f4f6a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-141">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-142">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4f6a-143">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f4f6a-143">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f4f6a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4f6a-144">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4f6a-145">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-146">Search-Flags</span></span>           | <span data-ttu-id="f4f6a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4f6a-147">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-148">System-Flags</span></span>           | <span data-ttu-id="f4f6a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4f6a-149">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-150">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f4f6a-150">Classes used in</span></span>        | [<span data-ttu-id="f4f6a-151">**Archivio classi**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-151">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f4f6a-152">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f4f6a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4f6a-153">Windows Server 2003</span></span>



| <span data-ttu-id="f4f6a-154">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-154">Entry</span></span> | <span data-ttu-id="f4f6a-155">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f6a-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-156">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-157">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4f6a-158">System-Only</span></span>            | <span data-ttu-id="f4f6a-159">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-159">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f4f6a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f4f6a-161">Vero</span><span class="sxs-lookup"><span data-stu-id="f4f6a-161">True</span></span>                                                                                                            |
| <span data-ttu-id="f4f6a-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f4f6a-162">Is Indexed</span></span>             | <span data-ttu-id="f4f6a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-163">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f4f6a-164">In Global Catalog</span></span>      | <span data-ttu-id="f4f6a-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-165">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4f6a-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f4f6a-167">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f4f6a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4f6a-168">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4f6a-169">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-170">Search-Flags</span></span>           | <span data-ttu-id="f4f6a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4f6a-171">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-172">System-Flags</span></span>           | <span data-ttu-id="f4f6a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4f6a-173">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f4f6a-174">Classes used in</span></span>        | [<span data-ttu-id="f4f6a-175">**Archivio classi**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-175">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f4f6a-176">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-176">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4f6a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4f6a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4f6a-178">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-178">Entry</span></span> | <span data-ttu-id="f4f6a-179">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-179">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f6a-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-180">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-181">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4f6a-182">System-Only</span></span>            | <span data-ttu-id="f4f6a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-183">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f4f6a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f4f6a-185">Vero</span><span class="sxs-lookup"><span data-stu-id="f4f6a-185">True</span></span>                                                                                                            |
| <span data-ttu-id="f4f6a-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f4f6a-186">Is Indexed</span></span>             | <span data-ttu-id="f4f6a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-187">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f4f6a-188">In Global Catalog</span></span>      | <span data-ttu-id="f4f6a-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-189">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4f6a-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f4f6a-191">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f4f6a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4f6a-192">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4f6a-193">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-194">Search-Flags</span></span>           | <span data-ttu-id="f4f6a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4f6a-195">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-196">System-Flags</span></span>           | <span data-ttu-id="f4f6a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4f6a-197">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f4f6a-198">Classes used in</span></span>        | [<span data-ttu-id="f4f6a-199">**Archivio classi**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-199">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f4f6a-200">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-200">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4f6a-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4f6a-201">Windows Server 2008</span></span>



| <span data-ttu-id="f4f6a-202">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-202">Entry</span></span> | <span data-ttu-id="f4f6a-203">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-203">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f6a-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-204">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-205">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4f6a-206">System-Only</span></span>            | <span data-ttu-id="f4f6a-207">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-207">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f4f6a-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f4f6a-209">Vero</span><span class="sxs-lookup"><span data-stu-id="f4f6a-209">True</span></span>                                                                                                            |
| <span data-ttu-id="f4f6a-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f4f6a-210">Is Indexed</span></span>             | <span data-ttu-id="f4f6a-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-211">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f4f6a-212">In Global Catalog</span></span>      | <span data-ttu-id="f4f6a-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-213">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4f6a-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f4f6a-215">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f4f6a-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4f6a-216">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4f6a-217">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-218">Search-Flags</span></span>           | <span data-ttu-id="f4f6a-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4f6a-219">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-220">System-Flags</span></span>           | <span data-ttu-id="f4f6a-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4f6a-221">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f4f6a-222">Classes used in</span></span>        | [<span data-ttu-id="f4f6a-223">**Archivio classi**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-223">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f4f6a-224">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-224">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4f6a-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4f6a-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4f6a-226">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-226">Entry</span></span> | <span data-ttu-id="f4f6a-227">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f6a-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-228">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-229">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4f6a-230">System-Only</span></span>            | <span data-ttu-id="f4f6a-231">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-231">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f4f6a-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f4f6a-233">Vero</span><span class="sxs-lookup"><span data-stu-id="f4f6a-233">True</span></span>                                                                                                            |
| <span data-ttu-id="f4f6a-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f4f6a-234">Is Indexed</span></span>             | <span data-ttu-id="f4f6a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-235">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f4f6a-236">In Global Catalog</span></span>      | <span data-ttu-id="f4f6a-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-237">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4f6a-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f4f6a-239">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f4f6a-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4f6a-240">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4f6a-241">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-242">Search-Flags</span></span>           | <span data-ttu-id="f4f6a-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4f6a-243">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-244">System-Flags</span></span>           | <span data-ttu-id="f4f6a-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4f6a-245">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f4f6a-246">Classes used in</span></span>        | [<span data-ttu-id="f4f6a-247">**Archivio classi**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-247">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f4f6a-248">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-248">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4f6a-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4f6a-249">Windows Server 2012</span></span>



| <span data-ttu-id="f4f6a-250">Voce</span><span class="sxs-lookup"><span data-stu-id="f4f6a-250">Entry</span></span> | <span data-ttu-id="f4f6a-251">Valore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-251">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f6a-252">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f4f6a-252">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4f6a-253">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f4f6a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4f6a-254">System-Only</span></span>            | <span data-ttu-id="f4f6a-255">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-255">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-256">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f4f6a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f4f6a-257">Vero</span><span class="sxs-lookup"><span data-stu-id="f4f6a-257">True</span></span>                                                                                                            |
| <span data-ttu-id="f4f6a-258">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f4f6a-258">Is Indexed</span></span>             | <span data-ttu-id="f4f6a-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-259">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-260">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f4f6a-260">In Global Catalog</span></span>      | <span data-ttu-id="f4f6a-261">Falso</span><span class="sxs-lookup"><span data-stu-id="f4f6a-261">False</span></span>                                                                                                           |
| <span data-ttu-id="f4f6a-262">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f4f6a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4f6a-263">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f4f6a-263">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f4f6a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4f6a-264">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4f6a-265">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f4f6a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-266">Search-Flags</span></span>           | <span data-ttu-id="f4f6a-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4f6a-267">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4f6a-268">System-Flags</span></span>           | <span data-ttu-id="f4f6a-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4f6a-269">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f4f6a-270">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f4f6a-270">Classes used in</span></span>        | [<span data-ttu-id="f4f6a-271">**Archivio classi**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-271">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f4f6a-272">**Registrazione pacchetto**</span><span class="sxs-lookup"><span data-stu-id="f4f6a-272">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





