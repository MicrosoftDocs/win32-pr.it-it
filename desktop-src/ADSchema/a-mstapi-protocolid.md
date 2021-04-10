---
title: attributo ms-TAPI-Protocol-ID
description: Questo attributo indica il tipo di conferenza TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-TAPI-Protocol-ID
- msTAPI-schema AD attributo ProtocolId
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122835"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="b10cd-105">attributo ms-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="b10cd-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="b10cd-106">Questo attributo indica il tipo di conferenza TAPI.</span><span class="sxs-lookup"><span data-stu-id="b10cd-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="b10cd-107">Questo attributo viene usato per determinare il modo in cui deve essere interpretato il BLOB binario nell'attributo [**MS-TAPI-Conference-BLOB**](a-mstapi-conferenceblob.md) .</span><span class="sxs-lookup"><span data-stu-id="b10cd-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="b10cd-108">Questo attributo è una stringa arbitraria, in genere di lunghezza inferiore a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b10cd-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="b10cd-109">Voce</span><span class="sxs-lookup"><span data-stu-id="b10cd-109">Entry</span></span> | <span data-ttu-id="b10cd-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b10cd-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="b10cd-111">CN</span><span class="sxs-lookup"><span data-stu-id="b10cd-111">CN</span></span>                | <span data-ttu-id="b10cd-112">MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="b10cd-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="b10cd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b10cd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b10cd-114">msTAPI-ProtocolId</span><span class="sxs-lookup"><span data-stu-id="b10cd-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="b10cd-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b10cd-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="b10cd-116">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-116">Update Privilege</span></span>  | <span data-ttu-id="b10cd-117">Non sono richiesti privilegi speciali.</span><span class="sxs-lookup"><span data-stu-id="b10cd-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="b10cd-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-118">Update Frequency</span></span>  | <span data-ttu-id="b10cd-119">Impostare una volta al momento della creazione dell'oggetto Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="b10cd-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="b10cd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b10cd-120">Attribute-Id</span></span>      | <span data-ttu-id="b10cd-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="b10cd-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="b10cd-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b10cd-122">System-Id-Guid</span></span>    | <span data-ttu-id="b10cd-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="b10cd-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="b10cd-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b10cd-124">Syntax</span></span>            | [<span data-ttu-id="b10cd-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b10cd-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="b10cd-126">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="b10cd-126">Implementations</span></span>

