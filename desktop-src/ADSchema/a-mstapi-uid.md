---
title: attributo ms-TAPI-Unique-Identifier
description: Fornisce il nome di una conferenza multicast TAPI. Si tratta dell'attributo Naming della classe Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-TAPI-Unique-Identifier
- msTAPI-schema AD dell'attributo UID
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400986"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="c741a-106">attributo ms-TAPI-Unique-Identifier</span><span class="sxs-lookup"><span data-stu-id="c741a-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="c741a-107">Fornisce il nome di una conferenza multicast TAPI.</span><span class="sxs-lookup"><span data-stu-id="c741a-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="c741a-108">Si tratta dell'attributo Naming della classe Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="c741a-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="c741a-109">Voce</span><span class="sxs-lookup"><span data-stu-id="c741a-109">Entry</span></span> | <span data-ttu-id="c741a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c741a-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c741a-111">CN</span><span class="sxs-lookup"><span data-stu-id="c741a-111">CN</span></span>                | <span data-ttu-id="c741a-112">ID MS-TAPI-Unique</span><span class="sxs-lookup"><span data-stu-id="c741a-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="c741a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c741a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c741a-114">msTAPI-UID</span><span class="sxs-lookup"><span data-stu-id="c741a-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="c741a-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c741a-115">Size</span></span>              | <span data-ttu-id="c741a-116">Può essere una stringa arbitraria, in genere di lunghezza inferiore a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c741a-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="c741a-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c741a-117">Update Privilege</span></span>  | <span data-ttu-id="c741a-118">Non sono richiesti privilegi speciali.</span><span class="sxs-lookup"><span data-stu-id="c741a-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="c741a-119">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c741a-119">Update Frequency</span></span>  | <span data-ttu-id="c741a-120">Impostare una volta al momento della creazione dell'oggetto Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="c741a-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="c741a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c741a-121">Attribute-Id</span></span>      | <span data-ttu-id="c741a-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="c741a-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="c741a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c741a-123">System-Id-Guid</span></span>    | <span data-ttu-id="c741a-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span><span class="sxs-lookup"><span data-stu-id="c741a-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="c741a-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c741a-125">Syntax</span></span>            | [<span data-ttu-id="c741a-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c741a-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="c741a-127">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="c741a-127">Implementations</span></span>

