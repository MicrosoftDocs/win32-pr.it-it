---
title: Attributo show-in-Address-Book
description: Questo attributo viene utilizzato per indicare in quale libro di indirizzi MAPI verrà visualizzato un oggetto.
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo show-in-Address-Book
- Schema AD dell'attributo showInAddressBook
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479928"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="5df94-105">Attributo show-in-Address-Book</span><span class="sxs-lookup"><span data-stu-id="5df94-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="5df94-106">Questo attributo viene utilizzato per indicare in quale libro di indirizzi MAPI verrà visualizzato un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5df94-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="5df94-107">Viene in genere gestito dal servizio aggiornamento destinatari di Exchange.</span><span class="sxs-lookup"><span data-stu-id="5df94-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="5df94-108">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-108">Entry</span></span> | <span data-ttu-id="5df94-109">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5df94-110">CN</span><span class="sxs-lookup"><span data-stu-id="5df94-110">CN</span></span>                | <span data-ttu-id="5df94-111">Mostra-in-indirizzo-libro</span><span class="sxs-lookup"><span data-stu-id="5df94-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="5df94-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5df94-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5df94-113">showInAddressBook</span><span class="sxs-lookup"><span data-stu-id="5df94-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="5df94-114">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5df94-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="5df94-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5df94-115">Update Privilege</span></span>  | <span data-ttu-id="5df94-116">Viene utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5df94-116">This is used by the system.</span></span>             |
| <span data-ttu-id="5df94-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5df94-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="5df94-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-118">Attribute-Id</span></span>      | <span data-ttu-id="5df94-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="5df94-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="5df94-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5df94-120">System-Id-Guid</span></span>    | <span data-ttu-id="5df94-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5df94-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="5df94-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5df94-122">Syntax</span></span>            | [<span data-ttu-id="5df94-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5df94-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5df94-124">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="5df94-124">Implementations</span></span>

-   [<span data-ttu-id="5df94-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5df94-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5df94-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5df94-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5df94-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5df94-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5df94-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5df94-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5df94-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5df94-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5df94-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5df94-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5df94-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5df94-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5df94-132">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-132">Entry</span></span> | <span data-ttu-id="5df94-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5df94-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5df94-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5df94-136">System-Only</span></span>            | <span data-ttu-id="5df94-137">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-137">False</span></span>                                                |
| <span data-ttu-id="5df94-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5df94-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5df94-139">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-139">False</span></span>                                                |
| <span data-ttu-id="5df94-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5df94-140">Is Indexed</span></span>             | <span data-ttu-id="5df94-141">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-141">False</span></span>                                                |
| <span data-ttu-id="5df94-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5df94-142">In Global Catalog</span></span>      | <span data-ttu-id="5df94-143">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-143">False</span></span>                                                |
| <span data-ttu-id="5df94-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5df94-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5df94-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5df94-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5df94-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5df94-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5df94-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-148">Search-Flags</span></span>           | <span data-ttu-id="5df94-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-149">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-150">System-Flags</span></span>           | <span data-ttu-id="5df94-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-151">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-152">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5df94-152">Classes used in</span></span>        | [<span data-ttu-id="5df94-153">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="5df94-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5df94-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5df94-154">Windows Server 2003</span></span>



| <span data-ttu-id="5df94-155">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-155">Entry</span></span> | <span data-ttu-id="5df94-156">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5df94-157">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5df94-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5df94-159">System-Only</span></span>            | <span data-ttu-id="5df94-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-160">False</span></span>                                                |
| <span data-ttu-id="5df94-161">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5df94-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5df94-162">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-162">False</span></span>                                                |
| <span data-ttu-id="5df94-163">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5df94-163">Is Indexed</span></span>             | <span data-ttu-id="5df94-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-164">False</span></span>                                                |
| <span data-ttu-id="5df94-165">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5df94-165">In Global Catalog</span></span>      | <span data-ttu-id="5df94-166">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-166">False</span></span>                                                |
| <span data-ttu-id="5df94-167">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5df94-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5df94-168">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5df94-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5df94-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5df94-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5df94-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-171">Search-Flags</span></span>           | <span data-ttu-id="5df94-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-172">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-173">System-Flags</span></span>           | <span data-ttu-id="5df94-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-174">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-175">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5df94-175">Classes used in</span></span>        | [<span data-ttu-id="5df94-176">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="5df94-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5df94-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5df94-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5df94-178">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-178">Entry</span></span> | <span data-ttu-id="5df94-179">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5df94-180">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5df94-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5df94-182">System-Only</span></span>            | <span data-ttu-id="5df94-183">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-183">False</span></span>                                                |
| <span data-ttu-id="5df94-184">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5df94-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5df94-185">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-185">False</span></span>                                                |
| <span data-ttu-id="5df94-186">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5df94-186">Is Indexed</span></span>             | <span data-ttu-id="5df94-187">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-187">False</span></span>                                                |
| <span data-ttu-id="5df94-188">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5df94-188">In Global Catalog</span></span>      | <span data-ttu-id="5df94-189">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-189">False</span></span>                                                |
| <span data-ttu-id="5df94-190">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5df94-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5df94-191">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5df94-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5df94-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5df94-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5df94-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-194">Search-Flags</span></span>           | <span data-ttu-id="5df94-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-195">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-196">System-Flags</span></span>           | <span data-ttu-id="5df94-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-197">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-198">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5df94-198">Classes used in</span></span>        | [<span data-ttu-id="5df94-199">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="5df94-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5df94-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5df94-200">Windows Server 2008</span></span>



| <span data-ttu-id="5df94-201">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-201">Entry</span></span> | <span data-ttu-id="5df94-202">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5df94-203">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5df94-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5df94-205">System-Only</span></span>            | <span data-ttu-id="5df94-206">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-206">False</span></span>                                                |
| <span data-ttu-id="5df94-207">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5df94-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5df94-208">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-208">False</span></span>                                                |
| <span data-ttu-id="5df94-209">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5df94-209">Is Indexed</span></span>             | <span data-ttu-id="5df94-210">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-210">False</span></span>                                                |
| <span data-ttu-id="5df94-211">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5df94-211">In Global Catalog</span></span>      | <span data-ttu-id="5df94-212">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-212">False</span></span>                                                |
| <span data-ttu-id="5df94-213">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5df94-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5df94-214">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5df94-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5df94-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5df94-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5df94-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-217">Search-Flags</span></span>           | <span data-ttu-id="5df94-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-218">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-219">System-Flags</span></span>           | <span data-ttu-id="5df94-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-220">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-221">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5df94-221">Classes used in</span></span>        | [<span data-ttu-id="5df94-222">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="5df94-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5df94-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5df94-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5df94-224">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-224">Entry</span></span> | <span data-ttu-id="5df94-225">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5df94-226">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5df94-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5df94-228">System-Only</span></span>            | <span data-ttu-id="5df94-229">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-229">False</span></span>                                                |
| <span data-ttu-id="5df94-230">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5df94-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5df94-231">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-231">False</span></span>                                                |
| <span data-ttu-id="5df94-232">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5df94-232">Is Indexed</span></span>             | <span data-ttu-id="5df94-233">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-233">False</span></span>                                                |
| <span data-ttu-id="5df94-234">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5df94-234">In Global Catalog</span></span>      | <span data-ttu-id="5df94-235">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-235">False</span></span>                                                |
| <span data-ttu-id="5df94-236">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5df94-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5df94-237">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5df94-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5df94-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5df94-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5df94-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-240">Search-Flags</span></span>           | <span data-ttu-id="5df94-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-241">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-242">System-Flags</span></span>           | <span data-ttu-id="5df94-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-243">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-244">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5df94-244">Classes used in</span></span>        | [<span data-ttu-id="5df94-245">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="5df94-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5df94-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5df94-246">Windows Server 2012</span></span>



| <span data-ttu-id="5df94-247">Voce</span><span class="sxs-lookup"><span data-stu-id="5df94-247">Entry</span></span> | <span data-ttu-id="5df94-248">Valore</span><span class="sxs-lookup"><span data-stu-id="5df94-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="5df94-249">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="5df94-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5df94-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="5df94-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5df94-251">System-Only</span></span>            | <span data-ttu-id="5df94-252">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-252">False</span></span>                                                |
| <span data-ttu-id="5df94-253">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="5df94-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5df94-254">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-254">False</span></span>                                                |
| <span data-ttu-id="5df94-255">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="5df94-255">Is Indexed</span></span>             | <span data-ttu-id="5df94-256">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-256">False</span></span>                                                |
| <span data-ttu-id="5df94-257">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="5df94-257">In Global Catalog</span></span>      | <span data-ttu-id="5df94-258">Falso</span><span class="sxs-lookup"><span data-stu-id="5df94-258">False</span></span>                                                |
| <span data-ttu-id="5df94-259">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="5df94-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5df94-260">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="5df94-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="5df94-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5df94-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5df94-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="5df94-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-263">Search-Flags</span></span>           | <span data-ttu-id="5df94-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-264">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5df94-265">System-Flags</span></span>           | <span data-ttu-id="5df94-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5df94-266">0x00000010</span></span>                                           |
| <span data-ttu-id="5df94-267">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="5df94-267">Classes used in</span></span>        | [<span data-ttu-id="5df94-268">**Destinatario posta**</span><span class="sxs-lookup"><span data-stu-id="5df94-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





