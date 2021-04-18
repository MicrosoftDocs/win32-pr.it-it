---
title: Admin-MultiSelect-proprietà-pagine-attributo
description: Si tratta di un attributo multivalore i cui valori sono un numero che rappresenta l'ordine in cui vengono aggiunte le pagine e un GUID di un oggetto COM che implementa pagine delle proprietà di selezione più diverse per lo snap-in utenti e computer di Active Directory.
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- Admin-MultiSelect-proprietà-pagine attributo schema AD
- Schema AD dell'attributo adminMultiselectPropertyPages
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e653568d4f8f6653e4c7dc939c91a7d3cd8b83c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303060"
---
# <a name="admin-multiselect-property-pages-attribute"></a><span data-ttu-id="1b64f-105">Admin-MultiSelect-proprietà-pagine-attributo</span><span class="sxs-lookup"><span data-stu-id="1b64f-105">Admin-Multiselect-Property-Pages attribute</span></span>

<span data-ttu-id="1b64f-106">Si tratta di un attributo multivalore i cui valori sono un numero che rappresenta l'ordine in cui vengono aggiunte le pagine e un GUID di un oggetto COM che implementa pagine delle proprietà di selezione più diverse per lo snap-in utenti e computer di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b64f-106">This is a multivalued attribute whose values are a number that represents the order in which the pages are added and a GUID of a COM object that implements multi-select property pages for the AD Users and Computers snap-in.</span></span>



