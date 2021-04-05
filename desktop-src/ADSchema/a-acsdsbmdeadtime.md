---
title: Attributo ACS-DSBM-DeadTime
description: Questo attributo contiene l'intervallo di tempo morto per l'elezione (DSBMDeadInterval) per un dominio.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ACS-DSBM-DeadTime
- Schema AD dell'attributo aCSDSBMDeadTime
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122211"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="a7c51-105">Attributo ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="a7c51-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="a7c51-106">Questo attributo contiene l'intervallo di tempo morto per l'elezione (DSBMDeadInterval) per un dominio.</span><span class="sxs-lookup"><span data-stu-id="a7c51-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="a7c51-107">Se il gestore della larghezza di banda della subnet designata non invia un \_ \_ annuncio DSBM durante questo intervallo, gli altri SBMS (subnet Bandwidth Manager) nel dominio eleggono un nuovo DSBM.</span><span class="sxs-lookup"><span data-stu-id="a7c51-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="a7c51-108">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-108">Entry</span></span> | <span data-ttu-id="a7c51-109">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a7c51-110">CN</span><span class="sxs-lookup"><span data-stu-id="a7c51-110">CN</span></span>                | <span data-ttu-id="a7c51-111">ACS-DSBM-DeadTime</span><span class="sxs-lookup"><span data-stu-id="a7c51-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="a7c51-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a7c51-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a7c51-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="a7c51-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="a7c51-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a7c51-114">Size</span></span>              | <span data-ttu-id="a7c51-115">4 byte</span><span class="sxs-lookup"><span data-stu-id="a7c51-115">4 bytes</span></span>                              |
| <span data-ttu-id="a7c51-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a7c51-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a7c51-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-118">Attribute-Id</span></span>      | <span data-ttu-id="a7c51-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="a7c51-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="a7c51-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a7c51-120">System-Id-Guid</span></span>    | <span data-ttu-id="a7c51-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a7c51-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="a7c51-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7c51-122">Syntax</span></span>            | [<span data-ttu-id="a7c51-123">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="a7c51-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a7c51-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="a7c51-124">Implementations</span></span>

