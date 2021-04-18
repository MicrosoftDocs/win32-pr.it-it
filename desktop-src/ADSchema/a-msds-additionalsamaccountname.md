---
title: ms-DS-additional-SAM-account-name (attributo)
description: Questo attributo viene usato per archiviare i nomi di account SAM che corrispondono ai nomi host DNS in ms-DS-additional-DNS-host-name.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-additional-SAM-account-name
- attributo msDS-AdditionalSamAccountName-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303536"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="0c740-105">ms-DS-additional-SAM-account-name (attributo)</span><span class="sxs-lookup"><span data-stu-id="0c740-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="0c740-106">Questo attributo viene usato per archiviare i nomi di account SAM che corrispondono ai nomi host DNS in ms-DS-additional-DNS-host-name.</span><span class="sxs-lookup"><span data-stu-id="0c740-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="0c740-107">Voce</span><span class="sxs-lookup"><span data-stu-id="0c740-107">Entry</span></span> | <span data-ttu-id="0c740-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0c740-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0c740-109">CN</span><span class="sxs-lookup"><span data-stu-id="0c740-109">CN</span></span>                | <span data-ttu-id="0c740-110">ms-DS-additional-SAM-account-name</span><span class="sxs-lookup"><span data-stu-id="0c740-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="0c740-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c740-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0c740-112">msDS-AdditionalSamAccountName</span><span class="sxs-lookup"><span data-stu-id="0c740-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="0c740-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0c740-113">Size</span></span>              | <span data-ttu-id="0c740-114">Meno di 20 byte.</span><span class="sxs-lookup"><span data-stu-id="0c740-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="0c740-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0c740-115">Update Privilege</span></span>  | <span data-ttu-id="0c740-116">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0c740-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="0c740-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0c740-117">Update Frequency</span></span>  | <span data-ttu-id="0c740-118">Quando il controller di dominio viene rinominato.</span><span class="sxs-lookup"><span data-stu-id="0c740-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="0c740-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c740-119">Attribute-Id</span></span>      | <span data-ttu-id="0c740-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="0c740-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="0c740-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c740-121">System-Id-Guid</span></span>    | <span data-ttu-id="0c740-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="0c740-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="0c740-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c740-123">Syntax</span></span>            | [<span data-ttu-id="0c740-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0c740-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0c740-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="0c740-125">Implementations</span></span>