-   [<span data-ttu-id="c741a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c741a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c741a-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c741a-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c741a-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c741a-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c741a-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c741a-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c741a-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c741a-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c741a-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c741a-133">Windows Server 2003</span></span>



| <span data-ttu-id="c741a-134">Voce</span><span class="sxs-lookup"><span data-stu-id="c741a-134">Entry</span></span> | <span data-ttu-id="c741a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c741a-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c741a-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c741a-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c741a-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="c741a-138">System-Only</span></span>            | <span data-ttu-id="c741a-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c741a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="c741a-141">Vero</span><span class="sxs-lookup"><span data-stu-id="c741a-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="c741a-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c741a-142">Is Indexed</span></span>             | <span data-ttu-id="c741a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c741a-144">In Global Catalog</span></span>      | <span data-ttu-id="c741a-145">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c741a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="c741a-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c741a-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="c741a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c741a-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c741a-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-150">Search-Flags</span></span>           | <span data-ttu-id="c741a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c741a-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-152">System-Flags</span></span>           | <span data-ttu-id="c741a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c741a-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c741a-154">Classes used in</span></span>        | [<span data-ttu-id="c741a-155">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="c741a-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="c741a-156">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="c741a-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c741a-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c741a-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c741a-158">Voce</span><span class="sxs-lookup"><span data-stu-id="c741a-158">Entry</span></span> | <span data-ttu-id="c741a-159">Valore</span><span class="sxs-lookup"><span data-stu-id="c741a-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c741a-160">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c741a-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c741a-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c741a-162">System-Only</span></span>            | <span data-ttu-id="c741a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-164">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c741a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c741a-165">Vero</span><span class="sxs-lookup"><span data-stu-id="c741a-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="c741a-166">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c741a-166">Is Indexed</span></span>             | <span data-ttu-id="c741a-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-168">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c741a-168">In Global Catalog</span></span>      | <span data-ttu-id="c741a-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-170">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c741a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c741a-171">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c741a-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="c741a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c741a-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c741a-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-174">Search-Flags</span></span>           | <span data-ttu-id="c741a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c741a-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-176">System-Flags</span></span>           | <span data-ttu-id="c741a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c741a-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-178">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c741a-178">Classes used in</span></span>        | [<span data-ttu-id="c741a-179">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="c741a-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="c741a-180">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="c741a-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c741a-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c741a-181">Windows Server 2008</span></span>



| <span data-ttu-id="c741a-182">Voce</span><span class="sxs-lookup"><span data-stu-id="c741a-182">Entry</span></span> | <span data-ttu-id="c741a-183">Valore</span><span class="sxs-lookup"><span data-stu-id="c741a-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c741a-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c741a-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c741a-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="c741a-186">System-Only</span></span>            | <span data-ttu-id="c741a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c741a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="c741a-189">Vero</span><span class="sxs-lookup"><span data-stu-id="c741a-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="c741a-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c741a-190">Is Indexed</span></span>             | <span data-ttu-id="c741a-191">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c741a-192">In Global Catalog</span></span>      | <span data-ttu-id="c741a-193">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c741a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="c741a-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c741a-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="c741a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c741a-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c741a-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-198">Search-Flags</span></span>           | <span data-ttu-id="c741a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c741a-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-200">System-Flags</span></span>           | <span data-ttu-id="c741a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c741a-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-202">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c741a-202">Classes used in</span></span>        | [<span data-ttu-id="c741a-203">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="c741a-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="c741a-204">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="c741a-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c741a-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c741a-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c741a-206">Voce</span><span class="sxs-lookup"><span data-stu-id="c741a-206">Entry</span></span> | <span data-ttu-id="c741a-207">Valore</span><span class="sxs-lookup"><span data-stu-id="c741a-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c741a-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c741a-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c741a-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c741a-210">System-Only</span></span>            | <span data-ttu-id="c741a-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c741a-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c741a-213">Vero</span><span class="sxs-lookup"><span data-stu-id="c741a-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="c741a-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c741a-214">Is Indexed</span></span>             | <span data-ttu-id="c741a-215">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c741a-216">In Global Catalog</span></span>      | <span data-ttu-id="c741a-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c741a-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c741a-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c741a-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="c741a-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c741a-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c741a-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-222">Search-Flags</span></span>           | <span data-ttu-id="c741a-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c741a-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-224">System-Flags</span></span>           | <span data-ttu-id="c741a-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c741a-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c741a-226">Classes used in</span></span>        | [<span data-ttu-id="c741a-227">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="c741a-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="c741a-228">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="c741a-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c741a-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c741a-229">Windows Server 2012</span></span>



| <span data-ttu-id="c741a-230">Voce</span><span class="sxs-lookup"><span data-stu-id="c741a-230">Entry</span></span> | <span data-ttu-id="c741a-231">Valore</span><span class="sxs-lookup"><span data-stu-id="c741a-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c741a-232">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="c741a-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c741a-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="c741a-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c741a-234">System-Only</span></span>            | <span data-ttu-id="c741a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-236">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="c741a-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c741a-237">Vero</span><span class="sxs-lookup"><span data-stu-id="c741a-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="c741a-238">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="c741a-238">Is Indexed</span></span>             | <span data-ttu-id="c741a-239">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-240">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="c741a-240">In Global Catalog</span></span>      | <span data-ttu-id="c741a-241">Falso</span><span class="sxs-lookup"><span data-stu-id="c741a-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="c741a-242">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="c741a-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c741a-243">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="c741a-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="c741a-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c741a-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c741a-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="c741a-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-246">Search-Flags</span></span>           | <span data-ttu-id="c741a-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c741a-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c741a-248">System-Flags</span></span>           | <span data-ttu-id="c741a-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c741a-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="c741a-250">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="c741a-250">Classes used in</span></span>        | [<span data-ttu-id="c741a-251">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="c741a-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="c741a-252">**MS-TAPI-RT-person**</span><span class="sxs-lookup"><span data-stu-id="c741a-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





