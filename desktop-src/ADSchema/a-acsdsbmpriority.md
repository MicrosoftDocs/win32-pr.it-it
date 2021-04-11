---
title: ACS-DSBM-attributo priority
description: Questo attributo contiene la priorità per questo gestore della larghezza di banda della subnet (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-schema AD dell'attributo priority
- Schema AD dell'attributo aCSDSBMPriority
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123234"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="ee35d-105">ACS-DSBM-attributo priority</span><span class="sxs-lookup"><span data-stu-id="ee35d-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="ee35d-106">Questo attributo contiene la priorità per questo gestore della larghezza di banda della subnet (SBM).</span><span class="sxs-lookup"><span data-stu-id="ee35d-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="ee35d-107">Quando è necessario eleggere un nuovo gestore della larghezza di banda della subnet designato (DSBM), questo valore viene inviato ad altri SBMs nel dominio come parte di un \_ messaggio DSBM.</span><span class="sxs-lookup"><span data-stu-id="ee35d-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="ee35d-108">La SBM con la priorità più alta viene eletta come nuova DSBM.</span><span class="sxs-lookup"><span data-stu-id="ee35d-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="ee35d-109">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-109">Entry</span></span> | <span data-ttu-id="ee35d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ee35d-111">CN</span><span class="sxs-lookup"><span data-stu-id="ee35d-111">CN</span></span>                | <span data-ttu-id="ee35d-112">ACS-DSBM-priorità</span><span class="sxs-lookup"><span data-stu-id="ee35d-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="ee35d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ee35d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ee35d-114">aCSDSBMPriority</span><span class="sxs-lookup"><span data-stu-id="ee35d-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="ee35d-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ee35d-115">Size</span></span>              | <span data-ttu-id="ee35d-116">4 byte</span><span class="sxs-lookup"><span data-stu-id="ee35d-116">4 bytes</span></span>                              |
| <span data-ttu-id="ee35d-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ee35d-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ee35d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-119">Attribute-Id</span></span>      | <span data-ttu-id="ee35d-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="ee35d-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="ee35d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ee35d-121">System-Id-Guid</span></span>    | <span data-ttu-id="ee35d-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ee35d-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="ee35d-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee35d-123">Syntax</span></span>            | [<span data-ttu-id="ee35d-124">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="ee35d-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ee35d-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="ee35d-125">Implementations</span></span>

-   [<span data-ttu-id="ee35d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ee35d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ee35d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee35d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee35d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee35d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee35d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee35d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee35d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee35d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee35d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee35d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ee35d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee35d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ee35d-133">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-133">Entry</span></span> | <span data-ttu-id="ee35d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee35d-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee35d-137">System-Only</span></span>            | <span data-ttu-id="ee35d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-138">False</span></span>                                        |
| <span data-ttu-id="ee35d-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ee35d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ee35d-140">Vero</span><span class="sxs-lookup"><span data-stu-id="ee35d-140">True</span></span>                                         |
| <span data-ttu-id="ee35d-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ee35d-141">Is Indexed</span></span>             | <span data-ttu-id="ee35d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-142">False</span></span>                                        |
| <span data-ttu-id="ee35d-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ee35d-143">In Global Catalog</span></span>      | <span data-ttu-id="ee35d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-144">False</span></span>                                        |
| <span data-ttu-id="ee35d-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ee35d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee35d-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ee35d-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee35d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee35d-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee35d-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-149">Search-Flags</span></span>           | <span data-ttu-id="ee35d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee35d-150">0x00000000</span></span>                                   |
| <span data-ttu-id="ee35d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-151">System-Flags</span></span>           | <span data-ttu-id="ee35d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee35d-152">0x00000010</span></span>                                   |
| <span data-ttu-id="ee35d-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ee35d-153">Classes used in</span></span>        | [<span data-ttu-id="ee35d-154">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="ee35d-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ee35d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee35d-155">Windows Server 2003</span></span>



| <span data-ttu-id="ee35d-156">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-156">Entry</span></span> | <span data-ttu-id="ee35d-157">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee35d-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee35d-160">System-Only</span></span>            | <span data-ttu-id="ee35d-161">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-161">False</span></span>                                        |
| <span data-ttu-id="ee35d-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ee35d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ee35d-163">Vero</span><span class="sxs-lookup"><span data-stu-id="ee35d-163">True</span></span>                                         |
| <span data-ttu-id="ee35d-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ee35d-164">Is Indexed</span></span>             | <span data-ttu-id="ee35d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-165">False</span></span>                                        |
| <span data-ttu-id="ee35d-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ee35d-166">In Global Catalog</span></span>      | <span data-ttu-id="ee35d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-167">False</span></span>                                        |
| <span data-ttu-id="ee35d-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ee35d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee35d-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ee35d-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee35d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee35d-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee35d-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-172">Search-Flags</span></span>           | <span data-ttu-id="ee35d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee35d-173">0x00000000</span></span>                                   |
| <span data-ttu-id="ee35d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-174">System-Flags</span></span>           | <span data-ttu-id="ee35d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee35d-175">0x00000010</span></span>                                   |
| <span data-ttu-id="ee35d-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ee35d-176">Classes used in</span></span>        | [<span data-ttu-id="ee35d-177">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="ee35d-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee35d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee35d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee35d-179">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-179">Entry</span></span> | <span data-ttu-id="ee35d-180">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee35d-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee35d-183">System-Only</span></span>            | <span data-ttu-id="ee35d-184">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-184">False</span></span>                                        |
| <span data-ttu-id="ee35d-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ee35d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ee35d-186">Vero</span><span class="sxs-lookup"><span data-stu-id="ee35d-186">True</span></span>                                         |
| <span data-ttu-id="ee35d-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ee35d-187">Is Indexed</span></span>             | <span data-ttu-id="ee35d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-188">False</span></span>                                        |
| <span data-ttu-id="ee35d-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ee35d-189">In Global Catalog</span></span>      | <span data-ttu-id="ee35d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-190">False</span></span>                                        |
| <span data-ttu-id="ee35d-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ee35d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee35d-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ee35d-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee35d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee35d-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee35d-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-195">Search-Flags</span></span>           | <span data-ttu-id="ee35d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee35d-196">0x00000000</span></span>                                   |
| <span data-ttu-id="ee35d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-197">System-Flags</span></span>           | <span data-ttu-id="ee35d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee35d-198">0x00000010</span></span>                                   |
| <span data-ttu-id="ee35d-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ee35d-199">Classes used in</span></span>        | [<span data-ttu-id="ee35d-200">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="ee35d-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee35d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee35d-201">Windows Server 2008</span></span>



| <span data-ttu-id="ee35d-202">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-202">Entry</span></span> | <span data-ttu-id="ee35d-203">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee35d-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee35d-206">System-Only</span></span>            | <span data-ttu-id="ee35d-207">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-207">False</span></span>                                        |
| <span data-ttu-id="ee35d-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ee35d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ee35d-209">Vero</span><span class="sxs-lookup"><span data-stu-id="ee35d-209">True</span></span>                                         |
| <span data-ttu-id="ee35d-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ee35d-210">Is Indexed</span></span>             | <span data-ttu-id="ee35d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-211">False</span></span>                                        |
| <span data-ttu-id="ee35d-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ee35d-212">In Global Catalog</span></span>      | <span data-ttu-id="ee35d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-213">False</span></span>                                        |
| <span data-ttu-id="ee35d-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ee35d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee35d-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ee35d-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee35d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee35d-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee35d-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-218">Search-Flags</span></span>           | <span data-ttu-id="ee35d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee35d-219">0x00000000</span></span>                                   |
| <span data-ttu-id="ee35d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-220">System-Flags</span></span>           | <span data-ttu-id="ee35d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee35d-221">0x00000010</span></span>                                   |
| <span data-ttu-id="ee35d-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ee35d-222">Classes used in</span></span>        | [<span data-ttu-id="ee35d-223">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="ee35d-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee35d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee35d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee35d-225">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-225">Entry</span></span> | <span data-ttu-id="ee35d-226">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee35d-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee35d-229">System-Only</span></span>            | <span data-ttu-id="ee35d-230">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-230">False</span></span>                                        |
| <span data-ttu-id="ee35d-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ee35d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ee35d-232">Vero</span><span class="sxs-lookup"><span data-stu-id="ee35d-232">True</span></span>                                         |
| <span data-ttu-id="ee35d-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ee35d-233">Is Indexed</span></span>             | <span data-ttu-id="ee35d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-234">False</span></span>                                        |
| <span data-ttu-id="ee35d-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ee35d-235">In Global Catalog</span></span>      | <span data-ttu-id="ee35d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-236">False</span></span>                                        |
| <span data-ttu-id="ee35d-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ee35d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee35d-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ee35d-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee35d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee35d-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee35d-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-241">Search-Flags</span></span>           | <span data-ttu-id="ee35d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee35d-242">0x00000000</span></span>                                   |
| <span data-ttu-id="ee35d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-243">System-Flags</span></span>           | <span data-ttu-id="ee35d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee35d-244">0x00000010</span></span>                                   |
| <span data-ttu-id="ee35d-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ee35d-245">Classes used in</span></span>        | [<span data-ttu-id="ee35d-246">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="ee35d-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee35d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee35d-247">Windows Server 2012</span></span>



| <span data-ttu-id="ee35d-248">Voce</span><span class="sxs-lookup"><span data-stu-id="ee35d-248">Entry</span></span> | <span data-ttu-id="ee35d-249">Valore</span><span class="sxs-lookup"><span data-stu-id="ee35d-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee35d-250">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="ee35d-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee35d-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee35d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee35d-252">System-Only</span></span>            | <span data-ttu-id="ee35d-253">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-253">False</span></span>                                        |
| <span data-ttu-id="ee35d-254">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="ee35d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ee35d-255">Vero</span><span class="sxs-lookup"><span data-stu-id="ee35d-255">True</span></span>                                         |
| <span data-ttu-id="ee35d-256">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="ee35d-256">Is Indexed</span></span>             | <span data-ttu-id="ee35d-257">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-257">False</span></span>                                        |
| <span data-ttu-id="ee35d-258">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="ee35d-258">In Global Catalog</span></span>      | <span data-ttu-id="ee35d-259">Falso</span><span class="sxs-lookup"><span data-stu-id="ee35d-259">False</span></span>                                        |
| <span data-ttu-id="ee35d-260">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="ee35d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee35d-261">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="ee35d-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee35d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee35d-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee35d-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee35d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-264">Search-Flags</span></span>           | <span data-ttu-id="ee35d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee35d-265">0x00000000</span></span>                                   |
| <span data-ttu-id="ee35d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee35d-266">System-Flags</span></span>           | <span data-ttu-id="ee35d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee35d-267">0x00000010</span></span>                                   |
| <span data-ttu-id="ee35d-268">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="ee35d-268">Classes used in</span></span>        | [<span data-ttu-id="ee35d-269">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="ee35d-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





