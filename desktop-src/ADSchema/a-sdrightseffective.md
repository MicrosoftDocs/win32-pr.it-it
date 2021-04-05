---
title: Attributo SD-Rights-effective
description: Questo attributo costruito restituisce un singolo valore DWORD che può avere fino a tre bit set OWNER \_ Security \_ INFORMATIONDACL \_ Security \_ INFORMATIONSACL \_ Security \_ Information se è impostato un bit, quindi l'utente ha accesso in scrittura alla parte corrispondente del descrittore di sicurezza. Il proprietario indica sia il proprietario che il gruppo.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo SD-Rights-effective
- Schema AD dell'attributo sDRightsEffective
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875162"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="cfa69-106">Attributo SD-Rights-effective</span><span class="sxs-lookup"><span data-stu-id="cfa69-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="cfa69-107">Questo attributo costruito restituisce un singolo valore **DWORD** che può avere fino a tre bit impostati:</span><span class="sxs-lookup"><span data-stu-id="cfa69-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="cfa69-108">\_informazioni di sicurezza del proprietario \_</span><span class="sxs-lookup"><span data-stu-id="cfa69-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="cfa69-109">\_informazioni di sicurezza DACL \_</span><span class="sxs-lookup"><span data-stu-id="cfa69-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="cfa69-110">\_informazioni di sicurezza SACL \_</span><span class="sxs-lookup"><span data-stu-id="cfa69-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="cfa69-111">Se viene impostato un bit, l'utente ha accesso in scrittura alla parte corrispondente del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="cfa69-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="cfa69-112">Il proprietario indica sia il proprietario che il gruppo.</span><span class="sxs-lookup"><span data-stu-id="cfa69-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="cfa69-113">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-113">Entry</span></span> | <span data-ttu-id="cfa69-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cfa69-115">CN</span><span class="sxs-lookup"><span data-stu-id="cfa69-115">CN</span></span>                | <span data-ttu-id="cfa69-116">SD-diritti-efficacia</span><span class="sxs-lookup"><span data-stu-id="cfa69-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="cfa69-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cfa69-117">Ldap-Display-Name</span></span> | <span data-ttu-id="cfa69-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="cfa69-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="cfa69-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cfa69-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="cfa69-120">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cfa69-121">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cfa69-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-122">Attribute-Id</span></span>      | <span data-ttu-id="cfa69-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="cfa69-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="cfa69-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cfa69-124">System-Id-Guid</span></span>    | <span data-ttu-id="cfa69-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cfa69-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="cfa69-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfa69-126">Syntax</span></span>            | [<span data-ttu-id="cfa69-127">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="cfa69-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cfa69-128">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="cfa69-128">Implementations</span></span>

