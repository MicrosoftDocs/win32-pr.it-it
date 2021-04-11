---
title: Telefono-IP-attributo primario
description: Indirizzo TCP/IP del telefono. Usato dalla telefonia.
ms.assetid: b51f28e4-4677-4798-87f1-2bd952a528ea
ms.tgt_platform: multiple
keywords:
- Telefono-IP-schema AD dell'attributo primario
- Schema AD dell'attributo ipPhone
topic_type:
- apiref
api_name:
- Phone-Ip-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4f16d29f6b3f45c5a229d76ec30c0dd7efdea2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104121999"
---
# <a name="phone-ip-primary-attribute"></a><span data-ttu-id="90bae-106">Telefono-IP-attributo primario</span><span class="sxs-lookup"><span data-stu-id="90bae-106">Phone-Ip-Primary attribute</span></span>

<span data-ttu-id="90bae-107">Indirizzo TCP/IP del telefono.</span><span class="sxs-lookup"><span data-stu-id="90bae-107">The TCP/IP address for the phone.</span></span> <span data-ttu-id="90bae-108">Usato dalla telefonia.</span><span class="sxs-lookup"><span data-stu-id="90bae-108">Used by Telephony.</span></span>



| <span data-ttu-id="90bae-109">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-109">Entry</span></span> | <span data-ttu-id="90bae-110">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="90bae-111">CN</span><span class="sxs-lookup"><span data-stu-id="90bae-111">CN</span></span>                | <span data-ttu-id="90bae-112">Telefono-IP-primario</span><span class="sxs-lookup"><span data-stu-id="90bae-112">Phone-Ip-Primary</span></span>                                                                 |
| <span data-ttu-id="90bae-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="90bae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="90bae-114">ipPhone</span><span class="sxs-lookup"><span data-stu-id="90bae-114">ipPhone</span></span>                                                                          |
| <span data-ttu-id="90bae-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="90bae-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="90bae-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="90bae-116">Update Privilege</span></span>  | <span data-ttu-id="90bae-117">Amministratore di dominio o proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="90bae-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="90bae-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="90bae-118">Update Frequency</span></span>  | <span data-ttu-id="90bae-119">Quando viene creato il record dell'utente e ogni volta che il numero di telefono deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="90bae-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="90bae-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-120">Attribute-Id</span></span>      | <span data-ttu-id="90bae-121">1.2.840.113556.1.4.721</span><span class="sxs-lookup"><span data-stu-id="90bae-121">1.2.840.113556.1.4.721</span></span>                                                           |
| <span data-ttu-id="90bae-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="90bae-122">System-Id-Guid</span></span>    | <span data-ttu-id="90bae-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="90bae-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="90bae-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90bae-124">Syntax</span></span>            | [<span data-ttu-id="90bae-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="90bae-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="90bae-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="90bae-126">Implementations</span></span>

