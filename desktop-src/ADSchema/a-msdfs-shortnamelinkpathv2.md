---
title: Attributo ms-DFS-Short-Name-Link-Path-v2
description: Percorso di collegamento DFS nome breve relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS. Usare barre (/) anziché barre rovesciate ( , in modo che le ricerche LDAP possano essere eseguite senza la necessità di \) usare caratteri di escape.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DFS-Short-Name-Link-Path-v2
- Schema AD dell'attributo msDFS-ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386850"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="f1e42-106">Attributo ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="f1e42-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="f1e42-107">Percorso di collegamento DFS nome breve relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="f1e42-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="f1e42-108">Usare barre (/) anziché barre rovesciate ( ), in modo che le ricerche LDAP possano essere eseguite senza la necessità di \\ usare caratteri di escape.</span><span class="sxs-lookup"><span data-stu-id="f1e42-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="f1e42-109">Voce</span><span class="sxs-lookup"><span data-stu-id="f1e42-109">Entry</span></span> | <span data-ttu-id="f1e42-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e42-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f1e42-111">CN</span><span class="sxs-lookup"><span data-stu-id="f1e42-111">CN</span></span>                | <span data-ttu-id="f1e42-112">ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="f1e42-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="f1e42-113">Ldap-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1e42-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f1e42-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="f1e42-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="f1e42-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f1e42-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f1e42-116">Privilegio di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f1e42-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f1e42-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f1e42-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f1e42-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1e42-118">Attribute-Id</span></span>      | <span data-ttu-id="f1e42-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="f1e42-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="f1e42-120">System-Id-Guid</span><span class="sxs-lookup"><span data-stu-id="f1e42-120">System-Id-Guid</span></span>    | <span data-ttu-id="f1e42-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="f1e42-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="f1e42-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e42-122">Syntax</span></span>            | [<span data-ttu-id="f1e42-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f1e42-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f1e42-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="f1e42-124">Implementations</span></span>

-   [<span data-ttu-id="f1e42-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1e42-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1e42-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1e42-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1e42-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="f1e42-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1e42-128">Windows Server 2008</span></span>



| <span data-ttu-id="f1e42-129">Voce</span><span class="sxs-lookup"><span data-stu-id="f1e42-129">Entry</span></span> | <span data-ttu-id="f1e42-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e42-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e42-131">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f1e42-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f1e42-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1e42-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f1e42-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1e42-133">System-Only</span></span>            | <span data-ttu-id="f1e42-134">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-135">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="f1e42-135">Is-Single-Valued</span></span>       | <span data-ttu-id="f1e42-136">Vero</span><span class="sxs-lookup"><span data-stu-id="f1e42-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="f1e42-137">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f1e42-137">Is Indexed</span></span>             | <span data-ttu-id="f1e42-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-139">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f1e42-139">In Global Catalog</span></span>      | <span data-ttu-id="f1e42-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1e42-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1e42-142">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="f1e42-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f1e42-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1e42-143">Range-Lower</span></span>            | <span data-ttu-id="f1e42-144">0</span><span class="sxs-lookup"><span data-stu-id="f1e42-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="f1e42-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1e42-145">Range-Upper</span></span>            | <span data-ttu-id="f1e42-146">32766</span><span class="sxs-lookup"><span data-stu-id="f1e42-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1e42-147">Search-Flags</span></span>           | <span data-ttu-id="f1e42-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1e42-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f1e42-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1e42-149">System-Flags</span></span>           | <span data-ttu-id="f1e42-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1e42-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f1e42-151">Classi usate in</span><span class="sxs-lookup"><span data-stu-id="f1e42-151">Classes used in</span></span>        | [<span data-ttu-id="f1e42-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f1e42-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1e42-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1e42-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1e42-155">Voce</span><span class="sxs-lookup"><span data-stu-id="f1e42-155">Entry</span></span> | <span data-ttu-id="f1e42-156">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e42-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e42-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f1e42-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f1e42-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1e42-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f1e42-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1e42-159">System-Only</span></span>            | <span data-ttu-id="f1e42-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-161">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="f1e42-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f1e42-162">Vero</span><span class="sxs-lookup"><span data-stu-id="f1e42-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="f1e42-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f1e42-163">Is Indexed</span></span>             | <span data-ttu-id="f1e42-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f1e42-165">In Global Catalog</span></span>      | <span data-ttu-id="f1e42-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1e42-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1e42-168">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="f1e42-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f1e42-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1e42-169">Range-Lower</span></span>            | <span data-ttu-id="f1e42-170">0</span><span class="sxs-lookup"><span data-stu-id="f1e42-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="f1e42-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1e42-171">Range-Upper</span></span>            | <span data-ttu-id="f1e42-172">32766</span><span class="sxs-lookup"><span data-stu-id="f1e42-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1e42-173">Search-Flags</span></span>           | <span data-ttu-id="f1e42-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1e42-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f1e42-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1e42-175">System-Flags</span></span>           | <span data-ttu-id="f1e42-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1e42-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f1e42-177">Classi usate in</span><span class="sxs-lookup"><span data-stu-id="f1e42-177">Classes used in</span></span>        | [<span data-ttu-id="f1e42-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f1e42-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1e42-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1e42-180">Windows Server 2012</span></span>



| <span data-ttu-id="f1e42-181">Voce</span><span class="sxs-lookup"><span data-stu-id="f1e42-181">Entry</span></span> | <span data-ttu-id="f1e42-182">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e42-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e42-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="f1e42-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f1e42-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1e42-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f1e42-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1e42-185">System-Only</span></span>            | <span data-ttu-id="f1e42-186">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-187">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="f1e42-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f1e42-188">Vero</span><span class="sxs-lookup"><span data-stu-id="f1e42-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="f1e42-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="f1e42-189">Is Indexed</span></span>             | <span data-ttu-id="f1e42-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="f1e42-191">In Global Catalog</span></span>      | <span data-ttu-id="f1e42-192">Falso</span><span class="sxs-lookup"><span data-stu-id="f1e42-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1e42-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1e42-194">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="f1e42-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f1e42-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1e42-195">Range-Lower</span></span>            | <span data-ttu-id="f1e42-196">0</span><span class="sxs-lookup"><span data-stu-id="f1e42-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="f1e42-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1e42-197">Range-Upper</span></span>            | <span data-ttu-id="f1e42-198">32766</span><span class="sxs-lookup"><span data-stu-id="f1e42-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f1e42-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1e42-199">Search-Flags</span></span>           | <span data-ttu-id="f1e42-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1e42-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f1e42-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1e42-201">System-Flags</span></span>           | <span data-ttu-id="f1e42-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1e42-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f1e42-203">Classi usate in</span><span class="sxs-lookup"><span data-stu-id="f1e42-203">Classes used in</span></span>        | [<span data-ttu-id="f1e42-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f1e42-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f1e42-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





