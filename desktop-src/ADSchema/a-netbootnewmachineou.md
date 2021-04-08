---
title: attributo per la nuova-macchina-OU
description: Indica la posizione in cui verrà creato il nuovo account computer client.
ms.assetid: 0e1a9145-65cc-499f-a264-c56f9028341b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo "New-Machine-OU"
- Schema AD dell'attributo netbootNewMachineOU
topic_type:
- apiref
api_name:
- netboot-New-Machine-OU
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3f4a8169d91dc206f6b57cba96374903077b7f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875222"
---
# <a name="netboot-new-machine-ou-attribute"></a><span data-ttu-id="2bd2f-105">attributo per la nuova-macchina-OU</span><span class="sxs-lookup"><span data-stu-id="2bd2f-105">netboot-New-Machine-OU attribute</span></span>

<span data-ttu-id="2bd2f-106">Indica la posizione in cui verrà creato il nuovo account computer client.</span><span class="sxs-lookup"><span data-stu-id="2bd2f-106">Indicates where the new client computer account will be created.</span></span>



| <span data-ttu-id="2bd2f-107">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-107">Entry</span></span> | <span data-ttu-id="2bd2f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2bd2f-109">CN</span><span class="sxs-lookup"><span data-stu-id="2bd2f-109">CN</span></span>                | <span data-ttu-id="2bd2f-110">-Nuovo-computer-OU</span><span class="sxs-lookup"><span data-stu-id="2bd2f-110">netboot-New-Machine-OU</span></span>                  |
| <span data-ttu-id="2bd2f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2bd2f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2bd2f-112">netbootNewMachineOU</span><span class="sxs-lookup"><span data-stu-id="2bd2f-112">netbootNewMachineOU</span></span>                     |
| <span data-ttu-id="2bd2f-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2bd2f-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2bd2f-114">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-114">Update Privilege</span></span>  | <span data-ttu-id="2bd2f-115">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2bd2f-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="2bd2f-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2bd2f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-117">Attribute-Id</span></span>      | <span data-ttu-id="2bd2f-118">1.2.840.113556.1.4.856</span><span class="sxs-lookup"><span data-stu-id="2bd2f-118">1.2.840.113556.1.4.856</span></span>                  |
| <span data-ttu-id="2bd2f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2bd2f-119">System-Id-Guid</span></span>    | <span data-ttu-id="2bd2f-120">0738307d-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2bd2f-120">0738307d-91df-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="2bd2f-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bd2f-121">Syntax</span></span>            | [<span data-ttu-id="2bd2f-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2bd2f-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="2bd2f-123">Implementations</span></span>

