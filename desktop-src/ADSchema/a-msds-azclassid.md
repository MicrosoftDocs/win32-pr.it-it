---
title: attributo ms-DS-AZ-Class-ID
description: ID di classe richiesto dall'interfaccia utente di AzRoles nell'oggetto AzApplication.
ms.assetid: cbbdc898-82b2-410e-8c9d-ae4f9641ac1a
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-AZ-Class-ID
- attributo msDS-AzClassId-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Az-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77d7ae6376deceaf23a9b7fa3c85ee8cb2b9748
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122979"
---
# <a name="ms-ds-az-class-id-attribute"></a><span data-ttu-id="8ff91-105">attributo ms-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="8ff91-105">ms-DS-Az-Class-ID attribute</span></span>

<span data-ttu-id="8ff91-106">ID di classe richiesto dall'interfaccia utente di AzRoles nell'oggetto AzApplication.</span><span class="sxs-lookup"><span data-stu-id="8ff91-106">A class ID required by the AzRoles UI on the AzApplication object.</span></span>



| <span data-ttu-id="8ff91-107">Voce</span><span class="sxs-lookup"><span data-stu-id="8ff91-107">Entry</span></span> | <span data-ttu-id="8ff91-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff91-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8ff91-109">CN</span><span class="sxs-lookup"><span data-stu-id="8ff91-109">CN</span></span>                | <span data-ttu-id="8ff91-110">ms-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="8ff91-110">ms-DS-Az-Class-ID</span></span>                           |
| <span data-ttu-id="8ff91-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8ff91-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8ff91-112">msDS-AzClassId</span><span class="sxs-lookup"><span data-stu-id="8ff91-112">msDS-AzClassId</span></span>                              |
| <span data-ttu-id="8ff91-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8ff91-113">Size</span></span>              | <span data-ttu-id="8ff91-114">36 caratteri</span><span class="sxs-lookup"><span data-stu-id="8ff91-114">36 characters</span></span>                               |
| <span data-ttu-id="8ff91-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-115">Update Privilege</span></span>  | <span data-ttu-id="8ff91-116">Amministratore di AzRoles</span><span class="sxs-lookup"><span data-stu-id="8ff91-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="8ff91-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-117">Update Frequency</span></span>  | <span data-ttu-id="8ff91-118">Durante l'inizializzazione o la modifica dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8ff91-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="8ff91-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8ff91-119">Attribute-Id</span></span>      | <span data-ttu-id="8ff91-120">1.2.840.113556.1.4.1816</span><span class="sxs-lookup"><span data-stu-id="8ff91-120">1.2.840.113556.1.4.1816</span></span>                     |
| <span data-ttu-id="8ff91-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8ff91-121">System-Id-Guid</span></span>    | <span data-ttu-id="8ff91-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span><span class="sxs-lookup"><span data-stu-id="8ff91-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span></span>        |
| <span data-ttu-id="8ff91-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ff91-123">Syntax</span></span>            | [<span data-ttu-id="8ff91-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8ff91-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8ff91-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="8ff91-125">Implementations</span></span>

-   [<span data-ttu-id="8ff91-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8ff91-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8ff91-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8ff91-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8ff91-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8ff91-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8ff91-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8ff91-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8ff91-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8ff91-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8ff91-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ff91-131">Windows Server 2003</span></span>



| <span data-ttu-id="8ff91-132">Voce</span><span class="sxs-lookup"><span data-stu-id="8ff91-132">Entry</span></span> | <span data-ttu-id="8ff91-133">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff91-133">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8ff91-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-134">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ff91-135">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ff91-136">System-Only</span></span>            | <span data-ttu-id="8ff91-137">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-137">False</span></span>        |
| <span data-ttu-id="8ff91-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8ff91-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8ff91-139">Vero</span><span class="sxs-lookup"><span data-stu-id="8ff91-139">True</span></span>         |
| <span data-ttu-id="8ff91-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8ff91-140">Is Indexed</span></span>             | <span data-ttu-id="8ff91-141">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-141">False</span></span>        |
| <span data-ttu-id="8ff91-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8ff91-142">In Global Catalog</span></span>      | <span data-ttu-id="8ff91-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-143">False</span></span>        |
| <span data-ttu-id="8ff91-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8ff91-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ff91-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8ff91-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8ff91-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ff91-146">Range-Lower</span></span>            | <span data-ttu-id="8ff91-147">0</span><span class="sxs-lookup"><span data-stu-id="8ff91-147">0</span></span>            |
| <span data-ttu-id="8ff91-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ff91-148">Range-Upper</span></span>            | <span data-ttu-id="8ff91-149">40</span><span class="sxs-lookup"><span data-stu-id="8ff91-149">40</span></span>           |
| <span data-ttu-id="8ff91-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-150">Search-Flags</span></span>           | <span data-ttu-id="8ff91-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ff91-151">0x00000000</span></span>   |
| <span data-ttu-id="8ff91-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-152">System-Flags</span></span>           | <span data-ttu-id="8ff91-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ff91-153">0x00000010</span></span>   |
| <span data-ttu-id="8ff91-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8ff91-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8ff91-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8ff91-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8ff91-156">Voce</span><span class="sxs-lookup"><span data-stu-id="8ff91-156">Entry</span></span> | <span data-ttu-id="8ff91-157">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff91-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8ff91-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ff91-159">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ff91-160">System-Only</span></span>            | <span data-ttu-id="8ff91-161">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-161">False</span></span>        |
| <span data-ttu-id="8ff91-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8ff91-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8ff91-163">Vero</span><span class="sxs-lookup"><span data-stu-id="8ff91-163">True</span></span>         |
| <span data-ttu-id="8ff91-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8ff91-164">Is Indexed</span></span>             | <span data-ttu-id="8ff91-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-165">False</span></span>        |
| <span data-ttu-id="8ff91-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8ff91-166">In Global Catalog</span></span>      | <span data-ttu-id="8ff91-167">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-167">False</span></span>        |
| <span data-ttu-id="8ff91-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8ff91-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ff91-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8ff91-169">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8ff91-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ff91-170">Range-Lower</span></span>            | <span data-ttu-id="8ff91-171">0</span><span class="sxs-lookup"><span data-stu-id="8ff91-171">0</span></span>            |
| <span data-ttu-id="8ff91-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ff91-172">Range-Upper</span></span>            | <span data-ttu-id="8ff91-173">40</span><span class="sxs-lookup"><span data-stu-id="8ff91-173">40</span></span>           |
| <span data-ttu-id="8ff91-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-174">Search-Flags</span></span>           | <span data-ttu-id="8ff91-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ff91-175">0x00000000</span></span>   |
| <span data-ttu-id="8ff91-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-176">System-Flags</span></span>           | <span data-ttu-id="8ff91-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ff91-177">0x00000010</span></span>   |
| <span data-ttu-id="8ff91-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8ff91-178">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="8ff91-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ff91-179">Windows Server 2008</span></span>



| <span data-ttu-id="8ff91-180">Voce</span><span class="sxs-lookup"><span data-stu-id="8ff91-180">Entry</span></span> | <span data-ttu-id="8ff91-181">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff91-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8ff91-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ff91-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ff91-184">System-Only</span></span>            | <span data-ttu-id="8ff91-185">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-185">False</span></span>        |
| <span data-ttu-id="8ff91-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8ff91-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8ff91-187">Vero</span><span class="sxs-lookup"><span data-stu-id="8ff91-187">True</span></span>         |
| <span data-ttu-id="8ff91-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8ff91-188">Is Indexed</span></span>             | <span data-ttu-id="8ff91-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-189">False</span></span>        |
| <span data-ttu-id="8ff91-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8ff91-190">In Global Catalog</span></span>      | <span data-ttu-id="8ff91-191">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-191">False</span></span>        |
| <span data-ttu-id="8ff91-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8ff91-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ff91-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8ff91-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8ff91-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ff91-194">Range-Lower</span></span>            | <span data-ttu-id="8ff91-195">0</span><span class="sxs-lookup"><span data-stu-id="8ff91-195">0</span></span>            |
| <span data-ttu-id="8ff91-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ff91-196">Range-Upper</span></span>            | <span data-ttu-id="8ff91-197">40</span><span class="sxs-lookup"><span data-stu-id="8ff91-197">40</span></span>           |
| <span data-ttu-id="8ff91-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-198">Search-Flags</span></span>           | <span data-ttu-id="8ff91-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ff91-199">0x00000000</span></span>   |
| <span data-ttu-id="8ff91-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-200">System-Flags</span></span>           | <span data-ttu-id="8ff91-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ff91-201">0x00000010</span></span>   |
| <span data-ttu-id="8ff91-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8ff91-202">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8ff91-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8ff91-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8ff91-204">Voce</span><span class="sxs-lookup"><span data-stu-id="8ff91-204">Entry</span></span> | <span data-ttu-id="8ff91-205">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff91-205">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8ff91-206">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-206">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ff91-207">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ff91-208">System-Only</span></span>            | <span data-ttu-id="8ff91-209">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-209">False</span></span>        |
| <span data-ttu-id="8ff91-210">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8ff91-210">Is-Single-Valued</span></span>       | <span data-ttu-id="8ff91-211">Vero</span><span class="sxs-lookup"><span data-stu-id="8ff91-211">True</span></span>         |
| <span data-ttu-id="8ff91-212">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8ff91-212">Is Indexed</span></span>             | <span data-ttu-id="8ff91-213">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-213">False</span></span>        |
| <span data-ttu-id="8ff91-214">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8ff91-214">In Global Catalog</span></span>      | <span data-ttu-id="8ff91-215">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-215">False</span></span>        |
| <span data-ttu-id="8ff91-216">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8ff91-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ff91-217">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8ff91-217">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8ff91-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ff91-218">Range-Lower</span></span>            | <span data-ttu-id="8ff91-219">0</span><span class="sxs-lookup"><span data-stu-id="8ff91-219">0</span></span>            |
| <span data-ttu-id="8ff91-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ff91-220">Range-Upper</span></span>            | <span data-ttu-id="8ff91-221">40</span><span class="sxs-lookup"><span data-stu-id="8ff91-221">40</span></span>           |
| <span data-ttu-id="8ff91-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-222">Search-Flags</span></span>           | <span data-ttu-id="8ff91-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ff91-223">0x00000000</span></span>   |
| <span data-ttu-id="8ff91-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-224">System-Flags</span></span>           | <span data-ttu-id="8ff91-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ff91-225">0x00000010</span></span>   |
| <span data-ttu-id="8ff91-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8ff91-226">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="8ff91-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ff91-227">Windows Server 2012</span></span>



| <span data-ttu-id="8ff91-228">Voce</span><span class="sxs-lookup"><span data-stu-id="8ff91-228">Entry</span></span> | <span data-ttu-id="8ff91-229">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff91-229">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="8ff91-230">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="8ff91-230">Link-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ff91-231">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="8ff91-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ff91-232">System-Only</span></span>            | <span data-ttu-id="8ff91-233">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-233">False</span></span>        |
| <span data-ttu-id="8ff91-234">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="8ff91-234">Is-Single-Valued</span></span>       | <span data-ttu-id="8ff91-235">Vero</span><span class="sxs-lookup"><span data-stu-id="8ff91-235">True</span></span>         |
| <span data-ttu-id="8ff91-236">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="8ff91-236">Is Indexed</span></span>             | <span data-ttu-id="8ff91-237">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-237">False</span></span>        |
| <span data-ttu-id="8ff91-238">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="8ff91-238">In Global Catalog</span></span>      | <span data-ttu-id="8ff91-239">Falso</span><span class="sxs-lookup"><span data-stu-id="8ff91-239">False</span></span>        |
| <span data-ttu-id="8ff91-240">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="8ff91-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ff91-241">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="8ff91-241">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="8ff91-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ff91-242">Range-Lower</span></span>            | <span data-ttu-id="8ff91-243">0</span><span class="sxs-lookup"><span data-stu-id="8ff91-243">0</span></span>            |
| <span data-ttu-id="8ff91-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ff91-244">Range-Upper</span></span>            | <span data-ttu-id="8ff91-245">40</span><span class="sxs-lookup"><span data-stu-id="8ff91-245">40</span></span>           |
| <span data-ttu-id="8ff91-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-246">Search-Flags</span></span>           | <span data-ttu-id="8ff91-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ff91-247">0x00000000</span></span>   |
| <span data-ttu-id="8ff91-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ff91-248">System-Flags</span></span>           | <span data-ttu-id="8ff91-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ff91-249">0x00000010</span></span>   |
| <span data-ttu-id="8ff91-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="8ff91-250">Classes used in</span></span>        | \-           |



 

 




