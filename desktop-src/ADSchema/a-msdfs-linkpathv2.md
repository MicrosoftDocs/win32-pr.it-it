---
title: Attributo ms-DFS-Link-Path-v2
description: Percorso di collegamento DFS relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS. Usare barre (/) anziché barre rovesciate ( , in modo che le ricerche LDAP possano essere eseguite senza la necessità di \) usare caratteri di escape.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Attributo ms-DFS-Link-Path-v2 Schema DI AD
- Schema AD dell'attributo msDFS-LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386860"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="1d609-106">Attributo ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="1d609-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="1d609-107">Percorso di collegamento DFS relativo alla condivisione di destinazione radice DFS, ovvero senza i componenti server/dominio e nome spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="1d609-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="1d609-108">Usare barre (/) anziché barre rovesciate ( ), in modo che le ricerche LDAP possano essere eseguite senza la necessità di \\ usare caratteri di escape.</span><span class="sxs-lookup"><span data-stu-id="1d609-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="1d609-109">Voce</span><span class="sxs-lookup"><span data-stu-id="1d609-109">Entry</span></span> | <span data-ttu-id="1d609-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1d609-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1d609-111">CN</span><span class="sxs-lookup"><span data-stu-id="1d609-111">CN</span></span>                | <span data-ttu-id="1d609-112">ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="1d609-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="1d609-113">Ldap-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1d609-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1d609-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="1d609-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="1d609-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1d609-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="1d609-116">Privilegio di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1d609-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1d609-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1d609-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1d609-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d609-118">Attribute-Id</span></span>      | <span data-ttu-id="1d609-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="1d609-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="1d609-120">System-Id-Guid</span><span class="sxs-lookup"><span data-stu-id="1d609-120">System-Id-Guid</span></span>    | <span data-ttu-id="1d609-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="1d609-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="1d609-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d609-122">Syntax</span></span>            | [<span data-ttu-id="1d609-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1d609-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1d609-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="1d609-124">Implementations</span></span>

-   [<span data-ttu-id="1d609-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d609-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d609-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d609-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d609-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d609-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="1d609-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d609-128">Windows Server 2008</span></span>



| <span data-ttu-id="1d609-129">Voce</span><span class="sxs-lookup"><span data-stu-id="1d609-129">Entry</span></span> | <span data-ttu-id="1d609-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1d609-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d609-131">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d609-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="1d609-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d609-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="1d609-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d609-133">System-Only</span></span>            | <span data-ttu-id="1d609-134">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-135">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="1d609-135">Is-Single-Valued</span></span>       | <span data-ttu-id="1d609-136">Vero</span><span class="sxs-lookup"><span data-stu-id="1d609-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="1d609-137">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d609-137">Is Indexed</span></span>             | <span data-ttu-id="1d609-138">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-139">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d609-139">In Global Catalog</span></span>      | <span data-ttu-id="1d609-140">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d609-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d609-142">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="1d609-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1d609-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d609-143">Range-Lower</span></span>            | <span data-ttu-id="1d609-144">0</span><span class="sxs-lookup"><span data-stu-id="1d609-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="1d609-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d609-145">Range-Upper</span></span>            | <span data-ttu-id="1d609-146">32766</span><span class="sxs-lookup"><span data-stu-id="1d609-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d609-147">Search-Flags</span></span>           | <span data-ttu-id="1d609-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d609-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="1d609-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d609-149">System-Flags</span></span>           | <span data-ttu-id="1d609-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d609-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1d609-151">Classi usate in</span><span class="sxs-lookup"><span data-stu-id="1d609-151">Classes used in</span></span>        | [<span data-ttu-id="1d609-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="1d609-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="1d609-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="1d609-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d609-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d609-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d609-155">Voce</span><span class="sxs-lookup"><span data-stu-id="1d609-155">Entry</span></span> | <span data-ttu-id="1d609-156">Valore</span><span class="sxs-lookup"><span data-stu-id="1d609-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d609-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d609-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="1d609-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d609-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="1d609-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d609-159">System-Only</span></span>            | <span data-ttu-id="1d609-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-161">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="1d609-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1d609-162">Vero</span><span class="sxs-lookup"><span data-stu-id="1d609-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="1d609-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d609-163">Is Indexed</span></span>             | <span data-ttu-id="1d609-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d609-165">In Global Catalog</span></span>      | <span data-ttu-id="1d609-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d609-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d609-168">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="1d609-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1d609-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d609-169">Range-Lower</span></span>            | <span data-ttu-id="1d609-170">0</span><span class="sxs-lookup"><span data-stu-id="1d609-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="1d609-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d609-171">Range-Upper</span></span>            | <span data-ttu-id="1d609-172">32766</span><span class="sxs-lookup"><span data-stu-id="1d609-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d609-173">Search-Flags</span></span>           | <span data-ttu-id="1d609-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d609-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="1d609-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d609-175">System-Flags</span></span>           | <span data-ttu-id="1d609-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d609-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1d609-177">Classi usate in</span><span class="sxs-lookup"><span data-stu-id="1d609-177">Classes used in</span></span>        | [<span data-ttu-id="1d609-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="1d609-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="1d609-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="1d609-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d609-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d609-180">Windows Server 2012</span></span>



| <span data-ttu-id="1d609-181">Voce</span><span class="sxs-lookup"><span data-stu-id="1d609-181">Entry</span></span> | <span data-ttu-id="1d609-182">Valore</span><span class="sxs-lookup"><span data-stu-id="1d609-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d609-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="1d609-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="1d609-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d609-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="1d609-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d609-185">System-Only</span></span>            | <span data-ttu-id="1d609-186">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-187">Is-Single-Valued</span><span class="sxs-lookup"><span data-stu-id="1d609-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1d609-188">Vero</span><span class="sxs-lookup"><span data-stu-id="1d609-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="1d609-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="1d609-189">Is Indexed</span></span>             | <span data-ttu-id="1d609-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="1d609-191">In Global Catalog</span></span>      | <span data-ttu-id="1d609-192">Falso</span><span class="sxs-lookup"><span data-stu-id="1d609-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d609-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d609-194">O:BAG:BAD:S:</span><span class="sxs-lookup"><span data-stu-id="1d609-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1d609-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d609-195">Range-Lower</span></span>            | <span data-ttu-id="1d609-196">0</span><span class="sxs-lookup"><span data-stu-id="1d609-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="1d609-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d609-197">Range-Upper</span></span>            | <span data-ttu-id="1d609-198">32766</span><span class="sxs-lookup"><span data-stu-id="1d609-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="1d609-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d609-199">Search-Flags</span></span>           | <span data-ttu-id="1d609-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d609-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="1d609-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d609-201">System-Flags</span></span>           | <span data-ttu-id="1d609-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d609-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1d609-203">Classi usate in</span><span class="sxs-lookup"><span data-stu-id="1d609-203">Classes used in</span></span>        | [<span data-ttu-id="1d609-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="1d609-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="1d609-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="1d609-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





