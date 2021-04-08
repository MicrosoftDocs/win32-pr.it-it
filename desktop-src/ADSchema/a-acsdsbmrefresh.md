---
title: Attributo ACS-DSBM-Refresh
description: Questo attributo contiene il valore del timer interval che determina quando il gestore della larghezza di banda della subnet designato (DSBM) Invia un messaggio di aggiornamento ( \_ \_ DSBM) a tutti i gestori della larghezza di banda della subnet in un dominio.
ms.assetid: 018fd748-ca2e-41e1-a920-224a32e13e21
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ACS-DSBM-Refresh
- Schema AD dell'attributo aCSDSBMRefresh
topic_type:
- apiref
api_name:
- ACS-DSBM-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d662b886a8c97f3d155d3c1b40efcef67f7f1f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965148"
---
# <a name="acs-dsbm-refresh-attribute"></a><span data-ttu-id="63a4a-105">Attributo ACS-DSBM-Refresh</span><span class="sxs-lookup"><span data-stu-id="63a4a-105">ACS-DSBM-Refresh attribute</span></span>

<span data-ttu-id="63a4a-106">Questo attributo contiene il valore del timer interval che determina quando il gestore della larghezza di banda della subnet designato (DSBM) Invia un messaggio di aggiornamento ( \_ \_ DSBM) a tutti i gestori della larghezza di banda della subnet in un dominio.</span><span class="sxs-lookup"><span data-stu-id="63a4a-106">This attribute contains the interval timer value that determines when the Designated Subnet Bandwidth Manager (DSBM) sends out a refresh message (I\_AM\_DSBM) to all of the Subnet Bandwidth Managers in a domain.</span></span>