-   [<span data-ttu-id="a7c51-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a7c51-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a7c51-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7c51-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7c51-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7c51-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7c51-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7c51-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7c51-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7c51-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7c51-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7c51-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a7c51-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7c51-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a7c51-132">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-132">Entry</span></span> | <span data-ttu-id="a7c51-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a7c51-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7c51-136">System-Only</span></span>            | <span data-ttu-id="a7c51-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-137">False</span></span>                                        |
| <span data-ttu-id="a7c51-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a7c51-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a7c51-139">Vero</span><span class="sxs-lookup"><span data-stu-id="a7c51-139">True</span></span>                                         |
| <span data-ttu-id="a7c51-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a7c51-140">Is Indexed</span></span>             | <span data-ttu-id="a7c51-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-141">False</span></span>                                        |
| <span data-ttu-id="a7c51-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a7c51-142">In Global Catalog</span></span>      | <span data-ttu-id="a7c51-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-143">False</span></span>                                        |
| <span data-ttu-id="a7c51-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a7c51-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7c51-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a7c51-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a7c51-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7c51-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7c51-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-148">Search-Flags</span></span>           | <span data-ttu-id="a7c51-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7c51-149">0x00000000</span></span>                                   |
| <span data-ttu-id="a7c51-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-150">System-Flags</span></span>           | <span data-ttu-id="a7c51-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7c51-151">0x00000010</span></span>                                   |
| <span data-ttu-id="a7c51-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a7c51-152">Classes used in</span></span>        | [<span data-ttu-id="a7c51-153">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="a7c51-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a7c51-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7c51-154">Windows Server 2003</span></span>



| <span data-ttu-id="a7c51-155">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-155">Entry</span></span> | <span data-ttu-id="a7c51-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a7c51-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7c51-159">System-Only</span></span>            | <span data-ttu-id="a7c51-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-160">False</span></span>                                        |
| <span data-ttu-id="a7c51-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a7c51-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a7c51-162">Vero</span><span class="sxs-lookup"><span data-stu-id="a7c51-162">True</span></span>                                         |
| <span data-ttu-id="a7c51-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a7c51-163">Is Indexed</span></span>             | <span data-ttu-id="a7c51-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-164">False</span></span>                                        |
| <span data-ttu-id="a7c51-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a7c51-165">In Global Catalog</span></span>      | <span data-ttu-id="a7c51-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-166">False</span></span>                                        |
| <span data-ttu-id="a7c51-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a7c51-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7c51-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a7c51-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a7c51-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7c51-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7c51-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-171">Search-Flags</span></span>           | <span data-ttu-id="a7c51-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7c51-172">0x00000000</span></span>                                   |
| <span data-ttu-id="a7c51-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-173">System-Flags</span></span>           | <span data-ttu-id="a7c51-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7c51-174">0x00000010</span></span>                                   |
| <span data-ttu-id="a7c51-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a7c51-175">Classes used in</span></span>        | [<span data-ttu-id="a7c51-176">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="a7c51-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7c51-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7c51-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7c51-178">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-178">Entry</span></span> | <span data-ttu-id="a7c51-179">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a7c51-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7c51-182">System-Only</span></span>            | <span data-ttu-id="a7c51-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-183">False</span></span>                                        |
| <span data-ttu-id="a7c51-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a7c51-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a7c51-185">Vero</span><span class="sxs-lookup"><span data-stu-id="a7c51-185">True</span></span>                                         |
| <span data-ttu-id="a7c51-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a7c51-186">Is Indexed</span></span>             | <span data-ttu-id="a7c51-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-187">False</span></span>                                        |
| <span data-ttu-id="a7c51-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a7c51-188">In Global Catalog</span></span>      | <span data-ttu-id="a7c51-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-189">False</span></span>                                        |
| <span data-ttu-id="a7c51-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a7c51-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7c51-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a7c51-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a7c51-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7c51-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7c51-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-194">Search-Flags</span></span>           | <span data-ttu-id="a7c51-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7c51-195">0x00000000</span></span>                                   |
| <span data-ttu-id="a7c51-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-196">System-Flags</span></span>           | <span data-ttu-id="a7c51-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7c51-197">0x00000010</span></span>                                   |
| <span data-ttu-id="a7c51-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a7c51-198">Classes used in</span></span>        | [<span data-ttu-id="a7c51-199">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="a7c51-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7c51-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7c51-200">Windows Server 2008</span></span>



| <span data-ttu-id="a7c51-201">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-201">Entry</span></span> | <span data-ttu-id="a7c51-202">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a7c51-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7c51-205">System-Only</span></span>            | <span data-ttu-id="a7c51-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-206">False</span></span>                                        |
| <span data-ttu-id="a7c51-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a7c51-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a7c51-208">Vero</span><span class="sxs-lookup"><span data-stu-id="a7c51-208">True</span></span>                                         |
| <span data-ttu-id="a7c51-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a7c51-209">Is Indexed</span></span>             | <span data-ttu-id="a7c51-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-210">False</span></span>                                        |
| <span data-ttu-id="a7c51-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a7c51-211">In Global Catalog</span></span>      | <span data-ttu-id="a7c51-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-212">False</span></span>                                        |
| <span data-ttu-id="a7c51-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a7c51-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7c51-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a7c51-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a7c51-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7c51-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7c51-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-217">Search-Flags</span></span>           | <span data-ttu-id="a7c51-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7c51-218">0x00000000</span></span>                                   |
| <span data-ttu-id="a7c51-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-219">System-Flags</span></span>           | <span data-ttu-id="a7c51-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7c51-220">0x00000010</span></span>                                   |
| <span data-ttu-id="a7c51-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a7c51-221">Classes used in</span></span>        | [<span data-ttu-id="a7c51-222">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="a7c51-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7c51-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7c51-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7c51-224">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-224">Entry</span></span> | <span data-ttu-id="a7c51-225">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a7c51-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7c51-228">System-Only</span></span>            | <span data-ttu-id="a7c51-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-229">False</span></span>                                        |
| <span data-ttu-id="a7c51-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a7c51-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a7c51-231">Vero</span><span class="sxs-lookup"><span data-stu-id="a7c51-231">True</span></span>                                         |
| <span data-ttu-id="a7c51-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a7c51-232">Is Indexed</span></span>             | <span data-ttu-id="a7c51-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-233">False</span></span>                                        |
| <span data-ttu-id="a7c51-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a7c51-234">In Global Catalog</span></span>      | <span data-ttu-id="a7c51-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-235">False</span></span>                                        |
| <span data-ttu-id="a7c51-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a7c51-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7c51-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a7c51-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a7c51-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7c51-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7c51-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-240">Search-Flags</span></span>           | <span data-ttu-id="a7c51-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7c51-241">0x00000000</span></span>                                   |
| <span data-ttu-id="a7c51-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-242">System-Flags</span></span>           | <span data-ttu-id="a7c51-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7c51-243">0x00000010</span></span>                                   |
| <span data-ttu-id="a7c51-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a7c51-244">Classes used in</span></span>        | [<span data-ttu-id="a7c51-245">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="a7c51-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7c51-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7c51-246">Windows Server 2012</span></span>



| <span data-ttu-id="a7c51-247">Voce</span><span class="sxs-lookup"><span data-stu-id="a7c51-247">Entry</span></span> | <span data-ttu-id="a7c51-248">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c51-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a7c51-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="a7c51-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7c51-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a7c51-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7c51-251">System-Only</span></span>            | <span data-ttu-id="a7c51-252">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-252">False</span></span>                                        |
| <span data-ttu-id="a7c51-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="a7c51-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a7c51-254">Vero</span><span class="sxs-lookup"><span data-stu-id="a7c51-254">True</span></span>                                         |
| <span data-ttu-id="a7c51-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="a7c51-255">Is Indexed</span></span>             | <span data-ttu-id="a7c51-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-256">False</span></span>                                        |
| <span data-ttu-id="a7c51-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="a7c51-257">In Global Catalog</span></span>      | <span data-ttu-id="a7c51-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a7c51-258">False</span></span>                                        |
| <span data-ttu-id="a7c51-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="a7c51-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7c51-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="a7c51-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a7c51-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7c51-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7c51-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a7c51-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-263">Search-Flags</span></span>           | <span data-ttu-id="a7c51-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7c51-264">0x00000000</span></span>                                   |
| <span data-ttu-id="a7c51-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7c51-265">System-Flags</span></span>           | <span data-ttu-id="a7c51-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7c51-266">0x00000010</span></span>                                   |
| <span data-ttu-id="a7c51-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="a7c51-267">Classes used in</span></span>        | [<span data-ttu-id="a7c51-268">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="a7c51-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





