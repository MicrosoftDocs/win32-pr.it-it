---
title: MSMQ-destinatario-FormatName (attributo)
description: Utilizzato come nome del formato del destinatario nella classe MSMQ-Custom-Recipient.
ms.assetid: 26ee4cec-4e69-412e-914b-437f2f4cd88e
ms.tgt_platform: multiple
keywords:
- MSMQ-destinatario-FormatName attributo AD schema
- msMQ-destinatario-FormatName attributo AD schema
topic_type:
- apiref
api_name:
- MSMQ-Recipient-FormatName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57fbeee49ddf0c734212bc91926e5c848a9e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122898"
---
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="46cef-105">MSMQ-destinatario-FormatName (attributo)</span><span class="sxs-lookup"><span data-stu-id="46cef-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="46cef-106">Utilizzato come nome del formato del destinatario nella classe MSMQ-Custom-Recipient.</span><span class="sxs-lookup"><span data-stu-id="46cef-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="46cef-107">Voce</span><span class="sxs-lookup"><span data-stu-id="46cef-107">Entry</span></span> | <span data-ttu-id="46cef-108">Valore</span><span class="sxs-lookup"><span data-stu-id="46cef-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="46cef-109">CN</span><span class="sxs-lookup"><span data-stu-id="46cef-109">CN</span></span>                | <span data-ttu-id="46cef-110">MSMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="46cef-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="46cef-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="46cef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="46cef-112">msMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="46cef-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="46cef-113">Dimensione</span><span class="sxs-lookup"><span data-stu-id="46cef-113">Size</span></span>              | <span data-ttu-id="46cef-114">da 1 a 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="46cef-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="46cef-115">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="46cef-115">Update Privilege</span></span>  | <span data-ttu-id="46cef-116">Proprietario della coda.</span><span class="sxs-lookup"><span data-stu-id="46cef-116">The queue owner.</span></span>                            |
| <span data-ttu-id="46cef-117">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="46cef-117">Update Frequency</span></span>  | <span data-ttu-id="46cef-118">Solo dopo lo spostamento della coda esterna.</span><span class="sxs-lookup"><span data-stu-id="46cef-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="46cef-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="46cef-119">Attribute-Id</span></span>      | <span data-ttu-id="46cef-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="46cef-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="46cef-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="46cef-121">System-Id-Guid</span></span>    | <span data-ttu-id="46cef-122">3bfe6748-b544-485a-b067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="46cef-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="46cef-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46cef-123">Syntax</span></span>            | [<span data-ttu-id="46cef-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="46cef-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="46cef-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="46cef-125">Implementations</span></span>

-   [<span data-ttu-id="46cef-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="46cef-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="46cef-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="46cef-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="46cef-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="46cef-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="46cef-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="46cef-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="46cef-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="46cef-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="46cef-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46cef-131">Windows Server 2003</span></span>



| <span data-ttu-id="46cef-132">Voce</span><span class="sxs-lookup"><span data-stu-id="46cef-132">Entry</span></span> | <span data-ttu-id="46cef-133">Valore</span><span class="sxs-lookup"><span data-stu-id="46cef-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="46cef-134">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="46cef-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46cef-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="46cef-136">System-Only</span></span>            | <span data-ttu-id="46cef-137">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-137">False</span></span>                                                               |
| <span data-ttu-id="46cef-138">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="46cef-138">Is-Single-Valued</span></span>       | <span data-ttu-id="46cef-139">Vero</span><span class="sxs-lookup"><span data-stu-id="46cef-139">True</span></span>                                                                |
| <span data-ttu-id="46cef-140">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="46cef-140">Is Indexed</span></span>             | <span data-ttu-id="46cef-141">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-141">False</span></span>                                                               |
| <span data-ttu-id="46cef-142">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="46cef-142">In Global Catalog</span></span>      | <span data-ttu-id="46cef-143">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-143">False</span></span>                                                               |
| <span data-ttu-id="46cef-144">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="46cef-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="46cef-145">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="46cef-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="46cef-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46cef-146">Range-Lower</span></span>            | <span data-ttu-id="46cef-147">1</span><span class="sxs-lookup"><span data-stu-id="46cef-147">1</span></span>                                                                   |
| <span data-ttu-id="46cef-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46cef-148">Range-Upper</span></span>            | <span data-ttu-id="46cef-149">255</span><span class="sxs-lookup"><span data-stu-id="46cef-149">255</span></span>                                                                 |
| <span data-ttu-id="46cef-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-150">Search-Flags</span></span>           | <span data-ttu-id="46cef-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46cef-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="46cef-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-152">System-Flags</span></span>           | <span data-ttu-id="46cef-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46cef-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="46cef-154">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="46cef-154">Classes used in</span></span>        | [<span data-ttu-id="46cef-155">**MSMQ-personalizzato-destinatario**</span><span class="sxs-lookup"><span data-stu-id="46cef-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="46cef-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="46cef-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="46cef-157">Voce</span><span class="sxs-lookup"><span data-stu-id="46cef-157">Entry</span></span> | <span data-ttu-id="46cef-158">Valore</span><span class="sxs-lookup"><span data-stu-id="46cef-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="46cef-159">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="46cef-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46cef-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="46cef-161">System-Only</span></span>            | <span data-ttu-id="46cef-162">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-162">False</span></span>                                                               |
| <span data-ttu-id="46cef-163">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="46cef-163">Is-Single-Valued</span></span>       | <span data-ttu-id="46cef-164">Vero</span><span class="sxs-lookup"><span data-stu-id="46cef-164">True</span></span>                                                                |
| <span data-ttu-id="46cef-165">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="46cef-165">Is Indexed</span></span>             | <span data-ttu-id="46cef-166">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-166">False</span></span>                                                               |
| <span data-ttu-id="46cef-167">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="46cef-167">In Global Catalog</span></span>      | <span data-ttu-id="46cef-168">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-168">False</span></span>                                                               |
| <span data-ttu-id="46cef-169">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="46cef-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="46cef-170">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="46cef-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="46cef-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46cef-171">Range-Lower</span></span>            | <span data-ttu-id="46cef-172">1</span><span class="sxs-lookup"><span data-stu-id="46cef-172">1</span></span>                                                                   |
| <span data-ttu-id="46cef-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46cef-173">Range-Upper</span></span>            | <span data-ttu-id="46cef-174">255</span><span class="sxs-lookup"><span data-stu-id="46cef-174">255</span></span>                                                                 |
| <span data-ttu-id="46cef-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-175">Search-Flags</span></span>           | <span data-ttu-id="46cef-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46cef-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="46cef-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-177">System-Flags</span></span>           | <span data-ttu-id="46cef-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46cef-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="46cef-179">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="46cef-179">Classes used in</span></span>        | [<span data-ttu-id="46cef-180">**MSMQ-personalizzato-destinatario**</span><span class="sxs-lookup"><span data-stu-id="46cef-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="46cef-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46cef-181">Windows Server 2008</span></span>



| <span data-ttu-id="46cef-182">Voce</span><span class="sxs-lookup"><span data-stu-id="46cef-182">Entry</span></span> | <span data-ttu-id="46cef-183">Valore</span><span class="sxs-lookup"><span data-stu-id="46cef-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="46cef-184">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="46cef-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46cef-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="46cef-186">System-Only</span></span>            | <span data-ttu-id="46cef-187">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-187">False</span></span>                                                               |
| <span data-ttu-id="46cef-188">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="46cef-188">Is-Single-Valued</span></span>       | <span data-ttu-id="46cef-189">Vero</span><span class="sxs-lookup"><span data-stu-id="46cef-189">True</span></span>                                                                |
| <span data-ttu-id="46cef-190">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="46cef-190">Is Indexed</span></span>             | <span data-ttu-id="46cef-191">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-191">False</span></span>                                                               |
| <span data-ttu-id="46cef-192">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="46cef-192">In Global Catalog</span></span>      | <span data-ttu-id="46cef-193">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-193">False</span></span>                                                               |
| <span data-ttu-id="46cef-194">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="46cef-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="46cef-195">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="46cef-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="46cef-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46cef-196">Range-Lower</span></span>            | <span data-ttu-id="46cef-197">1</span><span class="sxs-lookup"><span data-stu-id="46cef-197">1</span></span>                                                                   |
| <span data-ttu-id="46cef-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46cef-198">Range-Upper</span></span>            | <span data-ttu-id="46cef-199">255</span><span class="sxs-lookup"><span data-stu-id="46cef-199">255</span></span>                                                                 |
| <span data-ttu-id="46cef-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-200">Search-Flags</span></span>           | <span data-ttu-id="46cef-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46cef-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="46cef-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-202">System-Flags</span></span>           | <span data-ttu-id="46cef-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46cef-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="46cef-204">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="46cef-204">Classes used in</span></span>        | [<span data-ttu-id="46cef-205">**MSMQ-personalizzato-destinatario**</span><span class="sxs-lookup"><span data-stu-id="46cef-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="46cef-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46cef-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="46cef-207">Voce</span><span class="sxs-lookup"><span data-stu-id="46cef-207">Entry</span></span> | <span data-ttu-id="46cef-208">Valore</span><span class="sxs-lookup"><span data-stu-id="46cef-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="46cef-209">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="46cef-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46cef-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="46cef-211">System-Only</span></span>            | <span data-ttu-id="46cef-212">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-212">False</span></span>                                                               |
| <span data-ttu-id="46cef-213">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="46cef-213">Is-Single-Valued</span></span>       | <span data-ttu-id="46cef-214">Vero</span><span class="sxs-lookup"><span data-stu-id="46cef-214">True</span></span>                                                                |
| <span data-ttu-id="46cef-215">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="46cef-215">Is Indexed</span></span>             | <span data-ttu-id="46cef-216">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-216">False</span></span>                                                               |
| <span data-ttu-id="46cef-217">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="46cef-217">In Global Catalog</span></span>      | <span data-ttu-id="46cef-218">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-218">False</span></span>                                                               |
| <span data-ttu-id="46cef-219">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="46cef-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="46cef-220">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="46cef-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="46cef-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46cef-221">Range-Lower</span></span>            | <span data-ttu-id="46cef-222">1</span><span class="sxs-lookup"><span data-stu-id="46cef-222">1</span></span>                                                                   |
| <span data-ttu-id="46cef-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46cef-223">Range-Upper</span></span>            | <span data-ttu-id="46cef-224">255</span><span class="sxs-lookup"><span data-stu-id="46cef-224">255</span></span>                                                                 |
| <span data-ttu-id="46cef-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-225">Search-Flags</span></span>           | <span data-ttu-id="46cef-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46cef-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="46cef-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-227">System-Flags</span></span>           | <span data-ttu-id="46cef-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46cef-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="46cef-229">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="46cef-229">Classes used in</span></span>        | [<span data-ttu-id="46cef-230">**MSMQ-personalizzato-destinatario**</span><span class="sxs-lookup"><span data-stu-id="46cef-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="46cef-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46cef-231">Windows Server 2012</span></span>



| <span data-ttu-id="46cef-232">Voce</span><span class="sxs-lookup"><span data-stu-id="46cef-232">Entry</span></span> | <span data-ttu-id="46cef-233">Valore</span><span class="sxs-lookup"><span data-stu-id="46cef-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="46cef-234">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="46cef-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="46cef-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="46cef-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="46cef-236">System-Only</span></span>            | <span data-ttu-id="46cef-237">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-237">False</span></span>                                                               |
| <span data-ttu-id="46cef-238">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="46cef-238">Is-Single-Valued</span></span>       | <span data-ttu-id="46cef-239">Vero</span><span class="sxs-lookup"><span data-stu-id="46cef-239">True</span></span>                                                                |
| <span data-ttu-id="46cef-240">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="46cef-240">Is Indexed</span></span>             | <span data-ttu-id="46cef-241">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-241">False</span></span>                                                               |
| <span data-ttu-id="46cef-242">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="46cef-242">In Global Catalog</span></span>      | <span data-ttu-id="46cef-243">Falso</span><span class="sxs-lookup"><span data-stu-id="46cef-243">False</span></span>                                                               |
| <span data-ttu-id="46cef-244">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="46cef-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="46cef-245">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="46cef-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="46cef-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="46cef-246">Range-Lower</span></span>            | <span data-ttu-id="46cef-247">1</span><span class="sxs-lookup"><span data-stu-id="46cef-247">1</span></span>                                                                   |
| <span data-ttu-id="46cef-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="46cef-248">Range-Upper</span></span>            | <span data-ttu-id="46cef-249">255</span><span class="sxs-lookup"><span data-stu-id="46cef-249">255</span></span>                                                                 |
| <span data-ttu-id="46cef-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-250">Search-Flags</span></span>           | <span data-ttu-id="46cef-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="46cef-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="46cef-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="46cef-252">System-Flags</span></span>           | <span data-ttu-id="46cef-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="46cef-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="46cef-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="46cef-254">Classes used in</span></span>        | [<span data-ttu-id="46cef-255">**MSMQ-personalizzato-destinatario**</span><span class="sxs-lookup"><span data-stu-id="46cef-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 





