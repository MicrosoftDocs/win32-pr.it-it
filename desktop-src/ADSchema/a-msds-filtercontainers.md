---
title: attributo ms-DS-Filter-container
description: Stringa a più valori che contiene i nomi delle classi utilizzate per determinare i tipi di contenitore che devono essere visualizzati dallo snap-in utenti e computer Active Directory durante il filtro.
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo di MS-DS-Filter-container
- attributo msDS-FilterContainers-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122958"
---
# <a name="ms-ds-filter-containers-attribute"></a><span data-ttu-id="187e2-105">attributo ms-DS-Filter-container</span><span class="sxs-lookup"><span data-stu-id="187e2-105">ms-DS-Filter-Containers attribute</span></span>

<span data-ttu-id="187e2-106">Stringa a più valori che contiene i nomi delle classi utilizzate per determinare i tipi di contenitore che devono essere visualizzati dallo snap-in utenti e computer Active Directory durante il filtro.</span><span class="sxs-lookup"><span data-stu-id="187e2-106">A multiple-valued string that contains the names of classes used to determine which container types should be shown by the Active Directory Users and Computers snap-in when filtering.</span></span>



| <span data-ttu-id="187e2-107">Voce</span><span class="sxs-lookup"><span data-stu-id="187e2-107">Entry</span></span> | <span data-ttu-id="187e2-108">Valore</span><span class="sxs-lookup"><span data-stu-id="187e2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="187e2-109">CN</span><span class="sxs-lookup"><span data-stu-id="187e2-109">CN</span></span>                | <span data-ttu-id="187e2-110">ms-DS-Filter-container</span><span class="sxs-lookup"><span data-stu-id="187e2-110">ms-DS-Filter-Containers</span></span>                     |
| <span data-ttu-id="187e2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="187e2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="187e2-112">msDS-FilterContainers</span><span class="sxs-lookup"><span data-stu-id="187e2-112">msDS-FilterContainers</span></span>                       |
| <span data-ttu-id="187e2-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="187e2-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="187e2-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="187e2-114">Update Privilege</span></span>  | <span data-ttu-id="187e2-115">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="187e2-115">Domain administrator</span></span>                        |
| <span data-ttu-id="187e2-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="187e2-116">Update Frequency</span></span>  | <span data-ttu-id="187e2-117">Quando viene modificato l'elenco dei tipi di contenitori.</span><span class="sxs-lookup"><span data-stu-id="187e2-117">When the list of container types changes.</span></span>   |
| <span data-ttu-id="187e2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="187e2-118">Attribute-Id</span></span>      | <span data-ttu-id="187e2-119">1.2.840.113556.1.4.1703</span><span class="sxs-lookup"><span data-stu-id="187e2-119">1.2.840.113556.1.4.1703</span></span>                     |
| <span data-ttu-id="187e2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="187e2-120">System-Id-Guid</span></span>    | <span data-ttu-id="187e2-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span><span class="sxs-lookup"><span data-stu-id="187e2-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span></span>        |
| <span data-ttu-id="187e2-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="187e2-122">Syntax</span></span>            | [<span data-ttu-id="187e2-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="187e2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="187e2-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="187e2-124">Implementations</span></span>