| <span data-ttu-id="63a4a-107">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-107">Entry</span></span> | <span data-ttu-id="63a4a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="63a4a-109">CN</span><span class="sxs-lookup"><span data-stu-id="63a4a-109">CN</span></span>                | <span data-ttu-id="63a4a-110">ACS-DSBM-Refresh</span><span class="sxs-lookup"><span data-stu-id="63a4a-110">ACS-DSBM-Refresh</span></span>                     |
| <span data-ttu-id="63a4a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="63a4a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="63a4a-112">aCSDSBMRefresh</span><span class="sxs-lookup"><span data-stu-id="63a4a-112">aCSDSBMRefresh</span></span>                       |
| <span data-ttu-id="63a4a-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="63a4a-113">Size</span></span>              | <span data-ttu-id="63a4a-114">4 byte</span><span class="sxs-lookup"><span data-stu-id="63a4a-114">4 bytes</span></span>                              |
| <span data-ttu-id="63a4a-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="63a4a-116">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="63a4a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-117">Attribute-Id</span></span>      | <span data-ttu-id="63a4a-118">1.2.840.113556.1.4.777</span><span class="sxs-lookup"><span data-stu-id="63a4a-118">1.2.840.113556.1.4.777</span></span>               |
| <span data-ttu-id="63a4a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="63a4a-119">System-Id-Guid</span></span>    | <span data-ttu-id="63a4a-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="63a4a-120">1cb3559f-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="63a4a-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63a4a-121">Syntax</span></span>            | [<span data-ttu-id="63a4a-122">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="63a4a-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="63a4a-123">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="63a4a-123">Implementations</span></span>

-   [<span data-ttu-id="63a4a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="63a4a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="63a4a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63a4a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63a4a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63a4a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63a4a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63a4a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63a4a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63a4a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63a4a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63a4a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="63a4a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63a4a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="63a4a-131">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-131">Entry</span></span> | <span data-ttu-id="63a4a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="63a4a-133">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a4a-135">System-Only</span></span>            | <span data-ttu-id="63a4a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-136">False</span></span>                                        |
| <span data-ttu-id="63a4a-137">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a4a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="63a4a-138">Vero</span><span class="sxs-lookup"><span data-stu-id="63a4a-138">True</span></span>                                         |
| <span data-ttu-id="63a4a-139">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a4a-139">Is Indexed</span></span>             | <span data-ttu-id="63a4a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-140">False</span></span>                                        |
| <span data-ttu-id="63a4a-141">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a4a-141">In Global Catalog</span></span>      | <span data-ttu-id="63a4a-142">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-142">False</span></span>                                        |
| <span data-ttu-id="63a4a-143">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a4a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a4a-144">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a4a-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="63a4a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a4a-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a4a-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-147">Search-Flags</span></span>           | <span data-ttu-id="63a4a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63a4a-148">0x00000000</span></span>                                   |
| <span data-ttu-id="63a4a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-149">System-Flags</span></span>           | <span data-ttu-id="63a4a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a4a-150">0x00000010</span></span>                                   |
| <span data-ttu-id="63a4a-151">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a4a-151">Classes used in</span></span>        | [<span data-ttu-id="63a4a-152">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="63a4a-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="63a4a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63a4a-153">Windows Server 2003</span></span>



| <span data-ttu-id="63a4a-154">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-154">Entry</span></span> | <span data-ttu-id="63a4a-155">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="63a4a-156">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a4a-158">System-Only</span></span>            | <span data-ttu-id="63a4a-159">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-159">False</span></span>                                        |
| <span data-ttu-id="63a4a-160">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a4a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="63a4a-161">Vero</span><span class="sxs-lookup"><span data-stu-id="63a4a-161">True</span></span>                                         |
| <span data-ttu-id="63a4a-162">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a4a-162">Is Indexed</span></span>             | <span data-ttu-id="63a4a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-163">False</span></span>                                        |
| <span data-ttu-id="63a4a-164">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a4a-164">In Global Catalog</span></span>      | <span data-ttu-id="63a4a-165">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-165">False</span></span>                                        |
| <span data-ttu-id="63a4a-166">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a4a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a4a-167">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a4a-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="63a4a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a4a-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a4a-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-170">Search-Flags</span></span>           | <span data-ttu-id="63a4a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63a4a-171">0x00000000</span></span>                                   |
| <span data-ttu-id="63a4a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-172">System-Flags</span></span>           | <span data-ttu-id="63a4a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a4a-173">0x00000010</span></span>                                   |
| <span data-ttu-id="63a4a-174">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a4a-174">Classes used in</span></span>        | [<span data-ttu-id="63a4a-175">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="63a4a-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63a4a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63a4a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63a4a-177">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-177">Entry</span></span> | <span data-ttu-id="63a4a-178">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="63a4a-179">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a4a-181">System-Only</span></span>            | <span data-ttu-id="63a4a-182">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-182">False</span></span>                                        |
| <span data-ttu-id="63a4a-183">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a4a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="63a4a-184">Vero</span><span class="sxs-lookup"><span data-stu-id="63a4a-184">True</span></span>                                         |
| <span data-ttu-id="63a4a-185">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a4a-185">Is Indexed</span></span>             | <span data-ttu-id="63a4a-186">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-186">False</span></span>                                        |
| <span data-ttu-id="63a4a-187">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a4a-187">In Global Catalog</span></span>      | <span data-ttu-id="63a4a-188">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-188">False</span></span>                                        |
| <span data-ttu-id="63a4a-189">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a4a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a4a-190">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a4a-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="63a4a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a4a-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a4a-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-193">Search-Flags</span></span>           | <span data-ttu-id="63a4a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63a4a-194">0x00000000</span></span>                                   |
| <span data-ttu-id="63a4a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-195">System-Flags</span></span>           | <span data-ttu-id="63a4a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a4a-196">0x00000010</span></span>                                   |
| <span data-ttu-id="63a4a-197">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a4a-197">Classes used in</span></span>        | [<span data-ttu-id="63a4a-198">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="63a4a-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63a4a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63a4a-199">Windows Server 2008</span></span>



| <span data-ttu-id="63a4a-200">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-200">Entry</span></span> | <span data-ttu-id="63a4a-201">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="63a4a-202">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a4a-204">System-Only</span></span>            | <span data-ttu-id="63a4a-205">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-205">False</span></span>                                        |
| <span data-ttu-id="63a4a-206">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a4a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="63a4a-207">Vero</span><span class="sxs-lookup"><span data-stu-id="63a4a-207">True</span></span>                                         |
| <span data-ttu-id="63a4a-208">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a4a-208">Is Indexed</span></span>             | <span data-ttu-id="63a4a-209">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-209">False</span></span>                                        |
| <span data-ttu-id="63a4a-210">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a4a-210">In Global Catalog</span></span>      | <span data-ttu-id="63a4a-211">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-211">False</span></span>                                        |
| <span data-ttu-id="63a4a-212">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a4a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a4a-213">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a4a-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="63a4a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a4a-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a4a-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-216">Search-Flags</span></span>           | <span data-ttu-id="63a4a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63a4a-217">0x00000000</span></span>                                   |
| <span data-ttu-id="63a4a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-218">System-Flags</span></span>           | <span data-ttu-id="63a4a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a4a-219">0x00000010</span></span>                                   |
| <span data-ttu-id="63a4a-220">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a4a-220">Classes used in</span></span>        | [<span data-ttu-id="63a4a-221">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="63a4a-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63a4a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63a4a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63a4a-223">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-223">Entry</span></span> | <span data-ttu-id="63a4a-224">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="63a4a-225">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a4a-227">System-Only</span></span>            | <span data-ttu-id="63a4a-228">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-228">False</span></span>                                        |
| <span data-ttu-id="63a4a-229">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a4a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="63a4a-230">Vero</span><span class="sxs-lookup"><span data-stu-id="63a4a-230">True</span></span>                                         |
| <span data-ttu-id="63a4a-231">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a4a-231">Is Indexed</span></span>             | <span data-ttu-id="63a4a-232">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-232">False</span></span>                                        |
| <span data-ttu-id="63a4a-233">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a4a-233">In Global Catalog</span></span>      | <span data-ttu-id="63a4a-234">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-234">False</span></span>                                        |
| <span data-ttu-id="63a4a-235">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a4a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a4a-236">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a4a-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="63a4a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a4a-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a4a-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-239">Search-Flags</span></span>           | <span data-ttu-id="63a4a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63a4a-240">0x00000000</span></span>                                   |
| <span data-ttu-id="63a4a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-241">System-Flags</span></span>           | <span data-ttu-id="63a4a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a4a-242">0x00000010</span></span>                                   |
| <span data-ttu-id="63a4a-243">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a4a-243">Classes used in</span></span>        | [<span data-ttu-id="63a4a-244">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="63a4a-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63a4a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63a4a-245">Windows Server 2012</span></span>



| <span data-ttu-id="63a4a-246">Voce</span><span class="sxs-lookup"><span data-stu-id="63a4a-246">Entry</span></span> | <span data-ttu-id="63a4a-247">Valore</span><span class="sxs-lookup"><span data-stu-id="63a4a-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="63a4a-248">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="63a4a-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63a4a-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="63a4a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="63a4a-250">System-Only</span></span>            | <span data-ttu-id="63a4a-251">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-251">False</span></span>                                        |
| <span data-ttu-id="63a4a-252">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="63a4a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="63a4a-253">Vero</span><span class="sxs-lookup"><span data-stu-id="63a4a-253">True</span></span>                                         |
| <span data-ttu-id="63a4a-254">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="63a4a-254">Is Indexed</span></span>             | <span data-ttu-id="63a4a-255">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-255">False</span></span>                                        |
| <span data-ttu-id="63a4a-256">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="63a4a-256">In Global Catalog</span></span>      | <span data-ttu-id="63a4a-257">Falso</span><span class="sxs-lookup"><span data-stu-id="63a4a-257">False</span></span>                                        |
| <span data-ttu-id="63a4a-258">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="63a4a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="63a4a-259">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="63a4a-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="63a4a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63a4a-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63a4a-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="63a4a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-262">Search-Flags</span></span>           | <span data-ttu-id="63a4a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63a4a-263">0x00000000</span></span>                                   |
| <span data-ttu-id="63a4a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63a4a-264">System-Flags</span></span>           | <span data-ttu-id="63a4a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63a4a-265">0x00000010</span></span>                                   |
| <span data-ttu-id="63a4a-266">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="63a4a-266">Classes used in</span></span>        | [<span data-ttu-id="63a4a-267">**ACS-subnet**</span><span class="sxs-lookup"><span data-stu-id="63a4a-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