-   [<span data-ttu-id="cfa69-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cfa69-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cfa69-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cfa69-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cfa69-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cfa69-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cfa69-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cfa69-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cfa69-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cfa69-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cfa69-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cfa69-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cfa69-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cfa69-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cfa69-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cfa69-136">Windows 2000 Server</span></span>



| <span data-ttu-id="cfa69-137">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-137">Entry</span></span> | <span data-ttu-id="cfa69-138">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-139">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-141">System-Only</span></span>            | <span data-ttu-id="cfa69-142">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-142">False</span></span>                           |
| <span data-ttu-id="cfa69-143">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-143">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-144">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-144">True</span></span>                            |
| <span data-ttu-id="cfa69-145">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-145">Is Indexed</span></span>             | <span data-ttu-id="cfa69-146">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-146">False</span></span>                           |
| <span data-ttu-id="cfa69-147">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-147">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-148">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-148">False</span></span>                           |
| <span data-ttu-id="cfa69-149">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-150">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-153">Search-Flags</span></span>           | <span data-ttu-id="cfa69-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-154">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-155">System-Flags</span></span>           | <span data-ttu-id="cfa69-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-156">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-157">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-157">Classes used in</span></span>        | [<span data-ttu-id="cfa69-158">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cfa69-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfa69-159">Windows Server 2003</span></span>



| <span data-ttu-id="cfa69-160">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-160">Entry</span></span> | <span data-ttu-id="cfa69-161">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-162">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-164">System-Only</span></span>            | <span data-ttu-id="cfa69-165">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-165">False</span></span>                           |
| <span data-ttu-id="cfa69-166">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-166">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-167">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-167">True</span></span>                            |
| <span data-ttu-id="cfa69-168">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-168">Is Indexed</span></span>             | <span data-ttu-id="cfa69-169">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-169">False</span></span>                           |
| <span data-ttu-id="cfa69-170">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-170">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-171">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-171">False</span></span>                           |
| <span data-ttu-id="cfa69-172">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-173">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-176">Search-Flags</span></span>           | <span data-ttu-id="cfa69-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-177">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-178">System-Flags</span></span>           | <span data-ttu-id="cfa69-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-179">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-180">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-180">Classes used in</span></span>        | [<span data-ttu-id="cfa69-181">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cfa69-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="cfa69-182">ADAM</span></span>



| <span data-ttu-id="cfa69-183">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-183">Entry</span></span> | <span data-ttu-id="cfa69-184">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-185">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-187">System-Only</span></span>            | <span data-ttu-id="cfa69-188">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-188">False</span></span>                           |
| <span data-ttu-id="cfa69-189">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-189">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-190">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-190">True</span></span>                            |
| <span data-ttu-id="cfa69-191">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-191">Is Indexed</span></span>             | <span data-ttu-id="cfa69-192">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-192">False</span></span>                           |
| <span data-ttu-id="cfa69-193">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-193">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-194">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-194">False</span></span>                           |
| <span data-ttu-id="cfa69-195">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-196">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-199">Search-Flags</span></span>           | <span data-ttu-id="cfa69-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-200">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-201">System-Flags</span></span>           | <span data-ttu-id="cfa69-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-202">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-203">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-203">Classes used in</span></span>        | [<span data-ttu-id="cfa69-204">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cfa69-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfa69-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cfa69-206">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-206">Entry</span></span> | <span data-ttu-id="cfa69-207">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-208">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-210">System-Only</span></span>            | <span data-ttu-id="cfa69-211">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-211">False</span></span>                           |
| <span data-ttu-id="cfa69-212">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-212">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-213">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-213">True</span></span>                            |
| <span data-ttu-id="cfa69-214">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-214">Is Indexed</span></span>             | <span data-ttu-id="cfa69-215">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-215">False</span></span>                           |
| <span data-ttu-id="cfa69-216">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-216">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-217">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-217">False</span></span>                           |
| <span data-ttu-id="cfa69-218">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-219">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-222">Search-Flags</span></span>           | <span data-ttu-id="cfa69-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-223">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-224">System-Flags</span></span>           | <span data-ttu-id="cfa69-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-225">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-226">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-226">Classes used in</span></span>        | [<span data-ttu-id="cfa69-227">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cfa69-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfa69-228">Windows Server 2008</span></span>



| <span data-ttu-id="cfa69-229">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-229">Entry</span></span> | <span data-ttu-id="cfa69-230">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-231">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-233">System-Only</span></span>            | <span data-ttu-id="cfa69-234">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-234">False</span></span>                           |
| <span data-ttu-id="cfa69-235">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-235">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-236">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-236">True</span></span>                            |
| <span data-ttu-id="cfa69-237">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-237">Is Indexed</span></span>             | <span data-ttu-id="cfa69-238">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-238">False</span></span>                           |
| <span data-ttu-id="cfa69-239">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-239">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-240">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-240">False</span></span>                           |
| <span data-ttu-id="cfa69-241">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-242">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-245">Search-Flags</span></span>           | <span data-ttu-id="cfa69-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-246">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-247">System-Flags</span></span>           | <span data-ttu-id="cfa69-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-248">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-249">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-249">Classes used in</span></span>        | [<span data-ttu-id="cfa69-250">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cfa69-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfa69-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cfa69-252">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-252">Entry</span></span> | <span data-ttu-id="cfa69-253">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-254">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-256">System-Only</span></span>            | <span data-ttu-id="cfa69-257">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-257">False</span></span>                           |
| <span data-ttu-id="cfa69-258">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-258">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-259">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-259">True</span></span>                            |
| <span data-ttu-id="cfa69-260">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-260">Is Indexed</span></span>             | <span data-ttu-id="cfa69-261">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-261">False</span></span>                           |
| <span data-ttu-id="cfa69-262">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-262">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-263">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-263">False</span></span>                           |
| <span data-ttu-id="cfa69-264">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-265">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-268">Search-Flags</span></span>           | <span data-ttu-id="cfa69-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-269">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-270">System-Flags</span></span>           | <span data-ttu-id="cfa69-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-271">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-272">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-272">Classes used in</span></span>        | [<span data-ttu-id="cfa69-273">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cfa69-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfa69-274">Windows Server 2012</span></span>



| <span data-ttu-id="cfa69-275">Voce</span><span class="sxs-lookup"><span data-stu-id="cfa69-275">Entry</span></span> | <span data-ttu-id="cfa69-276">Valore</span><span class="sxs-lookup"><span data-stu-id="cfa69-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cfa69-277">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="cfa69-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cfa69-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cfa69-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="cfa69-279">System-Only</span></span>            | <span data-ttu-id="cfa69-280">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-280">False</span></span>                           |
| <span data-ttu-id="cfa69-281">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="cfa69-281">Is-Single-Valued</span></span>       | <span data-ttu-id="cfa69-282">Vero</span><span class="sxs-lookup"><span data-stu-id="cfa69-282">True</span></span>                            |
| <span data-ttu-id="cfa69-283">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="cfa69-283">Is Indexed</span></span>             | <span data-ttu-id="cfa69-284">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-284">False</span></span>                           |
| <span data-ttu-id="cfa69-285">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="cfa69-285">In Global Catalog</span></span>      | <span data-ttu-id="cfa69-286">Falso</span><span class="sxs-lookup"><span data-stu-id="cfa69-286">False</span></span>                           |
| <span data-ttu-id="cfa69-287">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="cfa69-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="cfa69-288">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="cfa69-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cfa69-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cfa69-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cfa69-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cfa69-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cfa69-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-291">Search-Flags</span></span>           | <span data-ttu-id="cfa69-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cfa69-292">0x00000000</span></span>                      |
| <span data-ttu-id="cfa69-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cfa69-293">System-Flags</span></span>           | <span data-ttu-id="cfa69-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="cfa69-294">0x08000014</span></span>                      |
| <span data-ttu-id="cfa69-295">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="cfa69-295">Classes used in</span></span>        | [<span data-ttu-id="cfa69-296">**In alto**</span><span class="sxs-lookup"><span data-stu-id="cfa69-296">**Top**</span></span>](c-top.md)<br/> |



 

 





