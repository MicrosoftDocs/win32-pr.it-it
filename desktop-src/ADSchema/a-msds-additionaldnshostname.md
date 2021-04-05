---
title: attributo ms-DS-additional-DNS-host-name
description: L'attributo viene utilizzato per archiviare il nome host DNS aggiuntivo di un oggetto computer. Questo attributo viene usato al momento della ridenominazione di un controller di dominio.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-additional-DNS-host-name
- attributo msDS-AdditionalDnsHostName-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965275"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="ddebe-106">attributo ms-DS-additional-DNS-host-name</span><span class="sxs-lookup"><span data-stu-id="ddebe-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="ddebe-107">L'attributo viene utilizzato per archiviare il nome host DNS aggiuntivo di un oggetto computer.</span><span class="sxs-lookup"><span data-stu-id="ddebe-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="ddebe-108">Questo attributo viene usato al momento della ridenominazione di un computer o se i nomi vengono gestiti con "netdom computername".</span><span class="sxs-lookup"><span data-stu-id="ddebe-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="ddebe-109">Voce</span><span class="sxs-lookup"><span data-stu-id="ddebe-109">Entry</span></span> | <span data-ttu-id="ddebe-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ddebe-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="ddebe-111">CN</span><span class="sxs-lookup"><span data-stu-id="ddebe-111">CN</span></span>                | <span data-ttu-id="ddebe-112">ms-DS-additional-DNS-host-name</span><span class="sxs-lookup"><span data-stu-id="ddebe-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="ddebe-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ddebe-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ddebe-114">msDS-AdditionalDnsHostName</span><span class="sxs-lookup"><span data-stu-id="ddebe-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="ddebe-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ddebe-115">Size</span></span>              | <span data-ttu-id="ddebe-116">Ogni valore può essere di 2048 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ddebe-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="ddebe-117">Il numero di valore è il limite del database di circa 1200 valori.</span><span class="sxs-lookup"><span data-stu-id="ddebe-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="ddebe-118">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-118">Update Privilege</span></span>  | <span data-ttu-id="ddebe-119">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ddebe-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="ddebe-120">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-120">Update Frequency</span></span>  | <span data-ttu-id="ddebe-121">Quando un computer viene rinominato.</span><span class="sxs-lookup"><span data-stu-id="ddebe-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="ddebe-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ddebe-122">Attribute-Id</span></span>      | <span data-ttu-id="ddebe-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="ddebe-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="ddebe-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ddebe-124">System-Id-Guid</span></span>    | <span data-ttu-id="ddebe-125">80863791-dbe9-4EB8-837E-7f0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="ddebe-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="ddebe-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddebe-126">Syntax</span></span>            | [<span data-ttu-id="ddebe-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ddebe-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="ddebe-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ddebe-128">Implementations</span></span>