-   [<span data-ttu-id="2bd2f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2bd2f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2bd2f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2bd2f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2bd2f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2bd2f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2bd2f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bd2f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2bd2f-131">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-131">Entry</span></span> | <span data-ttu-id="2bd2f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bd2f-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bd2f-135">System-Only</span></span>            | <span data-ttu-id="2bd2f-136">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-136">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2bd2f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2bd2f-138">Vero</span><span class="sxs-lookup"><span data-stu-id="2bd2f-138">True</span></span>                                                       |
| <span data-ttu-id="2bd2f-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2bd2f-139">Is Indexed</span></span>             | <span data-ttu-id="2bd2f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-140">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2bd2f-141">In Global Catalog</span></span>      | <span data-ttu-id="2bd2f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-142">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bd2f-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2bd2f-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="2bd2f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bd2f-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bd2f-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-147">Search-Flags</span></span>           | <span data-ttu-id="2bd2f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bd2f-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="2bd2f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-149">System-Flags</span></span>           | <span data-ttu-id="2bd2f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bd2f-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="2bd2f-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2bd2f-151">Classes used in</span></span>        | [<span data-ttu-id="2bd2f-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2bd2f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2bd2f-153">Windows Server 2003</span></span>



| <span data-ttu-id="2bd2f-154">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-154">Entry</span></span> | <span data-ttu-id="2bd2f-155">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bd2f-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bd2f-158">System-Only</span></span>            | <span data-ttu-id="2bd2f-159">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-159">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2bd2f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2bd2f-161">Vero</span><span class="sxs-lookup"><span data-stu-id="2bd2f-161">True</span></span>                                                       |
| <span data-ttu-id="2bd2f-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2bd2f-162">Is Indexed</span></span>             | <span data-ttu-id="2bd2f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-163">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2bd2f-164">In Global Catalog</span></span>      | <span data-ttu-id="2bd2f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-165">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bd2f-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2bd2f-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="2bd2f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bd2f-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bd2f-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-170">Search-Flags</span></span>           | <span data-ttu-id="2bd2f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bd2f-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="2bd2f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-172">System-Flags</span></span>           | <span data-ttu-id="2bd2f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bd2f-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="2bd2f-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2bd2f-174">Classes used in</span></span>        | [<span data-ttu-id="2bd2f-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2bd2f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2bd2f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2bd2f-177">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-177">Entry</span></span> | <span data-ttu-id="2bd2f-178">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bd2f-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bd2f-181">System-Only</span></span>            | <span data-ttu-id="2bd2f-182">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-182">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2bd2f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2bd2f-184">Vero</span><span class="sxs-lookup"><span data-stu-id="2bd2f-184">True</span></span>                                                       |
| <span data-ttu-id="2bd2f-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2bd2f-185">Is Indexed</span></span>             | <span data-ttu-id="2bd2f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-186">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2bd2f-187">In Global Catalog</span></span>      | <span data-ttu-id="2bd2f-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-188">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bd2f-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2bd2f-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="2bd2f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bd2f-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bd2f-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-193">Search-Flags</span></span>           | <span data-ttu-id="2bd2f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bd2f-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="2bd2f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-195">System-Flags</span></span>           | <span data-ttu-id="2bd2f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bd2f-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="2bd2f-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2bd2f-197">Classes used in</span></span>        | [<span data-ttu-id="2bd2f-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2bd2f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bd2f-199">Windows Server 2008</span></span>



| <span data-ttu-id="2bd2f-200">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-200">Entry</span></span> | <span data-ttu-id="2bd2f-201">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bd2f-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bd2f-204">System-Only</span></span>            | <span data-ttu-id="2bd2f-205">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-205">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2bd2f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2bd2f-207">Vero</span><span class="sxs-lookup"><span data-stu-id="2bd2f-207">True</span></span>                                                       |
| <span data-ttu-id="2bd2f-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2bd2f-208">Is Indexed</span></span>             | <span data-ttu-id="2bd2f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-209">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2bd2f-210">In Global Catalog</span></span>      | <span data-ttu-id="2bd2f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-211">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bd2f-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2bd2f-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="2bd2f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bd2f-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bd2f-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-216">Search-Flags</span></span>           | <span data-ttu-id="2bd2f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bd2f-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="2bd2f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-218">System-Flags</span></span>           | <span data-ttu-id="2bd2f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bd2f-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="2bd2f-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2bd2f-220">Classes used in</span></span>        | [<span data-ttu-id="2bd2f-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2bd2f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2bd2f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2bd2f-223">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-223">Entry</span></span> | <span data-ttu-id="2bd2f-224">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bd2f-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bd2f-227">System-Only</span></span>            | <span data-ttu-id="2bd2f-228">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-228">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2bd2f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2bd2f-230">Vero</span><span class="sxs-lookup"><span data-stu-id="2bd2f-230">True</span></span>                                                       |
| <span data-ttu-id="2bd2f-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2bd2f-231">Is Indexed</span></span>             | <span data-ttu-id="2bd2f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-232">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2bd2f-233">In Global Catalog</span></span>      | <span data-ttu-id="2bd2f-234">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-234">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bd2f-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2bd2f-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="2bd2f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bd2f-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bd2f-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-239">Search-Flags</span></span>           | <span data-ttu-id="2bd2f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bd2f-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="2bd2f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-241">System-Flags</span></span>           | <span data-ttu-id="2bd2f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bd2f-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="2bd2f-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2bd2f-243">Classes used in</span></span>        | [<span data-ttu-id="2bd2f-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2bd2f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2bd2f-245">Windows Server 2012</span></span>



| <span data-ttu-id="2bd2f-246">Voce</span><span class="sxs-lookup"><span data-stu-id="2bd2f-246">Entry</span></span> | <span data-ttu-id="2bd2f-247">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bd2f-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="2bd2f-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2bd2f-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="2bd2f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2bd2f-250">System-Only</span></span>            | <span data-ttu-id="2bd2f-251">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-251">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="2bd2f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2bd2f-253">Vero</span><span class="sxs-lookup"><span data-stu-id="2bd2f-253">True</span></span>                                                       |
| <span data-ttu-id="2bd2f-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="2bd2f-254">Is Indexed</span></span>             | <span data-ttu-id="2bd2f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-255">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="2bd2f-256">In Global Catalog</span></span>      | <span data-ttu-id="2bd2f-257">Falso</span><span class="sxs-lookup"><span data-stu-id="2bd2f-257">False</span></span>                                                      |
| <span data-ttu-id="2bd2f-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="2bd2f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2bd2f-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="2bd2f-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="2bd2f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2bd2f-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2bd2f-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="2bd2f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-262">Search-Flags</span></span>           | <span data-ttu-id="2bd2f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2bd2f-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="2bd2f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2bd2f-264">System-Flags</span></span>           | <span data-ttu-id="2bd2f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2bd2f-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="2bd2f-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="2bd2f-266">Classes used in</span></span>        | [<span data-ttu-id="2bd2f-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="2bd2f-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