-   [<span data-ttu-id="90bae-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90bae-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90bae-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90bae-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90bae-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90bae-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90bae-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90bae-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90bae-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90bae-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90bae-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90bae-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90bae-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90bae-133">Windows 2000 Server</span></span>



| <span data-ttu-id="90bae-134">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-134">Entry</span></span> | <span data-ttu-id="90bae-135">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="90bae-136">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90bae-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bae-138">System-Only</span></span>            | <span data-ttu-id="90bae-139">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-139">False</span></span>                                                              |
| <span data-ttu-id="90bae-140">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90bae-140">Is-Single-Valued</span></span>       | <span data-ttu-id="90bae-141">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-141">True</span></span>                                                               |
| <span data-ttu-id="90bae-142">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90bae-142">Is Indexed</span></span>             | <span data-ttu-id="90bae-143">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-143">False</span></span>                                                              |
| <span data-ttu-id="90bae-144">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90bae-144">In Global Catalog</span></span>      | <span data-ttu-id="90bae-145">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-145">True</span></span>                                                               |
| <span data-ttu-id="90bae-146">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90bae-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bae-147">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90bae-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="90bae-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bae-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bae-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-150">Search-Flags</span></span>           | <span data-ttu-id="90bae-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bae-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="90bae-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-152">System-Flags</span></span>           | <span data-ttu-id="90bae-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bae-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="90bae-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90bae-154">Classes used in</span></span>        | [<span data-ttu-id="90bae-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="90bae-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90bae-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90bae-156">Windows Server 2003</span></span>



| <span data-ttu-id="90bae-157">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-157">Entry</span></span> | <span data-ttu-id="90bae-158">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="90bae-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90bae-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bae-161">System-Only</span></span>            | <span data-ttu-id="90bae-162">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-162">False</span></span>                                                              |
| <span data-ttu-id="90bae-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90bae-163">Is-Single-Valued</span></span>       | <span data-ttu-id="90bae-164">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-164">True</span></span>                                                               |
| <span data-ttu-id="90bae-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90bae-165">Is Indexed</span></span>             | <span data-ttu-id="90bae-166">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-166">False</span></span>                                                              |
| <span data-ttu-id="90bae-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90bae-167">In Global Catalog</span></span>      | <span data-ttu-id="90bae-168">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-168">True</span></span>                                                               |
| <span data-ttu-id="90bae-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90bae-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bae-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90bae-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="90bae-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bae-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bae-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-173">Search-Flags</span></span>           | <span data-ttu-id="90bae-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bae-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="90bae-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-175">System-Flags</span></span>           | <span data-ttu-id="90bae-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bae-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="90bae-177">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90bae-177">Classes used in</span></span>        | [<span data-ttu-id="90bae-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="90bae-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90bae-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90bae-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90bae-180">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-180">Entry</span></span> | <span data-ttu-id="90bae-181">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="90bae-182">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90bae-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bae-184">System-Only</span></span>            | <span data-ttu-id="90bae-185">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-185">False</span></span>                                                              |
| <span data-ttu-id="90bae-186">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90bae-186">Is-Single-Valued</span></span>       | <span data-ttu-id="90bae-187">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-187">True</span></span>                                                               |
| <span data-ttu-id="90bae-188">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90bae-188">Is Indexed</span></span>             | <span data-ttu-id="90bae-189">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-189">False</span></span>                                                              |
| <span data-ttu-id="90bae-190">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90bae-190">In Global Catalog</span></span>      | <span data-ttu-id="90bae-191">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-191">True</span></span>                                                               |
| <span data-ttu-id="90bae-192">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90bae-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bae-193">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90bae-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="90bae-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bae-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bae-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-196">Search-Flags</span></span>           | <span data-ttu-id="90bae-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bae-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="90bae-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-198">System-Flags</span></span>           | <span data-ttu-id="90bae-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bae-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="90bae-200">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90bae-200">Classes used in</span></span>        | [<span data-ttu-id="90bae-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="90bae-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90bae-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90bae-202">Windows Server 2008</span></span>



| <span data-ttu-id="90bae-203">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-203">Entry</span></span> | <span data-ttu-id="90bae-204">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="90bae-205">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90bae-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bae-207">System-Only</span></span>            | <span data-ttu-id="90bae-208">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-208">False</span></span>                                                              |
| <span data-ttu-id="90bae-209">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90bae-209">Is-Single-Valued</span></span>       | <span data-ttu-id="90bae-210">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-210">True</span></span>                                                               |
| <span data-ttu-id="90bae-211">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90bae-211">Is Indexed</span></span>             | <span data-ttu-id="90bae-212">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-212">False</span></span>                                                              |
| <span data-ttu-id="90bae-213">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90bae-213">In Global Catalog</span></span>      | <span data-ttu-id="90bae-214">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-214">True</span></span>                                                               |
| <span data-ttu-id="90bae-215">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90bae-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bae-216">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90bae-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="90bae-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bae-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bae-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-219">Search-Flags</span></span>           | <span data-ttu-id="90bae-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bae-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="90bae-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-221">System-Flags</span></span>           | <span data-ttu-id="90bae-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bae-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="90bae-223">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90bae-223">Classes used in</span></span>        | [<span data-ttu-id="90bae-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="90bae-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90bae-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90bae-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90bae-226">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-226">Entry</span></span> | <span data-ttu-id="90bae-227">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="90bae-228">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90bae-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bae-230">System-Only</span></span>            | <span data-ttu-id="90bae-231">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-231">False</span></span>                                                              |
| <span data-ttu-id="90bae-232">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90bae-232">Is-Single-Valued</span></span>       | <span data-ttu-id="90bae-233">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-233">True</span></span>                                                               |
| <span data-ttu-id="90bae-234">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90bae-234">Is Indexed</span></span>             | <span data-ttu-id="90bae-235">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-235">False</span></span>                                                              |
| <span data-ttu-id="90bae-236">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90bae-236">In Global Catalog</span></span>      | <span data-ttu-id="90bae-237">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-237">True</span></span>                                                               |
| <span data-ttu-id="90bae-238">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90bae-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bae-239">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90bae-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="90bae-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bae-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bae-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-242">Search-Flags</span></span>           | <span data-ttu-id="90bae-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bae-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="90bae-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-244">System-Flags</span></span>           | <span data-ttu-id="90bae-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bae-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="90bae-246">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90bae-246">Classes used in</span></span>        | [<span data-ttu-id="90bae-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="90bae-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90bae-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90bae-248">Windows Server 2012</span></span>



| <span data-ttu-id="90bae-249">Voce</span><span class="sxs-lookup"><span data-stu-id="90bae-249">Entry</span></span> | <span data-ttu-id="90bae-250">Valore</span><span class="sxs-lookup"><span data-stu-id="90bae-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="90bae-251">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="90bae-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90bae-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="90bae-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="90bae-253">System-Only</span></span>            | <span data-ttu-id="90bae-254">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-254">False</span></span>                                                              |
| <span data-ttu-id="90bae-255">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="90bae-255">Is-Single-Valued</span></span>       | <span data-ttu-id="90bae-256">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-256">True</span></span>                                                               |
| <span data-ttu-id="90bae-257">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="90bae-257">Is Indexed</span></span>             | <span data-ttu-id="90bae-258">Falso</span><span class="sxs-lookup"><span data-stu-id="90bae-258">False</span></span>                                                              |
| <span data-ttu-id="90bae-259">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="90bae-259">In Global Catalog</span></span>      | <span data-ttu-id="90bae-260">Vero</span><span class="sxs-lookup"><span data-stu-id="90bae-260">True</span></span>                                                               |
| <span data-ttu-id="90bae-261">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="90bae-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="90bae-262">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="90bae-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="90bae-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90bae-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90bae-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="90bae-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-265">Search-Flags</span></span>           | <span data-ttu-id="90bae-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90bae-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="90bae-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90bae-267">System-Flags</span></span>           | <span data-ttu-id="90bae-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90bae-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="90bae-269">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="90bae-269">Classes used in</span></span>        | [<span data-ttu-id="90bae-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="90bae-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





