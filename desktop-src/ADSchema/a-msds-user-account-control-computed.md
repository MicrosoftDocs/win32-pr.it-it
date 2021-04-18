---
title: ms-DS-User-Account-Control-attributo calcolato
description: msDS-User-Account-Control-calcolato è molto simile a userAccountControl, ma il valore dell'attributo può contenere bit aggiuntivi che non sono salvati in modo permanente.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Account-Control-schema AD dell'attributo calcolato
- msDS-User-Account-Control-schema AD dell'attributo calcolato
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303235"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="9a7c2-105">ms-DS-User-Account-Control-attributo calcolato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="9a7c2-106">**msDS-User-Account-Control-calcolato** è molto simile a [**userAccountControl**](a-useraccountcontrol.md), ma il valore dell'attributo può contenere bit aggiuntivi che non sono salvati in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="9a7c2-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="9a7c2-107">I bit calcolati includono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="9a7c2-107">The computed bits include the following.</span></span>



| <span data-ttu-id="9a7c2-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-108">Value</span></span>                | <span data-ttu-id="9a7c2-109">Nome (definito in IADs. h)</span><span class="sxs-lookup"><span data-stu-id="9a7c2-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="9a7c2-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="9a7c2-110">0x0010</span></span><br/>    | <span data-ttu-id="9a7c2-111">**\_blocco UF**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="9a7c2-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-112">0x800000</span></span><br/>  | <span data-ttu-id="9a7c2-113">**\_password UF \_ scaduta**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="9a7c2-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-114">0x4000000</span></span><br/> | <span data-ttu-id="9a7c2-115">**\_account dei \_ segreti PARZIALi UF \_**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="9a7c2-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-116">0x8000000</span></span><br/> | <span data-ttu-id="9a7c2-117">**UF \_ usare \_ \_ chiavi AES**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="9a7c2-118">L'elenco completo dei bit che possono essere contenuti da [**User-Account-Control**](a-useraccountcontrol.md) e quindi da **msDS-User-Account-Control-Compute** è disponibile nella pagina di riferimento **User-Account-Control** (mappata tramite il flag [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) o nelle pagine di riferimento per la gestione della rete per la struttura [**\_ Info utente \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .</span><span class="sxs-lookup"><span data-stu-id="9a7c2-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="9a7c2-119">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-119">Entry</span></span> | <span data-ttu-id="9a7c2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9a7c2-121">CN</span><span class="sxs-lookup"><span data-stu-id="9a7c2-121">CN</span></span>                | <span data-ttu-id="9a7c2-122">ms-DS-User-Account-Control-calcolato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="9a7c2-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a7c2-123">Ldap-Display-Name</span></span> | <span data-ttu-id="9a7c2-124">msDS-User-Account-Control-calcolato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="9a7c2-125">Dimensione</span><span class="sxs-lookup"><span data-stu-id="9a7c2-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="9a7c2-126">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9a7c2-127">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9a7c2-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-128">Attribute-Id</span></span>      | <span data-ttu-id="9a7c2-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="9a7c2-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="9a7c2-130">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a7c2-130">System-Id-Guid</span></span>    | <span data-ttu-id="9a7c2-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span><span class="sxs-lookup"><span data-stu-id="9a7c2-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="9a7c2-132">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a7c2-132">Syntax</span></span>            | [<span data-ttu-id="9a7c2-133">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9a7c2-134">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="9a7c2-134">Implementations</span></span>

