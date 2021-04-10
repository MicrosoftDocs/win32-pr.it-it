---
title: attributo ms-DFS-Link-Path-V2
description: Percorso collegamento DFS relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS. Utilizzare le barre (/) anziché le barre rovesciate ( \) , in modo che le ricerche LDAP possano essere eseguite senza utilizzare caratteri di escape.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DFS-Link-Path-V2
- msDFS-schema AD attributo LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123018"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="dfaf7-106">attributo ms-DFS-Link-Path-V2</span><span class="sxs-lookup"><span data-stu-id="dfaf7-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="dfaf7-107">Percorso collegamento DFS relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="dfaf7-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="dfaf7-108">Utilizzare le barre (/) anziché le barre rovesciate ( \) , in modo che le ricerche LDAP possano essere eseguite senza utilizzare caratteri di escape.</span><span class="sxs-lookup"><span data-stu-id="dfaf7-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="dfaf7-109">Voce</span><span class="sxs-lookup"><span data-stu-id="dfaf7-109">Entry</span></span> | <span data-ttu-id="dfaf7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dfaf7-111">CN</span><span class="sxs-lookup"><span data-stu-id="dfaf7-111">CN</span></span>                | <span data-ttu-id="dfaf7-112">MS-DFS-Link-Path-V2</span><span class="sxs-lookup"><span data-stu-id="dfaf7-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="dfaf7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dfaf7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dfaf7-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="dfaf7-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="dfaf7-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="dfaf7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="dfaf7-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dfaf7-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="dfaf7-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="dfaf7-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="dfaf7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfaf7-118">Attribute-Id</span></span>      | <span data-ttu-id="dfaf7-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="dfaf7-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="dfaf7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dfaf7-120">System-Id-Guid</span></span>    | <span data-ttu-id="dfaf7-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="dfaf7-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="dfaf7-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfaf7-122">Syntax</span></span>            | [<span data-ttu-id="dfaf7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dfaf7-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="dfaf7-124">Implementations</span></span>

-   [<span data-ttu-id="dfaf7-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfaf7-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfaf7-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="dfaf7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfaf7-128">Windows Server 2008</span></span>



| <span data-ttu-id="dfaf7-129">Voce</span><span class="sxs-lookup"><span data-stu-id="dfaf7-129">Entry</span></span> | <span data-ttu-id="dfaf7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaf7-131">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dfaf7-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dfaf7-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfaf7-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dfaf7-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfaf7-133">System-Only</span></span>            | <span data-ttu-id="dfaf7-134">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-135">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dfaf7-135">Is-Single-Valued</span></span>       | <span data-ttu-id="dfaf7-136">Vero</span><span class="sxs-lookup"><span data-stu-id="dfaf7-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="dfaf7-137">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dfaf7-137">Is Indexed</span></span>             | <span data-ttu-id="dfaf7-138">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-139">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dfaf7-139">In Global Catalog</span></span>      | <span data-ttu-id="dfaf7-140">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-141">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfaf7-142">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dfaf7-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="dfaf7-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfaf7-143">Range-Lower</span></span>            | <span data-ttu-id="dfaf7-144">0</span><span class="sxs-lookup"><span data-stu-id="dfaf7-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="dfaf7-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfaf7-145">Range-Upper</span></span>            | <span data-ttu-id="dfaf7-146">32766</span><span class="sxs-lookup"><span data-stu-id="dfaf7-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfaf7-147">Search-Flags</span></span>           | <span data-ttu-id="dfaf7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfaf7-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="dfaf7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfaf7-149">System-Flags</span></span>           | <span data-ttu-id="dfaf7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfaf7-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="dfaf7-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dfaf7-151">Classes used in</span></span>        | [<span data-ttu-id="dfaf7-152">**MS-DFS-deleted-link-V2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="dfaf7-153">**MS-DFS-link-V2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfaf7-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfaf7-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfaf7-155">Voce</span><span class="sxs-lookup"><span data-stu-id="dfaf7-155">Entry</span></span> | <span data-ttu-id="dfaf7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaf7-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dfaf7-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dfaf7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfaf7-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dfaf7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfaf7-159">System-Only</span></span>            | <span data-ttu-id="dfaf7-160">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dfaf7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dfaf7-162">Vero</span><span class="sxs-lookup"><span data-stu-id="dfaf7-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="dfaf7-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dfaf7-163">Is Indexed</span></span>             | <span data-ttu-id="dfaf7-164">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dfaf7-165">In Global Catalog</span></span>      | <span data-ttu-id="dfaf7-166">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfaf7-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dfaf7-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="dfaf7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfaf7-169">Range-Lower</span></span>            | <span data-ttu-id="dfaf7-170">0</span><span class="sxs-lookup"><span data-stu-id="dfaf7-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="dfaf7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfaf7-171">Range-Upper</span></span>            | <span data-ttu-id="dfaf7-172">32766</span><span class="sxs-lookup"><span data-stu-id="dfaf7-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfaf7-173">Search-Flags</span></span>           | <span data-ttu-id="dfaf7-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfaf7-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="dfaf7-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfaf7-175">System-Flags</span></span>           | <span data-ttu-id="dfaf7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfaf7-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="dfaf7-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dfaf7-177">Classes used in</span></span>        | [<span data-ttu-id="dfaf7-178">**MS-DFS-deleted-link-V2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="dfaf7-179">**MS-DFS-link-V2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfaf7-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfaf7-180">Windows Server 2012</span></span>



| <span data-ttu-id="dfaf7-181">Voce</span><span class="sxs-lookup"><span data-stu-id="dfaf7-181">Entry</span></span> | <span data-ttu-id="dfaf7-182">Valore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaf7-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="dfaf7-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dfaf7-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfaf7-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dfaf7-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfaf7-185">System-Only</span></span>            | <span data-ttu-id="dfaf7-186">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="dfaf7-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dfaf7-188">Vero</span><span class="sxs-lookup"><span data-stu-id="dfaf7-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="dfaf7-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="dfaf7-189">Is Indexed</span></span>             | <span data-ttu-id="dfaf7-190">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="dfaf7-191">In Global Catalog</span></span>      | <span data-ttu-id="dfaf7-192">Falso</span><span class="sxs-lookup"><span data-stu-id="dfaf7-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="dfaf7-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfaf7-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="dfaf7-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="dfaf7-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfaf7-195">Range-Lower</span></span>            | <span data-ttu-id="dfaf7-196">0</span><span class="sxs-lookup"><span data-stu-id="dfaf7-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="dfaf7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfaf7-197">Range-Upper</span></span>            | <span data-ttu-id="dfaf7-198">32766</span><span class="sxs-lookup"><span data-stu-id="dfaf7-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="dfaf7-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfaf7-199">Search-Flags</span></span>           | <span data-ttu-id="dfaf7-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfaf7-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="dfaf7-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfaf7-201">System-Flags</span></span>           | <span data-ttu-id="dfaf7-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfaf7-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="dfaf7-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="dfaf7-203">Classes used in</span></span>        | [<span data-ttu-id="dfaf7-204">**MS-DFS-deleted-link-V2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="dfaf7-205">**MS-DFS-link-V2**</span><span class="sxs-lookup"><span data-stu-id="dfaf7-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





