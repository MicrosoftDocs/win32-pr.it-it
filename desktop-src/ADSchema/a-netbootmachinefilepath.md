---
title: Attributo via-macchina-file-percorso
description: Questo attributo specifica il server che risponde al client. A partire dal sistema operativo Windows Server 2003, può indicare la Startrom.com che il client ottiene.
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo-Machine-file-path
- Schema AD dell'attributo netbootMachineFilePath
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303182"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="021cf-106">Attributo via-macchina-file-percorso</span><span class="sxs-lookup"><span data-stu-id="021cf-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="021cf-107">Questo attributo specifica il server che risponde al client.</span><span class="sxs-lookup"><span data-stu-id="021cf-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="021cf-108">A partire dal sistema operativo Windows Server 2003, può indicare la Startrom.com che il client ottiene.</span><span class="sxs-lookup"><span data-stu-id="021cf-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="021cf-109">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-109">Entry</span></span> | <span data-ttu-id="021cf-110">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="021cf-111">CN</span><span class="sxs-lookup"><span data-stu-id="021cf-111">CN</span></span>                | <span data-ttu-id="021cf-112">Percorso-computer-file-percorso</span><span class="sxs-lookup"><span data-stu-id="021cf-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="021cf-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="021cf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="021cf-114">netbootMachineFilePath</span><span class="sxs-lookup"><span data-stu-id="021cf-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="021cf-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="021cf-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="021cf-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="021cf-116">Update Privilege</span></span>  | <span data-ttu-id="021cf-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="021cf-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="021cf-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="021cf-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="021cf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-119">Attribute-Id</span></span>      | <span data-ttu-id="021cf-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="021cf-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="021cf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="021cf-121">System-Id-Guid</span></span>    | <span data-ttu-id="021cf-122">3e978923-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="021cf-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="021cf-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="021cf-123">Syntax</span></span>            | [<span data-ttu-id="021cf-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="021cf-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="021cf-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="021cf-125">Implementations</span></span>

