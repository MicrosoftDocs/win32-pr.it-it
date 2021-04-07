---
title: Attributo Proxy-Addresses
description: Un indirizzo proxy è l'indirizzo mediante il quale un oggetto destinatario di Microsoft Exchange Server viene riconosciuto in un sistema di posta elettronica esterno. Gli indirizzi proxy sono necessari per tutti gli oggetti destinatari, ad esempio i destinatari personalizzati e le liste di distribuzione.
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- Schema AD Proxy-Addresses attribute
- Schema AD dell'attributo proxyAddresses
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875554"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="4dfc5-106">Attributo Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="4dfc5-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="4dfc5-107">Un indirizzo proxy è l'indirizzo mediante il quale un oggetto destinatario di Microsoft Exchange Server viene riconosciuto in un sistema di posta elettronica esterno.</span><span class="sxs-lookup"><span data-stu-id="4dfc5-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="4dfc5-108">Gli indirizzi proxy sono necessari per tutti gli oggetti destinatari, ad esempio i destinatari personalizzati e le liste di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4dfc5-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="4dfc5-109">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-109">Entry</span></span> | <span data-ttu-id="4dfc5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dfc5-111">CN</span><span class="sxs-lookup"><span data-stu-id="4dfc5-111">CN</span></span>                | <span data-ttu-id="4dfc5-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="4dfc5-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="4dfc5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4dfc5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4dfc5-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="4dfc5-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="4dfc5-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4dfc5-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="4dfc5-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-116">Update Privilege</span></span>  | <span data-ttu-id="4dfc5-117">Questo valore viene impostato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4dfc5-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="4dfc5-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-118">Update Frequency</span></span>  | <span data-ttu-id="4dfc5-119">Creato da una DLL fornita con l'oggetto Address-Type directory quando viene installato il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="4dfc5-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="4dfc5-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-120">Attribute-Id</span></span>      | <span data-ttu-id="4dfc5-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="4dfc5-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="4dfc5-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4dfc5-122">System-Id-Guid</span></span>    | <span data-ttu-id="4dfc5-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4dfc5-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="4dfc5-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dfc5-124">Syntax</span></span>            | [<span data-ttu-id="4dfc5-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="4dfc5-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="4dfc5-126">Implementations</span></span>

-   [<span data-ttu-id="4dfc5-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4dfc5-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4dfc5-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4dfc5-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4dfc5-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4dfc5-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4dfc5-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4dfc5-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4dfc5-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4dfc5-135">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-135">Entry</span></span> | <span data-ttu-id="4dfc5-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-137">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-138">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-139">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-140">System-Only</span></span>            | <span data-ttu-id="4dfc5-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-141">False</span></span>                           |
| <span data-ttu-id="4dfc5-142">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-143">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-143">False</span></span>                           |
| <span data-ttu-id="4dfc5-144">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-144">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-145">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-145">True</span></span>                            |
| <span data-ttu-id="4dfc5-146">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-146">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-147">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-147">False</span></span>                           |
| <span data-ttu-id="4dfc5-148">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-149">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-150">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-151">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-151">1</span></span>                               |
| <span data-ttu-id="4dfc5-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-152">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-153">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-153">1123</span></span>                            |
| <span data-ttu-id="4dfc5-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-154">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-155">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-156">System-Flags</span></span>           | <span data-ttu-id="4dfc5-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-157">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-158">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-158">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-159">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4dfc5-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4dfc5-160">Windows Server 2003</span></span>



| <span data-ttu-id="4dfc5-161">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-161">Entry</span></span> | <span data-ttu-id="4dfc5-162">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-163">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-164">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-165">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-166">System-Only</span></span>            | <span data-ttu-id="4dfc5-167">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-167">False</span></span>                           |
| <span data-ttu-id="4dfc5-168">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-168">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-169">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-169">False</span></span>                           |
| <span data-ttu-id="4dfc5-170">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-170">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-171">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-171">True</span></span>                            |
| <span data-ttu-id="4dfc5-172">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-172">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-173">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-173">False</span></span>                           |
| <span data-ttu-id="4dfc5-174">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-175">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-176">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-177">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-177">1</span></span>                               |
| <span data-ttu-id="4dfc5-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-178">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-179">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-179">1123</span></span>                            |
| <span data-ttu-id="4dfc5-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-180">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-181">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-182">System-Flags</span></span>           | <span data-ttu-id="4dfc5-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-183">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-184">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-184">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-185">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4dfc5-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="4dfc5-186">ADAM</span></span>



| <span data-ttu-id="4dfc5-187">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-187">Entry</span></span> | <span data-ttu-id="4dfc5-188">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-189">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-190">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-191">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-192">System-Only</span></span>            | <span data-ttu-id="4dfc5-193">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-193">False</span></span>                           |
| <span data-ttu-id="4dfc5-194">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-194">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-195">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-195">False</span></span>                           |
| <span data-ttu-id="4dfc5-196">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-196">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-197">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-197">True</span></span>                            |
| <span data-ttu-id="4dfc5-198">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-198">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-199">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-199">False</span></span>                           |
| <span data-ttu-id="4dfc5-200">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-201">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-202">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-203">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-203">1</span></span>                               |
| <span data-ttu-id="4dfc5-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-204">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-205">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-205">1123</span></span>                            |
| <span data-ttu-id="4dfc5-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-206">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-207">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-208">System-Flags</span></span>           | <span data-ttu-id="4dfc5-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-209">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-210">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-210">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-211">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4dfc5-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4dfc5-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4dfc5-213">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-213">Entry</span></span> | <span data-ttu-id="4dfc5-214">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-215">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-216">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-217">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-218">System-Only</span></span>            | <span data-ttu-id="4dfc5-219">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-219">False</span></span>                           |
| <span data-ttu-id="4dfc5-220">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-220">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-221">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-221">False</span></span>                           |
| <span data-ttu-id="4dfc5-222">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-222">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-223">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-223">True</span></span>                            |
| <span data-ttu-id="4dfc5-224">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-224">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-225">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-225">False</span></span>                           |
| <span data-ttu-id="4dfc5-226">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-227">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-228">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-229">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-229">1</span></span>                               |
| <span data-ttu-id="4dfc5-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-230">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-231">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-231">1123</span></span>                            |
| <span data-ttu-id="4dfc5-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-232">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-233">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-234">System-Flags</span></span>           | <span data-ttu-id="4dfc5-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-235">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-236">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-236">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-237">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4dfc5-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4dfc5-238">Windows Server 2008</span></span>



| <span data-ttu-id="4dfc5-239">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-239">Entry</span></span> | <span data-ttu-id="4dfc5-240">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-241">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-242">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-243">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-244">System-Only</span></span>            | <span data-ttu-id="4dfc5-245">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-245">False</span></span>                           |
| <span data-ttu-id="4dfc5-246">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-246">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-247">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-247">False</span></span>                           |
| <span data-ttu-id="4dfc5-248">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-248">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-249">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-249">True</span></span>                            |
| <span data-ttu-id="4dfc5-250">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-250">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-251">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-251">False</span></span>                           |
| <span data-ttu-id="4dfc5-252">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-253">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-254">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-255">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-255">1</span></span>                               |
| <span data-ttu-id="4dfc5-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-256">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-257">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-257">1123</span></span>                            |
| <span data-ttu-id="4dfc5-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-258">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-259">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-260">System-Flags</span></span>           | <span data-ttu-id="4dfc5-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-261">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-262">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-262">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-263">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4dfc5-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4dfc5-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4dfc5-265">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-265">Entry</span></span> | <span data-ttu-id="4dfc5-266">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-267">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-268">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-269">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-270">System-Only</span></span>            | <span data-ttu-id="4dfc5-271">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-271">False</span></span>                           |
| <span data-ttu-id="4dfc5-272">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-272">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-273">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-273">False</span></span>                           |
| <span data-ttu-id="4dfc5-274">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-274">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-275">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-275">True</span></span>                            |
| <span data-ttu-id="4dfc5-276">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-276">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-277">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-277">False</span></span>                           |
| <span data-ttu-id="4dfc5-278">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-279">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-280">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-281">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-281">1</span></span>                               |
| <span data-ttu-id="4dfc5-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-282">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-283">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-283">1123</span></span>                            |
| <span data-ttu-id="4dfc5-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-284">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-285">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-286">System-Flags</span></span>           | <span data-ttu-id="4dfc5-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-287">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-288">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-288">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-289">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4dfc5-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4dfc5-290">Windows Server 2012</span></span>



| <span data-ttu-id="4dfc5-291">Voce</span><span class="sxs-lookup"><span data-stu-id="4dfc5-291">Entry</span></span> | <span data-ttu-id="4dfc5-292">Valore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4dfc5-293">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="4dfc5-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4dfc5-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4dfc5-294">MAPI-Id</span></span>                | <span data-ttu-id="4dfc5-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="4dfc5-295">0x800F</span></span>                          |
| <span data-ttu-id="4dfc5-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="4dfc5-296">System-Only</span></span>            | <span data-ttu-id="4dfc5-297">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-297">False</span></span>                           |
| <span data-ttu-id="4dfc5-298">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="4dfc5-298">Is-Single-Valued</span></span>       | <span data-ttu-id="4dfc5-299">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-299">False</span></span>                           |
| <span data-ttu-id="4dfc5-300">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="4dfc5-300">Is Indexed</span></span>             | <span data-ttu-id="4dfc5-301">Vero</span><span class="sxs-lookup"><span data-stu-id="4dfc5-301">True</span></span>                            |
| <span data-ttu-id="4dfc5-302">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="4dfc5-302">In Global Catalog</span></span>      | <span data-ttu-id="4dfc5-303">Falso</span><span class="sxs-lookup"><span data-stu-id="4dfc5-303">False</span></span>                           |
| <span data-ttu-id="4dfc5-304">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="4dfc5-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="4dfc5-305">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="4dfc5-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4dfc5-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4dfc5-306">Range-Lower</span></span>            | <span data-ttu-id="4dfc5-307">1</span><span class="sxs-lookup"><span data-stu-id="4dfc5-307">1</span></span>                               |
| <span data-ttu-id="4dfc5-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4dfc5-308">Range-Upper</span></span>            | <span data-ttu-id="4dfc5-309">1123</span><span class="sxs-lookup"><span data-stu-id="4dfc5-309">1123</span></span>                            |
| <span data-ttu-id="4dfc5-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-310">Search-Flags</span></span>           | <span data-ttu-id="4dfc5-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4dfc5-311">0x00000005</span></span>                      |
| <span data-ttu-id="4dfc5-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4dfc5-312">System-Flags</span></span>           | <span data-ttu-id="4dfc5-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4dfc5-313">0x00000010</span></span>                      |
| <span data-ttu-id="4dfc5-314">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="4dfc5-314">Classes used in</span></span>        | [<span data-ttu-id="4dfc5-315">**In alto**</span><span class="sxs-lookup"><span data-stu-id="4dfc5-315">**Top**</span></span>](c-top.md)<br/> |



 

 