-   [<span data-ttu-id="0c740-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c740-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c740-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c740-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c740-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c740-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c740-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c740-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c740-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c740-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0c740-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c740-131">Windows Server 2003</span></span>



| <span data-ttu-id="0c740-132">Voce</span><span class="sxs-lookup"><span data-stu-id="0c740-132">Entry</span></span> | <span data-ttu-id="0c740-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0c740-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="0c740-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c740-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c740-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c740-136">System-Only</span></span>            | <span data-ttu-id="0c740-137">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-137">True</span></span>                                      |
| <span data-ttu-id="0c740-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c740-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0c740-139">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-139">False</span></span>                                     |
| <span data-ttu-id="0c740-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c740-140">Is Indexed</span></span>             | <span data-ttu-id="0c740-141">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-141">True</span></span>                                      |
| <span data-ttu-id="0c740-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c740-142">In Global Catalog</span></span>      | <span data-ttu-id="0c740-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-143">False</span></span>                                     |
| <span data-ttu-id="0c740-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c740-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c740-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c740-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="0c740-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c740-146">Range-Lower</span></span>            | <span data-ttu-id="0c740-147">0</span><span class="sxs-lookup"><span data-stu-id="0c740-147">0</span></span>                                         |
| <span data-ttu-id="0c740-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c740-148">Range-Upper</span></span>            | <span data-ttu-id="0c740-149">256</span><span class="sxs-lookup"><span data-stu-id="0c740-149">256</span></span>                                       |
| <span data-ttu-id="0c740-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-150">Search-Flags</span></span>           | <span data-ttu-id="0c740-151">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="0c740-151">0x0000000D</span></span>                                |
| <span data-ttu-id="0c740-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-152">System-Flags</span></span>           | <span data-ttu-id="0c740-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c740-153">0x00000010</span></span>                                |
| <span data-ttu-id="0c740-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c740-154">Classes used in</span></span>        | [<span data-ttu-id="0c740-155">**Computer**</span><span class="sxs-lookup"><span data-stu-id="0c740-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c740-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c740-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c740-157">Voce</span><span class="sxs-lookup"><span data-stu-id="0c740-157">Entry</span></span> | <span data-ttu-id="0c740-158">Valore</span><span class="sxs-lookup"><span data-stu-id="0c740-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="0c740-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c740-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c740-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c740-161">System-Only</span></span>            | <span data-ttu-id="0c740-162">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-162">True</span></span>                                      |
| <span data-ttu-id="0c740-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c740-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0c740-164">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-164">False</span></span>                                     |
| <span data-ttu-id="0c740-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c740-165">Is Indexed</span></span>             | <span data-ttu-id="0c740-166">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-166">True</span></span>                                      |
| <span data-ttu-id="0c740-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c740-167">In Global Catalog</span></span>      | <span data-ttu-id="0c740-168">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-168">False</span></span>                                     |
| <span data-ttu-id="0c740-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c740-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c740-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c740-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="0c740-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c740-171">Range-Lower</span></span>            | <span data-ttu-id="0c740-172">0</span><span class="sxs-lookup"><span data-stu-id="0c740-172">0</span></span>                                         |
| <span data-ttu-id="0c740-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c740-173">Range-Upper</span></span>            | <span data-ttu-id="0c740-174">256</span><span class="sxs-lookup"><span data-stu-id="0c740-174">256</span></span>                                       |
| <span data-ttu-id="0c740-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-175">Search-Flags</span></span>           | <span data-ttu-id="0c740-176">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="0c740-176">0x0000000D</span></span>                                |
| <span data-ttu-id="0c740-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-177">System-Flags</span></span>           | <span data-ttu-id="0c740-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c740-178">0x00000010</span></span>                                |
| <span data-ttu-id="0c740-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c740-179">Classes used in</span></span>        | [<span data-ttu-id="0c740-180">**Computer**</span><span class="sxs-lookup"><span data-stu-id="0c740-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c740-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c740-181">Windows Server 2008</span></span>



| <span data-ttu-id="0c740-182">Voce</span><span class="sxs-lookup"><span data-stu-id="0c740-182">Entry</span></span> | <span data-ttu-id="0c740-183">Valore</span><span class="sxs-lookup"><span data-stu-id="0c740-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="0c740-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c740-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c740-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c740-186">System-Only</span></span>            | <span data-ttu-id="0c740-187">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-187">True</span></span>                                      |
| <span data-ttu-id="0c740-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c740-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0c740-189">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-189">False</span></span>                                     |
| <span data-ttu-id="0c740-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c740-190">Is Indexed</span></span>             | <span data-ttu-id="0c740-191">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-191">True</span></span>                                      |
| <span data-ttu-id="0c740-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c740-192">In Global Catalog</span></span>      | <span data-ttu-id="0c740-193">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-193">False</span></span>                                     |
| <span data-ttu-id="0c740-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c740-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c740-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c740-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="0c740-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c740-196">Range-Lower</span></span>            | <span data-ttu-id="0c740-197">0</span><span class="sxs-lookup"><span data-stu-id="0c740-197">0</span></span>                                         |
| <span data-ttu-id="0c740-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c740-198">Range-Upper</span></span>            | <span data-ttu-id="0c740-199">256</span><span class="sxs-lookup"><span data-stu-id="0c740-199">256</span></span>                                       |
| <span data-ttu-id="0c740-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-200">Search-Flags</span></span>           | <span data-ttu-id="0c740-201">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="0c740-201">0x0000000D</span></span>                                |
| <span data-ttu-id="0c740-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-202">System-Flags</span></span>           | <span data-ttu-id="0c740-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c740-203">0x00000010</span></span>                                |
| <span data-ttu-id="0c740-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c740-204">Classes used in</span></span>        | [<span data-ttu-id="0c740-205">**Computer**</span><span class="sxs-lookup"><span data-stu-id="0c740-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c740-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c740-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c740-207">Voce</span><span class="sxs-lookup"><span data-stu-id="0c740-207">Entry</span></span> | <span data-ttu-id="0c740-208">Valore</span><span class="sxs-lookup"><span data-stu-id="0c740-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="0c740-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c740-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c740-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c740-211">System-Only</span></span>            | <span data-ttu-id="0c740-212">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-212">True</span></span>                                      |
| <span data-ttu-id="0c740-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c740-213">Is-Single-Valued</span></span>       | <span data-ttu-id="0c740-214">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-214">False</span></span>                                     |
| <span data-ttu-id="0c740-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c740-215">Is Indexed</span></span>             | <span data-ttu-id="0c740-216">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-216">True</span></span>                                      |
| <span data-ttu-id="0c740-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c740-217">In Global Catalog</span></span>      | <span data-ttu-id="0c740-218">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-218">False</span></span>                                     |
| <span data-ttu-id="0c740-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c740-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c740-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c740-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="0c740-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c740-221">Range-Lower</span></span>            | <span data-ttu-id="0c740-222">0</span><span class="sxs-lookup"><span data-stu-id="0c740-222">0</span></span>                                         |
| <span data-ttu-id="0c740-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c740-223">Range-Upper</span></span>            | <span data-ttu-id="0c740-224">256</span><span class="sxs-lookup"><span data-stu-id="0c740-224">256</span></span>                                       |
| <span data-ttu-id="0c740-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-225">Search-Flags</span></span>           | <span data-ttu-id="0c740-226">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="0c740-226">0x0000000D</span></span>                                |
| <span data-ttu-id="0c740-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-227">System-Flags</span></span>           | <span data-ttu-id="0c740-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c740-228">0x00000010</span></span>                                |
| <span data-ttu-id="0c740-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c740-229">Classes used in</span></span>        | [<span data-ttu-id="0c740-230">**Computer**</span><span class="sxs-lookup"><span data-stu-id="0c740-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c740-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c740-231">Windows Server 2012</span></span>



| <span data-ttu-id="0c740-232">Voce</span><span class="sxs-lookup"><span data-stu-id="0c740-232">Entry</span></span> | <span data-ttu-id="0c740-233">Valore</span><span class="sxs-lookup"><span data-stu-id="0c740-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="0c740-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="0c740-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c740-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="0c740-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c740-236">System-Only</span></span>            | <span data-ttu-id="0c740-237">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-237">True</span></span>                                      |
| <span data-ttu-id="0c740-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="0c740-238">Is-Single-Valued</span></span>       | <span data-ttu-id="0c740-239">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-239">False</span></span>                                     |
| <span data-ttu-id="0c740-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="0c740-240">Is Indexed</span></span>             | <span data-ttu-id="0c740-241">Vero</span><span class="sxs-lookup"><span data-stu-id="0c740-241">True</span></span>                                      |
| <span data-ttu-id="0c740-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="0c740-242">In Global Catalog</span></span>      | <span data-ttu-id="0c740-243">Falso</span><span class="sxs-lookup"><span data-stu-id="0c740-243">False</span></span>                                     |
| <span data-ttu-id="0c740-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="0c740-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c740-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="0c740-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="0c740-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c740-246">Range-Lower</span></span>            | <span data-ttu-id="0c740-247">0</span><span class="sxs-lookup"><span data-stu-id="0c740-247">0</span></span>                                         |
| <span data-ttu-id="0c740-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c740-248">Range-Upper</span></span>            | <span data-ttu-id="0c740-249">256</span><span class="sxs-lookup"><span data-stu-id="0c740-249">256</span></span>                                       |
| <span data-ttu-id="0c740-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-250">Search-Flags</span></span>           | <span data-ttu-id="0c740-251">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="0c740-251">0x0000000D</span></span>                                |
| <span data-ttu-id="0c740-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c740-252">System-Flags</span></span>           | <span data-ttu-id="0c740-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c740-253">0x00000010</span></span>                                |
| <span data-ttu-id="0c740-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="0c740-254">Classes used in</span></span>        | [<span data-ttu-id="0c740-255">**Computer**</span><span class="sxs-lookup"><span data-stu-id="0c740-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





