---
title: Attributo Extra-Columns
description: Si tratta di un attributo multivalore i cui valori sono costituiti da un 5 Tuple (nome di attributo), (titolo della colonna), (visibilità predefinita (0, 1)), (larghezza della colonna (\ 8211; 1 per la larghezza automatica), 0 (riservato per un utilizzo futuro deve essere zero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Schema AD Extra-Columns attribute
- Schema AD dell'attributo di colonne di colonne
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744378"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="6b587-105">Attributo Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="6b587-105">Extra-Columns attribute</span></span>

<span data-ttu-id="6b587-106">Si tratta di un attributo multivalore i cui valori sono costituiti da un 5 tuple: (nome attributo), (titolo colonna), (visibilità predefinita (0, 1)), (larghezza colonna (1 per larghezza automatica), 0 (riservato per uso futuro deve essere zero).</span><span class="sxs-lookup"><span data-stu-id="6b587-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="6b587-107">Questo valore viene usato dalla console utenti e computer di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b587-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="6b587-108">Voce</span><span class="sxs-lookup"><span data-stu-id="6b587-108">Entry</span></span> | <span data-ttu-id="6b587-109">Valore</span><span class="sxs-lookup"><span data-stu-id="6b587-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b587-110">CN</span><span class="sxs-lookup"><span data-stu-id="6b587-110">CN</span></span>                | <span data-ttu-id="6b587-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="6b587-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="6b587-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6b587-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6b587-113">extraColumns</span><span class="sxs-lookup"><span data-stu-id="6b587-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="6b587-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="6b587-114">Size</span></span>              | <span data-ttu-id="6b587-115">Ogni valore corrisponde alla dimensione della stringa della 5 tupla sopra.</span><span class="sxs-lookup"><span data-stu-id="6b587-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="6b587-116">Per impostazione predefinita, nel contenitore DisplaySpecifier saranno presenti 22 valori nell'oggetto visualizzato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6b587-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="6b587-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b587-117">Update Privilege</span></span>  | <span data-ttu-id="6b587-118">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="6b587-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="6b587-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b587-119">Update Frequency</span></span>  | <span data-ttu-id="6b587-120">Questa operazione verrà aggiornata solo se è installato un servizio come Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b587-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="6b587-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b587-121">Attribute-Id</span></span>      | <span data-ttu-id="6b587-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="6b587-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="6b587-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6b587-123">System-Id-Guid</span></span>    | <span data-ttu-id="6b587-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="6b587-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="6b587-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b587-125">Syntax</span></span>            | [<span data-ttu-id="6b587-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6b587-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="6b587-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="6b587-127">Implementations</span></span>

-   [<span data-ttu-id="6b587-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6b587-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6b587-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6b587-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6b587-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6b587-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6b587-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6b587-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6b587-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b587-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6b587-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b587-133">Windows Server 2003</span></span>



| <span data-ttu-id="6b587-134">Voce</span><span class="sxs-lookup"><span data-stu-id="6b587-134">Entry</span></span> | <span data-ttu-id="6b587-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6b587-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="6b587-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b587-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b587-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b587-138">System-Only</span></span>            | <span data-ttu-id="6b587-139">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-139">False</span></span>                                                      |
| <span data-ttu-id="6b587-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b587-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6b587-141">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-141">False</span></span>                                                      |
| <span data-ttu-id="6b587-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b587-142">Is Indexed</span></span>             | <span data-ttu-id="6b587-143">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-143">False</span></span>                                                      |
| <span data-ttu-id="6b587-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b587-144">In Global Catalog</span></span>      | <span data-ttu-id="6b587-145">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-145">False</span></span>                                                      |
| <span data-ttu-id="6b587-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b587-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b587-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b587-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="6b587-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b587-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b587-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-150">Search-Flags</span></span>           | <span data-ttu-id="6b587-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b587-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="6b587-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-152">System-Flags</span></span>           | <span data-ttu-id="6b587-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b587-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="6b587-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b587-154">Classes used in</span></span>        | [<span data-ttu-id="6b587-155">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="6b587-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6b587-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6b587-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6b587-157">Voce</span><span class="sxs-lookup"><span data-stu-id="6b587-157">Entry</span></span> | <span data-ttu-id="6b587-158">Valore</span><span class="sxs-lookup"><span data-stu-id="6b587-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="6b587-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b587-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b587-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b587-161">System-Only</span></span>            | <span data-ttu-id="6b587-162">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-162">False</span></span>                                                      |
| <span data-ttu-id="6b587-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b587-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6b587-164">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-164">False</span></span>                                                      |
| <span data-ttu-id="6b587-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b587-165">Is Indexed</span></span>             | <span data-ttu-id="6b587-166">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-166">False</span></span>                                                      |
| <span data-ttu-id="6b587-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b587-167">In Global Catalog</span></span>      | <span data-ttu-id="6b587-168">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-168">False</span></span>                                                      |
| <span data-ttu-id="6b587-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b587-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b587-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b587-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="6b587-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b587-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b587-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-173">Search-Flags</span></span>           | <span data-ttu-id="6b587-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b587-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="6b587-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-175">System-Flags</span></span>           | <span data-ttu-id="6b587-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b587-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="6b587-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b587-177">Classes used in</span></span>        | [<span data-ttu-id="6b587-178">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="6b587-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6b587-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b587-179">Windows Server 2008</span></span>



| <span data-ttu-id="6b587-180">Voce</span><span class="sxs-lookup"><span data-stu-id="6b587-180">Entry</span></span> | <span data-ttu-id="6b587-181">Valore</span><span class="sxs-lookup"><span data-stu-id="6b587-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="6b587-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b587-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b587-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b587-184">System-Only</span></span>            | <span data-ttu-id="6b587-185">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-185">False</span></span>                                                      |
| <span data-ttu-id="6b587-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b587-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6b587-187">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-187">False</span></span>                                                      |
| <span data-ttu-id="6b587-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b587-188">Is Indexed</span></span>             | <span data-ttu-id="6b587-189">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-189">False</span></span>                                                      |
| <span data-ttu-id="6b587-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b587-190">In Global Catalog</span></span>      | <span data-ttu-id="6b587-191">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-191">False</span></span>                                                      |
| <span data-ttu-id="6b587-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b587-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b587-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b587-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="6b587-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b587-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b587-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-196">Search-Flags</span></span>           | <span data-ttu-id="6b587-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b587-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="6b587-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-198">System-Flags</span></span>           | <span data-ttu-id="6b587-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b587-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="6b587-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b587-200">Classes used in</span></span>        | [<span data-ttu-id="6b587-201">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="6b587-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6b587-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b587-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6b587-203">Voce</span><span class="sxs-lookup"><span data-stu-id="6b587-203">Entry</span></span> | <span data-ttu-id="6b587-204">Valore</span><span class="sxs-lookup"><span data-stu-id="6b587-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="6b587-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b587-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b587-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b587-207">System-Only</span></span>            | <span data-ttu-id="6b587-208">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-208">False</span></span>                                                      |
| <span data-ttu-id="6b587-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b587-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6b587-210">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-210">False</span></span>                                                      |
| <span data-ttu-id="6b587-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b587-211">Is Indexed</span></span>             | <span data-ttu-id="6b587-212">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-212">False</span></span>                                                      |
| <span data-ttu-id="6b587-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b587-213">In Global Catalog</span></span>      | <span data-ttu-id="6b587-214">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-214">False</span></span>                                                      |
| <span data-ttu-id="6b587-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b587-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b587-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b587-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="6b587-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b587-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b587-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-219">Search-Flags</span></span>           | <span data-ttu-id="6b587-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b587-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="6b587-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-221">System-Flags</span></span>           | <span data-ttu-id="6b587-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b587-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="6b587-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b587-223">Classes used in</span></span>        | [<span data-ttu-id="6b587-224">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="6b587-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6b587-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b587-225">Windows Server 2012</span></span>



| <span data-ttu-id="6b587-226">Voce</span><span class="sxs-lookup"><span data-stu-id="6b587-226">Entry</span></span> | <span data-ttu-id="6b587-227">Valore</span><span class="sxs-lookup"><span data-stu-id="6b587-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="6b587-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="6b587-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b587-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="6b587-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b587-230">System-Only</span></span>            | <span data-ttu-id="6b587-231">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-231">False</span></span>                                                      |
| <span data-ttu-id="6b587-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="6b587-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6b587-233">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-233">False</span></span>                                                      |
| <span data-ttu-id="6b587-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="6b587-234">Is Indexed</span></span>             | <span data-ttu-id="6b587-235">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-235">False</span></span>                                                      |
| <span data-ttu-id="6b587-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="6b587-236">In Global Catalog</span></span>      | <span data-ttu-id="6b587-237">Falso</span><span class="sxs-lookup"><span data-stu-id="6b587-237">False</span></span>                                                      |
| <span data-ttu-id="6b587-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="6b587-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b587-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="6b587-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="6b587-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b587-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b587-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="6b587-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-242">Search-Flags</span></span>           | <span data-ttu-id="6b587-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b587-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="6b587-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b587-244">System-Flags</span></span>           | <span data-ttu-id="6b587-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b587-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="6b587-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="6b587-246">Classes used in</span></span>        | [<span data-ttu-id="6b587-247">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="6b587-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