-   [<span data-ttu-id="ddebe-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ddebe-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ddebe-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ddebe-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ddebe-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ddebe-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ddebe-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ddebe-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ddebe-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ddebe-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ddebe-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddebe-134">Windows Server 2003</span></span>



| <span data-ttu-id="ddebe-135">Voce</span><span class="sxs-lookup"><span data-stu-id="ddebe-135">Entry</span></span> | <span data-ttu-id="ddebe-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ddebe-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ddebe-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddebe-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddebe-139">System-Only</span></span>            | <span data-ttu-id="ddebe-140">Vero</span><span class="sxs-lookup"><span data-stu-id="ddebe-140">True</span></span>                                      |
| <span data-ttu-id="ddebe-141">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddebe-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ddebe-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-142">False</span></span>                                     |
| <span data-ttu-id="ddebe-143">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddebe-143">Is Indexed</span></span>             | <span data-ttu-id="ddebe-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-144">False</span></span>                                     |
| <span data-ttu-id="ddebe-145">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddebe-145">In Global Catalog</span></span>      | <span data-ttu-id="ddebe-146">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-146">False</span></span>                                     |
| <span data-ttu-id="ddebe-147">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddebe-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddebe-148">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddebe-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ddebe-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddebe-149">Range-Lower</span></span>            | <span data-ttu-id="ddebe-150">0</span><span class="sxs-lookup"><span data-stu-id="ddebe-150">0</span></span>                                         |
| <span data-ttu-id="ddebe-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddebe-151">Range-Upper</span></span>            | <span data-ttu-id="ddebe-152">2048</span><span class="sxs-lookup"><span data-stu-id="ddebe-152">2048</span></span>                                      |
| <span data-ttu-id="ddebe-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-153">Search-Flags</span></span>           | <span data-ttu-id="ddebe-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddebe-154">0x00000000</span></span>                                |
| <span data-ttu-id="ddebe-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-155">System-Flags</span></span>           | <span data-ttu-id="ddebe-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddebe-156">0x00000010</span></span>                                |
| <span data-ttu-id="ddebe-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddebe-157">Classes used in</span></span>        | [<span data-ttu-id="ddebe-158">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ddebe-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ddebe-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ddebe-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ddebe-160">Voce</span><span class="sxs-lookup"><span data-stu-id="ddebe-160">Entry</span></span> | <span data-ttu-id="ddebe-161">Valore</span><span class="sxs-lookup"><span data-stu-id="ddebe-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ddebe-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddebe-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddebe-164">System-Only</span></span>            | <span data-ttu-id="ddebe-165">Vero</span><span class="sxs-lookup"><span data-stu-id="ddebe-165">True</span></span>                                      |
| <span data-ttu-id="ddebe-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddebe-166">Is-Single-Valued</span></span>       | <span data-ttu-id="ddebe-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-167">False</span></span>                                     |
| <span data-ttu-id="ddebe-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddebe-168">Is Indexed</span></span>             | <span data-ttu-id="ddebe-169">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-169">False</span></span>                                     |
| <span data-ttu-id="ddebe-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddebe-170">In Global Catalog</span></span>      | <span data-ttu-id="ddebe-171">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-171">False</span></span>                                     |
| <span data-ttu-id="ddebe-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddebe-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddebe-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddebe-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ddebe-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddebe-174">Range-Lower</span></span>            | <span data-ttu-id="ddebe-175">0</span><span class="sxs-lookup"><span data-stu-id="ddebe-175">0</span></span>                                         |
| <span data-ttu-id="ddebe-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddebe-176">Range-Upper</span></span>            | <span data-ttu-id="ddebe-177">2048</span><span class="sxs-lookup"><span data-stu-id="ddebe-177">2048</span></span>                                      |
| <span data-ttu-id="ddebe-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-178">Search-Flags</span></span>           | <span data-ttu-id="ddebe-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddebe-179">0x00000000</span></span>                                |
| <span data-ttu-id="ddebe-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-180">System-Flags</span></span>           | <span data-ttu-id="ddebe-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddebe-181">0x00000010</span></span>                                |
| <span data-ttu-id="ddebe-182">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddebe-182">Classes used in</span></span>        | [<span data-ttu-id="ddebe-183">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ddebe-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ddebe-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddebe-184">Windows Server 2008</span></span>



| <span data-ttu-id="ddebe-185">Voce</span><span class="sxs-lookup"><span data-stu-id="ddebe-185">Entry</span></span> | <span data-ttu-id="ddebe-186">Valore</span><span class="sxs-lookup"><span data-stu-id="ddebe-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ddebe-187">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddebe-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddebe-189">System-Only</span></span>            | <span data-ttu-id="ddebe-190">Vero</span><span class="sxs-lookup"><span data-stu-id="ddebe-190">True</span></span>                                      |
| <span data-ttu-id="ddebe-191">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddebe-191">Is-Single-Valued</span></span>       | <span data-ttu-id="ddebe-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-192">False</span></span>                                     |
| <span data-ttu-id="ddebe-193">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddebe-193">Is Indexed</span></span>             | <span data-ttu-id="ddebe-194">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-194">False</span></span>                                     |
| <span data-ttu-id="ddebe-195">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddebe-195">In Global Catalog</span></span>      | <span data-ttu-id="ddebe-196">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-196">False</span></span>                                     |
| <span data-ttu-id="ddebe-197">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddebe-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddebe-198">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddebe-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ddebe-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddebe-199">Range-Lower</span></span>            | <span data-ttu-id="ddebe-200">0</span><span class="sxs-lookup"><span data-stu-id="ddebe-200">0</span></span>                                         |
| <span data-ttu-id="ddebe-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddebe-201">Range-Upper</span></span>            | <span data-ttu-id="ddebe-202">2048</span><span class="sxs-lookup"><span data-stu-id="ddebe-202">2048</span></span>                                      |
| <span data-ttu-id="ddebe-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-203">Search-Flags</span></span>           | <span data-ttu-id="ddebe-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddebe-204">0x00000000</span></span>                                |
| <span data-ttu-id="ddebe-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-205">System-Flags</span></span>           | <span data-ttu-id="ddebe-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddebe-206">0x00000010</span></span>                                |
| <span data-ttu-id="ddebe-207">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddebe-207">Classes used in</span></span>        | [<span data-ttu-id="ddebe-208">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ddebe-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ddebe-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ddebe-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ddebe-210">Voce</span><span class="sxs-lookup"><span data-stu-id="ddebe-210">Entry</span></span> | <span data-ttu-id="ddebe-211">Valore</span><span class="sxs-lookup"><span data-stu-id="ddebe-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ddebe-212">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddebe-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddebe-214">System-Only</span></span>            | <span data-ttu-id="ddebe-215">Vero</span><span class="sxs-lookup"><span data-stu-id="ddebe-215">True</span></span>                                      |
| <span data-ttu-id="ddebe-216">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddebe-216">Is-Single-Valued</span></span>       | <span data-ttu-id="ddebe-217">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-217">False</span></span>                                     |
| <span data-ttu-id="ddebe-218">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddebe-218">Is Indexed</span></span>             | <span data-ttu-id="ddebe-219">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-219">False</span></span>                                     |
| <span data-ttu-id="ddebe-220">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddebe-220">In Global Catalog</span></span>      | <span data-ttu-id="ddebe-221">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-221">False</span></span>                                     |
| <span data-ttu-id="ddebe-222">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddebe-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddebe-223">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddebe-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ddebe-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddebe-224">Range-Lower</span></span>            | <span data-ttu-id="ddebe-225">0</span><span class="sxs-lookup"><span data-stu-id="ddebe-225">0</span></span>                                         |
| <span data-ttu-id="ddebe-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddebe-226">Range-Upper</span></span>            | <span data-ttu-id="ddebe-227">2048</span><span class="sxs-lookup"><span data-stu-id="ddebe-227">2048</span></span>                                      |
| <span data-ttu-id="ddebe-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-228">Search-Flags</span></span>           | <span data-ttu-id="ddebe-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddebe-229">0x00000000</span></span>                                |
| <span data-ttu-id="ddebe-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-230">System-Flags</span></span>           | <span data-ttu-id="ddebe-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddebe-231">0x00000010</span></span>                                |
| <span data-ttu-id="ddebe-232">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddebe-232">Classes used in</span></span>        | [<span data-ttu-id="ddebe-233">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ddebe-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ddebe-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddebe-234">Windows Server 2012</span></span>



| <span data-ttu-id="ddebe-235">Voce</span><span class="sxs-lookup"><span data-stu-id="ddebe-235">Entry</span></span> | <span data-ttu-id="ddebe-236">Valore</span><span class="sxs-lookup"><span data-stu-id="ddebe-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ddebe-237">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ddebe-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddebe-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ddebe-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddebe-239">System-Only</span></span>            | <span data-ttu-id="ddebe-240">Vero</span><span class="sxs-lookup"><span data-stu-id="ddebe-240">True</span></span>                                      |
| <span data-ttu-id="ddebe-241">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ddebe-241">Is-Single-Valued</span></span>       | <span data-ttu-id="ddebe-242">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-242">False</span></span>                                     |
| <span data-ttu-id="ddebe-243">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ddebe-243">Is Indexed</span></span>             | <span data-ttu-id="ddebe-244">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-244">False</span></span>                                     |
| <span data-ttu-id="ddebe-245">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ddebe-245">In Global Catalog</span></span>      | <span data-ttu-id="ddebe-246">Falso</span><span class="sxs-lookup"><span data-stu-id="ddebe-246">False</span></span>                                     |
| <span data-ttu-id="ddebe-247">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ddebe-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddebe-248">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ddebe-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ddebe-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddebe-249">Range-Lower</span></span>            | <span data-ttu-id="ddebe-250">0</span><span class="sxs-lookup"><span data-stu-id="ddebe-250">0</span></span>                                         |
| <span data-ttu-id="ddebe-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddebe-251">Range-Upper</span></span>            | <span data-ttu-id="ddebe-252">2048</span><span class="sxs-lookup"><span data-stu-id="ddebe-252">2048</span></span>                                      |
| <span data-ttu-id="ddebe-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-253">Search-Flags</span></span>           | <span data-ttu-id="ddebe-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddebe-254">0x00000000</span></span>                                |
| <span data-ttu-id="ddebe-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddebe-255">System-Flags</span></span>           | <span data-ttu-id="ddebe-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddebe-256">0x00000010</span></span>                                |
| <span data-ttu-id="ddebe-257">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ddebe-257">Classes used in</span></span>        | [<span data-ttu-id="ddebe-258">**Computer**</span><span class="sxs-lookup"><span data-stu-id="ddebe-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