-   [<span data-ttu-id="9a7c2-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a7c2-136">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9a7c2-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a7c2-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a7c2-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a7c2-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9a7c2-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a7c2-141">Windows Server 2003</span></span>



| <span data-ttu-id="9a7c2-142">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-142">Entry</span></span> | <span data-ttu-id="9a7c2-143">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9a7c2-144">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a7c2-146">System-Only</span></span>            | <span data-ttu-id="9a7c2-147">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-147">False</span></span>                             |
| <span data-ttu-id="9a7c2-148">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9a7c2-148">Is-Single-Valued</span></span>       | <span data-ttu-id="9a7c2-149">Vero</span><span class="sxs-lookup"><span data-stu-id="9a7c2-149">True</span></span>                              |
| <span data-ttu-id="9a7c2-150">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-150">Is Indexed</span></span>             | <span data-ttu-id="9a7c2-151">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-151">False</span></span>                             |
| <span data-ttu-id="9a7c2-152">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9a7c2-152">In Global Catalog</span></span>      | <span data-ttu-id="9a7c2-153">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-153">False</span></span>                             |
| <span data-ttu-id="9a7c2-154">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a7c2-155">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9a7c2-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9a7c2-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a7c2-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a7c2-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-158">Search-Flags</span></span>           | <span data-ttu-id="9a7c2-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-159">0x00000000</span></span>                        |
| <span data-ttu-id="9a7c2-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-160">System-Flags</span></span>           | <span data-ttu-id="9a7c2-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="9a7c2-161">0x00000014</span></span>                        |
| <span data-ttu-id="9a7c2-162">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9a7c2-162">Classes used in</span></span>        | [<span data-ttu-id="9a7c2-163">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9a7c2-164">ADAM</span><span class="sxs-lookup"><span data-stu-id="9a7c2-164">ADAM</span></span>



| <span data-ttu-id="9a7c2-165">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-165">Entry</span></span> | <span data-ttu-id="9a7c2-166">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9a7c2-167">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9a7c2-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9a7c2-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a7c2-169">System-Only</span></span>            | <span data-ttu-id="9a7c2-170">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-170">False</span></span>                                                             |
| <span data-ttu-id="9a7c2-171">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9a7c2-171">Is-Single-Valued</span></span>       | <span data-ttu-id="9a7c2-172">Vero</span><span class="sxs-lookup"><span data-stu-id="9a7c2-172">True</span></span>                                                              |
| <span data-ttu-id="9a7c2-173">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-173">Is Indexed</span></span>             | <span data-ttu-id="9a7c2-174">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-174">False</span></span>                                                             |
| <span data-ttu-id="9a7c2-175">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9a7c2-175">In Global Catalog</span></span>      | <span data-ttu-id="9a7c2-176">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-176">False</span></span>                                                             |
| <span data-ttu-id="9a7c2-177">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a7c2-178">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9a7c2-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9a7c2-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a7c2-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9a7c2-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a7c2-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9a7c2-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-181">Search-Flags</span></span>           | <span data-ttu-id="9a7c2-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="9a7c2-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-183">System-Flags</span></span>           | <span data-ttu-id="9a7c2-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="9a7c2-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="9a7c2-185">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9a7c2-185">Classes used in</span></span>        | [<span data-ttu-id="9a7c2-186">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a7c2-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a7c2-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a7c2-188">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-188">Entry</span></span> | <span data-ttu-id="9a7c2-189">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9a7c2-190">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a7c2-192">System-Only</span></span>            | <span data-ttu-id="9a7c2-193">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-193">False</span></span>                             |
| <span data-ttu-id="9a7c2-194">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9a7c2-194">Is-Single-Valued</span></span>       | <span data-ttu-id="9a7c2-195">Vero</span><span class="sxs-lookup"><span data-stu-id="9a7c2-195">True</span></span>                              |
| <span data-ttu-id="9a7c2-196">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-196">Is Indexed</span></span>             | <span data-ttu-id="9a7c2-197">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-197">False</span></span>                             |
| <span data-ttu-id="9a7c2-198">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9a7c2-198">In Global Catalog</span></span>      | <span data-ttu-id="9a7c2-199">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-199">False</span></span>                             |
| <span data-ttu-id="9a7c2-200">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a7c2-201">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9a7c2-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9a7c2-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a7c2-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a7c2-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-204">Search-Flags</span></span>           | <span data-ttu-id="9a7c2-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-205">0x00000000</span></span>                        |
| <span data-ttu-id="9a7c2-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-206">System-Flags</span></span>           | <span data-ttu-id="9a7c2-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="9a7c2-207">0x00000014</span></span>                        |
| <span data-ttu-id="9a7c2-208">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9a7c2-208">Classes used in</span></span>        | [<span data-ttu-id="9a7c2-209">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a7c2-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a7c2-210">Windows Server 2008</span></span>



| <span data-ttu-id="9a7c2-211">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-211">Entry</span></span> | <span data-ttu-id="9a7c2-212">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9a7c2-213">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a7c2-215">System-Only</span></span>            | <span data-ttu-id="9a7c2-216">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-216">False</span></span>                             |
| <span data-ttu-id="9a7c2-217">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9a7c2-217">Is-Single-Valued</span></span>       | <span data-ttu-id="9a7c2-218">Vero</span><span class="sxs-lookup"><span data-stu-id="9a7c2-218">True</span></span>                              |
| <span data-ttu-id="9a7c2-219">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-219">Is Indexed</span></span>             | <span data-ttu-id="9a7c2-220">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-220">False</span></span>                             |
| <span data-ttu-id="9a7c2-221">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9a7c2-221">In Global Catalog</span></span>      | <span data-ttu-id="9a7c2-222">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-222">False</span></span>                             |
| <span data-ttu-id="9a7c2-223">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a7c2-224">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9a7c2-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9a7c2-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a7c2-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a7c2-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-227">Search-Flags</span></span>           | <span data-ttu-id="9a7c2-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-228">0x00000000</span></span>                        |
| <span data-ttu-id="9a7c2-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-229">System-Flags</span></span>           | <span data-ttu-id="9a7c2-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="9a7c2-230">0x00000014</span></span>                        |
| <span data-ttu-id="9a7c2-231">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9a7c2-231">Classes used in</span></span>        | [<span data-ttu-id="9a7c2-232">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a7c2-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a7c2-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a7c2-234">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-234">Entry</span></span> | <span data-ttu-id="9a7c2-235">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9a7c2-236">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a7c2-238">System-Only</span></span>            | <span data-ttu-id="9a7c2-239">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-239">False</span></span>                             |
| <span data-ttu-id="9a7c2-240">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9a7c2-240">Is-Single-Valued</span></span>       | <span data-ttu-id="9a7c2-241">Vero</span><span class="sxs-lookup"><span data-stu-id="9a7c2-241">True</span></span>                              |
| <span data-ttu-id="9a7c2-242">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-242">Is Indexed</span></span>             | <span data-ttu-id="9a7c2-243">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-243">False</span></span>                             |
| <span data-ttu-id="9a7c2-244">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9a7c2-244">In Global Catalog</span></span>      | <span data-ttu-id="9a7c2-245">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-245">False</span></span>                             |
| <span data-ttu-id="9a7c2-246">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a7c2-247">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9a7c2-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9a7c2-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a7c2-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a7c2-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-250">Search-Flags</span></span>           | <span data-ttu-id="9a7c2-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-251">0x00000000</span></span>                        |
| <span data-ttu-id="9a7c2-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-252">System-Flags</span></span>           | <span data-ttu-id="9a7c2-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="9a7c2-253">0x00000014</span></span>                        |
| <span data-ttu-id="9a7c2-254">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9a7c2-254">Classes used in</span></span>        | [<span data-ttu-id="9a7c2-255">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a7c2-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a7c2-256">Windows Server 2012</span></span>



| <span data-ttu-id="9a7c2-257">Voce</span><span class="sxs-lookup"><span data-stu-id="9a7c2-257">Entry</span></span> | <span data-ttu-id="9a7c2-258">Valore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9a7c2-259">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="9a7c2-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a7c2-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9a7c2-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a7c2-261">System-Only</span></span>            | <span data-ttu-id="9a7c2-262">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-262">False</span></span>                             |
| <span data-ttu-id="9a7c2-263">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="9a7c2-263">Is-Single-Valued</span></span>       | <span data-ttu-id="9a7c2-264">Vero</span><span class="sxs-lookup"><span data-stu-id="9a7c2-264">True</span></span>                              |
| <span data-ttu-id="9a7c2-265">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="9a7c2-265">Is Indexed</span></span>             | <span data-ttu-id="9a7c2-266">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-266">False</span></span>                             |
| <span data-ttu-id="9a7c2-267">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="9a7c2-267">In Global Catalog</span></span>      | <span data-ttu-id="9a7c2-268">Falso</span><span class="sxs-lookup"><span data-stu-id="9a7c2-268">False</span></span>                             |
| <span data-ttu-id="9a7c2-269">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="9a7c2-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a7c2-270">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="9a7c2-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9a7c2-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a7c2-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a7c2-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9a7c2-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-273">Search-Flags</span></span>           | <span data-ttu-id="9a7c2-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a7c2-274">0x00000000</span></span>                        |
| <span data-ttu-id="9a7c2-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a7c2-275">System-Flags</span></span>           | <span data-ttu-id="9a7c2-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="9a7c2-276">0x00000014</span></span>                        |
| <span data-ttu-id="9a7c2-277">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="9a7c2-277">Classes used in</span></span>        | [<span data-ttu-id="9a7c2-278">**Utente**</span><span class="sxs-lookup"><span data-stu-id="9a7c2-278">**User**</span></span>](c-user.md)<br/> |



 