| <span data-ttu-id="1b64f-107">Voce</span><span class="sxs-lookup"><span data-stu-id="1b64f-107">Entry</span></span> | <span data-ttu-id="1b64f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1b64f-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b64f-109">CN</span><span class="sxs-lookup"><span data-stu-id="1b64f-109">CN</span></span>                | <span data-ttu-id="1b64f-110">Admin-MultiSelect-proprietà-pagine</span><span class="sxs-lookup"><span data-stu-id="1b64f-110">Admin-Multiselect-Property-Pages</span></span>                                                                                                            |
| <span data-ttu-id="1b64f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1b64f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1b64f-112">adminMultiselectPropertyPages</span><span class="sxs-lookup"><span data-stu-id="1b64f-112">adminMultiselectPropertyPages</span></span>                                                                                                               |
| <span data-ttu-id="1b64f-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1b64f-113">Size</span></span>              | <span data-ttu-id="1b64f-114">40 byte</span><span class="sxs-lookup"><span data-stu-id="1b64f-114">40 bytes</span></span>                                                                                                                                    |
| <span data-ttu-id="1b64f-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-115">Update Privilege</span></span>  | <span data-ttu-id="1b64f-116">Amministratore di dominio</span><span class="sxs-lookup"><span data-stu-id="1b64f-116">Domain administrator</span></span>                                                                                                                        |
| <span data-ttu-id="1b64f-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-117">Update Frequency</span></span>  | <span data-ttu-id="1b64f-118">Questa operazione verrà aggiornata solo se è installato un servizio come Exchange o Terminal Server che implementa le proprie pagine delle proprietà di selezione più diverse.</span><span class="sxs-lookup"><span data-stu-id="1b64f-118">This will only be updated if a service like Exchange or Terminal Server is installed that implements their own multi-select property pages.</span></span> |
| <span data-ttu-id="1b64f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b64f-119">Attribute-Id</span></span>      | <span data-ttu-id="1b64f-120">1.2.840.113556.1.4.1690</span><span class="sxs-lookup"><span data-stu-id="1b64f-120">1.2.840.113556.1.4.1690</span></span>                                                                                                                     |
| <span data-ttu-id="1b64f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1b64f-121">System-Id-Guid</span></span>    | <span data-ttu-id="1b64f-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span><span class="sxs-lookup"><span data-stu-id="1b64f-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span></span>                                                                                                        |
| <span data-ttu-id="1b64f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b64f-123">Syntax</span></span>            | [<span data-ttu-id="1b64f-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1b64f-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a><span data-ttu-id="1b64f-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1b64f-125">Implementations</span></span>

-   [<span data-ttu-id="1b64f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b64f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b64f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b64f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b64f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b64f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b64f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b64f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b64f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b64f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1b64f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b64f-131">Windows Server 2003</span></span>



| <span data-ttu-id="1b64f-132">Voce</span><span class="sxs-lookup"><span data-stu-id="1b64f-132">Entry</span></span> | <span data-ttu-id="1b64f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1b64f-133">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b64f-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-134">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b64f-135">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b64f-136">System-Only</span></span>            | <span data-ttu-id="1b64f-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-137">False</span></span>                                                      |
| <span data-ttu-id="1b64f-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b64f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1b64f-139">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-139">False</span></span>                                                      |
| <span data-ttu-id="1b64f-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b64f-140">Is Indexed</span></span>             | <span data-ttu-id="1b64f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-141">False</span></span>                                                      |
| <span data-ttu-id="1b64f-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b64f-142">In Global Catalog</span></span>      | <span data-ttu-id="1b64f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-143">False</span></span>                                                      |
| <span data-ttu-id="1b64f-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b64f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b64f-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b64f-145">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="1b64f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b64f-146">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b64f-147">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-148">Search-Flags</span></span>           | <span data-ttu-id="1b64f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b64f-149">0x00000000</span></span>                                                 |
| <span data-ttu-id="1b64f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-150">System-Flags</span></span>           | <span data-ttu-id="1b64f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b64f-151">0x00000010</span></span>                                                 |
| <span data-ttu-id="1b64f-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b64f-152">Classes used in</span></span>        | [<span data-ttu-id="1b64f-153">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="1b64f-153">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b64f-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b64f-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b64f-155">Voce</span><span class="sxs-lookup"><span data-stu-id="1b64f-155">Entry</span></span> | <span data-ttu-id="1b64f-156">Valore</span><span class="sxs-lookup"><span data-stu-id="1b64f-156">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b64f-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-157">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b64f-158">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b64f-159">System-Only</span></span>            | <span data-ttu-id="1b64f-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-160">False</span></span>                                                      |
| <span data-ttu-id="1b64f-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b64f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1b64f-162">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-162">False</span></span>                                                      |
| <span data-ttu-id="1b64f-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b64f-163">Is Indexed</span></span>             | <span data-ttu-id="1b64f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-164">False</span></span>                                                      |
| <span data-ttu-id="1b64f-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b64f-165">In Global Catalog</span></span>      | <span data-ttu-id="1b64f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-166">False</span></span>                                                      |
| <span data-ttu-id="1b64f-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b64f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b64f-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b64f-168">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="1b64f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b64f-169">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b64f-170">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-171">Search-Flags</span></span>           | <span data-ttu-id="1b64f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b64f-172">0x00000000</span></span>                                                 |
| <span data-ttu-id="1b64f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-173">System-Flags</span></span>           | <span data-ttu-id="1b64f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b64f-174">0x00000010</span></span>                                                 |
| <span data-ttu-id="1b64f-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b64f-175">Classes used in</span></span>        | [<span data-ttu-id="1b64f-176">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="1b64f-176">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b64f-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b64f-177">Windows Server 2008</span></span>



| <span data-ttu-id="1b64f-178">Voce</span><span class="sxs-lookup"><span data-stu-id="1b64f-178">Entry</span></span> | <span data-ttu-id="1b64f-179">Valore</span><span class="sxs-lookup"><span data-stu-id="1b64f-179">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b64f-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-180">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b64f-181">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b64f-182">System-Only</span></span>            | <span data-ttu-id="1b64f-183">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-183">False</span></span>                                                      |
| <span data-ttu-id="1b64f-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b64f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1b64f-185">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-185">False</span></span>                                                      |
| <span data-ttu-id="1b64f-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b64f-186">Is Indexed</span></span>             | <span data-ttu-id="1b64f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-187">False</span></span>                                                      |
| <span data-ttu-id="1b64f-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b64f-188">In Global Catalog</span></span>      | <span data-ttu-id="1b64f-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-189">False</span></span>                                                      |
| <span data-ttu-id="1b64f-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b64f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b64f-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b64f-191">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="1b64f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b64f-192">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b64f-193">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-194">Search-Flags</span></span>           | <span data-ttu-id="1b64f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b64f-195">0x00000000</span></span>                                                 |
| <span data-ttu-id="1b64f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-196">System-Flags</span></span>           | <span data-ttu-id="1b64f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b64f-197">0x00000010</span></span>                                                 |
| <span data-ttu-id="1b64f-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b64f-198">Classes used in</span></span>        | [<span data-ttu-id="1b64f-199">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="1b64f-199">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b64f-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b64f-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b64f-201">Voce</span><span class="sxs-lookup"><span data-stu-id="1b64f-201">Entry</span></span> | <span data-ttu-id="1b64f-202">Valore</span><span class="sxs-lookup"><span data-stu-id="1b64f-202">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b64f-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-203">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b64f-204">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b64f-205">System-Only</span></span>            | <span data-ttu-id="1b64f-206">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-206">False</span></span>                                                      |
| <span data-ttu-id="1b64f-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b64f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1b64f-208">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-208">False</span></span>                                                      |
| <span data-ttu-id="1b64f-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b64f-209">Is Indexed</span></span>             | <span data-ttu-id="1b64f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-210">False</span></span>                                                      |
| <span data-ttu-id="1b64f-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b64f-211">In Global Catalog</span></span>      | <span data-ttu-id="1b64f-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-212">False</span></span>                                                      |
| <span data-ttu-id="1b64f-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b64f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b64f-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b64f-214">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="1b64f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b64f-215">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b64f-216">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-217">Search-Flags</span></span>           | <span data-ttu-id="1b64f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b64f-218">0x00000000</span></span>                                                 |
| <span data-ttu-id="1b64f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-219">System-Flags</span></span>           | <span data-ttu-id="1b64f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b64f-220">0x00000010</span></span>                                                 |
| <span data-ttu-id="1b64f-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b64f-221">Classes used in</span></span>        | [<span data-ttu-id="1b64f-222">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="1b64f-222">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b64f-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b64f-223">Windows Server 2012</span></span>



| <span data-ttu-id="1b64f-224">Voce</span><span class="sxs-lookup"><span data-stu-id="1b64f-224">Entry</span></span> | <span data-ttu-id="1b64f-225">Valore</span><span class="sxs-lookup"><span data-stu-id="1b64f-225">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b64f-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1b64f-226">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b64f-227">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="1b64f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b64f-228">System-Only</span></span>            | <span data-ttu-id="1b64f-229">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-229">False</span></span>                                                      |
| <span data-ttu-id="1b64f-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="1b64f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1b64f-231">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-231">False</span></span>                                                      |
| <span data-ttu-id="1b64f-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1b64f-232">Is Indexed</span></span>             | <span data-ttu-id="1b64f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-233">False</span></span>                                                      |
| <span data-ttu-id="1b64f-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1b64f-234">In Global Catalog</span></span>      | <span data-ttu-id="1b64f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1b64f-235">False</span></span>                                                      |
| <span data-ttu-id="1b64f-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="1b64f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b64f-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="1b64f-237">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="1b64f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b64f-238">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b64f-239">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="1b64f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-240">Search-Flags</span></span>           | <span data-ttu-id="1b64f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b64f-241">0x00000000</span></span>                                                 |
| <span data-ttu-id="1b64f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b64f-242">System-Flags</span></span>           | <span data-ttu-id="1b64f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b64f-243">0x00000010</span></span>                                                 |
| <span data-ttu-id="1b64f-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="1b64f-244">Classes used in</span></span>        | [<span data-ttu-id="1b64f-245">**Display-specifier**</span><span class="sxs-lookup"><span data-stu-id="1b64f-245">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





