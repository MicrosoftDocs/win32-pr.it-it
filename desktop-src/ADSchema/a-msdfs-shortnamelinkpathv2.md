---
title: attributo ms-DFS-short-name-link-Path-V2
description: Percorso collegamento DFS nome breve relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS. Utilizzare le barre (/) anziché le barre rovesciate ( \) , in modo che le ricerche LDAP possano essere eseguite senza utilizzare caratteri di escape.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DFS-short-name-link-Path-V2
- msDFS-schema AD attributo ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a536abdf13bed7acc99c1036d3c259493994b28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303558"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="f2222-106">attributo ms-DFS-short-name-link-Path-V2</span><span class="sxs-lookup"><span data-stu-id="f2222-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="f2222-107">Percorso collegamento DFS nome breve relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="f2222-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="f2222-108">Utilizzare le barre (/) anziché le barre rovesciate ( \) , in modo che le ricerche LDAP possano essere eseguite senza utilizzare caratteri di escape.</span><span class="sxs-lookup"><span data-stu-id="f2222-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="f2222-109">Voce</span><span class="sxs-lookup"><span data-stu-id="f2222-109">Entry</span></span> | <span data-ttu-id="f2222-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f2222-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f2222-111">CN</span><span class="sxs-lookup"><span data-stu-id="f2222-111">CN</span></span>                | <span data-ttu-id="f2222-112">MS-DFS-short-name-link-Path-V2</span><span class="sxs-lookup"><span data-stu-id="f2222-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="f2222-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f2222-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f2222-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="f2222-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="f2222-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f2222-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f2222-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f2222-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f2222-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f2222-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f2222-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2222-118">Attribute-Id</span></span>      | <span data-ttu-id="f2222-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="f2222-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="f2222-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f2222-120">System-Id-Guid</span></span>    | <span data-ttu-id="f2222-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="f2222-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="f2222-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2222-122">Syntax</span></span>            | [<span data-ttu-id="f2222-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f2222-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f2222-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f2222-124">Implementations</span></span>

-   [<span data-ttu-id="f2222-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2222-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2222-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2222-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2222-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2222-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="f2222-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2222-128">Windows Server 2008</span></span>



| <span data-ttu-id="f2222-129">Voce</span><span class="sxs-lookup"><span data-stu-id="f2222-129">Entry</span></span> | <span data-ttu-id="f2222-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f2222-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2222-131">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f2222-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2222-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2222-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2222-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2222-133">System-Only</span></span>            | <span data-ttu-id="f2222-134">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-135">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f2222-135">Is-Single-Valued</span></span>       | <span data-ttu-id="f2222-136">Vero</span><span class="sxs-lookup"><span data-stu-id="f2222-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2222-137">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f2222-137">Is Indexed</span></span>             | <span data-ttu-id="f2222-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-139">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f2222-139">In Global Catalog</span></span>      | <span data-ttu-id="f2222-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-141">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f2222-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2222-142">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f2222-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2222-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2222-143">Range-Lower</span></span>            | <span data-ttu-id="f2222-144">0</span><span class="sxs-lookup"><span data-stu-id="f2222-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="f2222-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2222-145">Range-Upper</span></span>            | <span data-ttu-id="f2222-146">32766</span><span class="sxs-lookup"><span data-stu-id="f2222-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2222-147">Search-Flags</span></span>           | <span data-ttu-id="f2222-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2222-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f2222-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2222-149">System-Flags</span></span>           | <span data-ttu-id="f2222-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2222-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2222-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f2222-151">Classes used in</span></span>        | [<span data-ttu-id="f2222-152">**MS-DFS-deleted-link-V2**</span><span class="sxs-lookup"><span data-stu-id="f2222-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f2222-153">**MS-DFS-link-V2**</span><span class="sxs-lookup"><span data-stu-id="f2222-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2222-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2222-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2222-155">Voce</span><span class="sxs-lookup"><span data-stu-id="f2222-155">Entry</span></span> | <span data-ttu-id="f2222-156">Valore</span><span class="sxs-lookup"><span data-stu-id="f2222-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2222-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f2222-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2222-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2222-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2222-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2222-159">System-Only</span></span>            | <span data-ttu-id="f2222-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f2222-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f2222-162">Vero</span><span class="sxs-lookup"><span data-stu-id="f2222-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2222-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f2222-163">Is Indexed</span></span>             | <span data-ttu-id="f2222-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f2222-165">In Global Catalog</span></span>      | <span data-ttu-id="f2222-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f2222-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2222-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f2222-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2222-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2222-169">Range-Lower</span></span>            | <span data-ttu-id="f2222-170">0</span><span class="sxs-lookup"><span data-stu-id="f2222-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="f2222-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2222-171">Range-Upper</span></span>            | <span data-ttu-id="f2222-172">32766</span><span class="sxs-lookup"><span data-stu-id="f2222-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2222-173">Search-Flags</span></span>           | <span data-ttu-id="f2222-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2222-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f2222-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2222-175">System-Flags</span></span>           | <span data-ttu-id="f2222-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2222-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2222-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f2222-177">Classes used in</span></span>        | [<span data-ttu-id="f2222-178">**MS-DFS-deleted-link-V2**</span><span class="sxs-lookup"><span data-stu-id="f2222-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f2222-179">**MS-DFS-link-V2**</span><span class="sxs-lookup"><span data-stu-id="f2222-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2222-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2222-180">Windows Server 2012</span></span>



| <span data-ttu-id="f2222-181">Voce</span><span class="sxs-lookup"><span data-stu-id="f2222-181">Entry</span></span> | <span data-ttu-id="f2222-182">Valore</span><span class="sxs-lookup"><span data-stu-id="f2222-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2222-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f2222-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2222-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2222-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f2222-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2222-185">System-Only</span></span>            | <span data-ttu-id="f2222-186">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="f2222-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f2222-188">Vero</span><span class="sxs-lookup"><span data-stu-id="f2222-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="f2222-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f2222-189">Is Indexed</span></span>             | <span data-ttu-id="f2222-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f2222-191">In Global Catalog</span></span>      | <span data-ttu-id="f2222-192">Falso</span><span class="sxs-lookup"><span data-stu-id="f2222-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="f2222-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2222-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="f2222-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f2222-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2222-195">Range-Lower</span></span>            | <span data-ttu-id="f2222-196">0</span><span class="sxs-lookup"><span data-stu-id="f2222-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="f2222-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2222-197">Range-Upper</span></span>            | <span data-ttu-id="f2222-198">32766</span><span class="sxs-lookup"><span data-stu-id="f2222-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f2222-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2222-199">Search-Flags</span></span>           | <span data-ttu-id="f2222-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2222-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f2222-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2222-201">System-Flags</span></span>           | <span data-ttu-id="f2222-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2222-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f2222-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="f2222-203">Classes used in</span></span>        | [<span data-ttu-id="f2222-204">**MS-DFS-deleted-link-V2**</span><span class="sxs-lookup"><span data-stu-id="f2222-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f2222-205">**MS-DFS-link-V2**</span><span class="sxs-lookup"><span data-stu-id="f2222-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