-   [<span data-ttu-id="187e2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="187e2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="187e2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="187e2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="187e2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="187e2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="187e2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="187e2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="187e2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="187e2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="187e2-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="187e2-130">Windows Server 2003</span></span>



| <span data-ttu-id="187e2-131">Voce</span><span class="sxs-lookup"><span data-stu-id="187e2-131">Entry</span></span> | <span data-ttu-id="187e2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="187e2-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="187e2-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187e2-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187e2-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="187e2-135">System-Only</span></span>            | <span data-ttu-id="187e2-136">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-136">False</span></span>                                               |
| <span data-ttu-id="187e2-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187e2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="187e2-138">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-138">False</span></span>                                               |
| <span data-ttu-id="187e2-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187e2-139">Is Indexed</span></span>             | <span data-ttu-id="187e2-140">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-140">False</span></span>                                               |
| <span data-ttu-id="187e2-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187e2-141">In Global Catalog</span></span>      | <span data-ttu-id="187e2-142">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-142">False</span></span>                                               |
| <span data-ttu-id="187e2-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187e2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="187e2-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187e2-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="187e2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187e2-145">Range-Lower</span></span>            | <span data-ttu-id="187e2-146">1</span><span class="sxs-lookup"><span data-stu-id="187e2-146">1</span></span>                                                   |
| <span data-ttu-id="187e2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187e2-147">Range-Upper</span></span>            | <span data-ttu-id="187e2-148">64</span><span class="sxs-lookup"><span data-stu-id="187e2-148">64</span></span>                                                  |
| <span data-ttu-id="187e2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-149">Search-Flags</span></span>           | <span data-ttu-id="187e2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187e2-150">0x00000000</span></span>                                          |
| <span data-ttu-id="187e2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-151">System-Flags</span></span>           | <span data-ttu-id="187e2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187e2-152">0x00000010</span></span>                                          |
| <span data-ttu-id="187e2-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187e2-153">Classes used in</span></span>        | [<span data-ttu-id="187e2-154">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="187e2-154">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="187e2-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="187e2-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="187e2-156">Voce</span><span class="sxs-lookup"><span data-stu-id="187e2-156">Entry</span></span> | <span data-ttu-id="187e2-157">Valore</span><span class="sxs-lookup"><span data-stu-id="187e2-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="187e2-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187e2-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187e2-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="187e2-160">System-Only</span></span>            | <span data-ttu-id="187e2-161">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-161">False</span></span>                                               |
| <span data-ttu-id="187e2-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187e2-162">Is-Single-Valued</span></span>       | <span data-ttu-id="187e2-163">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-163">False</span></span>                                               |
| <span data-ttu-id="187e2-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187e2-164">Is Indexed</span></span>             | <span data-ttu-id="187e2-165">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-165">False</span></span>                                               |
| <span data-ttu-id="187e2-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187e2-166">In Global Catalog</span></span>      | <span data-ttu-id="187e2-167">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-167">False</span></span>                                               |
| <span data-ttu-id="187e2-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187e2-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="187e2-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187e2-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="187e2-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187e2-170">Range-Lower</span></span>            | <span data-ttu-id="187e2-171">1</span><span class="sxs-lookup"><span data-stu-id="187e2-171">1</span></span>                                                   |
| <span data-ttu-id="187e2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187e2-172">Range-Upper</span></span>            | <span data-ttu-id="187e2-173">64</span><span class="sxs-lookup"><span data-stu-id="187e2-173">64</span></span>                                                  |
| <span data-ttu-id="187e2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-174">Search-Flags</span></span>           | <span data-ttu-id="187e2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187e2-175">0x00000000</span></span>                                          |
| <span data-ttu-id="187e2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-176">System-Flags</span></span>           | <span data-ttu-id="187e2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187e2-177">0x00000010</span></span>                                          |
| <span data-ttu-id="187e2-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187e2-178">Classes used in</span></span>        | [<span data-ttu-id="187e2-179">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="187e2-179">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="187e2-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="187e2-180">Windows Server 2008</span></span>



| <span data-ttu-id="187e2-181">Voce</span><span class="sxs-lookup"><span data-stu-id="187e2-181">Entry</span></span> | <span data-ttu-id="187e2-182">Valore</span><span class="sxs-lookup"><span data-stu-id="187e2-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="187e2-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187e2-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187e2-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="187e2-185">System-Only</span></span>            | <span data-ttu-id="187e2-186">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-186">False</span></span>                                               |
| <span data-ttu-id="187e2-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187e2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="187e2-188">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-188">False</span></span>                                               |
| <span data-ttu-id="187e2-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187e2-189">Is Indexed</span></span>             | <span data-ttu-id="187e2-190">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-190">False</span></span>                                               |
| <span data-ttu-id="187e2-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187e2-191">In Global Catalog</span></span>      | <span data-ttu-id="187e2-192">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-192">False</span></span>                                               |
| <span data-ttu-id="187e2-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187e2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="187e2-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187e2-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="187e2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187e2-195">Range-Lower</span></span>            | <span data-ttu-id="187e2-196">1</span><span class="sxs-lookup"><span data-stu-id="187e2-196">1</span></span>                                                   |
| <span data-ttu-id="187e2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187e2-197">Range-Upper</span></span>            | <span data-ttu-id="187e2-198">64</span><span class="sxs-lookup"><span data-stu-id="187e2-198">64</span></span>                                                  |
| <span data-ttu-id="187e2-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-199">Search-Flags</span></span>           | <span data-ttu-id="187e2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187e2-200">0x00000000</span></span>                                          |
| <span data-ttu-id="187e2-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-201">System-Flags</span></span>           | <span data-ttu-id="187e2-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187e2-202">0x00000010</span></span>                                          |
| <span data-ttu-id="187e2-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187e2-203">Classes used in</span></span>        | [<span data-ttu-id="187e2-204">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="187e2-204">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="187e2-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="187e2-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="187e2-206">Voce</span><span class="sxs-lookup"><span data-stu-id="187e2-206">Entry</span></span> | <span data-ttu-id="187e2-207">Valore</span><span class="sxs-lookup"><span data-stu-id="187e2-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="187e2-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187e2-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187e2-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="187e2-210">System-Only</span></span>            | <span data-ttu-id="187e2-211">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-211">False</span></span>                                               |
| <span data-ttu-id="187e2-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187e2-212">Is-Single-Valued</span></span>       | <span data-ttu-id="187e2-213">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-213">False</span></span>                                               |
| <span data-ttu-id="187e2-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187e2-214">Is Indexed</span></span>             | <span data-ttu-id="187e2-215">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-215">False</span></span>                                               |
| <span data-ttu-id="187e2-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187e2-216">In Global Catalog</span></span>      | <span data-ttu-id="187e2-217">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-217">False</span></span>                                               |
| <span data-ttu-id="187e2-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187e2-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="187e2-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187e2-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="187e2-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187e2-220">Range-Lower</span></span>            | <span data-ttu-id="187e2-221">1</span><span class="sxs-lookup"><span data-stu-id="187e2-221">1</span></span>                                                   |
| <span data-ttu-id="187e2-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187e2-222">Range-Upper</span></span>            | <span data-ttu-id="187e2-223">64</span><span class="sxs-lookup"><span data-stu-id="187e2-223">64</span></span>                                                  |
| <span data-ttu-id="187e2-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-224">Search-Flags</span></span>           | <span data-ttu-id="187e2-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187e2-225">0x00000000</span></span>                                          |
| <span data-ttu-id="187e2-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-226">System-Flags</span></span>           | <span data-ttu-id="187e2-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187e2-227">0x00000010</span></span>                                          |
| <span data-ttu-id="187e2-228">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187e2-228">Classes used in</span></span>        | [<span data-ttu-id="187e2-229">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="187e2-229">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="187e2-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="187e2-230">Windows Server 2012</span></span>



| <span data-ttu-id="187e2-231">Voce</span><span class="sxs-lookup"><span data-stu-id="187e2-231">Entry</span></span> | <span data-ttu-id="187e2-232">Valore</span><span class="sxs-lookup"><span data-stu-id="187e2-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="187e2-233">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="187e2-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="187e2-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="187e2-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="187e2-235">System-Only</span></span>            | <span data-ttu-id="187e2-236">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-236">False</span></span>                                               |
| <span data-ttu-id="187e2-237">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="187e2-237">Is-Single-Valued</span></span>       | <span data-ttu-id="187e2-238">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-238">False</span></span>                                               |
| <span data-ttu-id="187e2-239">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="187e2-239">Is Indexed</span></span>             | <span data-ttu-id="187e2-240">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-240">False</span></span>                                               |
| <span data-ttu-id="187e2-241">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="187e2-241">In Global Catalog</span></span>      | <span data-ttu-id="187e2-242">Falso</span><span class="sxs-lookup"><span data-stu-id="187e2-242">False</span></span>                                               |
| <span data-ttu-id="187e2-243">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="187e2-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="187e2-244">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="187e2-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="187e2-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="187e2-245">Range-Lower</span></span>            | <span data-ttu-id="187e2-246">1</span><span class="sxs-lookup"><span data-stu-id="187e2-246">1</span></span>                                                   |
| <span data-ttu-id="187e2-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="187e2-247">Range-Upper</span></span>            | <span data-ttu-id="187e2-248">64</span><span class="sxs-lookup"><span data-stu-id="187e2-248">64</span></span>                                                  |
| <span data-ttu-id="187e2-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-249">Search-Flags</span></span>           | <span data-ttu-id="187e2-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="187e2-250">0x00000000</span></span>                                          |
| <span data-ttu-id="187e2-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="187e2-251">System-Flags</span></span>           | <span data-ttu-id="187e2-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="187e2-252">0x00000010</span></span>                                          |
| <span data-ttu-id="187e2-253">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="187e2-253">Classes used in</span></span>        | [<span data-ttu-id="187e2-254">**DS-interfaccia utente-impostazioni**</span><span class="sxs-lookup"><span data-stu-id="187e2-254">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