-   [<span data-ttu-id="021cf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="021cf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="021cf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="021cf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="021cf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="021cf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="021cf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="021cf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="021cf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="021cf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="021cf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="021cf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="021cf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="021cf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="021cf-133">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-133">Entry</span></span> | <span data-ttu-id="021cf-134">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021cf-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="021cf-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="021cf-137">System-Only</span></span>            | <span data-ttu-id="021cf-138">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-138">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="021cf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="021cf-140">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-140">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="021cf-141">Is Indexed</span></span>             | <span data-ttu-id="021cf-142">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-142">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="021cf-143">In Global Catalog</span></span>      | <span data-ttu-id="021cf-144">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-144">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="021cf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="021cf-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="021cf-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="021cf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="021cf-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="021cf-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-149">Search-Flags</span></span>           | <span data-ttu-id="021cf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="021cf-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="021cf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-151">System-Flags</span></span>           | <span data-ttu-id="021cf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="021cf-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="021cf-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="021cf-153">Classes used in</span></span>        | [<span data-ttu-id="021cf-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="021cf-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="021cf-155">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="021cf-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="021cf-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="021cf-156">Windows Server 2003</span></span>



| <span data-ttu-id="021cf-157">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-157">Entry</span></span> | <span data-ttu-id="021cf-158">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021cf-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="021cf-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="021cf-161">System-Only</span></span>            | <span data-ttu-id="021cf-162">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-162">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="021cf-163">Is-Single-Valued</span></span>       | <span data-ttu-id="021cf-164">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-164">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="021cf-165">Is Indexed</span></span>             | <span data-ttu-id="021cf-166">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-166">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="021cf-167">In Global Catalog</span></span>      | <span data-ttu-id="021cf-168">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-168">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="021cf-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="021cf-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="021cf-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="021cf-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="021cf-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="021cf-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-173">Search-Flags</span></span>           | <span data-ttu-id="021cf-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="021cf-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="021cf-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-175">System-Flags</span></span>           | <span data-ttu-id="021cf-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="021cf-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="021cf-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="021cf-177">Classes used in</span></span>        | [<span data-ttu-id="021cf-178">**Computer**</span><span class="sxs-lookup"><span data-stu-id="021cf-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="021cf-179">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="021cf-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="021cf-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="021cf-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="021cf-181">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-181">Entry</span></span> | <span data-ttu-id="021cf-182">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021cf-183">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="021cf-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="021cf-185">System-Only</span></span>            | <span data-ttu-id="021cf-186">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-186">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-187">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="021cf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="021cf-188">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-188">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-189">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="021cf-189">Is Indexed</span></span>             | <span data-ttu-id="021cf-190">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-190">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-191">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="021cf-191">In Global Catalog</span></span>      | <span data-ttu-id="021cf-192">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-192">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-193">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="021cf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="021cf-194">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="021cf-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="021cf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="021cf-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="021cf-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-197">Search-Flags</span></span>           | <span data-ttu-id="021cf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="021cf-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="021cf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-199">System-Flags</span></span>           | <span data-ttu-id="021cf-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="021cf-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="021cf-201">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="021cf-201">Classes used in</span></span>        | [<span data-ttu-id="021cf-202">**Computer**</span><span class="sxs-lookup"><span data-stu-id="021cf-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="021cf-203">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="021cf-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="021cf-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="021cf-204">Windows Server 2008</span></span>



| <span data-ttu-id="021cf-205">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-205">Entry</span></span> | <span data-ttu-id="021cf-206">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021cf-207">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="021cf-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="021cf-209">System-Only</span></span>            | <span data-ttu-id="021cf-210">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-210">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-211">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="021cf-211">Is-Single-Valued</span></span>       | <span data-ttu-id="021cf-212">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-212">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-213">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="021cf-213">Is Indexed</span></span>             | <span data-ttu-id="021cf-214">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-214">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-215">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="021cf-215">In Global Catalog</span></span>      | <span data-ttu-id="021cf-216">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-216">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-217">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="021cf-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="021cf-218">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="021cf-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="021cf-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="021cf-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="021cf-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-221">Search-Flags</span></span>           | <span data-ttu-id="021cf-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="021cf-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="021cf-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-223">System-Flags</span></span>           | <span data-ttu-id="021cf-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="021cf-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="021cf-225">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="021cf-225">Classes used in</span></span>        | [<span data-ttu-id="021cf-226">**Computer**</span><span class="sxs-lookup"><span data-stu-id="021cf-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="021cf-227">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="021cf-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="021cf-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="021cf-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="021cf-229">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-229">Entry</span></span> | <span data-ttu-id="021cf-230">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021cf-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="021cf-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="021cf-233">System-Only</span></span>            | <span data-ttu-id="021cf-234">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-234">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="021cf-235">Is-Single-Valued</span></span>       | <span data-ttu-id="021cf-236">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-236">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="021cf-237">Is Indexed</span></span>             | <span data-ttu-id="021cf-238">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-238">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="021cf-239">In Global Catalog</span></span>      | <span data-ttu-id="021cf-240">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-240">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="021cf-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="021cf-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="021cf-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="021cf-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="021cf-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="021cf-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-245">Search-Flags</span></span>           | <span data-ttu-id="021cf-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="021cf-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="021cf-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-247">System-Flags</span></span>           | <span data-ttu-id="021cf-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="021cf-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="021cf-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="021cf-249">Classes used in</span></span>        | [<span data-ttu-id="021cf-250">**Computer**</span><span class="sxs-lookup"><span data-stu-id="021cf-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="021cf-251">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="021cf-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="021cf-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="021cf-252">Windows Server 2012</span></span>



| <span data-ttu-id="021cf-253">Voce</span><span class="sxs-lookup"><span data-stu-id="021cf-253">Entry</span></span> | <span data-ttu-id="021cf-254">Valore</span><span class="sxs-lookup"><span data-stu-id="021cf-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021cf-255">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="021cf-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="021cf-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="021cf-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="021cf-257">System-Only</span></span>            | <span data-ttu-id="021cf-258">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-258">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-259">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="021cf-259">Is-Single-Valued</span></span>       | <span data-ttu-id="021cf-260">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-260">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-261">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="021cf-261">Is Indexed</span></span>             | <span data-ttu-id="021cf-262">Falso</span><span class="sxs-lookup"><span data-stu-id="021cf-262">False</span></span>                                                                                                |
| <span data-ttu-id="021cf-263">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="021cf-263">In Global Catalog</span></span>      | <span data-ttu-id="021cf-264">Vero</span><span class="sxs-lookup"><span data-stu-id="021cf-264">True</span></span>                                                                                                 |
| <span data-ttu-id="021cf-265">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="021cf-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="021cf-266">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="021cf-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="021cf-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="021cf-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="021cf-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="021cf-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-269">Search-Flags</span></span>           | <span data-ttu-id="021cf-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="021cf-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="021cf-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="021cf-271">System-Flags</span></span>           | <span data-ttu-id="021cf-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="021cf-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="021cf-273">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="021cf-273">Classes used in</span></span>        | [<span data-ttu-id="021cf-274">**Computer**</span><span class="sxs-lookup"><span data-stu-id="021cf-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="021cf-275">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="021cf-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