-   [<span data-ttu-id="b10cd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b10cd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b10cd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b10cd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b10cd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b10cd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b10cd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b10cd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b10cd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b10cd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b10cd-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b10cd-132">Windows Server 2003</span></span>



| <span data-ttu-id="b10cd-133">Voce</span><span class="sxs-lookup"><span data-stu-id="b10cd-133">Entry</span></span> | <span data-ttu-id="b10cd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b10cd-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b10cd-135">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b10cd-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b10cd-137">System-Only</span></span>            | <span data-ttu-id="b10cd-138">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-138">False</span></span>                                                             |
| <span data-ttu-id="b10cd-139">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b10cd-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b10cd-140">Vero</span><span class="sxs-lookup"><span data-stu-id="b10cd-140">True</span></span>                                                              |
| <span data-ttu-id="b10cd-141">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b10cd-141">Is Indexed</span></span>             | <span data-ttu-id="b10cd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-142">False</span></span>                                                             |
| <span data-ttu-id="b10cd-143">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b10cd-143">In Global Catalog</span></span>      | <span data-ttu-id="b10cd-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-144">False</span></span>                                                             |
| <span data-ttu-id="b10cd-145">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b10cd-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b10cd-146">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b10cd-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="b10cd-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b10cd-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b10cd-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-149">Search-Flags</span></span>           | <span data-ttu-id="b10cd-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b10cd-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="b10cd-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-151">System-Flags</span></span>           | <span data-ttu-id="b10cd-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b10cd-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="b10cd-153">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b10cd-153">Classes used in</span></span>        | [<span data-ttu-id="b10cd-154">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="b10cd-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b10cd-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b10cd-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b10cd-156">Voce</span><span class="sxs-lookup"><span data-stu-id="b10cd-156">Entry</span></span> | <span data-ttu-id="b10cd-157">Valore</span><span class="sxs-lookup"><span data-stu-id="b10cd-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b10cd-158">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b10cd-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b10cd-160">System-Only</span></span>            | <span data-ttu-id="b10cd-161">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-161">False</span></span>                                                             |
| <span data-ttu-id="b10cd-162">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b10cd-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b10cd-163">Vero</span><span class="sxs-lookup"><span data-stu-id="b10cd-163">True</span></span>                                                              |
| <span data-ttu-id="b10cd-164">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b10cd-164">Is Indexed</span></span>             | <span data-ttu-id="b10cd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-165">False</span></span>                                                             |
| <span data-ttu-id="b10cd-166">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b10cd-166">In Global Catalog</span></span>      | <span data-ttu-id="b10cd-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-167">False</span></span>                                                             |
| <span data-ttu-id="b10cd-168">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b10cd-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b10cd-169">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b10cd-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="b10cd-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b10cd-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b10cd-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-172">Search-Flags</span></span>           | <span data-ttu-id="b10cd-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b10cd-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="b10cd-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-174">System-Flags</span></span>           | <span data-ttu-id="b10cd-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b10cd-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="b10cd-176">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b10cd-176">Classes used in</span></span>        | [<span data-ttu-id="b10cd-177">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="b10cd-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b10cd-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b10cd-178">Windows Server 2008</span></span>



| <span data-ttu-id="b10cd-179">Voce</span><span class="sxs-lookup"><span data-stu-id="b10cd-179">Entry</span></span> | <span data-ttu-id="b10cd-180">Valore</span><span class="sxs-lookup"><span data-stu-id="b10cd-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b10cd-181">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b10cd-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b10cd-183">System-Only</span></span>            | <span data-ttu-id="b10cd-184">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-184">False</span></span>                                                             |
| <span data-ttu-id="b10cd-185">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b10cd-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b10cd-186">Vero</span><span class="sxs-lookup"><span data-stu-id="b10cd-186">True</span></span>                                                              |
| <span data-ttu-id="b10cd-187">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b10cd-187">Is Indexed</span></span>             | <span data-ttu-id="b10cd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-188">False</span></span>                                                             |
| <span data-ttu-id="b10cd-189">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b10cd-189">In Global Catalog</span></span>      | <span data-ttu-id="b10cd-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-190">False</span></span>                                                             |
| <span data-ttu-id="b10cd-191">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b10cd-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b10cd-192">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b10cd-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="b10cd-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b10cd-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b10cd-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-195">Search-Flags</span></span>           | <span data-ttu-id="b10cd-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b10cd-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="b10cd-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-197">System-Flags</span></span>           | <span data-ttu-id="b10cd-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b10cd-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="b10cd-199">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b10cd-199">Classes used in</span></span>        | [<span data-ttu-id="b10cd-200">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="b10cd-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b10cd-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b10cd-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b10cd-202">Voce</span><span class="sxs-lookup"><span data-stu-id="b10cd-202">Entry</span></span> | <span data-ttu-id="b10cd-203">Valore</span><span class="sxs-lookup"><span data-stu-id="b10cd-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b10cd-204">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b10cd-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b10cd-206">System-Only</span></span>            | <span data-ttu-id="b10cd-207">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-207">False</span></span>                                                             |
| <span data-ttu-id="b10cd-208">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b10cd-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b10cd-209">Vero</span><span class="sxs-lookup"><span data-stu-id="b10cd-209">True</span></span>                                                              |
| <span data-ttu-id="b10cd-210">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b10cd-210">Is Indexed</span></span>             | <span data-ttu-id="b10cd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-211">False</span></span>                                                             |
| <span data-ttu-id="b10cd-212">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b10cd-212">In Global Catalog</span></span>      | <span data-ttu-id="b10cd-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-213">False</span></span>                                                             |
| <span data-ttu-id="b10cd-214">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b10cd-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b10cd-215">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b10cd-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="b10cd-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b10cd-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b10cd-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-218">Search-Flags</span></span>           | <span data-ttu-id="b10cd-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b10cd-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="b10cd-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-220">System-Flags</span></span>           | <span data-ttu-id="b10cd-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b10cd-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="b10cd-222">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b10cd-222">Classes used in</span></span>        | [<span data-ttu-id="b10cd-223">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="b10cd-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b10cd-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b10cd-224">Windows Server 2012</span></span>



| <span data-ttu-id="b10cd-225">Voce</span><span class="sxs-lookup"><span data-stu-id="b10cd-225">Entry</span></span> | <span data-ttu-id="b10cd-226">Valore</span><span class="sxs-lookup"><span data-stu-id="b10cd-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b10cd-227">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="b10cd-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b10cd-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="b10cd-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b10cd-229">System-Only</span></span>            | <span data-ttu-id="b10cd-230">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-230">False</span></span>                                                             |
| <span data-ttu-id="b10cd-231">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="b10cd-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b10cd-232">Vero</span><span class="sxs-lookup"><span data-stu-id="b10cd-232">True</span></span>                                                              |
| <span data-ttu-id="b10cd-233">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="b10cd-233">Is Indexed</span></span>             | <span data-ttu-id="b10cd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-234">False</span></span>                                                             |
| <span data-ttu-id="b10cd-235">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="b10cd-235">In Global Catalog</span></span>      | <span data-ttu-id="b10cd-236">Falso</span><span class="sxs-lookup"><span data-stu-id="b10cd-236">False</span></span>                                                             |
| <span data-ttu-id="b10cd-237">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="b10cd-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b10cd-238">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="b10cd-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="b10cd-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b10cd-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b10cd-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="b10cd-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-241">Search-Flags</span></span>           | <span data-ttu-id="b10cd-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b10cd-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="b10cd-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b10cd-243">System-Flags</span></span>           | <span data-ttu-id="b10cd-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b10cd-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="b10cd-245">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="b10cd-245">Classes used in</span></span>        | [<span data-ttu-id="b10cd-246">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="b10cd-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





